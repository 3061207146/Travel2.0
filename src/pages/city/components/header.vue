<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped lang="stylus">
@import '~styles/varibles.styl'
.header
  position: relative
  overflow:hidden
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  color: #fff
  background: $bgColor
  font-size: .32rem
  .header-back
    position: absolute
    top:0
    width: .6rem
    text-align: center
    font-size: .4rem
    color:#fff
</style>
