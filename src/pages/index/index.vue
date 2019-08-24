<template>
  <div>
    <div class="search">
      <div class="input-box">
        <!-- 搜索框 -->
        <input type="text" @click="goSearch()" :class="{focused:focused}">
        <p display:none>取消</p>
      </div>
      <!-- 搜索历史 -->
      <div class="history"></div>
    </div>
    <swiper indicator-dots indicator-color="rgba(255, 255, 255, .3)" indicator-active-color="rgba(255, 255, 255, 1)" autoplay interval="2000" circular>
        <swiper-item>
          <a href="#">
            <img src="/static/uploads/banner1.png"/>
          </a>
        </swiper-item>
        <swiper-item>
          <a href="">
            <img src="/static/uploads/banner2.png"/>
          </a>
        </swiper-item>
        <swiper-item>
          <a href="#">
            <img src="/static/uploads/banner3.png"/>
          </a>
        </swiper-item>
    </swiper>
    <div class="nav">
      <a href="#"><img src="/static/uploads/icon_index_nav_1@2x.png" alt=""></a>
      <a href="#"><img src="/static/uploads/icon_index_nav_2@2x.png" alt=""></a>
      <a href="#"><img src="/static/uploads/icon_index_nav_3@2x.png" alt=""></a>
      <a href="#"><img src="/static/uploads/icon_index_nav_4@2x.png" alt=""></a>
    </div>
    <div class="floors">
      <div class="title">
        <a href="#"><img src="/static/uploads/pic_floor01_title.png" alt=""></a>
      </div>
      <div class="goods">        
        <a href="#"><img src="/static/uploads/pic_floor01_1@2x.png" alt=""></a>
        <a href="#"><img src="/static/uploads/pic_floor01_2@2x.png" alt=""></a>
        <a href="#"><img src="/static/uploads/pic_floor01_3@2x.png" alt=""></a>
        <a href="#"><img src="/static/uploads/pic_floor01_4@2x.png" alt=""></a>
        <a href="#"><img src="/static/uploads/pic_floor01_5@2x.png" alt=""></a>
      </div>
    </div>
</div>
</template>

<script>
  export default {
    data() {
      return {
        focused:false
      }
    },
    methods: {
      goSearch () {
        this.focused = true;
      }
    }
  }
</script>

<style scoped lang="less">
.search{
  padding: 15rpx 20rpx;
  background-color: #ea4451;
 .input-box{
  display:flex;
  height: 60rpx;
  input{
  background-color: #fff;
  border-radius: 8rpx;
  }
  p{
    width: 160rpx;
    font-size: 24rpx;
    color: #333;
    line-height: 60rpx;
    border: 1rpx solid #bfbebf;
    border-radius: 15rpx;
    margin-left: 20rpx;
    padding-left: 48rpx;
    display: none;
  }
  &.focused{
    background-color: #eee;
    p{
      display: block;
    }
} 
}
}
swiper{
  width: 750rpx;
  height: 340rpx;
  img{
    width: 750rpx;
    height: 340rpx;
  }
}
  .nav a{
    display:inline-block;
    padding: 24rpx 30rpx;
  }
  .nav img{
    width: 128rpx;
    height: 128rpx;
  }
  .floors .title{
    background-color: #f4f4f4;
    margin-bottom: 20rpx;
    img{
    width: 750rpx;
    height: 60rpx;
    padding-top: 30rpx;
  }
  }
  .floors .goods{
    overflow: hidden;
    margin: 20rpx 16rpx;
  }
  .floors .goods {
    a:nth-child(2n+1){
    margin-right: 0;
  }
  a{
    float: left;
    margin-right: 10rpx;
    margin-bottom: 10rpx;
  }
  a:first-child{
    width: 235rpx;
    height: 386rpx;
    margin-right: 10rpx;
  }
  a:nth-child(2),
  a:nth-child(5){
    width: 273rpx;
    height: 188rpx;
  }
  a:nth-child(3),
  a:nth-child(4){
    width: 193rpx;
    height: 188rpx;
  }
  img{
    width: 100%;
    height: 100%;
  }
  }
</style>