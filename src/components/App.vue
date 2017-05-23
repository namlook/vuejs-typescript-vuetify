<template>
  <v-app id="app">
    <v-navigation-drawer persistent light :mini-variant.sync="mini" v-model="drawer">
      <v-list class="pa-0">
        <v-list-item>
          <v-list-tile avatar tag="div">
            <v-list-tile-avatar>
              <img src="https://randomuser.me/api/portraits/men/85.jpg" />
            </v-list-tile-avatar>
            <v-list-tile-content>
              <v-list-tile-title>John Leider</v-list-tile-title>
            </v-list-tile-content>
            <v-list-tile-action>
              <v-btn icon @click.native.stop="mini = !mini">
                <v-icon>chevron_left</v-icon>
              </v-btn>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>
      </v-list>
      <v-list class="pt-0" dense>
        <v-divider></v-divider>
        <v-list-item>
          <v-list-tile>
            <v-list-tile-action>
              <v-icon> favorite</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title> item.title</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed class="green">
      <v-toolbar-side-icon light @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Scanner Zerosix</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon light>
        <v-icon>account_circle</v-icon>
      </v-btn>
      <v-btn icon light>
        <v-icon>favorite</v-icon>
      </v-btn>
      <v-btn icon light>
        <v-icon>more_vert</v-icon>
      </v-btn>
    </v-toolbar>
    <main>
      <v-container fluid>
        <!--v-router-->
        <img src="../assets/logo.png">    
        <Hello :greeting="message"></Hello>
        <Date></Date>
      </v-container>
    </main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

import Hello from './Hello'
import Date from './Date'
import UserManager from './UserManager'

@Component({
  components: {
    Hello,
    Date,
    UserManager,
  }
})
export default class extends Vue {
  message = 'Welcome to Your Vue.js App'
  mini: boolean = false
  drawer: boolean = false
}
</script>

<style src="vuetify/dist/vuetify.min.css">

