<template>
  <div id="app">
    <FileUpload></FileUpload>
  </div>
</template>

<script>
import FileUpload from './components/FileUpload'

export default {
  name: 'App',
  components: {
    FileUpload
  }
}
</script>

<style>
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}
#app {
  height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
