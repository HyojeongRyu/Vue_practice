<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Hello Vue!</h1>
  <h2>{{food}}</h2>
  <input type="text" v-model="food"/>
  <!-- v-html은 텍스트가 아닌 태그 그대로 받아들인다. -->
  <div v-html = "alertMessage"></div>
  <!-- 받을 데이터를 신뢰할 수 있을 때 사용 -->
  <div>{{test}}</div>
  <img v-bind:src="imageSource" alt="random">
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      animal: "monkey",
      food: "banana",
      choco: "milk",
      alertMssage: "<h1>Caution!!!</h1>",
      test: `<button onclick="document.querySelector('body').style.display = 'none'">test</button>`,
      imageSource: "https://placeimg.com/100/100/any"
    }
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
input{
  font-size: 20px;
}
</style>
