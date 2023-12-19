<template>
  <header>
    <Navbar />
  </header>
  <main>
    <router-view />
  </main>
  <footer class="bg-dark">
  </footer>
</template>

<script>
import { computed } from 'vue'
import { AppState } from './AppState'
import Navbar from './components/Navbar.vue'

export default {
  setup() {
    return {
      appState: computed(() => AppState)
    }
  },
  components: { Navbar }
}
</script>
<style lang="scss">
@import "./assets/scss/main.scss";

:root {
  --main-height: calc(100vh - 32px - 64px);
}

.background {
  background-image: url('https://th.bing.com/th/id/R.23ad2ade410c8e0fd9fdf2b439316f3d?rik=qkvVAjRUSl38LA&pid=ImgRaw&r=0');
  background-position: center;
  background-size: cover;
}
</style>
