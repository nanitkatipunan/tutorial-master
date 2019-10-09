<template>
  <div id="lawas">
    <div v-if="auth.user !== null">
      <sideBar></sideBar>
        <transition>
          <router-view></router-view>
        </transition>
    </div>
    <div v-else>
      <transition>
        <router-view></router-view>
      </transition>
    </div>
  </div>
</template>

<style >
    body{
        background-image: url(https://mcdn.wallpapersafari.com/medium/81/14/SvmD6n.jpg);
        background-size: cover;
        background-repeat: no-repeat;
        background-attachment: fixed;
    }
    
</style>

<script>
import sideBar from "components/frame/sidebar.vue";
import AUTH from 'services/auth'
export default {
  name: "lawas",
  components: {
    sideBar
  },
  data(){
      return{ 
          auth: AUTH,
      }
  }
};
</script>