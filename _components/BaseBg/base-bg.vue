<template>
  <div class="base-bg">
    <img class="base-bg__img lazyload"
         :src="baseBgSrc"
         :data-srcset="baseBgSrc1x + ',' + baseBgSrc2x"
         :alt="baseBgAlt">
  </div>
</template>

<script>
  module.exports = {
    data: function () {
      return {
        baseBgSrc: 'https://content.sentimony.com/assets/img/backgrounds/sombrero-red.jpg',
        baseBgSrc1x: 'https://content.sentimony.com/assets/img/backgrounds/sombrero-red@1x.jpg 1x',
        baseBgSrc2x: 'https://content.sentimony.com/assets/img/backgrounds/sombrero-red@2x.jpg 2x',
        baseBgAlt: 'Sombrero Red Background'
      }
    }
  };
</script>

<style lang="scss?outputStyle=compressed">
  .base-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;

    &__img {
      display: block;
      width: auto;
      height: 100%;
      max-width: inherit;
      position: relative;
      left: 50%;
      transform: translateX(-50%);
    }
  }
</style>
