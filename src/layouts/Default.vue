<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link text-black-400 hover:text-blue-600 navi" to="/">Home</g-link>
        <g-link class="nav__link text-black-400 hover:text-blue-600 navi" to="/about">About</g-link>
        <g-link class="nav__link text-black-400 hover:text-blue-600 navi" to="/projects">Projects</g-link>
        <g-link class="nav__link text-black-400 hover:text-blue-600 navi" to="/blogs">Blogs</g-link>
      </nav>
    </header>
    <slot />
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}

.navi:hover {
  border-bottom: 2px solid cornflowerblue;
  transition: border-width 0.25s linear;
}
</style>
