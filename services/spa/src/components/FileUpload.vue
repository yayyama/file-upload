<template>
  <div class="container"
       :class="containerClass"
       @dragenter="dragenter"
       @dragleave.prevent="dragleave"
       @dragover="dragover"
       @drop.prevent="drop"
  >
    <div class="uploader"
    >
      file upload
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    containerClass: {
      'on-dragenter': false
    }
  }),
  methods: {
    dragenter: function (e) {
      if (e.target === e.currentTarget) {
        this.containerClass['on-dragenter'] = true
        console.log('** dragenter ' + new Date().getTime())
        console.log(e.target)
      }
    },
    dragleave: function (e) {
      if (e.target === e.currentTarget) {
        this.containerClass['on-dragenter'] = false
        console.log('-- dragleave ' + new Date().getTime())
        console.log(e.target)
      }
    },
    dragover: function () {
      // console.log('$$ dragover ' + new Date())
    },
    drop: function () {

    }
  }
}
</script>

<style scoped>
.container {
  width: 100%;
  height: 100%;
  display: flex;
}
.uploader {
  width: 200px;
  height: 300px;
  margin: auto;
  background-color: yellow;
}
.on-dragenter {
  background-color: pink;
}
</style>
