<template>
  <div class="logo-cube">
    <div class="logo-cube-box1">
      <img :src="showImg[0]" alt="">
    </div>
    <div class="logo-cube-box2">
      <img :src="showImg[1]" alt="">
    </div>
    <div class="logo-cube-box3">
      <img :src="showImg[2]" alt="">
    </div>
    <div class="logo-cube-box4">
      <img :src="showImg[3]" alt="">
    </div>
    <div class="logo-cube-box5">
      <img :src="showImg[4]" alt="">
    </div>
    <div class="logo-cube-box6">
      <img :src="showImg[5]" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: "logoCube",
  props: {
    showImg: {
      type: Array,
      default() {
        return []
      }
    }
  }
}
</script>

<style scoped>
  .logo-cube {
    width: 50px;
    height: 50px;
    transform-style: preserve-3d;
    transform: rotateX(45deg) rotateZ(45deg);
    animation: rotate 20s infinite linear;
  }

  .logo-cube > div {
    width: 50px;
    height: 50px;
/*    opacity: 0.7;*/
    position: absolute;
  }

  .logo-cube img {
    height: 50px;
    width: 50px;
  }

  .logo-cube-box1 {
    transform: rotateY(90deg) translateZ(25px);

  }

  .logo-cube-box2 {
    transform: rotateY(-90deg) translateZ(25px);
  }

  .logo-cube-box3 {
    transform: rotateX(90deg) translateZ(25px)
  }

  .logo-cube-box4 {
    transform: rotateX(-90deg) translateZ(25px)
  }

  .logo-cube-box5 {
    transform: rotateY(180deg) translateZ(25px);
  }

  .logo-cube-box6 {
    transform: rotateY(0deg) translateZ(25px);
  }

  @keyframes rotate {
    from {
      transform: rotateX(0) rotateZ(0);
    }
    to {
      transform: rotateX(1turn) rotateZ(1turn);
    }
  }
</style>
