<template>
    <v-navigation-drawer location="right">
      <v-list>
        <v-list-item
          v-for="n in 5"
          :key="n"
          :title="`Item ${ n }`"
          link
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<v-list-subheader><h4>SATU RSSA</h4></v-list-subheader>
        
    
<v-list-item prepend-icon="mdi-home" title="Home"></v-list-item>