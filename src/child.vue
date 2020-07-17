<template>
  <div>
    <h1>Hello!! I am the child....</h1>
    <h2>my name is {{childname}} .</h2>
    <button @click="changehere">Change name in child</button>
    <button @click="changeeverywhere">Change name in both paremt and child ($emit is used) </button>
  </div>
</template>

<script>
export default {
  props: ["childname"],
  methods:{
      changehere(){
          this.childname = "yash";
      },
      changeeverywhere(){
          this.$emit("pleasechange","chirag");
      }
  }
}
</script>

<style scoped>
    h1{
        color: blue;
    }
    div{
        background-color: burlywood;
        padding: 2rem;
    }
</style>>

