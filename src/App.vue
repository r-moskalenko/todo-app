<template>
  <app-navbar 
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="(index) => activePage = index">
  </app-navbar>

  <page-viewer 
    :page="pages[activePage]">
  </page-viewer>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue'
import PageViewer from './components/PageViewer.vue'

export default {
  name: 'App',
  components: {
    AppNavbar,
    PageViewer
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          link: {text: "Home", url: 'index.html'},
          pageTitle: 'Home Page',
          content: 'This is the home content'
        },
        {
          link: {text: "About", url: 'about.html'},
          pageTitle: 'About Page',
          content: 'This is the about content'
        },
        {
          link: {text: "Contact", url: 'contact.html'},
          pageTitle: "Contact Page",
          content: 'This is the contact content'
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
