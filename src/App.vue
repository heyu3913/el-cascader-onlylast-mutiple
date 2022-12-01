<template>
  <div id="app">
    <Cascader
    :props="props"
    :options="options"
    :collapseTags = true
    :visibleData="visibleData"
    @change="change"
    ></Cascader>
    <h2>
      visibleData: {{visibleData}}
    </h2>
  </div>
</template>

<script>
import Cascader from  'el-cascader-onlylast-mutiple'
// import  Cascader  from './lib/ElCascaderOnlaylastMutiple/lib/el-cascader-onlylast-mutiple';
export default {
  name: 'App',
  data(){
    return {
      props: { multiple: true },
      options: [
        {
          value: 1,
          label: '东南',
          children: [{
            value: 2,
            label: '上海',
            children: [
              {
                value: 3,
                label: '普陀'
              },
              {
                value: 4,
                label: '黄埔'
              },
              {
                value: 5,
                label: '徐汇'
              }
            ]
          }, {
            value: 7,
            label: '江苏',
            children: [
              {
                value: 8,
                label: '南京'
              },
              {
                value: 9,
                label: '苏州'
              },
              {
                value: 10,
                label: '无锡'
              }
            ]
          }, {
            value: 12,
            label: '浙江',
            children: [
              {
                value: 13,
                label: '杭州'
              },
              {
                value: 14,
                label: '宁波'
              },
              {
                value: 15,
                label: '嘉兴'
              }
            ]
          }]
        }, {
          value: 17,
          label: '西北',
          children: [{
            value: 18,
            label: '陕西',
            children: [
              {
                value: 19,
                label: '西安'
              },
              {
                value: 20,
                label: '延安'
              }
            ]
          }, {
            value: 21,
            label: '新疆维吾尔族自治区',
            children: [
              {
                value: 22,
                label: '乌鲁木齐'
              },
              {
                value: 23,
                label: '克拉玛依'
              }
            ]
          }]
        }],
      visibleData:[]
    }
  },
  components: {
    Cascader
  },
  methods:{
    change(data){
      console.log(data)
      this.visibleData = data
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
