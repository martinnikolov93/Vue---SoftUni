<template>
  <div id="app">
    <div class="counter">
      <h1>
        60
      </h1>
    </div>
    <section class="memory-game">
      <div v-on:click="showCard()" class="memory-card" data-framework="aurelia">
        <img class="front-face" src="./assets/img/aurelia.svg" alt="Aurelia" />
        <img v-if="test" class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="aurelia">
        <img class="front-face" src="./assets/img/aurelia.svg" alt="Aurelia" />
        <img v-if="test" class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>

      <div class="memory-card" data-framework="vue">
        <img class="front-face" src="./assets/img/vue.svg" alt="Vue" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="vue">
        <img class="front-face" src="./assets/img/vue.svg" alt="Vue" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>

      <div class="memory-card" data-framework="angular">
        <img class="front-face" src="./assets/img/angular.svg" alt="Angular" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="angular">
        <img class="front-face" src="./assets/img/angular.svg" alt="Angular" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>

      <div class="memory-card" data-framework="ember">
        <img class="front-face" src="./assets/img/ember.svg" alt="Ember" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="ember">
        <img class="front-face" src="./assets/img/ember.svg" alt="Ember" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>

      <div class="memory-card" data-framework="backbone">
        <img class="front-face" src="./assets/img/backbone.svg" alt="Backbone" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="backbone">
        <img class="front-face" src="./assets/img/backbone.svg" alt="Backbone" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>

      <div class="memory-card" data-framework="react">
        <img class="front-face" src="./assets/img/react.svg" alt="React" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
      <div class="memory-card" data-framework="react">
        <img class="front-face" src="./assets/img/react.svg" alt="React" />
        <img class="back-face" src="./assets/img/js-badge.svg" alt="JS Badge" />
      </div>
    </section>
  </div>
</template>

<script>


export default {
  name: 'App',
  data: function(){
    return {
      test: false,
    }
  },
  methods: {
    showCard(){
      
    }
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  height: 100vh;
  display: flex;
  background-image: linear-gradient(120deg, #d4fc79 0%, #96e6a1 100%);
}

#app {
  width: 100%;
  padding: 7%;
}
.memory-game {
  width: 640px;
  height: 640px;
  margin: auto;
  display: flex;
  flex-wrap: wrap;
  perspective: 1000px;
}

.memory-card {
  width: calc(25% - 10px);
  height: calc(33.333% - 10px);
  margin: 5px;
  position: relative;
  transform: scale(1);
  transform-style: preserve-3d;
  transition: transform .5s;
  box-shadow: 1px 1px 1px rgba(0,0,0,.3);
}

.disable-card {
  pointer-events: none;
}

.memory-card:active {
  transform: scale(0.97);
  transition: transform .2s;
}

.memory-card.flip {
  transform: rotateY(180deg);
}

.front-face,
.back-face {
  width: 100%;
  height: 100%;
  padding: 20px;
  position: absolute;
  border-radius: 5px;
  background: #FFF29E;
  backface-visibility: hidden; 
}

.front-face {
  transform: rotateY(180deg);
}

.counter {
  position: absolute;
  top: 0px;
  right: 0px;
}
</style>
