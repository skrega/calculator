<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- <h2>{{ message }}</h2>
    <button v-on:click="onClickBtn">Click me</button>  -->
    <!-- <button @click="onClickBtn">Click me</button> -->
    <!-- Можно и так и так-->
    <!-- <br>
    <input type="text" @focus="onInputFoucs" @blur="onBlur"> -->
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data(){ //инициализациях наших данных
    return{
      message: "Привет, Vue!"
    }
  },
  methods:{
    // onClickBtn(){
    //   console.log('clicked btn')
    // },
    // onInputFoucs(){
    //   console.log('is focused')
    // },
    //  onBlur(){
    //   console.log('bluer') //когда не в фокусе
    // }
  } 
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- стили scoped используются только для компонента, то есть ограничиваем облость видимости стил -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
