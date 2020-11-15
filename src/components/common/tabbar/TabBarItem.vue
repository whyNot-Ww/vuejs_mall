<template>
  <div class="tab-bar-item" @click="itemclick">
    <!-- <img src="../../assets/img/tabbar/shouye.svg" alt="">
    <div>首页</div> -->
    <div v-if="!isactive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="activestyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name:'TabBarItem',
  props:{
    path:String,
    activecolor:{
      type:String,
      default:'black'
    }
  },
  data() {
    return {
      // isactive:true,
    }
  },
  computed: {
    isactive(){
      return this.$route.path.indexOf(this.path)!==-1
    },
    activestyle(){
      return this.isactive ? {color:this.activecolor}:{}
    }
  },
  methods: {
    itemclick(){
      this.$router.push(this.path)
    }
  },
}
</script>

<style scoped>
  .tab-bar-item{
    flex: 1;
    height: 49px;
    text-align: center;
    font-size: 14px;
    color: gray;
  }
  .tab-bar-item img{
    height: 24px;
    width: 24px;
    vertical-align: middle;
    margin-top: 3px;
    margin-bottom: 2px;
  }
</style>