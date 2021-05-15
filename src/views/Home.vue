<template>
  <div>
    <input type="text" v-model="NUM" />
    <button @click="click">click</button>
    <div v-for="(sum,index) in sum" :key="index">
{{sum}}
    </div>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      NUM: 0,
      sum: "",
      sum1: "",
    };
  },
  methods: {
    click() {
      var NUMint = parseInt(this.NUM);
      console.log(NUMint);
      for (let i = 1; i <= NUMint; i++) {
        console.log(i);
        for (let j = 1; j <= i; j++) {
          this.sum = "*";
          console.log(this.sum);
        }
        this.sum = "<br>";
        console.log(this.sum);
      }
      // for (let index = 1; index < NUMint; index++) {
      //   const element = array[index];

      // }
    },
  },
};
</script>

<style>
</style>