<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="nav-container">
    <nav class="nav-main">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/blog">Blog</RouterLink>
    </nav>
  </div>
  <div class="router-view">
    <RouterView />
  </div>
</template>

<style scoped>
.router-view {
  padding: 2rem 2rem 2rem 0;
}

.nav-container {
  position: fixed;
  width: 100%;
  height: 2rem;
  padding: 10px 0 10px 0;
  z-index: 10;
}

.nav-main {
  width: fit-content;
  display: flex;
  flex-direction: row;
  gap: 0.25rem;
  margin: auto;
  padding: 0.25rem;
  border-radius: 100px;
  background-color: var(--nav-cont-bg);
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
  background-color: var(--nav-button-bg-selected);
}

nav a:not(.router-link-exact-active):hover {
  background-color: var(--nav-button-bg-hover);
}

nav a {
  text-decoration: none;
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: none;
  border-radius: 100px;
  border-left: 1px solid var(--color-border);
  color: white;
}

nav a:active {
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
