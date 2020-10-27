<template>
  <div class="login-container">
    <!-- 导航栏 -->
    <van-nav-bar class="page-nav-bar" title="登录" />
    <!-- 登录表单 -->
    <van-form @submit="onSubmit">
      <van-field name="手机号" placeholder="请输入手机号">
        <i slot="left-icon" class="toutiao toutiao-shouji"></i>
      </van-field>
      <van-field name="验证码" placeholder="请输入验证码">
        <i slot="left-icon" class="toutiao toutiao-yanzhengma"></i>
        <template #button>
          <van-button class="send-sms-btn" round size="small" type="default"
            >发送验证码</van-button
          >
        </template>
      </van-field>
      <div class="login-btn-wrap">
        <van-button class="login-btn" block type="info" native-type="submit">
          登录
        </van-button>
      </div>
    </van-form>
    <div class="yinsi"><a href="javascript:;">----隐私政策----</a></div>
  </div>
</template>

<script>
export default {
  name: 'loginindex',
  components: {},
  data() {
    return {}
  },
  methods: {
    onSubmit() {
      console.log('submit')
    }
  }
}
</script>

<style scoped lang="less">
.login-container {
  .toutiao {
    font-size: 46px;
  }
  .send-sms-btn {
    width: 152px;
    height: 46px;
    line-height: 46px;
    background-color: #ededed;
    font-size: 22px;
    color: #666;
    border: none;
  }
  .login-btn-wrap {
    padding: 53px 33px;
    .login-btn {
      background-color: #6db4fb;
      border: none;
    }
  }
  .yinsi {
    position: absolute;
    bottom: 55px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 25px;
    color: #000;
  }
  /deep/ .van-field__button {
    border-left: 1px solid #eee;
  }
}
</style>
