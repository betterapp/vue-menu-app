<template>
  <div id="app">
    <img alt="Vue logo" src="https://vuejs.org/images/logo.png">
    <Menu @link-clicked="linkClicked"></Menu>
    <Page :link="link"/>
  </div>
</template>

<script>
import Page from './components/Page.vue'
import Menu from './components/Menu.vue'

export default {
  name: 'App',
  data() {
    return {
      link: ''
    }
  },
  components: {
    Menu,
    Page
  },
  methods: {
    linkClicked(link) {
      this.link = link
    }
  }
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
