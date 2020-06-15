<template>
  <div class="header">
    <div class="nav-topbar">
      <div class="container">
        <div class="topbar-menu">
          <a href="javascript:;">小米商城</a>
          <a href="javascript:;">MUI</a>
          <a href="javascript:;">云服务</a>
          <a href="javascript:;">协议规则</a>
        </div>
        <div class="topbar-user">
          <a href="javascript:;" @click="login">登录</a>
          <a href="javascript:;" @click="login">注册</a>
          <a href="/#/order/list" v-if="username">我的订单</a>
          <a href="javascript:;" class="my-cart" @click="goToCart"><span class="icon-cart"></span>购物车({{cartCount}})</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavHeader'
}
</script>

<style lang="scss">
  .header{
    .nav-topbar{
      height: 39px;
      line-height: 39px;
      background-color: #333333;
      color: #b0b0b0;
    }
    .container{
      width: 1226px;
      margin-right: auto;
      margin-left: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      a{
        display: inline-block;
        color: #b0b0b0;
        margin-left: 17px;
      }
      .my-cart{
        width: 110px;
        background-color: #FF6600;
        text-align: center;
        color: #ffffff;
      }
      .icon-cart{
        display: inline-block;
        width: 16px;
        height: 12px;
        background: url('/imgs/icon-cart-checked.png') no-repeat center;
        background-size: contain;
        margin-right: 4px;
      }
    }
  }
</style>
