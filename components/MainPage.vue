<template>
  <div>
    <div class="header">
      <img src="./assets/logo.png" class="logo-img"/>
      <div class="header-text" style="display: inline-block;">
        <div class="title-text">求职招聘管理系统</div>
        <div class="text-eng">
          <div class="line"></div>Recruitment management system<div class="line"></div>
        </div>
        <div class="right-header">
          个人注册&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;公司注册
        </div>
        <div class="search">
          <el-input placeholder="职位搜索">
            <template slot="append">搜索</template>
          </el-input>
        </div>
      </div>
    </div>
    <div class="nav">
      <el-menu
        default-active="1"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="#283535"
        text-color="#fff"
        active-text-color="#ffd04b">
        <el-menu-item index="1">首页</el-menu-item>
        <el-menu-item index="2">个人注册</el-menu-item>
        <el-menu-item index="3">公司注册</el-menu-item>
        <el-menu-item index="4">招聘信息</el-menu-item>
        <el-menu-item index="5">个人用户</el-menu-item>
        <el-menu-item index="6">公司信息</el-menu-item>
        <el-menu-item index="7">职场资讯</el-menu-item>
        <el-menu-item index="8">用户中心</el-menu-item>
      </el-menu>
    </div>
    <div class="title">
      智能招聘管理系统，提升企业人才获取竞争力
    </div>
    <div class="content">
      <div class="news">
        <el-menu default-active="1" mode="horizontal">
          <el-menu-item index="1">最新资讯</el-menu-item>
        </el-menu>
        <div class="news-list">
          <div class="news-text">
            系统公告9
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告8
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告7
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告6系统公告系统公告系统公告系统公告系统公告系统公告
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告5
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告4系统公告系统公告系统公告系统公告系统公告系统公告系统公告
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告3
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
        <div class="news-list">
          <div class="news-text">
            系统公告1
          </div>
          <div>
            2021/1/23 19:57:32
          </div>
        </div>
      </div>
      <div class="login">
        <div class="login-title">
          用户登录
        </div>
        <el-form :model="loginForm" ref="loginForm" label-position="left" label-width="60px" class="form">
          <el-form-item label="角色：">
              <el-select placeholder="请选择" v-model="loginForm.role">
                <el-option label="个人会员" value="1"></el-option>
                <el-option label="公司会员" value="2"></el-option>
              </el-select>
          </el-form-item>
          <el-form-item label="账号：">
            <el-input type="text" v-model="loginForm.account" auto-complete="off" placeholder="账号/手机号"></el-input>
          </el-form-item>
          <el-form-item label="密码">
            <el-input type="password" v-model="loginForm.password" auto-complete="off" placeholder="密码"></el-input>
          </el-form-item>
        </el-form>
        <el-button style="width: 40%;margin-left: 114px;margin-bottom: 21px;" @click.native.prevent="login">登 录</el-button>
      </div>
    </div>
    <div class="bottom-content">
      <div class="ent">
        <el-menu default-active="1" mode="horizontal">
          <el-menu-item index="1">最新企业</el-menu-item>
        </el-menu>
        <div class="ent-list">
          <img src="./assets/ent-1.jpg" class="ent-img"/>
          <div class="ent-text">联想科技有限公司</div>
        </div>
        <div class="ent-list">
          <img src="./assets/ent-2.jpg" class="ent-img"/>
          <div class="ent-text">百度科技有限公司</div>
        </div>
        <div class="ent-list">
          <img src="./assets/ent-3.jpg" class="ent-img"/>
          <div class="ent-text">华为电子科技有限公司</div>
        </div>
        <hr/>
      </div>
      <div class="notice">
        <div class="notice-title">
          最新公告
        </div>
        <div class="notice-list">系统公告9系统公告9系统公告9系统公告9系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
        <div class="notice-list">系统公告9</div>
      </div>
    </div>
    <div class="footer">
      <div class="footer-text">快速导航
        <div class="footer-mini">求职注册<br/>招聘注册</div>
      </div>
      <div class="footer-text">求职招聘
        <div class="footer-mini">招聘信息<br/>公司信息<br/>个人会员</div>
      </div>
      <div class="footer-text">相关链接
        <div class="footer-mini">职场资讯</div>
      </div>
      <div class="footer-text info">获取更多最新消息
        <div class="img-info">
          <img src="./assets/news-1.jpg" class="footer-img"/>
          <img src="./assets/news-2.jpg" class="footer-img"/>
          <img src="./assets/news-3.jpg" class="footer-img"/>
        </div>
        <div class="img-info">
          <img src="./assets/qr-1.jpg" class="footer-qr"/>
          <img src="./assets/qr-2.jpg" class="footer-qr"/>
        </div>
        <div class="footer-mini">微信加关注</div>
      </div>
    </div>
    <div class="footer-bottom">
      <img src="./assets/footer.jpg" class="img-bottom">
      <div class="bottom-text">
        2019-2020求职招聘管理系统&nbsp;&nbsp;求职招聘管理系统版权所有
        <div class="login-text">管理员登录</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainPage',
  data () {
    return {
      loginForm: {}
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    login () {}
  }
}
</script>
<style>
  .header {
    width: 100%;
    height: 150px;
  }
  .logo-img {
    width: 110px;
    position: relative;
    top: 40px;
    left: 256px;
    display: inline-block;
  }
  .title-text {
    font-size: 40px;
    position: relative;
    left: 256px;
    display: inline-block;
    font-weight: 500;
  }
  .header-text: {
    margin-left: 300px;
    margin-right: 300px;
  }
  .line {
    display: inline-block;
    width: 20px;
    height: 4px;
    border-top: 1px solid black;
  }
  .text-eng {
    display: inline-block;
    position: relative;
    top: 28px;
    right: 62px;
  }
  .right-header {
    display: inline-block;
    position: relative;
    bottom: 30px;
    left: 276px;
  }
  .search {
    display: inline-block;
  }
  .title {
    line-height: 100px;
    height: 100px;
    text-align: center;
    background-color: #283535;
    color: white;
    font-size: 35px;
  }
  .content {
    display: flex;
    justify-content: center;
  }
  .news-list > div {
    display: inline-block;
  }
  .news-text {
    display: inline-block;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    width: 300px;
    margin-right: 250px;
  }
  .login {
    width: 300px;
    background-color: #283535;
    margin-top: 25px;
    margin-left: 25px;
    border-radius: 10px;
    padding-left: 12px;
    padding-right: 12px;
  }
  .el-select {
    width: 240px!important;
  }
  .el-form-item__label {
    color: white;
  }
  .el-input-group__append {
    color: white;
    background-color: #283535;
  }
  .el-menu-demo {
    display: flex;
    justify-content:center;
  }
  .bottom-content {
    display: flex;
    justify-content: center;
  }
  .ent {
    width: 703px;
    margin-right: 28px;
  }
  .ent-list {
    display: inline-block;
    width: 230px;
  }
  .ent-text {
    width: 140px;
    text-align: center;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .ent-img {
    width: 140px;
    height: 140px;
    box-shadow: 0 0 10px #8d9d9d;
  }
  .notice {
    width: 324px;
    margin-top: 28px;
  }
  .notice-title {
    background-color: #283535;
    color: white;
    padding-left: 12px;
    padding-right: 12px;
    height: 50px;
    line-height: 50px;
  }
  .notice-list {
    padding-left: 12px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .footer {
    margin-top: 12px;
    display: flex;
    justify-content: space-between;
    padding-left: 135px;
    padding-top: 28px;
    background-color: #f1f1f1;
  }
  .footer-text {
    width: 332px;
    font-size: 20px;
    font-weight: bold;
  }
  .footer-mini {
    width: 80px;
    font-size: 12px;
    font-weight: 200;
    text-align: center;
  }
  .footer-img {
    display: inline-block;
    margin-top: 16px;
    width: 60px;
    height: 60px;
  }
  .info {
    width: 300px;
    margin-right: 216px;
    text-align: center;
  }
  .img-info {
    display: flex;
    justify-content: space-between;
  }
  .footer-qr {
    margin-top: 16px;
    width: 90px;
    height: 90px;
  }
  .footer-bottom {
    padding-top: 28px;
    text-align: center;
    background-color: #f1f1f1;
  }
  .img-bottom {
    width: 20px;
  }
  .bottom-text {
    font-size: 12px;
    font-weight: 200;
    text-align: center;
    display: inline-block;
    position: relative;
    top: 11px;
  }
  .login-text {
    font-size: 12px;
    font-weight: 400;
    position: relative;
    left: 120px;
  }
</style>
