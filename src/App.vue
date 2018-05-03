<template>
  <div id="app">
    <img class="logo" src="./assets/logo.svg">
    <table-component/>
  </div>
</template>

<script>
import TableComponent from './components/TableComponent'

export default {
  name: 'App',
  components: {
    TableComponent
  },
  mounted () {
    this.$lx.init()
      .then(setup => {
        this.$lx.ready({})
      })
  }
}
</script>

<style lang="stylus" scoped>
  #app
    display flex
    flex-flow column
    justify-content center
    align-items center

  .logo
    width 250px
    margin 2rem
    align-self flex-end
</style>
