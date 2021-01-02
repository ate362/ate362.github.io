<template>
  <v-app id="inspire">
    <v-app-bar app dark clipped-left>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>
    
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
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
