<template>
  <div id="register">
    <div class="register_box">
      <el-row type="flex" justify="center">
        <el-col :span="22">
          <h2>注册</h2>
          <el-form ref="form" :model="form" label-width="0.8rem">
            <el-form-item label="用户名：">
              <el-input v-model="form.username" placeholder="请输入用户名！"></el-input>
            </el-form-item>
            <el-form-item label="密码：">
              <el-input v-model="form.pwd"  placeholder="请输入密码！" show-password></el-input>
            </el-form-item>
            <el-form-item label="再次输入密码：">
              <el-input v-model="form.rpwd"  placeholder="请二次输入密码！" show-password></el-input>
            </el-form-item>
            <el-form-item class="register_button">
              <el-row>
                <el-col :span="12">
                  <el-button type="primary">注册</el-button>
                </el-col>
                <el-col :span="12">
                  <router-link to="/"><el-button>返回</el-button></router-link>
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
  name: 'register',
  data () {
    return {
      form: {
        username: '',
        pwd: '',
        rpwd: ''
      }
    }
  }
}
</script>

<style>
  #register{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .register_box{
    background: rgba(255,255,255,0.5);
    width: 7rem;
    padding: 0.1rem;
    text-align: center;
    border-radius: 0.2rem;
  }
  .register_box /deep/ .el-form-item{
    margin: 0.5rem 0;
  }
  .register_box /deep/ .el-form-item__label{
    text-align: left;
    width: 2rem !important;
    font-size: 0.26rem;
    text-align: right;
  }
  .register_box /deep/ .el-form-item__content{
    margin-left:2rem !important;
  }
  .register_button /deep/ .el-form-item__content{
    margin-left:0rem !important;
  }
  .register_button /deep/ .el-button{
    line-height: 1.5;
    font-size: 0.2rem;
    padding: 0.15rem 0.3rem;
  }
  .register_box /deep/ .el-input__inner{
    height: 0.6rem;
    font-size: .2rem;
  }
</style>
