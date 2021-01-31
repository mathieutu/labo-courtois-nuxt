<template>
  <div class="prose prose-sm sm:prose lg:prose-lg xl:prose-2xl mx-auto">
    {{ home }}
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    async asyncData({ $content }) {
      // const home = await $content('home').fetch()

      return {
        home: {},
      }
    },
  })
</script>

<style>
</style>
