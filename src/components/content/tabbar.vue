<template>
    <div class="tabBar">
        <div class="tab-item" v-for="item in tabList" :key="item.id" tag="div" :to="item.path">
            <tabItem :path="item.path">
                <img slot="icon" :src="item.tabicon" alt="">
                <div slot="text">{{item.text}}</div>
            </tabItem>
        </div>
    </div>
</template>

<script>
import tabItem from 'components/common/tabItem.vue'
export default {
  name:'tabBar',
  components: {
      tabItem
  },
  data(){
   return {
       tabList: [
           {
               tabicon: '~assets/image/101_home.svg',
               path: '/home',
               text: '首页'
           },
           {
               tabicon: '@/assets/image/120_applocation.svg',
               path: '/category',
               text: '分类'
           },
           {
               tabicon: '@/assets/image/112_cart.svg',
               path: '/cart',
               text: '购物车'
           },
           {
               tabicon: '@/assets/image/103_user.svg',
               path: '/profile',
               text: '我的'
           }
       ]
   }
  }
}
</script>

<style scoped style="scss">
.tabBar {
    width: 100%;
    height: 50px;
    position: fixed;
    left: 0;
    bottom: 0;
    display: flex;
}
.tab-item {
    width: 25%;
}
</style>
