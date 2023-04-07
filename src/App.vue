<template>
  <HeaderItem></HeaderItem>
  <Footer-item></Footer-item>
  
  
</template>

<script>
import HeaderItem from './components/HeaderItem.vue';
import FooterItem from './components/FooterItem.vue';

export default {
  name: 'App',
  components: {
    HeaderItem,
    FooterItem
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
