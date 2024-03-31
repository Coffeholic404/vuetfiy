<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <v-app>
  <v-toolbar density="compact">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>
        <RouterLink to="/">Vuetify</RouterLink>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn to="/login" size="small" variant="outlined" color="purple-darken-4" text="Login">
        
      </v-btn>
    </v-toolbar>
  <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
    <RouterView />
  </v-main>
</v-app>
</template>
