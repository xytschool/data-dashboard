<template>
  <dv-full-screen-container>
    <dv-border-box-11 >
      <dv-charts :option="option" />
    </dv-border-box-11>

    <dv-border-box-11 >
      <dv-charts :option="option" />
    </dv-border-box-11>

  </dv-full-screen-container>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return {
      option:{
        title: {
          text: '剩余油量表',
          style: {
            fill: '#fff'
          }
        },
        series: [
          {
            type: 'gauge',
            data: [ { name: 'itemA', value: 55 } ],
            center: ['50%', '55%'],
            axisLabel: {
              formatter: '{value}%',
              style: {
                fill: '#fff'
              }
            },
            axisTick: {
              style: {
                stroke: '#fff'
              }
            },
            animationCurve: 'easeInOutBack'
          }
        ]
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
