<template>
  <div id="app">
    <img src="~assets/logo.png" alt="">
    <router-view></router-view>  
    <tabBar></tabBar>
  </div>
</template>

<script>
import tabBar from 'components/content/tabbar.vue'
export default {
  name: 'App',
  components: {
    tabBar
  }
}
</script>

<style>
  @import 'assets/css/normallize.css'
</style>
