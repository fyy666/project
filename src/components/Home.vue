<template>
  <el-container class="home-container">
    <el-header>
      <div class="header-left">
        <span>南水北调东线一期工程江苏段<br />调度运行管理应用软件系统</span>
      </div>
      <div class="header-right">
        <el-menu
          :default-active="activeIndex2"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#0c54b6"
          text-color="#fff"
          active-text-color="#2778E1"
        >
          <el-menu-item index="1">调度一张图</el-menu-item>
          <el-menu-item index="2">日常调度管理</el-menu-item>
          <el-menu-item index="3">水量调度方案</el-menu-item>
          <el-menu-item index="4">实时调度管理</el-menu-item>
          <el-menu-item index="5">调度统计评价</el-menu-item>
          <el-menu-item index="6">供水经营管理</el-menu-item>
          <el-menu-item index="7">紧急响应管理</el-menu-item>
        </el-menu>
      </div>
      <el-button @click="logout">退出</el-button>
    </el-header>
    <el-main>Main</el-main>
  </el-container>
</template>

<script>
export default {
  methods: {
    logout () {
      window.sessionStorage.clear();
      this.$router.push("/login");
    }
  }
};
</script>

<style lang="less" scoped>
.home-container {
  height: 100%;
}

.el-header {
  display: flex;
  justify-content: space-between;
  background-color: #0c54b6;
  align-items: center;
}
.header-left {
  color: #fff;
  text-align: center;
}
.header-left img {
  width: 50px;
  height: 50px;
}
.el-main {
  background-color: #eeeeee;
}
</style>
