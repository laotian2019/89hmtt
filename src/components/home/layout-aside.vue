<template>
<!-- 左侧导航 -->
   <div class="layout-aside">
       <div class="title">
           <img src="../../assets/img/logo_admin.png" alt="">
       </div>
       <!-- //开启路由模式 :router="true" 简写为router-->
        <el-menu router style="width:231px" background-color="#353b4e" text-color="#adafb5" active-text-color="#ffd04b">
        <!-- 导航组件  index作为跳转的地址 类似于router-link to-->
        <el-menu-item index="/home">
            首页
        </el-menu-item>
        <!-- 二级导航 -->
        <el-submenu index='1'>
            <span slot="title">内容管理</span>
            <!-- 放置el-menu-item -->
            <el-menu-item index="/home/publish">发布文章</el-menu-item>
            <el-menu-item index='/home/articles'>内容列表</el-menu-item>
            <el-menu-item index='/home/comment'>评论列表</el-menu-item>
            <el-menu-item index='/home/material'>素材管理</el-menu-item>
        </el-submenu>
        <el-submenu index='2'>
            <span slot="title">粉丝管理</span>
            <!-- 放置el-menu-item -->
            <el-menu-item index='/home/picture'>图文数据</el-menu-item>
            <el-menu-item index='/home/fansinfo'>粉丝概况</el-menu-item>
            <el-menu-item index='/home/fanslife'>粉丝画像</el-menu-item>
            <el-menu-item index='/home/fanslist'>粉丝列表</el-menu-item>
        </el-submenu>
        <el-menu-item>
            账户信息
        </el-menu-item>
    </el-menu>
   </div>
</template>

<script>
// export default {
//   data () {
//     return {
//       userInfo: {}// 用户信息
//     }
//   },
//   created () {
//     let token = window.localStorage.getItem('user-token') // 获取令牌信息
//     // 查询数据
//     this.$axios({
//       url: '/user/profile',
//       // headers参数
//       headers: {
//         Authorization: `Bearer ${token}`
//       }
//     }).then(result => {
//       this.userInfo = result.data.data // 获取用户个人信息
//     })
//   }
// }
</script>

<style lang='less' scoped>
    .layout-aside{
        width: 230px;
        overflow: hidden;
        .title{
            text-align: center;
            background-color: #2e2f32;
            padding: 10px 0;
            img {
                height: 35px;
            }
        }
    }
</style>
