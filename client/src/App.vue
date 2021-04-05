<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div v-for="product in products">
      <p>name:{{product.name}}</p>
      <p>price:{{product.price}}</p>
      <p>count:{{product.count}}</p>
      <p>views:{{product.views}}</p>
      <p>description:{{product.description}}</p>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      products: [],
    }
  },
  mounted(){
    this.getProducts()
  },
  // methods: {
  //   getProducts(){
  //     // this.axios.post("link",this.newproduct)
  //   }
  // }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
