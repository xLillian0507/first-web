**技术要点：**

1、利用jsonfile扫描json文件并读取其中内容；

2、将读取的json内容放入js文件中，并用
(function (global) {
  var wordsList = [/其中放json数据]；
  ....
  global.wordsList = wordsList
})(this)
进行全局定义并调用。

3、在HTML中利用Vue设置锚点

<script>
  // vue官网： https://cn.vuejs.org/v2/guide/
  // 初始化Vue

  new Vue({
    el: '#app',   // #app 和html中div#id的 app 对应
    data: {
      wordsList: wordsList // 变量wordsList可以在html使用
    }
  });
  
  
  4、将HTML文件push到GitHub上，便可以形成一个http开头的网页。（这是利用了GitHub的服务器，速度较慢）
