<template>
  <v-app id="inspire">
    <!-- Navigation kiri-->
    <Navigation1 />

    <!-- Navigation kiri 2-->
    <Navigation2 />

    <!-- Header -->
    <Header />

   
    <!-- Main -->
    <v-main>
      <v-container>
        <RouterView/>
      </v-container>
    </v-main>

 
    </v-app>
</template>

<script setup>
 
</script>