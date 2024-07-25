<script setup>
import BlogPreviewCardLink from '@/components/BlogPreviewCardLink.vue';
</script>

<template>
  <main>
    <BlogPreviewCardLink />
  </main>
</template>

<style scoped lang="scss">
main {
  height: 100%;
  padding: var(--spacing-300);
  display: grid;
  place-content: center;
}
</style>
