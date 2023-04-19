<script>
import { computed } from '@vue/reactivity';
import { AppState } from "../src/AppState";


export default {
  
  setup(){
    
    return {
      number: computed(()=> AppState.number),
      num(){
        AppState.number++
      }


      
    }
  }
}
</script>

<template>

<h1 class="bg-yellow-100 text-9xl rounded-xl cursor-pointer flex justify-center harmony-title align-start">Harmony<span class="copyright">©</span></h1>

<div class="container mx-auto ">
<div class="grid-rows-1 flex justify-center">
  <h1 class="second-title">Sorry i made this tester stuff in harmony, just delete it im messing with tailwind</h1>
</div>
<div class="grid-rows-1 flex justify-center">
  <button class="btn bg-gradient-to-r from-green-400 to-blue-500 rounded p-5 mt-2 cursor-pointer

  hover:transform hover:rotate-180 hover:bg-gradient-to-r hover:from-blue-500 hover:to-green-400
  " @click="num()">Click this to make the number below go up</button>
</div>
<div class="grid-rows-1 flex justify-center">
  <h1 class="text-9xl">{{ number }}</h1>
</div>
</div>
</template>

<style scoped>
.btn{
  font-size: 32px;
  min-height: 5vh;
  min-width: 5vh;
}

.second-title{
  font-size: 32px;
}

.copyright{
  font-size: 48px;
}
.harmony-title{
  font-family: 'Nova Oval', cursive;
  color: #e4dfaa;
}
</style>
