<template>
  <v-app>
    <v-main>
      <Lobby/>
    </v-main>
  </v-app>
</template>

<script>
import Lobby from './views/Lobby.vue';

export default {
  name: 'App',

  components: {
    Lobby,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
@font-face {
  font-family: "Azonix";
  src: local("Azonix"),
   url(./fonts/Azonix.otf) format("truetype");
}
@font-face {
  font-family: "OratorStd";
  src: local("OratorStd"),
   url(./fonts/OratorStd.otf) format("truetype");
}
@font-face {
  font-family: "oceanicdriftlaser";
  src: local("oceanicdriftlaser"),
   url(./fonts/oceanicdriftlaser.ttf) format("truetype");
}
</style>
