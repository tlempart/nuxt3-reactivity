<template>
  <div>
    <div :class="divClass">Reactivity</div>
  </div>
</template>

<script setup>
import { computed, ref } from 'vue'
import { useDisplay } from 'vuetify'

const counter = ref(1)
const { lgAndUp } = useDisplay()

const divClass = computed(() => {
  const result = lgAndUp.value ? 'green' : 'red'
  console.log('result', result)

  return result
})
</script>

<style>
  .green {
    background-color: green;
  }
  .red {
    background-color: red;
  }
</style>
