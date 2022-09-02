<template>
  <div class="header">
    <img src="~/static/logo.png" alt="" />

    <div class="navigation">
      <div class="btn" id="nav" @click="anim()"></div>
      <div class="nav" id="menu">
        <div class="text" id="text">
          <a href="">who am i?</a>
          <a href="">what have i done?</a>
          <a href="">where did i learn that?</a>
          <a href="">wanna go for a coffee?</a>
        </div>
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
      let txt = document.getElementById("text");
      if (!element.classList.contains("anim")) {
        element.classList.add("anim");
        menu.style.height = "100%";
        txt.style.height = "100%";
      } else {
        element.classList.remove("anim");
        menu.style.height = "0%";
        txt.style.height = "0%";
      }
    },
  },
};
</script>