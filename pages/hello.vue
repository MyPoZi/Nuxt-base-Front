<template>
  <div v-if="data">
    {{ data }}
  </div>
</template>

<script>
  export default {
    async asyncData ({ app }) {
      const data = await app.$axios.$get(`https://laravel-base-api.herokuapp.com/api/`)
      return { data }
    }
  }
</script>
