<script>
import { RouterLink, RouterView } from 'vue-router'
export default {
  components: {
    RouterLink,
    RouterView
  }
}
</script>

<template>
  <header>
    <div class="wrapper">
      <h1>Hello to vue</h1>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/testcomputed">Test Computed</RouterLink>
      </nav>
    </div>
  </header>
</template>