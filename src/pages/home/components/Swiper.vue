<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {id: '0001', imgUrl: '//img1.qunarzz.com/vc/2a/96/76/d149c7a3a5b113f876f9a66e09.png'},
        {id: '0002', imgUrl: '//img1.qunarzz.com/vc/80/80/1a/72b8f423c33e581ca72fc136da.jpg'}
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 30%
  background: #eee
  .swiper-img
    width: 100%
</style>
