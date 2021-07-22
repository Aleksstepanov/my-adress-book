<template>
  <div id="app">
    <VueExtendLayouts />
  </div>
</template>

<script>
import VueExtendLayouts from "vue-extend-layout";

export default {
  name: "App",

  components: {
    VueExtendLayouts,
  },
};
</script>
<style lang="scss">
@import "@/assets/global-style/global-style.scss";
</style>
