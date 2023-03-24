<script setup>
import {ref, computed} from 'vue'
const contador1 = ref(0)
const contador2 = ref(0)
const mostrar = ref(true)
const soma = computed(() => contador1.value + contador2.value)
</script>
<template>
  <div class="container">
    <button class="btn btn-primary" @click="mostrar = !mostrar">ok</button>
    <div v-if="mostrar"  class="mt-4">
      
      <button class="btn btn-primary" @click="contador1--">-</button>
      <span class="mx-3 fs-4">{{ contador1 }}</span>
      <button class="btn btn-primary" @click="contador1++">+</button>
    </div>
  <div >
    <button class="btn btn-dark" @click="contador2--">-</button>
    <span class="mx-3 fs-4">{{ contador2 }}</span>
    <button class="btn btn-dark" @click="contador2++">+</button>
    <div >
      <div >
        <p class="fs-4">A soma é {{ soma }}</p>
        <p v-if="soma > 10" class="fs-4">A soma é maior do que 10</p>
        <p v-else class="fs-4">A soma é menor ou igual a 10</p>
        <p v-if="soma % 2 === 0" class="fs-4">A soma é maior do que 10</p>
        <p v-else class="fs-4">A soma é ímpar</p>

      </div>
    </div>
  </div>
</div>

</template>

<style scoped>

</style>
