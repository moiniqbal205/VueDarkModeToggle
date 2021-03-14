<template>
  <div 
    class="app"
    :class="mode"
  >
    <Header 
      :mode="mode"
      @toggle="toggle" 
    />
    <Content :mode="mode" />
  </div>
</template>

<script>
import Header from './components/Header';
import Content from './components/Content';

export default {
  name: 'App',
  data () {
    return {
      mode: 'light'
    }
  },
  components: {
    Header,
    Content
  },
  created () {
    window.addEventListener('keyup', this.keyPress);
  },
  methods: {
    keyPress (e) {
      if (e.key === 't' || e.key === 'T') {
        this.toggle();
      }
    },
    toggle () {
      if (this.mode === 'dark') {
        this.mode = 'light';
      } else {
        this.mode = 'dark';
      }
    }
  }
}
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  width: 100vw;
  min-height: 100vh;
  background: #f3f3f3;
  color: #15202B;
  transition: background 0.3s ease-in-out;
}

.dark {
  background: #192734;
  color: #e8e8e8;
}
</style>
