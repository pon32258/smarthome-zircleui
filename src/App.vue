<template>
  <z-canvas :views="$options.components"></z-canvas>
</template>
<script>
// TO SET UP VUE-ROUTER UNCOMMENT THE FOLLOWING LINES
// import Vue from 'vue'
// import Router from 'vue-router'
// Vue.use(Router)
// const router = new Router()

import living from './views/living';
import home from './views/home';
import settings from './views/settings';
import rooms from './views/rooms';
import scenes from './views/scenes';
import family from './views/family';
export default {
  components: {
    living,
    home,
    settings,
    rooms,
    scenes,
    family
  },
  mounted() {
    this.$zircle.config({
      mode: 'full',
      style: {
        theme: 'black',
        mode: 'dark'
      },
      debug: true
    });
    this.$zircle.setView('home');
  }
};
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro:400,700');
@import url('https://use.fontawesome.com/releases/v5.1.0/css/all.css');
</style>
