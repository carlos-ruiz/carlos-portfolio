<template>
  <header>
    <nav>
      <img
        class="nav-item"
        alt="carlos logo"
        width="100px"
        src="@/assets/cruiz_logo_small.png"
      />
      <a
        class="nav-item"
        v-for="menu in menus"
        :key="menu.name"
        href="menu.url"
        >{{ menu.name }}</a
      >
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
    menus: [
      {name: 'About me', url: '/about-me'},
      {name: 'Curriculum', url: '/curriculum'},
      {name: 'Projects', url: '/projects'}
    ]
  })
}
</script>

<style scoped>
nav {
  width: 100%;
  display: flex;
  padding: 2em;
  align-items: center;
}

.nav-item {
  margin: 0 2em;
}
</style>
