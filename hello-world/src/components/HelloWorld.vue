<template>
  <h1 v-show='toggle'>hello !</h1>
  <ul id="example-1">
    <li v-for="item in items" :key="item.message">
      {{ item.message }}
    </li>
  </ul>
  <div id="example-2">
    <button @click='toggle = !toggle'>Afficher / Masquer</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      toggle: true,
      items: [
        {message:'Sofiane'},
        {message:'Anton'},
        {message:'Fatma'},
        {message:'Tristan'},
        {message:'Leo'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  li {
    list-style-type: none;
  }
</style>