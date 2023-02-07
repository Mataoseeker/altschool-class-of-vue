<template>
  <h1>Color Picker Game</h1>
<br />

  <div class="msg">{{ message }}</div>
<br />
  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>

</template>

<script setup>
import useColorPickerGame from "../composables/ColorPickerGame";
const { colors, message, matchColor } = useColorPickerGame();
</script>

<style>
.msg{
  font-size: 1.0rem;
  font-weight: bold;
}
h1{
  color: blueviolet;
}
button{
  padding: 10px;
  margin: 10px;
  border: 1px solid black;
  border-radius: 5px;
  background-color: rgb(46, 42, 42);
  color: White;
  font-size: 1.2rem;  
}
</style>