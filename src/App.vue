<template>
  <div id="app">
    <router-view/>
    <vue-particles 
      color="#dedede"
        :particleOpacity="0.7"
        :particlesNumber="80"
        shapeType="circle"
        :particleSize="4"
        linesColor="#dedede"
        :linesWidth="1"
        :lineLinked="true"
        :lineOpacity="0.4"
        :linesDistance="150"
        :moveSpeed="3"
        :hoverEffect="true"
        hoverMode="grab"
        :clickEffect="true"
        clickMode="push"
    >
      
    </vue-particles>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  @import 'style/reset.css';
  #app{
    height: 100%;
  }
  #particles-js {
    background: url('assets/sky.871d198.jpg');
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
</style>
