<template>
  <div class="login-container">
<div class="content">
  <t-card>
    <h1>Vue3-Admin</h1>
    <t-form ref="form" :data="LoginForm" class="login-form" :rules="rules" :colon="true" :label-width="0" >
      <t-form-item name="username">
        <t-input v-model="LoginForm.username" clearable placeholder="请输入用户名">
          <template #prefix-icon>
            <icon name="desktop"/>
          </template>
        </t-input>
      </t-form-item>

      <t-form-item name="password">
        <t-input v-model="LoginForm.password" type="password" clearable placeholder="请输入密码">
          <template #prefix-icon>
            <icon name="lock-on"/>
          </template>
        </t-input>
      </t-form-item>

      <t-form-item>
        <t-button theme="primary" type="submit" block>登录</t-button>
      </t-form-item>
    </t-form>
  </t-card>
</div>
  </div>
</template>

<script lang="ts" setup>
import {Icon} from "tdesign-vue-next"
import { reactive } from "vue";

const rules= {
  username:[
    {required: true, message: '请填写用户名'}
  ],
  password:[
    {required: true, message: '请填写密码'}
  ]
}

type LoginForm ={
  username:string,
  password:string
}

const LoginForm = reactive<LoginForm>({
  username:'',
  password:''
})
</script>

<style lang="less" scoped>
.login-container{
  width: 100vw;
  height: 100vh;
  background-color: #f5f5f5;
  display: flex;
  align-items: center;
  justify-content: center;
  .content{
    width: 400px;
    h1{
      text-align:center;
    }
    .login-form{
      margin: 20px 0;
    }
  }
}
</style>