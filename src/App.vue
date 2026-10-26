<script setup>
import SiteHeader from './components/SiteHeader.vue';
import HeroSection from './components/HeroSection.vue';
import StorySection from './components/StorySection.vue';
import SeasonalMenu from './components/SeasonalMenu.vue';
import SpaceSection from './components/SpaceSection.vue';
import VisitSection from './components/VisitSection.vue';
</script>

<template>
  <a class="skip-link" href="#main">跳转到主要内容</a>
  <SiteHeader />
  <main id="main">
    <HeroSection />
    <StorySection />
    <SeasonalMenu />
    <SpaceSection />
    <VisitSection />
  </main>
</template>
