<template>
  <div id="app">
    <div class="background">
      <div style="display: flex;margin: 320px 50px">
        <div style="width: 40%;">
          <div style="font-size:28px;color:#dc0303">红色导览</div>
          <el-carousel trigger="click" interval=5000>
            <el-carousel-item v-for="item in imgItems" :key="item">
              <img :src="item" />
            </el-carousel-item>
          </el-carousel>
        </div>
        <div style="width: 60%;margin: -20px 0px 0 100px">
          <div style="font-size:22px;color:#dc0303">开始探索</div>
          <el-row type="flex" class="row-bg">
            <el-col :span="12">
              <div class="item1" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/48')">
              </div>
              <span style="margin-left:4%;color:#dc0303;font-size:20px">泸定桥</span>
            </el-col>
            <el-col :span="12">
              <div class="item2" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/51')">
              </div>
              <span style="margin-left:4%;color:#dc0303;font-size:20px">磨西古镇</span>
            </el-col>
          </el-row>
          <el-row type="flex" class="row-bg">
            <el-col :span="12">
              <div class="item3" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/48')">
              </div>
              <span style="margin-left:4%;color:white;font-size:20px">大瀑布</span>
            </el-col>
          </el-row>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import banner3 from './assets/dapubu.gif'
import banner2 from './assets/moxiguzhen.gif'
import banner1 from './assets/ludingqiao.gif'
export default {
  components: {

  },
  data() {
    return {
      imgItems: [banner1, banner2, banner3]
    }
  },
  mounted() {
  },

  methods: {
    jumpToAppSys(item) {
      window.open(item, '_blank')
    }
  }
}
</script>

<style lang="scss" scoped>
 .background {
    background: url(./assets/background-red-pc.png) no-repeat;
    background-size: 100% 100%;
    height: 100%;
  }

  .el-carousel__container {
    height: 360px;
  }

  .el-carousel {
    margin: 20px
  }

  .list {
    margin-top: 80px
  }

  .item1 {
    margin: 6% 6% 4% 0;
    background-image: url("~@/assets/coming.jpg");
    background-size: cover;
    height: 190px
  }
  .item2 {
    margin: 6% 0 4% 6%;
    background-image: url("~@/assets/circle.jpg");
    background-size: cover;
    height: 190px
  }
  .item3 {
    margin: 6% 6% 4% 0;
    background-image: url("~@/assets/avatar.jpg");
    background-size: cover;
    height: 190px
  }

</style>
