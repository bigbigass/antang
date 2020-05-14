<template>
  <div>
    <el-row :gutter="20">
      <el-col :span="2">
        <div class="grid-main"></div>
      </el-col>
      <el-col :span="20">
        <!--走马灯-->
        <div class="grid-main">
          <el-carousel :interval="2000" arrow="always" height="800px" >
            <el-carousel-item v-for="item in 5" :key="item">
              <el-image
                style="width: 100%; height: 100%"
                :src="require('../assets/zoumadeng/'+item+'.jpg')"
                :fit="none"
              ></el-image>
            </el-carousel-item>
          </el-carousel>
        </div>
      </el-col>
      <el-col :span="2">
        <div class="grid-main"></div>
      </el-col>
    </el-row>

    <el-row :gutter="20">
      <el-col :span="2">
        <div class="grid-gap"></div>
      </el-col>
      <el-col :span="20">
        <div class="grid-gap">
        </div>
      </el-col>
      <el-col :span="2">
        <div class="grid-gap"></div>
      </el-col>
    </el-row>

    <el-row :gutter="20">
      <el-col :span="2">
        <div class="grid-main"></div>
      </el-col>
      <el-col :span="20">
         <el-divider><i class="el-icon-caret-bottom"></i></el-divider>
        <div class="grid-main">
          <font size="9">产品展示</font>
        </div>
      </el-col>
      <el-col :span="2">
        <div class="grid-main"></div>
      </el-col>
    </el-row>
  </div>
</template>
<style scoped>
.grid-main {
  border-radius: 4px;
  min-height: 800px;
}
.grid-gap{
  min-height: 100px;
}
.grid-aside {
  height: 500px;
}
.bg-red {
  background-color: red;
}
</style>