<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://img1.qunarzz.com/p/tts9/1802/7d/7045f8196aeef502.jpg_r_640x420x90_a3645734.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">北京出发-跟团游 纯玩0购物巴厘岛5晚</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe632;</span>39</div>
      </div>
    </div>
    <fade-animation>
      <common-gallary @close="handeGallaryClose" :imgs="imgs" v-show="showGallary"></common-gallary>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/gallary'
import FadeAnimation from 'common/fade/fadeanimation'
export default {
  data() {
    return {
      showGallary: false,
      imgs:[
        'https://img1.qunarzz.com/p/tts9/1802/7d/7045f8196aeef502.jpg_r_1280x840x90_e9642f0b.jpg',
        'https://img1.qunarzz.com/p/tts1/1801/f1/cf752e67b2c29502.jpg_r_1280x840x90_278258e3.jpg'
      ]
    }
  },
  methods: {
    handleBannerClick() {
      this.showGallary = true
    },
    handeGallaryClose() {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left:0
    right:0
    bottom: 0
    line-height: .6rem
    color:#fff
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    .banner-title
      flex:1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      padding:0 .4rem
      height: .32rem
      line-height:.32rem
      margin-top: .14rem
      border-radius: .2rem
      font-size: .24rem
      background: rgba(0, 0, 0, .8)
      .banner-icon
        font-size: .24rem
</style>
