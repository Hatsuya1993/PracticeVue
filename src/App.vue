<template>
  <div id="app test">
    <h1>Sign Up</h1>
    <p>{{value}}</p>
    <input type="text" v-model="value">
    <button onClick="alert('value')" :class="{red: value.length === 0}" :disabled="value.length === 0">Submit</button>
    <ul>
      <li v-for="cat in cats" :key="cat">{{cat}}</li>
    </ul>
    <input type="text" v-model="value">
    <p>{{value}}</p>
    <button v-on:click="addKitty">Submit</button>
    <ul>
      <li v-for="cat in cats" :key="cat">{{cat | capitalize}}</li>
    </ul>
    <HelloWorld :data="cats" msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>

import HelloWorld from "./components/HelloWorld"

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){ 
    return {value: '',
    check : true,
    cats: ['cat1','cat2','cat3']
    }},
    methods: {
      addKitty: function() {
        this.cats.push(this.value)
        this.value = ""
        return 
      }
    },
    filters: {
      capitalize : function(value){
        return value.toUpperCase()
      }
    }
}
</script>

<style>

.red{
  background-color: red;
}

</style>
