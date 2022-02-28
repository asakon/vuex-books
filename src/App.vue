<template>
  <div id="app">
    <p>書籍は全部で{{ booksCount }}冊あります。</p>
    <ul v-for="b of getBookByPrice(4000)" v-bind:key="b.isbn">
      <li>{{ b.title }} {{ b.price }}円<br>ISBN: {{ b.isbn }}</li>
    </ul>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'App',
  computed: mapGetters([ 'booksCount', 'getBookByPrice' ])
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
