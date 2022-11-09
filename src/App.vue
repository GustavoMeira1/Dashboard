<template>
  <v-app>
    <Dashboard/>
  </v-app>
</template>

<script>
import Dashboard from './components/Dashboard';

export default {
  name: 'App',

  components: {
    Dashboard,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik&display=swap');
#app{
background-color: hsl(226, 43%, 10%);
font-family: 'Rubik', sans-serif;
}
</style>