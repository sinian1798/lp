<template>
  <div class="">
    <button type="button" @click="increment">Increment</button>
    <button type="button" @click="decrement">Decrement</button>
  </div>
</template>

<script>
  import {mapMutations} from "vuex"
  import {COUNTER_INCREMENT,COUNTER_DECREMENT} from "../store/types"
  export default {
    data() {
      return {
      }
    },
    created() {
    },
    methods: {
      // ...mapMutations([
      //   "increment",
      //   "decrement"
      // ])
      increment(){
        this.$store.commit(COUNTER_INCREMENT,10);
      },
      decrement(){
        this.$store.commit(COUNTER_DECREMENT,10)
      }
    }
  }
</script>

<style>
</style>
