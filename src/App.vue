<template>
  <div class="app-wrapper">
    <AppHeader />

    <main class="content">
      <router-view />
    </main>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import AppHeader from '@/components/AppHeader.vue';

export default Vue.extend({
  name: 'App',
  components: { AppHeader },
});
</script>

<style lang="scss">
@import "@/assets/scss/variables.scss";
@import "@/assets/scss/mixins.scss";

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.app-wrapper {
  position: relative;
  min-height: 100vh;
  overflow: hidden;
  font-family: $font-base;
}

.content {
  position: relative;
  z-index: 1;
  padding: 0 $spacing-md;
  @include flex-center(flex, center, start, column);
  color: $text;
  font-size: $font-size-base;
}
</style>
