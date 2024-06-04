<template>
  <mdui-navigation-rail>
    <mdui-button-icon
      icon="menu"
      slot="top"
      @click="openNavigationDrawer"
    ></mdui-button-icon>
    <mdui-fab lowered icon="edit--outlined" slot="top"></mdui-fab>
    <mdui-button-icon icon="settings" slot="bottom"></mdui-button-icon>

    <mdui-navigation-rail-item icon="watch_later--outlined"
      >Recent</mdui-navigation-rail-item
    >
    <mdui-navigation-rail-item icon="image--outlined"
      >Images</mdui-navigation-rail-item
    >
    <mdui-navigation-rail-item icon="library_music--outlined"
      >Library</mdui-navigation-rail-item
    >
  </mdui-navigation-rail>

  <div
    class="example-contained"
    style="position: fixed; width: 300px; z-index: 2"
  >
    <mdui-navigation-drawer contained ref="navigationDrawerRef">
      <mdui-button class="close" @click="closeNavigationDrawer"
        >Close Navigation Drawer</mdui-button
      >
    </mdui-navigation-drawer>
  </div>
  <mdui-top-app-bar style="position: relative; width: 100%">
    <mdui-top-app-bar-title>Title</mdui-top-app-bar-title>
    <div style="flex-grow: 1"></div>
    <mdui-button-icon icon="more_vert"></mdui-button-icon>
  </mdui-top-app-bar>
</template>

<script setup lang="ts">
import { ref } from "vue";

const navigationDrawerRef = ref<HTMLElement | null>(null);

const openNavigationDrawer = () => {
  if (!navigationDrawerRef.value) return;
  navigationDrawerRef.value.open = true;
};

const closeNavigationDrawer = () => {
  if (!navigationDrawerRef.value) return;
  navigationDrawerRef.value.open = false;
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}
html,
body {
  margin: 0;
  padding: 0;
}
mdui-navigation-drawer::part(panel) {
  width: 300px;
  top: 0;
  height: 100vh;
}

mdui-navigation-drawer::part(overlay) {
  width: 100vw;
  height: 100vh;
}

mdui-top-app-bar {
  z-index: 1;
}
</style>
