<template>
  <div><h1>Hello DC</h1></div>
  <div>
  <select v-model="componentName">
    <option value="Home">Home</option>
    <option value="About">About</option>
  </select>
  <keep-alive>
    <component :is="componentName"></component>
  </keep-alive>
 
</div>
</template>

<script>
import Home from './components/Home.vue'
import About from './components/About.vue'

export default{
  name:'App',
  data(){
    return {
      componentName:"Home",
    }
  },
  components:{
    About:About,
    Home:Home,
  }
}

</script>