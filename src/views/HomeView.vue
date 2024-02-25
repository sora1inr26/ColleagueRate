<template>
  <div class="page">
    <div class="banner">
      如果这辈子都不为自己努力一次，那么你还有什么资格要求自己的生活有所改变？
    </div>
    <div class="search">
      <SearchComponent />
    </div>
    <div class="content">

    </div>
  </div>
</template>

<script>
import SearchComponent from '@/components/Search.vue';

export default {
  components: {
    SearchComponent
  },
};
</script>

<style scoped>
.page {
  min-height: calc(100vh - 64px - 64px);
}

.banner {
  height: 30px;
  /* 居中 */
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--color-primary-light-3);
}

.search {
  height: 100px;
  /* 居中 */
  display: flex;
  justify-content: center;
  align-items: center;

}

.content {
  min-height: 50vh;
}
</style>
