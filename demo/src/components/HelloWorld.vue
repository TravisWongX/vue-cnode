<template>
  <div>
    <h1> Axios之Get请求</h1>
    <button @click="getDate">获取数据</button>
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
Vue.prototype.$http = axios

export default {
  data(){
    return {

    }
  },
  methods:{
    getData(){
      this.$http.get('https://cnodejs.org/api/v1/topics')
      .then(function(res){
        console.log(res)
      })
      .catch(function(err){
        console.log(err)
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
