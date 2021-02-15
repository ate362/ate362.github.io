<template>
  <v-app id="inspire">
    <v-app-bar app dark prominent clipped-left>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
      <v-spacer></v-spacer>
  
      <v-btn icon>
        <v-icon>fa-instagram</v-icon>
      </v-btn>
    </v-app-bar>
    
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
      id="nav"
    >
      <!--  -->
    </v-navigation-drawer>

    <v-main>
      <slot/>
    </v-main>

    <!-- <v-bottom-navigation shift>

      <v-btn value="recent" to="/">
        <span>Recent</span>
  
        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn value="favorites" to="/about/">
        <span>Favorites</span>
  
        <v-icon>mdi-heart</v-icon>
      </v-btn>
    </v-bottom-navigation> -->

  </v-app>
</template>
<script>
export default {
  data () {
    return {
      drawer: false
    }
  },
}
</script>
<style>
#nav {
  background-color: orange;
}
</style>