<script setup lang="ts">
import { ref } from 'vue';
import SizeSelector from './components/SizeSelector.vue';

const selectedSize = ref('L');

</script>

<template>
  <h1>Seleccione la talla: {{ selectedSize }}</h1>
  <SizeSelector
   :selected-size="selectedSize"
   @onChangeSize="selectedSize = $event"
    />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: blue;
  margin-top: 60px;
}

button {
  padding: 5px;
  margin-right: 5px;
  border: none;
  border-radius: 5px;
  width: 75px;
  cursor: pointer;
}

.active {
  background-color: black;
  color: white;
  transition: all 0.3s ease-out;
}
</style>
