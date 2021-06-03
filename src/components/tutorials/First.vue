<template>
  <h1>{{title}}</h1>
  <!-- we can use the ref attribute to get a reference to a DOM element and then access it with our vue methods -->
  <input type="text" ref="name">
  <button @click="handleClick">click me</button>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      title: 'My first vue app :)'
    }
  },
  methods:{
    handleClick(){
        // to access any refs available we can do this.$refs
      console.log(this.$refs.name);
      this.$refs.name.classList.add('active');
      this.$refs.name.focus();
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
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}


</style>
