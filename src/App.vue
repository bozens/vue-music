<template>
  <div id="app">
    <Header/>
    <Tab/>
    <router-view/>
  </div>
</template>

<script>
import Header from 'components/header/index'
import Tab from 'components/tab/index'
export default {
  name: 'App',
  components: {
    Header,
    Tab
  }
}
</script>

<style scoped lang="stylus">
  @import "common/stylus/variable.styl"
#app {
  color $color-theme
}
</style>
