<template>
  <h1>Vue パレット</h1>
  <div class="app">
    <div
      class="palette"
      v-on:mousemove="changeColor"
      v-on:click="selectColor"
      v-bind:style="{ backgroundColor: `rgba(${red}, ${green}, 200, 0.5)` }"
    ></div>
    <p>rgba( {{ red }}, {{ green }}, 200, 0.5 )</p>
    <div class="colors-container">
      <div
        class="mini-palette"
        v-for="(miniPalette, index) in miniPalettes"
        :key="index"
        v-bind:style="{
          backgroundColor: `rgba(${miniPalette.red}, ${miniPalette.green}, 200, 0.5)`,
        }"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      red: 0,
      green: 0,
      miniPalettes: [],
    }
  },
  methods: {
    changeColor(e) {
      this.red = e.offsetX
      this.green = e.offsetY
    },
    selectColor() {
      this.miniPalettes.push({ red: this.red, green: this.green })
    },
  },
}
</script>

<style>
.app {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
}

.palette {
  width: 255px;
  height: 255px;
}

.mini-palette {
  min-width: 60px;
  height: 60px;
}

.colors-container {
  display: flex;
  flex-wrap: wrap;
  width: 300px;
  padding-top: 8px;
  /* background-color: rgba(106, 168, 73, 0.686); */
}
</style>
