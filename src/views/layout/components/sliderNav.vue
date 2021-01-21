<template>
  <div class="main-header">
    <a-button
      type="primary"
      style="margin-bottom: 16px"
      @click="toggleCollapsed"
    >
      <a-icon :type="$store.state.collapsed ? 'menu-unfold' : 'menu-fold'" />
    </a-button>
    <div class="breadcrumb">
      <a-breadcrumb>
        <a-breadcrumb-item>Home</a-breadcrumb-item>
        <a-breadcrumb-item><a href="">商品</a></a-breadcrumb-item>
      </a-breadcrumb>
    </div>
    <div class="user-info">
        <ul>
          <li>
            用户姓名
            <a-icon type="arrow-down" />
          </li>
          <li>退出登录</li>
        </ul>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    toggleCollapsed() {
      this.$store.dispatch('changeCollapsed');
    },
  },
};
</script>
