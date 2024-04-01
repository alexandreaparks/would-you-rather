<script setup>
// PARENT

import WouldYouRather from './components/WouldYouRather.vue'

import { ref } from 'vue'

// this data will be passed to the Child component
const wyrQuestion = ref('Dance or Sing?')
const wyrAnswer1 = ref('Dance')
const wyrAnswer2 = ref('Sing')

// store user's answer
const userSelection = ref('')



</script>

<template>

  <h1>Would You Rather...</h1>

  <!--link data in Parent component to Child props-->
  <!--the Child prop 'question' binds to the Parent 'wyrQuestion'-->
  <WouldYouRather
      v-bind:question="wyrQuestion"
      v-bind:answer1="wyrAnswer1"
      v-bind:answer2="wyrAnswer2"
  ></WouldYouRather>

</template>

<style scoped>

</style>
