<template>
  <div class="footr">

    <menu-main></menu-main>
    <menu-social></menu-social>

    <div class="footr__copyright">
      <div>2006 - 2017 © Sentimony Records</div>
      <div>All Rights Reserved</div>
      <div>
        <img class="footr__copyright-logo" src="/assets/img/svg-icons/sentimony-records-logo.svg" alt="Sentimony Records Logo SVG">
      </div>
    </div>

    <div class="footr__powered">
      <div>Web development by <a href="https://ihororlovskyi.com" target="_blank" rel="noopener">Ihor Orlovskyi</a></div>
      <div>Design by <a href="https://rooster-chess.netlify.com" target="_blank" rel="noopener">Anton Pivniuk</a></div>
    </div>

  </div>
</template>

<script>
  var MenuMain = require('./menu-main.vue');
  var MenuSocial = require('./menu-social.vue');

  module.exports = {
    components: {
      'menu-main': MenuMain,
      'menu-social': MenuSocial
    }
  };
</script>

<style lang="scss?outputStyle=compressed">
  .footr {
    padding: 100px .6em;
    background-color: #000;
    font-size: 12px;
    color: rgba(#fff,.5);
    position: relative;

    &__copyright {
      margin: 0 auto 2em;

      &-logo {
        display: block;
        margin: .5em auto 0;
        max-width: 30px;
        height: auto;
      }
    }

    &__powered {
      margin: 0 auto 2em;
      font-size: 10px;
    }
  }
</style>
