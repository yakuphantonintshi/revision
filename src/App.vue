<template>
 <div>
  <PropsExample numb1="66" numb2="12"/>
  <form class="container">
    <input type="text" placeholder="Enter your name" v-model="firstName">
    <label>{{ output }}</label>
    <button @click.prevent="greeting">Greeting</button>
  </form>
 </div>
</template>

<script>
import PropsExample from '@/components/PropsExample.vue'

export default {
  name: 'App',
  components: {
    PropsExample
  },
  data(){
    return {
      firstName: '',
      output: ''
    }
  },
  methods: {
    greeting(){
      this.output = `Hello ${this.firstName}`
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
