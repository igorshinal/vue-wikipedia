<template>
  <div class="Search">
    <input type="text" class="Search__input" v-model="query" v-on:keyup.13="search">
    <button class="Search__button" @click="search">Найти</button>
  </div>

</template>

<script>
    export default {
      data() {
        return {
          query: ''
        }
      },
      methods: {
        search() {
          this.$store.dispatch('search', this.query)
        }
      }

    }
</script>

<style scoped>

</style>
