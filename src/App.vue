<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">狗牙蔷薇</router-link> |
      <router-link to="/about">个人简历</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
*{
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
#nav {
  padding: 30px;
  background-color: rgb(2,202,212);
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  /*color: #42b983;*/
  color: #fff;
}
</style>
