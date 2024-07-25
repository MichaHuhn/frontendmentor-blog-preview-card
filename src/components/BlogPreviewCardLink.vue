<template>
  <a href="#" class="blog-preview-card-link">
    <article class="blog-preview-card">
      <img src="@/assets/images/illustration-article.svg" alt="" class="blog-image">
      
      <section class="card-content">
        <div class="blog-category">Learning</div>
        <p class="blog-publish-date">Published 21 Dev 2023</p>
        <h1 class="blog-title">HTML & CSS foundations</h1>
        <p class="blog-description">
          These languages are the backbone of every website, defining structure, content, and presentation.
        </p>
      </section>
      
      <div class="blog-author">
        <img src="@/assets/images/avatar.webp" alt="Author avatar" class="blog-author-avatar">
        <p class="blog-author-name">Greg Hooper</p>
      </div>
    </article>
  </a>
</template>

<style scoped lang="scss">
@import '@/styles/base/typography';

.blog-preview-card-link {
  text-decoration: none;
  outline: none;
  
  &:hover, &:focus-visible {
    .blog-preview-card {
      --box-shadow-offset: 16px;
      
      .blog-title {
        color: var(--color-yellow);
      }
    }
  }
  
  .blog-preview-card {
    --padding: var(--spacing-300);
    --inner-border-radius: 10px;
    --box-shadow-offset: 8px;
    --transition-duration: 250ms;
    
    max-width: 24rem;
    padding: var(--padding);
    color: var(--color-gray-950);
    background-color: var(--color-white);
    border: 1px solid var(--color-gray-950);
    border-radius: calc(var(--inner-border-radius) + var(--padding));
    box-shadow: var(--box-shadow-offset) var(--box-shadow-offset) black;
    cursor: pointer;
    display: grid;
    gap: var(--spacing-300);
    transition: box-shadow var(--transition-duration);
    
    .blog-image {
      border-radius: var(--inner-border-radius);
    }
    
    .card-content {
      display: grid;
      gap: var(--spacing-150);
      
      .blog-category {
        width: fit-content;
        padding: var(--spacing-50) var(--spacing-150);
        background-color: var(--color-yellow);
        @extend %typography-text-preset-3-bold;
        border-radius: 4px;
      }
      
      .blog-publish-date {
        @extend %typography-text-preset-3;
      }
      
      .blog-title {
        @extend %typography-text-preset-1;
        transition: color var(--transition-duration);
      }
      
      .blog-description {
        color: var(--color-gray-500);
        @extend %typography-text-preset-2;
      }
    }
    
    .blog-author {
      display: flex;
      align-items: center;
      gap: var(--spacing-150);
      
      .blog-author-avatar {
        width: 2rem;
      }
      
      .blog-author-name {
        @extend %typography-text-preset-3-bold;
      }
    }
  }
}
</style>
