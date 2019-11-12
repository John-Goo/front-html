<template>
  <div style="background: #ccc;">
    <el-radio-group v-model="isCollapse" style="margin-bottom:20px;">
      <el-radio-button :label="false">展开</el-radio-button>
      <el-radio-button :label="true">收起</el-radio-button>
    </el-radio-group>
    <el-menu default-active="1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose"
      :collapse="isCollapse">
      <el-menu-item index="1">
        <i class="el-icon-s-home"></i>
        <span slot="title">首页</span>
      </el-menu-item>
      <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-user-solid"></i>
          <span slot="title">用户管理</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="1-1">用户信息</el-menu-item>
          <el-menu-item index="1-2">意见反馈</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group>
          <el-menu-item index="1-3">用户资料</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <span slot="title">用户分布</span>
          <el-menu-item index="1-4-1">大数据</el-menu-item>
        </el-submenu>
      </el-submenu> 
      <el-submenu index="3">
          <template slot="title">
            <i class="el-icon-s-marketing"></i>
            <span slot="title">表格管理</span>
          </template>
          <el-menu-item-group>
            <el-menu-item index="3-1">带斑马纹表格</el-menu-item>
            <el-menu-item index="3-2">固定表头</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group>
            <el-menu-item index="3-3">筛选表格</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group>
            <el-menu-item index="3-5">树形数据与懒加载</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
      <el-menu-item index="4">
        <i class="el-icon-s-data"></i>
        <span slot="title">图表管理</span>
      </el-menu-item>
      <el-menu-item index="5">
        <i class="el-icon-s-order"></i>
        <span slot="title">表单管理</span>
      </el-menu-item>
      <el-menu-item index="6">
        <i class="el-icon-s-grid"></i>
        <span slot="title">系统管理</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        isCollapse: false
      };
    },
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>
<style lang="scss" scoped>
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
</style>