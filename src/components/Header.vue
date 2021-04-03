<template>
  <header>
    <nav>
      <router-link to="/"
        ><img
          class="nav-item"
          alt="carlos logo"
          width="100px"
          src="@/assets/cruiz_logo_small.png"
      /></router-link>
      <router-link
        class="nav-item"
        v-for="menu in menus"
        :key="menu.name"
        :to="menu.url"
        >{{ menu.name }}</router-link
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
  padding: 1em 0;
  align-items: center;
}

.nav-item {
  margin: 0 2em;
}

nav a {
  font-weight: bold;
  text-decoration: none;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
