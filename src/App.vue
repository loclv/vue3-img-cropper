<template>
  <div id="app">
    <Cropper
      class="cropper"
      :src="img"
      :stencil-props="{
        aspectRatio: 10 / 12,
      }"
      @change="change"
    />
  </div>

  <HelloWorld  msg="Hello! 🍀" />
</template>

<script lang="ts" setup>
import { Cropper, type Coordinates } from "vue-advanced-cropper"
import "vue-advanced-cropper/dist/style.css"

/**
 * Photo by [Vasilis Karkalas](https://www.pexels.com/@vasilis-karkalas-155349971/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from Pexels
 */
const img = "https://images.pexels.com/photos/11301535/pexels-photo-11301535.jpeg"

const change = ({ coordinates, canvas }: { coordinates: Coordinates; canvas: HTMLCanvasElement}) => {
  console.log("🌳 ~ coordinates", coordinates)
  console.log("🚀 ~ canvas", canvas)
}
</script>

<style scoped>
.cropper {
  height: 600px;
}
</style>