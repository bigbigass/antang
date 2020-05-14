<template>
  <el-container>
    <el-header style="text-align: right; font-size: 12px">
      <el-row>
        <el-col :span="8">
          <!--图标区-->
          <div class="grid-content">
            <el-row>
              <el-col :span="5"><div class="grid-content "></div></el-col>
              <el-col :span="5">
                <div class="grid-content " v-on:click="mainPage" style="cursor:pointer">
                  <el-image style="width: 60px; height: 60px" :src="require('./assets/logo.png')" :fit="fit"></el-image>
                </div>
                </el-col>
              <el-col :span="14">
                <div class="grid-content " style="text-align:left">
                  <font size="6">安棠</font>
                </div>
                </el-col>
            </el-row>
          </div>
        </el-col>
        <el-col :span="8">
          <div class="grid-content"></div>
        </el-col>
        <el-col :span="8">
          <!--菜单-->
          <div class="grid-content">
            <el-menu
              :default-active="activeIndex"
              class="el-menu-demo"
              mode="horizontal"
              @select="handleSelect"
            >
              <el-menu-item index="1">处理中心</el-menu-item>
              <el-submenu index="2">
                <template slot="title">我的工作台</template>
                <el-menu-item index="2-1">选项1</el-menu-item>
                <el-menu-item index="2-2">选项2</el-menu-item>
                <el-menu-item index="2-3">选项3</el-menu-item>
                <el-submenu index="2-4">
                  <template slot="title">选项4</template>
                  <el-menu-item index="2-4-1">选项1</el-menu-item>
                  <el-menu-item index="2-4-2">选项2</el-menu-item>
                  <el-menu-item index="2-4-3">选项3</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-menu-item index="3" disabled>消息中心</el-menu-item>
              <el-menu-item index="4">
                <a target="_blank">订单管理</a>
              </el-menu-item>
            </el-menu>
          </div>
        </el-col>
      </el-row>
    </el-header>

    <el-main style="padding: 0px;">
      <router-view></router-view>
    </el-main>
  </el-container>
</template>

<style>
.el-header {
  background-color: #ffffff;
  color: #333;
  line-height: 60px;
}

.el-main {
  height: 700px;
  background-color: #ffffff;
  padding: 0px;
}
html,
body,
#app,
.el-container {
  padding: 0px;
  margin: 0px;
  height: 100%;
}

.bg-purple {
    background: red;
  }

.grid-content {
  border-radius: 4px;
  min-height: 60px;
}
</style>

<script>

export default {
    data() {
      
      return {
      }
    },methods:{
      mainPage:function(){this.$router.push({path:'/'})}
    }
  };
</script>