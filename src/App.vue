<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <video
      id="video-remote"
      autoplay
      controls
      style="width: 600px; height: 600px"
    ></video>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      sipInfo: {
        phoneIp: "192.168.20.117",
        phoneCode: "1094",
        phonePwd: "1094",
        meetingPattern: 2,
        webSocketPhoneIp: "wss://192.168.20.117:7443",
        callNum: "777958594",
      },
      sipStack: null,
      sipRegister: null,
      videoCall: null,
    };
  },
  mounted() {
    const _this = this;
    SIPml.init(function () {
      _this.sipStack = new SIPml.Stack({
        realm: _this.sipInfo.phoneIp,
        impi: _this.sipInfo.phoneCode,
        impu: "sip:" + _this.sipInfo.phoneCode + "@" + _this.sipInfo.phoneIp,
        password: _this.sipInfo.phonePwd,
        display_name: _this.sipInfo.meetingPattern === 2 ? "police" : "",
        websocket_proxy_url: _this.sipInfo.webSocketPhoneIp,
        outbound_proxy_url: null,
        ice_servers: "[]",
        enable_rtcweb_breaker: true,
        events_listener: {
          events: "*",
          listener: function (e) {
            if (e.type === "failed_to_start") {
              console.log("error");
            }
            if (e.type == "started") {
              _this.sipRegister = _this.sipStack.newSession("register", {
                events_listener: {
                  events: "*",
                  listener: function (e) {
                    if (
                      e.type === "connected" &&
                      e.session == _this.sipRegister
                    ) {
                      _this.sipStack.o_stack.ao_headers[1].s_value =
                        _this.sipInfo.callNum;
                      const video = document.getElementById("video-remote");
                      console.log("registered");
                      _this.videoCall = _this.sipStack.newSession(
                        "call-video",
                        {
                          video_remote: video,
                          events_listener: {
                            events: "*",
                            listener: function () {},
                          },
                        }
                      );
                      _this.videoCall.call(_this.sipInfo.callNum);
                    }
                  },
                },
              });
              _this.sipRegister.register();
            }
          },
        },
        enable_early_ims: true,
        enable_media_stream_cache: true,
        sip_headers: [
          {
            name: "User-Agent",
            value: "IM-client/OMA1.0 sipML5-v1.2016.03.04",
          },
          { name: "Organization", value: "Doubango Telecom" },
        ],
      });
      _this.sipStack.start();
    });
    window.addEventListener("beforeunload", () => {
      this.sipStack && this.sipStack.stop();
    });
  },
  components: {
    // HelloWorld,
  },
};
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
