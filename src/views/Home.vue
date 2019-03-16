<template>
  <div class="home">
  	<el-carousel :interval="4000" type="card" height="520px" class="imgs">
    <el-carousel-item v-for="item in 4" :key="item">
    </el-carousel-item>
  </el-carousel>
  <div class="sec">
    <el-row>
  <el-col :span="8" v-for="(o, index) in 2" :key="o" :offset="index > 0 ? 2 : 0" >
    <el-card :body-style="{ padding: '0px' }">
      <img src="../assets/1.jpg" class="image">
      <div style="padding: 14px;">
        <span>因为遇见</span>
        <div class="bottom clearfix">
          <time class="time">{{ currentDate }}</time>
          <!-- <el-button type="text" class="button">操作按钮</el-button> -->
        </div>
      </div>
    </el-card>
  </el-col>
</el-row>
  </div>
  
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data(){
  		return{
  		  currentDate: new Date()
  		};
  }
}
</script>
<style scoped>
	.home{
		/*height: 500px;*/
		background-color:rgb(249,248,216); 
	}
	  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 200px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(n+1) {
    background-color: #99a9bf;
    background-image: url("../assets/20.jpg") ;
    width: 800px;
    background-repeat:no-repeat;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
    background-image: url("../assets/11.jpg");
    width: 800px;
    background-repeat:no-repeat;
  }
  .el-carousel__item:nth-child(3n+1) {
    background-color: #d3dce6;
    background-image: url("../assets/19.jpg");
    width: 800px;
    background-repeat:no-repeat;
  }
   .el-carousel__item:nth-child(4n+1) {
    background-color: #d3dce6;
    background-image: url("../assets/18.jpg");
    width: 800px;
    background-repeat:no-repeat;
  }
  .imgs{
    padding-top: 30px;
    padding-bottom: 30px;
  }
   .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
  .sec{
    width: 800px;
    margin: 0 auto;
    padding-bottom: 50px;
  }
  .el-col-offset-2{
    margin-left:33%;
  }

</style>
