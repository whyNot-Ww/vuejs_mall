<template>
  <tab-bar>
      <tab-bar-item path="/home" activecolor="black">
        <img slot="item-icon" src="~@/assets/img/tabbar/shouye.svg" alt="">
        <img slot="item-icon-active" src="~@/assets/img/tabbar/shouyefill.svg" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" activecolor="black">
        <img slot="item-icon" src="~@/assets/img/tabbar/caidan.svg" alt="">
        <img slot="item-icon-active" src="~@/assets/img/tabbar/sousuoleimufill.svg" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" activecolor="black">
        <img slot="item-icon" src="~@/assets/img/tabbar/gouwuche.svg" alt="">
        <img slot="item-icon-active" src="~@/assets/img/tabbar/gouwuchefill.svg" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" activecolor="black">
        <img slot="item-icon" src="~@/assets/img/tabbar/yonghu.svg" alt="">
        <img slot="item-icon-active" src="~@/assets/img/tabbar/yonghufill.svg" alt="">
        <div slot="item-text">用户</div>
      </tab-bar-item>
    </tab-bar>
</template>

<script>
import TabBar from '@/components/common/tabbar/TabBar'
import TabBarItem from '@/components/common/tabbar/TabBarItem'
export default {
  name:'MainTabBar',
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>