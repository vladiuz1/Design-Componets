<template>
  <div class="main-layout">
    <v-toolbar color="purple" class="main-layout__header" height="auto"></v-toolbar>
    <div class="main-layout__page">
      <navigation-drawer class="main-layout__navbar"></navigation-drawer>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import NavigationDrawer from './Components/NavigationDrawer.vue'

export default {
  name: 'MainLayout',
  components: {
    NavigationDrawer
  }
}
</script>

<style lang="scss">
.main-layout {
  height: 100vh;
  &__header {
    min-height: 64px;
  }
  &__page {
    display: flex;
    height: calc(100% - 64px);
  }
}
@include tablet {
  .main-layout {
    &__page {
      flex-direction: column;
    }
    &__navbar {
      order: 2;
    }
  }
}
</style>
