<template>
  <div class="hello">
      <div class="container">
      <h2>vm layout Demo</h2>
      <h3><a href="https://www.jianshu.com/p/1f1b23f8348f" target="_blank">查看原文</a></h3>
      <div class="test">设置的px文章尺寸，将会转化为vm单位</div>
      <div class="test ignore">设置的px文章尺寸和添加了ignore类，将会转化为vm单位, 是由postcss-px-to-viewport配置</div>
    </div>
    <div>
      <div class="box ignore"></div>
      在不想要把px转换为vw的时候，首先在对应的元素（html）中添加配置中指定的类名.ignore或.hairlines(.hairlines一般用于设置border-width:0.5px的元素中)：
    </div>
     <div class="example">
      asdfasdfasdf
    </div>
    <div style="border: 1px solid #00b1ff">jalskfjlkasjdflasdfjlasj</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
  /* background-color: #42b983; */
}
.test {
    margin: 10px;
    border: .5px solid black;
    border-bottom-width: 4px;
    font-size: 14px;
    /* line-height: 20px; */
    position: relative;
}
.ignore {
    font-size: 14px;
    /* background-color: red; */
}
[w-188-246] {
    width: 188px;
}
@svg 1px-border {
    height: 2px;
    @rect {
        fill: var(--color, black);
        width: 100%;
        height: 50%;
    }
}
.example {
    margin-bottom: 10px; 
    border: 1px solid transparent;
    border-image: svg(1px-border param(--color #00b1ff)) 2 2 stretch;
}
</style>
