<template>
  <div id="app">
    <div class="background">
      <div style="margin-top: 140px">
        <div style="font-size:18px;padding: 40px 15px 8px;color:#dc0303">红色导览</div>
        <el-carousel trigger="click" height="150px" interval="5000">
          <el-carousel-item v-for="item in imgItems" :key="item">
            <img :src="item" style="width: 100%" />
          </el-carousel-item>
        </el-carousel>
      </div>

      <div style="font-size:18px;padding: 30px 15px 8px;color:#dc0303">开始探索</div>
      <el-row type="flex" class="row-bg">
        <el-col :span="12">
          <div class="item1" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/48')">
          </div>
          <span style="margin-left:6%;color:#dc0303;font-weight: 900">泸定桥</span>
        </el-col>
        <el-col :span="12">
          <div class="item2" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/51')">
          </div>
          <span style="margin-left:6%;color:#dc0303;font-weight: 900">磨西古镇</span>
        </el-col>
      </el-row>
      <el-row type="flex" class="row-bg">
        <el-col :span="12">
          <div class="item3" @click="jumpToAppSys('https://xr.cmiivip.com/mobile/detail/1/48')">
          </div>
          <span style="margin-left:6%;color:#dc0303;font-weight: 900;">大瀑布</span>
        </el-col>
      </el-row>
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
    background: url("~@/assets/background-red.jpg");
    height: 100%;
    background-size: cover;
  }

  .el-carousel {
    width: 90%;
    margin: 0 auto;
  }

  .list {
    margin-top: 80px
  }

  .item1 {
    margin: 0 6% 5%;
    background-image: url("~@/assets/coming.jpg");
    background-size: cover;
    height: 90px
  }
  .item2 {
    margin: 0 6% 5%;
    background-image: url("~@/assets/circle.jpg");
    background-size: cover;
    height: 90px
  }
  .item3 {
    margin: 20% 6% 5%;
    background-image: url("~@/assets/avatar.jpg");
    background-size: cover;
    height: 90px
  }
</style>
