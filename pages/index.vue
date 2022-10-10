<template>
  <div>
    <div :class="divClass">Reactivity</div>
  </div>
</template>

<script setup>
import { computed, ref } from 'vue'
import { useDisplay } from 'vuetify'

const { lgAndUp } = useDisplay()
const divClass = computed(() => lgAndUp.value ? 'green' : 'red')
</script>

<style>
.green {
  background-color: green;
}
.red {
  background-color: red;
}
</style>