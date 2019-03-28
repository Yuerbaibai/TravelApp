<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//himg1.qunarzz.com/imgs/201812/12/C._M0DCif_djPyXHiPi1024.jpg">
      <div class="banner-info">
        <div class="banner-title">海燕时间</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe67f;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  data () {
    return {
      imgs: ['https://himg2.qunarzz.com/imgs/201603/04/C._M0DCiyngOwMrLhzi480.jpg',
        'https://himg1.qunarzz.com/imgs/201705/26/C._M0DCiclO9g928Uli480.jpg'],
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
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
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    color: #fff
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .2rem
    .banner-number
      line-height: .32rem
      height: .3rem
      margin-top: .1rem
      padding: 0 .3rem
      border-radius: .2rem
      background: rgba(0, 0, 0, .8)
      font-size: .24rem
      .banner-icon
        font-size: .24rem
</style>
