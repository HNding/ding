<template>
  <div id="index">
    <div class="login_box">
      <el-row type="flex" justify="center">
        <el-col :span="20">
          <h2>污水监控系统</h2>
          <el-form ref="form" :model="form" label-width="0.8rem">
            <el-form-item label="账号：">
              <el-input v-model="form.username" placeholder="请输入账号！"></el-input>
            </el-form-item>
            <el-form-item label="密码：">
              <el-input v-model="form.pwd"  placeholder="请输入密码！" show-password></el-input>
            </el-form-item>
            <el-form-item class="login_button">
              <el-row>
                <el-col :span="12">
                  <el-button type="primary">登录</el-button>
                </el-col>
                <el-col :span="12">
                  <router-link to="/register">注册</router-link>
                  <!--<a href="#">注册</a>-->
                </el-col>
              </el-row>
            </el-form-item>
          </el-form>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'index',
  data () {
    return {
      form: {
        username: '',
        pwd: ''
      }
    }
  }
}
</script>

<style>
  html,body{
    width: 100%;
    height: 100%;
    background: url("../assets/l.jpg") no-repeat center;
    background-size: cover;
    font-size: 0.3rem;
  }
  #index{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .login_box{
    background: rgba(255,255,255,0.5);
    width: 7rem;
    padding: 0.1rem;
    text-align: center;
    border-radius: 0.2rem;
  }
  .login_box /deep/ .el-form-item{
    margin: 0.5rem 0;
  }
  .login_box /deep/ .el-form-item__label{
    text-align: left;
    width: 0.9rem !important;
    font-size: 0.26rem;
  }
  .login_box /deep/ .el-form-item__content{
    margin-left:0.9rem !important;
  }
  .login_button /deep/ .el-form-item__content{
    margin-left:0rem !important;
  }
  .login_button /deep/ .el-button{
    line-height: 1.5;
    font-size: 0.2rem;
    padding: 0.15rem 0.3rem;
  }
  .login_button a{
    font-size: 0.4rem;
  }
  .login_box /deep/ .el-input__inner{
    height: 0.6rem;
    font-size: .2rem;
  }
</style>
