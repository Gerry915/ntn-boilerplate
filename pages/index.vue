<template>
  <section id="landing" class="flex justify-center items-center">
    <div class="video-wrapper">
      <video src="/bg.mp4" autoplay loop muted></video>
    </div>
    <div class="z-10 text-white text-6xl text-center">
      <div>
        <h1>Nuxt Tailwind + Netlify CMS</h1>
      </div>
      <div class="item-wrapper flex">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#landing {
  position: relative;
  height: 100vh;
  width: 100vw;
  background-color: green($color: #000000);
}

.item-wrapper {
  margin: 5rem 0;
  height: 55px;
  width: 110vw;
  background-color: green;
  position: relative;

  & div {
    height: 100%;
    transform: skew(-15deg) translateX(-15%);
    flex-basis: 10%;
  }

  & div:nth-child(odd) {
    background: greenyellow;
  }
  & div:nth-child(even) {
    background: black;
  }
}

.video-wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  overflow: hidden;

  &::after {
    content: '';
    backdrop-filter: blur(15px);
    background: linear-gradient(180deg, rgba(84, 5, 17, 0.7), rgba(3, 106, 65, 0.3));
    background-blend-mode: overlay;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  & video {
    object-fit: cover;
    min-width: 100%;
    min-height: 100%;
  }
}
</style>
