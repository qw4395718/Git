<template>
  <el-container style="height:100%">
    <el-header style="padding:0px">
      <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="black"
        text-color="#fff"
        active-text-color="#FF8C00"
        router="true"
        style="z-index:1000"
      >
        <img class="logo" src="../img/LOGO.png" />
        <div class="title" style="color:#47c0e8">凯文</div>
        <div class="title" style="color:#ffb05b">云客服</div>
        <el-menu-item index="1" route="/" class="item">
          主页
        </el-menu-item>
        <el-menu-item index="2" route="EnterSignUpPage" class="item">
          获取解决方案
        </el-menu-item>
        <el-menu-item index="3" route="EnterSignUpPage" class="item">
          成为客服
        </el-menu-item>
        <el-menu-item index="4" route="EnterSignUpPage" class="item">
          加入我们
        </el-menu-item>
      </el-menu>
    </el-header>
    <el-main class=".el-main" style="padding:0px;position:relative">
      <router-view></router-view>
    </el-main>
  </el-container>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '0',
      activeIndex2: '1'
    }
  },

  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style>
.title {
  float: left;
  height: 60px;
  line-height: 60px;
  font-size: 30px;
  font-weight: 600;
  margin: 0;
  padding: 0;
  color: white;
}

.logo {
  margin-left: 30px;
  float: left;
  width: 111px;
  height: 60px;
}
.item {
  position: relative;
  left: 30px;
  user-select: none;
}
</style>
