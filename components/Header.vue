<template>
  <div class="header">
    <img src="~/static/logo.png" alt="" />

    <div class="nav-btn" @click="anim()">
      <div class="center" id="nav"></div>
      <div class="nav" id="menu">
        <div class="text">
          <a href="">who am i?</a>
          <a href="">what have i done?</a>
          <a href="">where did i learn that?</a>
          <a href="">wanna go for a coffee?</a>
        </div>
        <div class="bg"></div>
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
        menu.style.display = "block";
      } else {
        element.classList.remove("anim");
        menu.style.display = "none";
      }
    },
  },
};
</script>