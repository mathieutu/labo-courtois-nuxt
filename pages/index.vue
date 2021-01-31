<template>
  <div class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto">
    <div v-for="employe in employes" :key="employe.name">
      <h2>{{ employe.name }}</h2>
      <h3>role</h3>
      <img :src="employe.photo" :alt="employe.name">
      <p>{{ employe.description }}</p>
    </div>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    async asyncData({ $content }) {
      const employes = await $content('employes').fetch()

      return {
        employes,
      }
    },
  })
</script>

<style>
</style>
