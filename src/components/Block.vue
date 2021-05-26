<template>
  <h2 class="block" v-if="showBlock" @click="stopTimer">Click Me</h2>
</template>

<script>
export default {
  props: ['delayProps'],
  data(){
    return{
      showBlock: false,
      timer: null,
      reactionTime: 0
    }
  },
  mounted(){
    setTimeout(() => {
      this.showBlock = true
      this.startTimer()
    }, this.delayProps)
  },
  methods:{
    startTimer(){
      this.timer=setInterval(()=>{
        this.reactionTime += 10
      },10)
    },
    stopTimer(){
      console.log(this.reactionTime)
      // clearInterval(this.timer)
      
    }
  }
}
</script>

<style>
.block {
    color: white;
    background: green;
    margin: 40px auto;
    text-align: center;
    padding: 100px 0;
    border-radius: 20px;
    width: 400px;
}
</style>