<template>
  <div class="home">
    <leftMenu></leftMenu>
    <div :class="{'main-app': true, 'menu-unfold':$store.state.collapsed}">
      <sliderNav></sliderNav>
      <!-- <router-view></router-view> -->
    </div>
  </div>
</template>
<script>
import leftMenu from './components/leftMenu.vue';
import sliderNav from './components/sliderNav.vue';

export default {
  components: {
    leftMenu,
    sliderNav,
  },
};
</script>
<style lang="less">
@import '~@/assets/css/home.less';
</style>
