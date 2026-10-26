<script setup>
import { ref } from 'vue';

const menuOpen = ref(false);

function toggleMenu() {
  menuOpen.value = !menuOpen.value;
}

function closeMenu() {
  menuOpen.value = false;
}
</script>

<template>
  <header class="site-header">
    <a class="brand" href="#top" aria-label="巷里首页" @click="closeMenu">
      <span class="brand-mark" aria-hidden="true">巷</span>
      <span class="brand-word">巷里<span>XIANG LI</span></span>
    </a>
    <button
      class="menu-toggle"
      type="button"
      :aria-expanded="menuOpen"
      aria-controls="primary-nav"
      :aria-label="menuOpen ? '关闭导航菜单' : '打开导航菜单'"
      @click="toggleMenu"
    >
      <span></span><span></span>
    </button>
    <nav class="primary-nav" id="primary-nav" :class="{ 'is-open': menuOpen }" aria-label="主导航">
      <a href="#story" @click="closeMenu">关于巷里</a>
      <a href="#menu" @click="closeMenu">当季菜单</a>
      <a href="#space" @click="closeMenu">一餐一席</a>
      <a class="nav-cta" href="#visit" @click="closeMenu">来巷里坐坐 <span aria-hidden="true">↗</span></a>
    </nav>
  </header>
</template>
