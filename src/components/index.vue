<template>
    <div>
      <el-container>
        <el-header style="background: rgba(105,105,105,0)">
          <el-row>
            <el-col :span="6"><div class="grid-content bg-purple">XXXXXXXX</div></el-col>
            <el-col :span="12"><div class="grid-content bg-purple-light">
              <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
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
                <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
              </el-menu>
              <div class="line"></div>
            </div></el-col>
            <el-col :span="4">
              <div style="margin-top: 15px;">
              <el-input placeholder="请输入内容" v-model="input3" class="input-with-select">
                <el-button slot="append" icon="el-icon-search"></el-button>
              </el-input>
            </div></el-col>
            <el-col :span="2">

            </el-col>
          </el-row>
        </el-header>

        <el-container style="height: 1000px;">
          <el-aside width="400px" style="background: #0a0d69">
            <el-row>
              <el-col :span="24"><div class="grid-content bg-purple-dark"></div></el-col>
            </el-row>

          </el-aside>

          <el-main style="background: #426925">
            <div class="block">
              <el-carousel height="150px">
                <el-carousel-item v-for="item in 4" :key="item">
                  <h3 class="small">{{ item }}</h3>
                </el-carousel-item>
              </el-carousel>
            </div>
            <div>
              <template>
                <ul class="infinite-list" v-infinite-scroll="load" style="overflow:auto">
                  <li v-for="i in 10" class="infinite-list-item">{{ i }}</li>
                </ul>
              </template>

            </div>

          </el-main>
        </el-container>

        <el-footer style="background: #69141c">Footer</el-footer>
      </el-container>
    </div>
</template>

<script>
    export default {
        name: "index"
    }
</script>

<style scoped>

</style>
