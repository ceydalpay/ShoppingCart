<template>
  <div id="nav">
    <router-link :class="{active: $route.name === 'Home'}" to="/">Home</router-link> |
    <router-link :class="{active: $route.name === 'Cart'}" to="/cart">Cart</router-link>
  </div>
  <router-view/>
</template>

<script>
export default {
  mounted() {
    this.$store.commit('updateCartFromLocalStorage')
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
}
html, body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
body{
  background-color: rgb(228, 194, 149);
}
#nav{
  padding: 10px;
  width: 100%;
  height: 30px;
  background-color: rgb(170, 56, 56);
  line-height: 30px;
  a {
    font-weight: bold;
    color: rgb(228, 194, 149);
    text-decoration: none;
    margin: 0 5 px 0 5 px;
    font-size: 1.25rem;
    &.active{
      color: rgb(228, 194, 149);
      }
  }
}
.text-center  {
  text-align: center;
}
</style>