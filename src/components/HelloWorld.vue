<template>
  <div class="container">
    <div class="left">
      <div class="top margin-8">
        <!-- 纵览 -->
        <div class="overview">
          <div class="item">
            <img src="@/assets/img/badge.png" style="margin-top: -8px" />
            <div>
              <div class="name">罪犯总积分</div>
              <div class="number">13005.20</div>
            </div>
          </div>
          <div class="item">
            <div class="name">本月兑换罪犯数</div>
            <div class="number">32</div>
            <div class="compared">
              同期对比<span style="color: #f95355">12</span>
              <img src="@/assets/img/up.png" />
            </div>
          </div>
          <div class="item">
            <div class="name">本月累积消耗</div>
            <div class="number">12520.00</div>
            <div class="compared">
              同期环比<span style="color: #00ae41">12.88%</span>
              <img src="@/assets/img/down.png" />
            </div>
          </div>
          <div class="item">
            <div class="name">本月累积上账</div>
            <div class="number">200.00</div>
            <div class="compared">
              同期环比<span style="color: #f95355">12.88%</span>
              <img src="@/assets/img/up.png" />
            </div>
          </div>
          <div class="item">
            <div class="name">本月累积下账</div>
            <div class="number">200.00</div>
            <div class="compared">
              同期环比<span style="color: #00ae41">12.88%</span>
              <img src="@/assets/img/down.png" />
            </div>
          </div>
        </div>
        <!-- 积分消耗走势 -->
        <div class="chart-box">
          <div class="title">积分消耗走势<span>（近7日）</span></div>
          <div class="chart" id="integral-consume"></div>
        </div>
      </div>
      <div class="bottom">
        <!-- 本月罪犯消耗排名 -->
        <div class="left margin-8">
          <div class="title">本月罪犯消耗排名</div>
          <table border="0" cellpadding="0" cellspacing="0">
            <thead>
              <tr>
                <th align="left">罪犯</th>
                <th align="left">编号</th>
                <th align="left">所属监区</th>
                <th align="left">消耗积分</th>
                <th></th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td align="left" style="font-weight: bold">
                  <img src="g.jpeg" />Alex Shatov
                </td>
                <td align="left">3059109</td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一监区朵追的似懂非懂舒服饭撒的"
                    style="max-width: 140px"
                  >
                    一监区朵追的似懂非懂舒服饭撒的
                  </div>
                </td>
                <td align="left" style="color: #10b981">2.249.88</td>
                <td>
                  <span style="color: #0256ff; font-size: 14px; cursor: pointer"
                    >详情</span
                  >
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <img src="g.jpeg" />Philip Harbach
                </td>
                <td align="left">3059109</td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一监区朵追的似懂非懂舒服饭撒的"
                    style="max-width: 140px"
                  >
                    一监区朵追的似懂非懂舒服饭撒的
                  </div>
                </td>
                <td align="left" style="color: #10b981">2.249.88</td>
                <td>
                  <span style="color: #0256ff; font-size: 14px; cursor: pointer"
                    >详情</span
                  >
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <img src="g.jpeg" />Mirko Fisuk
                </td>
                <td align="left">3059109</td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一监区朵追的似懂非懂舒服饭撒的"
                    style="max-width: 140px"
                  >
                    一监区朵追的似懂非懂舒服饭撒的
                  </div>
                </td>
                <td align="left" style="color: #10b981">2.249.88</td>
                <td>
                  <span style="color: #0256ff; font-size: 14px; cursor: pointer"
                    >详情</span
                  >
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <img src="g.jpeg" />Olga Semklo
                </td>
                <td align="left">3059109</td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一监区朵追的似懂非懂舒服饭撒的"
                    style="max-width: 140px"
                  >
                    一监区朵追的似懂非懂舒服饭撒的
                  </div>
                </td>
                <td align="left" style="color: #10b981">2.249.88</td>
                <td>
                  <span style="color: #0256ff; font-size: 14px; cursor: pointer"
                    >详情</span
                  >
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <img src="g.jpeg" />Burak Long
                </td>
                <td align="left">3059109</td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一监区朵追的似懂非懂舒服饭撒的"
                    style="max-width: 140px"
                  >
                    一监区朵追的似懂非懂舒服饭撒的
                  </div>
                </td>
                <td align="left" style="color: #10b981">2.249.88</td>
                <td>
                  <span style="color: #0256ff; font-size: 14px; cursor: pointer"
                    >详情</span
                  >
                </td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="right margin-8">
          <div class="title">本月商品兑换排名</div>
          <table border="0" cellpadding="0" cellspacing="0">
            <thead>
              <tr>
                <th align="left">排名</th>
                <th align="left">商品名称</th>
                <th align="left">兑换次数</th>
                <th align="left">总积分</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td align="left" style="font-weight: bold">
                  <div style="min-width: 30px">1</div>
                </td>
                <td align="left">
                  <div
                    class="ellipsis"
                    title="一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨"
                    style="max-width: 140px"
                  >
                    一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨
                  </div>
                </td>
                <td align="left"><div style="min-width: 60px">12</div></td>
                <td align="left" style="color: #10b981">
                  <div style="min-width: 40px">2.249.88</div>
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <div style="min-width: 30px">2</div>
                </td>
                <td align="left">
                  <div class="ellipsis" style="max-width: 140px">
                    一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨
                  </div>
                </td>
                <td align="left"><div style="min-width: 60px">12</div></td>
                <td align="left" style="color: #10b981">
                  <div style="min-width: 40px">2.249.88</div>
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <div style="min-width: 30px">3</div>
                </td>
                <td align="left">
                  <div class="ellipsis" style="max-width: 140px">
                    一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨
                  </div>
                </td>
                <td align="left"><div style="min-width: 60px">12</div></td>
                <td align="left" style="color: #10b981">
                  <div style="min-width: 40px">2.249.88</div>
                </td>
              </tr>
              <tr>
                <td align="left" style="font-weight: bold">
                  <div style="min-width: 30px">4</div>
                </td>
                <td align="left">
                  <div class="ellipsis" style="max-width: 140px">
                    一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨
                  </div>
                </td>
                <td align="left"><div style="min-width: 60px">12</div></td>
                <td align="left" style="color: #10b981">
                  <div style="min-width: 40px">2.249.88</div>
                </td>
              </tr>
              <!-- <tr>
                <td align="left" style="font-weight: bold">
                  <div style="min-width: 30px">5</div>
                </td>
                <td align="left">
                  <div class="ellipsis" style="max-width: 140px">
                    一朵追的似懂非懂舒服饭撒的方式打发撒的范德萨
                  </div>
                </td>
                <td align="left"><div style="min-width: 60px">12</div></td>
                <td align="left" style="color: #10b981">
                  <div style="min-width: 40px">2.249.88</div>
                </td>
              </tr> -->
            </tbody>
          </table>
        </div>
      </div>
    </div>
    <div class="right">
      <!-- 本月活动开展情况 -->
      <div class="top margin-8">
        <div class="title">本月活动开展情况</div>
        <div class="box">
          <div class="item">
            <img src="@/assets/img/activity1.png" />
            <div class="right">
              <div class="label">待审核</div>
              <div class="number">10</div>
            </div>
          </div>
          <div class="item">
            <img src="@/assets/img/activity2.png" />
            <div class="right">
              <div class="label">未确认</div>
              <div class="number">55</div>
            </div>
          </div>
          <div class="item">
            <img src="@/assets/img/activity3.png" />
            <div class="right">
              <div class="label">已完成</div>
              <div class="number">10</div>
            </div>
          </div>
          <div class="item">
            <img src="@/assets/img/activity4.png" />
            <div class="right">
              <div class="label">已驳回</div>
              <div class="number">55</div>
            </div>
          </div>
        </div>
      </div>
      <!-- 本月活动兑换排名 -->
      <div class="middle margin-8">
        <div class="title">本月活动兑换排名</div>
        <div class="chart" id="exchange-rank"></div>
      </div>
      <!-- 积分消耗占比 -->
      <div class="bottom margin-8">
        <div class="title">积分消耗占比<span>（本月累积）</span></div>
        <div class="chart" id="consume-percentage"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      integralConsumeChart: null, // 积分消费走势图表实例
      exchangeRankChart: null, // 渲染本月活动兑换排名图表实例
      consumePercentageChart: null, // 渲染积分消耗占比图表实例
    };
  },
  mounted() {
    this.renderIntegralConsume();
    this.renderExchangeRank();
    this.renderConsumePercentage();
    // 监听屏幕变化重新渲染图表
    window.addEventListener("resize", this.resize);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.resize);
  },
  methods: {
    /**
     * 屏幕尺寸变化处理函数
     */
    resize() {
      this.integralConsumeChart?.resize();
      this.exchangeRankChart?.resize();
      this.consumePercentageChart?.resize();
    },
    /**
     * 渲染积分消耗走势
     */
    renderIntegralConsume() {
      const chartDom = document.getElementById("integral-consume");
      // eslint-disable-next-line no-undef
      this.integralConsumeChart = echarts.init(chartDom);
      const option = {
        xAxis: {
          type: "category",
          boundaryGap: false,
          data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"],
          axisLine: {
            lineStyle: {
              color: "#E5E6EB",
            },
          },
          axisLabel: {
            color: "#4E5969",
          },
          axisTick: {
            show: false,
          },
        },
        yAxis: {
          type: "value",
          splitLine: {
            lineStyle: {
              color: ["#E5E6EB"],
            },
          },
          axisLabel: {
            color: "#4E5969",
          },
        },
        legend: {
          data: ["商品兑换", "活动兑换"],
          right: 24,
          itemWidth: 8,
          itemHeight: 8,
          icon: "circle",
        },
        tooltip: {
          show: true,
          trigger: "axis",
        },
        grid: {
          top: 40,
          left: 64,
          right: 24,
          bottom: 32,
        },
        series: [
          {
            name: "商品兑换",
            data: [820, 932, 901, 934, 1290, 1330, 1320],
            type: "line",
            smooth: true,
            symbol: "circle",
            lineStyle: {
              width: 3,
            },
            areaStyle: {
              // eslint-disable-next-line no-undef
              color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                {
                  offset: 0,
                  color: "rgba(17, 126, 255, 0.48)",
                },
                {
                  offset: 0.4,
                  color: "rgba(17, 126, 255, 0.16)",
                },
              ]),
            },
          },
          {
            name: "活动兑换",
            data: [180, 92, 453, 368, 620, 330, 132],
            type: "line",
            smooth: true,
            symbol: "circle",
            lineStyle: {
              width: 3,
            },
            areaStyle: {
              // eslint-disable-next-line no-undef
              color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                {
                  offset: 0,
                  color: "rgba(4, 209, 130, 0.48)",
                },
                {
                  offset: 0.4,
                  color: "rgba(4, 209, 130, 0.16)",
                },
              ]),
            },
          },
        ],
      };
      this.integralConsumeChart.setOption(option);
    },
    /**
     * 渲染本月活动兑换排名
     */
    renderExchangeRank() {
      const chartDom = document.getElementById("exchange-rank");
      // eslint-disable-next-line no-undef
      this.exchangeRankChart = echarts.init(chartDom);
      const option = {
        tooltip: {
          trigger: "axis",
          axisPointer: {
            type: "shadow",
          },
        },
        grid: {
          left: "3%",
          right: "4%",
          bottom: "3%",
          containLabel: true,
        },
        xAxis: {
          type: "value",
          boundaryGap: [0, 0.01],
          splitLine: {
            lineStyle: {
              color: ["#E5E6EB"],
            },
          },
          axisLabel: {
            formatter: `{value}k`,
            color: "#4E5969",
          },
        },
        yAxis: {
          type: "category",
          data: [
            "商品兑换丰富的风",
            "商品兑换丰富的风额舒服的沙发",
            "USA",
            "India",
            "China",
            "World",
          ],
          axisLine: {
            lineStyle: {
              color: "#E5E6EB",
            },
          },
          axisLabel: {
            color: "#4E5969",
            align: "left",
            lineHeight: 14,
            padding: [0, 0, 0, -60],
            formatter(v) {
              return v.length > 5
                ? v.slice(0, 5) +
                    "\n" +
                    v.slice(5, 9) +
                    (v.length > 9 ? "..." : "")
                : v;
            },
          },
          axisTick: { show: false },
        },
        series: [
          {
            name: "",
            type: "bar",
            data: [18, 23, 29, 104, 131, 630],
            color: "#366EF4",
            barWidth: 10,
            itemStyle: {
              borderRadius: 10,
            },
          },
        ],
      };
      this.exchangeRankChart.setOption(option);
    },
    /**
     * 渲染积分消耗占比
     */
    renderConsumePercentage() {
      const chartDom = document.getElementById("consume-percentage");
      // eslint-disable-next-line no-undef
      this.consumePercentageChart = echarts.init(chartDom);
      const option = {
        series: [
          {
            center: ["25%", "45%"],
            name: "",
            type: "gauge",
            radius: "65%",
            min: 0,
            max: 100,
            startAngle: 90,
            endAngle: -270,
            axisTick: {
              show: false,
            },
            axisLabel: {
              show: false,
            },
            splitLine: {
              show: false,
            },
            axisLine: {
              show: true,
            },
            pointer: {
              show: false,
            },
            itemStyle: {
              show: false,
              color: "#3E79F7",
            },
            progress: {
              show: true,
              width: 8,
              roundCap: true,
            },
            detail: {
              valueAnimation: true,
              formatter: "{value}%",
              offsetCenter: [0, 0],
              fontSize: 20,
            },
            data: [
              {
                value: 83,
                name: "商品兑换",
                title: {
                  offsetCenter: [0, "135%"],
                  fontWeight: "bold",
                },
              },
            ],
          },
          {
            center: ["75%", "45%"],
            name: "",
            type: "gauge",
            radius: "65%",
            min: 0,
            max: 100,
            startAngle: 90,
            endAngle: -270,
            axisTick: {
              show: false,
            },
            axisLabel: {
              show: false,
            },
            splitLine: {
              show: false,
            },
            axisLine: {
              show: true,
            },
            pointer: {
              show: false,
            },
            itemStyle: {
              show: false,
              color: "#04D182",
            },
            progress: {
              show: true,
              width: 8,
              roundCap: true,
            },
            detail: {
              valueAnimation: true,
              formatter: "{value}%",
              offsetCenter: [0, 0],
              fontSize: 20,
            },
            data: [
              {
                value: 66.58,
                name: "活动兑换",
                title: {
                  offsetCenter: [0, "135%"],
                  fontWeight: "bold",
                },
              },
            ],
          },
        ],
      };
      this.consumePercentageChart.setOption(option);
    },
  },
};
</script>
<style scoped>
.ellipsis {
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow: hidden;
}
.margin-8 {
  padding: 24px;
  margin: 8px;
  border-radius: 4px;
  background-color: #ffffff;
}
.container {
  padding: 8px;
  background-color: #f6f6f6;
  height: 100%;
  display: flex;
  box-sizing: border-box;
}
.title {
  font-weight: 500;
  text-align: left;
}
.title span {
  font-size: 12px;
  color: #999999;
}
.container .left {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}
.container .left .top {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.container .left .top .overview {
  display: flex;
  justify-content: space-between;
  margin-top: 12px;
  margin-right: 24px;
}
.container .left .top .overview .item {
  text-align: left;
}
.container .left .top .overview .item:first-child {
  display: flex;
  align-items: start;
}
.container .left .top .overview .item .name {
  font-size: 12px;
  color: #999999;
}
.container .left .top .overview .item .number {
  font-size: 32px;
  font-weight: 500;
}
.container .left .top .overview .item .compared {
  font-size: 12px;
  color: #bbbbbb;
  display: flex;
  align-items: center;
}
.container .left .top .overview .item .number {
  font-size: 32px;
  font-weight: 500;
}
.container .left .top .overview .item .compared img {
  margin-left: 4px;
  width: 14px;
  height: 14px;
}
.container .left .top .overview .item .compared span {
  margin-left: 4px;
  font-size: 14px;
}
.container .left .top .chart-box {
  margin-top: 32px;
  height: 0;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.container .left .top .chart-box .title {
  padding-left: 12px;
}
.container .left .top .chart-box .chart {
  height: 0;
  flex-grow: 1;
}
.container .left .bottom {
  height: 400px;
  display: flex;
}
.container .left .bottom table th {
  padding: 12px;
  font-size: 12px;
  color: #9ca3af;
  background: #f8fafc;
}
.container .left .bottom .left {
  display: flex;
  flex-direction: column;
}
.container .left .bottom .left table,
.container .left .bottom .right table {
  margin-top: 24px;
}
.container .left .bottom table td {
  padding: 0 12px;
  height: 52px;
}
.container .left .bottom table img {
  width: 32px;
  height: 32px;
  border-radius: 60px;
  object-fit: cover;
  vertical-align: middle;
  margin-right: 12px;
}
.container .left .bottom .left {
  width: 60%;
}
.container .left .bottom .right {
  width: 40%;
  display: flex;
  flex-direction: column;
}
.container .right {
  display: flex;
  flex-direction: column;
  width: 460px;
}
.container .right .top {
  height: 300px;
  display: flex;
  flex-direction: column;
}
.container .right .top .box {
  margin-top: 32px;
  display: flex;
  flex-wrap: wrap;
}
.container .right .top .box .item {
  margin: 6px;
  padding: 20px;
  box-sizing: border-box;
  width: calc(50% - 12px);
  text-align: left;
  display: flex;
  align-items: center;
  background-color: #f2f3ff;
  border-radius: 12px;
}
.container .right .top .box .item img {
  width: 72px;
}
.container .right .top .box .item .right {
  padding-left: 12px;
}
.container .right .top .box .item .right .label {
  font-size: 16px;
  font-weight: 500;
}
.container .right .top .box .item .right .number {
  color: #003cab;
  font-weight: bold;
  font-size: 24px;
}
.container .right .middle {
  flex-grow: 2;
  display: flex;
  flex-direction: column;
}
.container .right .middle .chart {
  height: 0;
  flex-grow: 1;
}
.container .right .bottom {
  padding-bottom: 12px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.container .right .bottom .chart {
  height: 0;
  flex-grow: 1;
}
</style>
