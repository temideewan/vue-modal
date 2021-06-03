<template>
  <h1>{{title}}</h1>
  <!-- binding data to props -->
  <Modal :header='header' :text='text' theme="sale"/>
</template>

<script>
import Modal from './components/Modal'

export default {
  name: 'App',
  data(){
    return {
      title: 'My first vue app :)',
      header:'Sign up now',
      text:'Come in and join the journey'
    }
    
  },

  components:{
    Modal
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
