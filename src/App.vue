<template>
  <v-app>

    <!--  *** App-Bar ***  -->

    <v-app-bar
      color="green lighten-1"
      app
      dark
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Campeonato Brasileiro ⚽</v-toolbar-title>
    </v-app-bar>

    <!--  *** Menu Gaveta ***  -->

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="green lighten-1--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Início</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-clipboard-list</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Classificação</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
        <Inicio />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Inicio from './components/Inicio.vue'

export default {
  name: 'App',

  components: {
    Inicio
  },

  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>
