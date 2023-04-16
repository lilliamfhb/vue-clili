<template>
  <HeaderItem></HeaderItem>
  <main id="smooth-wrapper">
    <div id="smooth-content">
      <HomePage></HomePage>
    </div>
  </main>
  <Footer-item></Footer-item>
  
  
</template>

<script>
import Lenis from '@studio-freight/lenis'
import HeaderItem from './components/HeaderItem.vue';
import FooterItem from './components/FooterItem.vue';
import HomePage from './pages/HomePage.vue';

export default {
  name: 'App',
  components: {
    HeaderItem,
    FooterItem,
    HomePage,
  },
  mounted() {
    const lenis = new Lenis()
    lenis.on('scroll', (e) => {
      console.log(e)
    })

    function raf(time) {
      lenis.raf(time)
      requestAnimationFrame(raf)
    }

    requestAnimationFrame(raf)
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
