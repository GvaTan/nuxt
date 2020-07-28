<template>
  <div>
      <!-- {{datalist}} -->
   <el-carousel indicator-position="outside">
    <el-carousel-item v-for="item in 4" :key="item">
      <h3>{{ item }}</h3>
    </el-carousel-item>
  </el-carousel>
     <el-row>
  <el-button>默认按钮</el-button>
  <el-button type="primary">主要按钮</el-button>
  <el-button type="success">成功按钮</el-button>
  <el-button type="info">信息按钮</el-button>
  <el-button type="warning">警告按钮</el-button>
  <el-button type="danger">危险按钮</el-button>
</el-row>



  </div>
</template>

<script>

import axios from "axios"
export default {
    layout:"myRoot",
    created(){

    },
    mounted(){
        this.$layer.alert("找不到对象！");
    },
    data(){
        return {

        }
    },
    asyncData(data){
        console.log(data.params);
        // return axios({
        //     url:"https://sp0.baidu.com/5a1Fazu8AA54nxGko9WTAnF6hhy/su?wd=ss&cb=soso",
        //     headers:{}
        // }).then(res=>{
        //     // 注意，这个打印在服务端打印的，浏览器看不见
        //     console.log(res.data);
        //     // 一定要返回，后面的then才能接受到
        //     return {
        //         datalist:res.data
        //     }
        // })
    }
}
</script>

<style>

</style>