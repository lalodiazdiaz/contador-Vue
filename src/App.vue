<script setup>
import { ref } from "vue";

const counter = ref(0);

const increment = () => {
  counter.value++;
};
const decrement = () => {
  counter.value--;
};
</script>

<template>
  <div id="root">
    <div class="infoContainer">
      <h1 class="title">Contador Vue</h1>
      <h1 class="counter">{{ counter }}</h1>
      <div class="buttonContainer">
        <button class="button" v-on:click="increment">Incremetar</button>
        <button class="button" v-on:click="decrement">Decremenar</button>
      </div>
    </div>
  </div>
</template>

<style>
#root {
  display: flex;
  width: 100%;
  height: 100%;
  justify-content: center;
  align-items: center;
}
.infoContainer {
  display: flex;
  background-color: darkgray;
  width: 20%;
  height: 250px;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  border-radius: 20%;
}
.buttonContainer {
  width: 90%;
  height: 50px;
  margin-bottom: 20px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.button {
  background-color: lightblue;
  height: 80%;
  border-radius: 10px;
  text-align: center;
  font-size: 18px;
  font-weight: bold;
}
</style>
