<script setup lang="ts">
import { ref, onMounted } from 'vue'

const currentPath = ref('')

onMounted(() => {
  currentPath.value = window.location.href
})
</script>

<template>
  <main>
    <div class="">
      <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    </div>
    <div class="container">
      <div className="inner-container">
        <h2 class="header">
          You’ve just ignited a new
          <span class="library">Vue 3</span> static site!
        </h2>
        <span class="pathname">
          {{ currentPath }}
        </span>
      </div>
      <p class="footer">Made in Nigeria with 💖</p>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 7px;
  align-items: center;
  justify-content: center;
  border: 1px solid #eaeaea;
}
.logo {
  width: 200px;
  height: 200px;
}
.container {
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: 25px;
}
.inner-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.header {
  font-size: 36px;
  font-weight: 400;
  color: #344054;
}
.pathname {
  color: #004eeb;
  font-size: 20px;
}
.footer {
  font-size: 20px;
  font-weight: 500;
  color: #344054;
}
.library {
  color: #00dc82;
  font-weight: 600;
}
</style>
