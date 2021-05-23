<template>
  <h1>Eric's Reaction Timer</h1>
  <button @click="turnOnBlock">Play</button>
  <Block v-if="showBlock"/>
</template>

<script>
import Block from './components/Block'

export default {
  name: 'App',
  components: { Block },
  data(){
    return{
      showBlock: false
    }
  },
  methods:{
    turnOnBlock(){
      this.showBlock=true
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
