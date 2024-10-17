<script setup>
  import brique from './components/brique.vue';
  import pad from './components/pad.vue';
  import ball from './components/ball.vue';
  import { ref } from 'vue';

  const tableau = ref([0,0,0,0,0,0,0,0,0,0])
  const etatBrique = (place) => {
    console.log(place)
    tableau.value[place]++
 }

</script>




<template>

  <div v-for="brique, index in 10">
    <brique @click="etatBrique(index)" :state="tableau[index]" />
  </div>
  <div>
    <ball />
  </div>
  <div>
    <pad />
  </div>

</template>




<style scoped>

</style>
