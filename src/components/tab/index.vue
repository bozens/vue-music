<template>
  <div class="tab">
    <router-link tag="div" class="tab-item" :to="item.path" v-for="(item,index) in linkList" :key="index">
      <span class="tab-link">{{item.name}}</span>
    </router-link>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'Tab',
  data() {
    return {
      linkList: [
        {name: '推荐', path: '/recommend'},
        {name: '歌手', path: '/singer'},
        {name: '排行', path: '/rank'},
        {name: '搜索', path: '/search'}
      ]
    }
  }
}

</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~common/stylus/variable"
  .tab
    display: flex
    height: 44px
    line-height: 44px
    font-size: $font-size-medium
    .tab-item
      flex: 1
      text-align: center
      .tab-link
        padding-bottom: 5px
        color: $color-text-l
      &.router-link-active
        .tab-link
          color: $color-theme
          border-bottom: 2px solid $color-theme
</style>
