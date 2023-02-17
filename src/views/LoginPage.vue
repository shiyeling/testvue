<template>
  <div class="login-module">
    <div class="login-logo">
      <img src="/static/product-logo.png" alt="" />
      <span>{{ subtitle }}</span>
    </div>
    <div class="login-box">
      <div class="login-title">用户登陆</div>
      <div class="login-form">
        <div class="login-form-row">
          <a-input
            v-model="name"
            ref="name"
            placeholder="用户名"
            autocomplete="off"
            @keyup.enter="login"
          >
            <a-icon slot="prefix" type="user" />
          </a-input>
        </div>
        <a-button type="primary" :loading="loading" @click="login">
          登录
        </a-button>
      </div>
    </div>
    <div class="copyright">
      Copyright © {{ new Date().getFullYear() }} 南京微著信息科技有限公司 All
      Rights Reserved<br />
      技术支持：南京微著信息科技有限公司
    </div>
    <div class="info">系统版本: V2.1</div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const subtitle = "llab";
const name = ref<string>("abc");
const loading = ref<boolean>(false);

function login() {
  loading.value = true;
  console.log("fixed");
}
</script>
<style scoped lang="scss"></style>
