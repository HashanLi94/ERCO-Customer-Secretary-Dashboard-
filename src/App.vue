<template>
  <div v-if="loggedIn=true">
    <dashboard-firm/>    
  </div>

  <div v-if="loggedIn=false">
    <nav-bar />
    <router-view />
    <home-footer/>
  </div>
</template>

<script>
import NavBar from "./home-wizard/shared-components/NavBar.vue";
import HomeFooter from "./home-wizard/shared-components/HomeFooter.vue";
import DashboardFirm from './components/dasshboardFirm/DashboardFirm';

export default {  
  components: {    
    NavBar: NavBar,
    HomeFooter: HomeFooter,
    DashboardFirm,
  },
};
</script>

<style lang="scss">
// @import "./App.scss";
</style>
