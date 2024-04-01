<script setup>
// CHILD

import { ref } from 'vue'


// Child stores data passed from Parent in props
defineProps({
  question: String,
  answer1: String,
  answer2: String
})

const choice = ref('')


</script>

<template>

  <h2>Make your choice!</h2>

  {{ question }} <br>

  <!--v-model links both radio buttons together so only one can be clicked
  and connects them to the reactive state ref choice - when a radio button
  is selected, the reactive value of choice changes to the selected choice-->

  <!--v-bind links the radio button to it's related prop-->

  <input v-model="choice" v-bind:value="answer1" type="radio" id="answer-1">
  <label for="answer-1">{{ answer1 }}</label>

  <input v-model="choice" v-bind:value="answer2" type="radio" id="answer-2">
  <label for="answer-2">{{ answer2 }}</label>


</template>

<style scoped>

</style>
