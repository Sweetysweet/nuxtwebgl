<template>
  <div class="layout">
    <div class="layout__animation">
      <Animation />
    </div>
    <div class="layout__content">
      <nuxt />
    </div>
    <div class="layout__navigation">
      <Navigation />
    </div>
  </div>
</template>
<script>
import Navigation from "@/Components/Navigation";
import Animation from "@/Components/Animation";
export default {
  components: {
    Navigation,
    Animation
  }
};
</script>
<style>
body {
  background: #000;
  font-family: helvetica, sans-serif;
  position: relative;
}
.layout__navigation {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}
.layout__content {
  font-size: 100px;
  letter-spacing: -1px;
  font-weight: bold;
  color: #fff;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  min-height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;
  text-transform: uppercase;
}
.slide-enter-active {
  transition: all 0.3s ease-in-out;
}
.slide-leave-active {
  transition: all 0.3s ease-in-out;
}
.slide-enter {
  transform: translateY(-100%);
  opacity: 0;
}
.slide-enter-to {
  transform: translateY(0%);
  opacity: 1;
}
.slide-leave {
  transform: translateY(0);
  opacity: 1;
}
.slide-leave-to {
  transform: translateY(100%);
  opacity: 0;
}
.letter {
  display: inline-block;
  position: relative;
}
</style>
