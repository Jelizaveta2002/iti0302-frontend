<script setup>
</script>

<template>
  <nav>
    <router-link to="/">Home</router-link>
    |
    <router-link to="/about">About</router-link>
    |
    <router-link to="/login">Login</router-link>
    |
    <router-link to="/register">Register</router-link>
    |
    <router-link to="/profile">User Profile</router-link>
    |
    <router-link to="/activity">Activities</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

.feedback {
  background-color: #31B0D5;
  color: white;
  padding: 10px 10px;
  border-radius: 4px;
  border-color: #46b8da;
}
</style>

<script>

import {onUnmounted} from "vue";

export default {

  setup() {
    onUnmounted(() => {
          localStorage.removeItem("token");
          console.log("token delete");
        }
    )
  }

}
</script>