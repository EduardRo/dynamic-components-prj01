<template>
  <button type="button" v-on:click="changeFlag">Toggle</button>
  <transition name="fade0" mode="out-in">
    <h2 v-if="flag" key="main">Hello Dynamic!</h2>
    <h1 v-else key="secondary">No Dynamic here!</h1>
  </transition>
  <transition name="fade1">
    <h3 v-if="flag">Hello Second Dynamic!</h3>
  </transition>
</template>

<script>
export default {
  name: "App",
  data(){
    return {
      flag:false,
    }
  },
  methods:{changeFlag(){
    this.flag=!this.flag
  }}
};
</script>

<style>
.fade0-enter-from{
  opacity:0;

}
.fade0-enter-active{
  transition:all 0.25s linear;
  color:red;
}
.fade0-enter-to{
  transition:all 0.25s linear;
  color:rgb(167, 30, 96);
  opacity: 1;
}
.fade0-leave-to {
  transition:all 0.25s linear;;
  transform: translateX(20px);
  color:green;
}


.fade1-enter-from{
  opacity:0;

}
.fade1-enter-active{
  transition:all 0.55s linear;
  color:rgb(50, 27, 182);
}
</style>
