<!--  -->
<template>
  <div class>
    <div class="nav">
      <span>京西商城</span>
    </div>
    <div class="box">
      <ul class="list">
        <li>苹果</li>
        <li>香蕉</li>
        <li>葡萄</li>
        <li>凤梨</li>
      </ul>
    </div>
  </div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';
import axios from "axios";
export default {
  //import引入的组件需要注入到对象中才能使用

  components: {},
  data() {
    //这里存放数据
    return {};
  },
  //监听属性 类似于data概念
  computed: {},
  //监控data中的数据变化
  watch: {},
  //方法集合
  methods: {},
  //生命周期 - 创建完成（可以访问当前this实例）
  created() {},
  //生命周期 - 挂载完成（可以访问DOM元素）
  async mounted() {
    // axios.get("http://s.linweiqin.com/api/s/getIndexLoopimg").then(res=>{
    //   console.log(res);
    // }).catch(err=>console.log(err)).finally(res=>console.log(res))
    try {
      let res = await axios.get("http://s.linweiqin.com/api/s/getIndexLoopimg");
      let res1 = await axios.get(
        "http://s.linweiqin.com/api/s/getIndexLoopimg"
      );
      console.log(res, res1);
    } catch (err) {
      console.log(err);
    }
  },
  beforeCreate() {}, //生命周期 - 创建之前
  beforeMount() {}, //生命周期 - 挂载之前
  beforeUpdate() {}, //生命周期 - 更新之前
  updated() {}, //生命周期 - 更新之后
  beforeDestroy() {}, //生命周期 - 销毁之前
  destroyed() {}, //生命周期 - 销毁完成
  activated() {} //如果页面有keep-alive缓存功能，这个函数会触发
};
</script>
<style lang='less' >
//@import url(); 引入公共css类
html,
body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.nav {
  width: 100%;
  height: 50px;
  background-color: #ec3b4e;
  // line-height: 50px;
  // text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  span {
    color: white;
  }
}
div.box {
  width: 100%;
  text-align: center;
  ul.list {
    list-style: none;
    margin: 0;
    padding: 0;
    li {
      height: 30px;
      line-height: 30px;
    }
    li:nth-child(2n){
      background: olivedrab;
    }
    li:nth-child(2n-1){
      background: orange;
    }
  }
}
</style>