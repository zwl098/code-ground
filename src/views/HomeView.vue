<script setup lang="ts">


const openProject = () => {
  window.open('https://github.com/zwl098/code-ground', '_blank')
}
</script>

<template>
  <main class="home-view">
    <div class="container hero">
      <h1 class="title">
        Welcome to my <br />
        <span class="gradient-text">Code Ground</span>
      </h1>
      <p class="subtitle">
        A showcase of my frontend engineering journey, <br />
        featuring Vue 3, TypeScript, and modern web tools.
      </p>
      
      <div class="actions">
        <button class="btn primary" @click="openProject">Explore Code</button>
        <button class="btn secondary">View Tools</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
.home-view {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  background: radial-gradient(circle at 50% 50%, rgba(99, 102, 241, 0.1) 0%, transparent 50%);
}

.hero {
  text-align: center;
  padding: 4rem 2rem;
}

.title {
  font-size: 4rem;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  letter-spacing: -0.02em;
}

.subtitle {
  font-size: 1.25rem;
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 3rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.actions {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
}

.btn {
  padding: 0.75rem 2rem;
  border-radius: 50px;
  font-weight: 600;
  font-size: 1rem;
  transition: all var(--transition-fast);
}

.btn.primary {
  background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
  color: white;
  box-shadow: 0 4px 20px var(--accent-glow);
}

.btn.primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 30px var(--accent-glow);
}

.btn.secondary {
  border: 1px solid var(--bg-secondary);
  background: rgba(255, 255, 255, 0.05);
  color: var(--text-primary);
  backdrop-filter: blur(10px);
}

.btn.secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: var(--text-secondary);
}

@media (max-width: 768px) {
  .title {
    font-size: 2.5rem;
  }
}
</style>
