<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <calculator/>
  </div>
</template>

<script>
import Calculator from './components/Calculator.vue';
import HelloWorld from "./components/HelloWorld.vue"; // тут импортируються все компонент, которые хотим использовать

export default {
  name: "App",
  components: {
    HelloWorld,
    Calculator, // указываем их тут
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
