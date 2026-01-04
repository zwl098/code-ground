<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <nav class="main-nav">
    <div class="container nav-content">
      <div class="logo">Code<span class="gradient-text">Ground</span></div>
      <div class="links">
        <router-link to="/">Home</router-link>
        <!-- Showcase link will be added later -->
      </div>
    </div>
  </nav>

  <RouterView />
</template>

<style scoped>
.main-nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 80px;
  backdrop-filter: blur(10px);
  z-index: 100;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.nav-content {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  font-weight: 700;
  font-size: 1.5rem;
  letter-spacing: -0.02em;
}

.links {
  display: flex;
  gap: 2rem;
}

.links a {
  font-weight: 500;
  font-size: 0.95rem;
  opacity: 0.8;
}

.links a:hover, .links a.router-link-active {
  opacity: 1;
  color: var(--accent-primary);
}
</style>
