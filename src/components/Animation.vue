<template>
  <div id="animation">
    <h1>
      <span class="letter">g</span><span class="letter">a</span><span class="letter">b</span><span class="letter">y</span>
      <div id="space"></div><span class="letter">d</span><span class="letter">e</span><span class="letter">v</span><span class="letter">w</span><span
        class="letter">e</span><span class="letter">b</span>
    </h1>
  </div>
</template>

<script>
import anime from 'animejs/lib/anime.es.js';
  export default {
    name: 'Animation',
    mounted() {
      // let tl = anime.timeline({})
      anime({
        targets: '.letter',
        keyframes: [
          { translateY: -50, easing: 'linear', duration: 200 },
          { translateY: 0, rotateY: 360, color: '#42b983', duration: 2000 },
          { scale: 1.2, color: '#FFAA00', duration: 200, easing: 'linear', },
          { scale: 1, color: '#FF0000', duration: 200, easing: 'linear', },
        ],
        delay: function(el, i) { return i * 150 },
      })
    },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  #animation {
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;

    h1 {
      font-size: 6rem;
      font-weight: 500;
      text-transform: uppercase;
      display: flex;
      justify-content: center;
      align-items: center;

      #space {
        width: 1rem;
      }
    }
  }
</style>