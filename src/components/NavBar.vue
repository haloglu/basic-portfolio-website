<template>
  <v-app-bar app color="#2C3333" dark flat class="px-12">
    <v-btn>
      <v-icon color="#0E8388" left class="mr-2">fas fa-signature</v-icon>
      <h3 class="nav-title">PORTFOLIO</h3>
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn
      style="font-size: 1.1rem"
      text
      @click="scroll('home')"
      color="#0E8388"
      >Home</v-btn
    >
    <v-btn style="font-size: 1.1rem" text @click="scroll('about')" color="white"
      >About</v-btn
    >
    <v-btn
      style="font-size: 1.1rem"
      text
      @click="scroll('portfolio')"
      color="white"
      >Portfolio</v-btn
    >
    <v-btn
      style="font-size: 1.1rem"
      text
      @click="scroll('services')"
      color="white"
      >Services</v-btn
    >
    <v-btn style="font-size: 1.1rem" text @click="scroll('page')" color="white"
      >Page</v-btn
    >
    <v-btn style="font-size: 1.1rem" text @click="scroll('blog')" color="white"
      >Blog</v-btn
    >
    <v-btn
      style="font-size: 1.1rem"
      text
      @click="scroll('contact')"
      color="white"
      >Contact</v-btn
    >
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style>
.nav-title {
  color: #cbe4de;
  font-size: 1.2rem;
}
</style>
