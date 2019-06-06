<template>
  <div>
    <el-button type="primary" @click="login">登录</el-button>
  </div>
</template>

<script>
import Axios from "axios";
export default {
  methods: {
    login() {
      Axios.get("https://www.easy-mock.com/mock/5cf8df38318e3421d8bb13a8/example/getbaserouters").then(res=>{
        const routers = res.data.data.router;
        console.log(routers)
      })
    }
  }
};
</script>

<style lang="scss" scoped>
</style>