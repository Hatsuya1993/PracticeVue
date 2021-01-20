<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="cat in data" :key="cat">{{cat}}</li>
    </ul>
    
   
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    data: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
