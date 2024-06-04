<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <mdui-button>Click me - Home</mdui-button>
    <div style="height: 1000px">Page Content</div>
  </div>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <mdui-button>Click me - Home</mdui-button>
    <div style="height: 1000px">Page Content</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
});
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
</style>
