<template>
  <div id="app">
    <div id="map" style="width: 600px; height: 400px"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  mounted () {
    ymaps.ready(() => {
      var map = new ymaps.Map("map", {
        center: [55.76, 37.64],
        zoom: 7
      });
    })
  },
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
