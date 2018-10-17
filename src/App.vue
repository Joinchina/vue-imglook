<template>
  <div id="app">
    <!-- 图片展示区域 -->
     <div class="imgbox">
       <ul>
         <li v-for="(imgview,index) in img" :key="index"><img :src="imgview.src" alt="" @click="showmodel(index)"></li>
       </ul>
     </div>
    <img-view :passimg="img"  ref="number"></img-view>
  </div>
</template>

<script>
import imgView from '../src/components/imgview '
export default {
data(){
  return {
     img:[
       {'src':'../static/imgmoudel/1.jpg','name':'我是1号美女'},
       {'src':'../static/imgmoudel/2.jpg','name':'我是2号美女'},
       {'src':'../static/imgmoudel/3.jpg','name':'我是3号美女'},
       {'src':'../static/imgmoudel/4.jpg','name':'我是4号美女'},
       {'src':'../static/imgmoudel/5.jpg','name':'我是5号美女'},
       {'src':'../static/imgmoudel/6.jpg','name':'我是6号美女'},
       {'src':'../static/imgmoudel/7.jpg','name':'我是7号美女'},
       {'src':'../static/imgmoudel/8.jpg','name':'我是8号美女'},
       {'src':'../static/imgmoudel/9.jpg','name':'我是9号美女'},
       {'src':'../static/imgmoudel/10.jpg','name':'我是10号美女'},
       ],
  }
},
methods:{
  showmodel(index){
     this.$refs.number.getpassindex(index);
  },
},
components:{
  'img-view':imgView
}
}
</script>

<style>
body{
  margin: 0;
  left: 0;
  overflow: hidden;
}
.imgbox{
  width: 1000px;
  margin: 0 auto;
   overflow: hidden;  
}
.imgbox ul{
  width: 100%;
  overflow: hidden;
}
.imgbox ul li{
   width: 200px;
   height: 150px;
   border: 1px solid #ccc;
   text-align: center;
   float: left;
   list-style: none;
   margin: 20px 20px;
   overflow: hidden;
}
.imgbox ul li:before {
  content: "";
  display: inline-block;
  height: 100%;
  vertical-align: middle;
  width: 0;
}
.imgbox ul li img{
 max-width: 200px;
 vertical-align: middle;
}
</style>
