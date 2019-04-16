<template>
  <div v-if="data">
    {{ data }}
  </div>
</template>

<script>
  export default {
    async asyncData ({ app }) {
      const data = await app.$axios.$get(`http://localhost/api`)
      return { data }
    }
  }
</script>
