<template>
<div>
  <t-layout class="main-layout">
<sidebar></sidebar>
    <t-layout>
      <global-header></global-header>
      <t-content><router-view></router-view></t-content>
      <t-footer>底部区域</t-footer>
    </t-layout>
  </t-layout>
</div>
</template>

<script lang="ts" setup>
import GlobalHeader from "@/views/common/header.vue"
import sidebar from "@/views/common/sidebar.vue"
import Sidebar from "@/views/common/sidebar.vue";
</script>

<style lang="less" scoped>
.main-layout{
  height: 100vh;
}


</style>