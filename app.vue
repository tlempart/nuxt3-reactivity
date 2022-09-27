<template>
  <div>
    <div :class="divClass">Reactivity</div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'
import { useDisplay } from 'vuetify'

const { lgAndUp } = useDisplay()
const divClass = ref('')

watch(lgAndUp, (val) => {
  console.log(val)
  divClass.value = val ? 'green' : 'red'
},{immediate:true})
</script>

<style>
.green {
  background-color: green;
}
.red {
  background-color: red;
}
</style>