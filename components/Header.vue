<template>
  <div class="header">
    <img src="~/static/logo.png" alt="" id="logo" />

    <div class="navigation">
      <div class="btn" id="nav" @click="anim()"></div>
      <div class="nav" id="menu">
        <a href="#about" @click="anim()">about me</a>
        <a href="#background" @click="anim()">background</a>
        <a href="#projects" @click="anim()">things done</a>
        <a href="#contact" @click="anim()">up for a coffee?</a>
      </div>
    </div>
  </div>
</template>

<style scoped src="~/styles/header.css">
</style>

<script>
export default {
  methods: {
    anim() {
      let element = document.getElementById("nav");
      let menu = document.getElementById("menu");
      if (!element.classList.contains("anim")) {
        element.classList.add("anim");
        menu.style.height = "100%";
      } else {
        element.classList.remove("anim");
        menu.style.height = "0%";
      }
    },
  },
};
</script>