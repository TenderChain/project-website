<script>
import particlesJS from "particlesjs";
export default {
  name: 'Landing',
}
</script>

<template>
  <div id="landing" class="view">
    <h1><img src="../assets/logo.png"/></h1>
    <vue-particles color="#000000"></vue-particles>
  </div>
</template>

<style lang="scss" scoped>
  .view{
    position: relative;
    #particles-js{
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      z-index:-999;
    }
  }
</style>
