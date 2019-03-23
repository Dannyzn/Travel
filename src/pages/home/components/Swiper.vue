<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img 
          class="swiper-img" 
          :src="item.imgUrl"
        >
      </swiper-slide>
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
        swiperList: [{
            id: '0001',
            imgUrl: 'https://img1.qunarzz.com/vc/d3/79/22/687da305c0ea0532a2c7d3cc23.jpg'
        }, {
            id: '0002',
            imgUrl: 'https://img1.qunarzz.com/vc/b8/25/51/f6173dbd12c1a0f783abe73855.jpg'
        }]
      }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 30.47%
    background: #eee 
    .swiper-img
      width: 100%
</style>