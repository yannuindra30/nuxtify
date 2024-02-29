<template>
  <v-navigation-drawer color="white">
    <!--  -->

    <v-list>
      <v-list-subheader color="black"
        ><h4>
          SATU RSSA <br />
          Satu Data Untuk RSSA
        </h4></v-list-subheader
      >

      <v-divider class="mx-0 my-3"></v-divider>
      <v-text-field
        label="Search Collection"
        variant="solo"
        class="mx-3 my-2"
      ></v-text-field>
      <v-list-item
        prepend-icon="mdi-home"
        title="Home"
        class="my-0"
      ></v-list-item>

      <v-list-group value="Users"
        >``
        <template v-slot:activator="{ props }">
          <v-list-item
            v-bind="props"
            prepend-icon="mdi-account-circle"
            title="Users"
          ></v-list-item>
        </template>

        <v-list-group value="Admin">
          <template v-slot:activator="{ props }">
            <v-list-item v-bind="props" title="Admin"></v-list-item>
          </template>

          <v-list-item
            v-for="([title, icon], i) in admins"
            :key="i"
            :title="title"
            :prepend-icon="icon"
            :value="title"
          ></v-list-item>
        </v-list-group>

        <v-list-group value="Actions">
          <template v-slot:activator="{ props }">
            <v-list-item v-bind="props" title="Actions"></v-list-item>
          </template>

          <v-list-item
            v-for="([title, icon], i) in cruds"
            :key="i"
            :value="title"
            :title="title"
            :prepend-icon="icon"
          ></v-list-item>
        </v-list-group>
      </v-list-group>
    </v-list>
    <v-divider class="mx-3 my-2"></v-divider>
    <v-list>
      <v-list-item
        prepend-icon="mdi-account-multiple-outline"
        title="Data Model"
        value="home"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-cog-outline"
        title="Access Control"
        value="AccessControl"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-plus-outline"
        title="Webhooks"
        value="home"
      ></v-list-item>
      <v-divider class="mx-3 my-2"></v-divider>
      <v-list-item
        prepend-icon="mdi-file-outline"
        title="Settings"
        value="home"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-update"
        title="Appereance"
        value="home"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-view-dashboard"
        title="Bookmarks"
        value="home"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
<script>
export default {
  data: () => ({
    open: ["Users"],
    admins: [
      ["Management", "mdi-account-multiple-outline"],
      ["Settings", "mdi-cog-outline"],
    ],
    cruds: [
      ["Create", "mdi-plus-outline"],
      ["Read", "mdi-file-outline"],
      ["Update", "mdi-update"],
      ["Delete", "mdi-delete"],
    ],
  }),
};
</script>
