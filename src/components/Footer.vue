<template>
  <footer class="bg-primary">
    <div class="container">
      <v-row no-gutters align="center" justify="space-between">
        <v-col cols="4"> © Red-Blue Swabia 1846 </v-col>
        <v-col cols="4" class="hidden-sm-and-down logo-container">
          <img class="logo" @click="redirectHome" src="/rbs.svg" />
        </v-col>
        <v-col cols="4" class="footer-links">
          <v-btn
            href="https://instagram.com/red_blue_swabia_1846"
            variant="text"
            icon="mdi-instagram"
            size="small"
          ></v-btn>
          <v-btn to="/impressum" variant="text">Impressum</v-btn>
        </v-col>
      </v-row>
    </div>
  </footer>
</template>

<script setup>
import { useRouter } from "vue-router";

const router = useRouter();

function redirectHome() {
  router.push("/");
}
</script>

<style scoped>
footer {
  width: 100%;
  height: 100px;
}

.container {
  max-width: var(--max-container-width);
  padding: 0 var(--container-padding);
  margin: 0 auto;
  height: 100%;
  display: flex;
  align-items: center;
}

.logo {
  width: 50px;
  cursor: pointer;
}

.logo-container {
  display: flex;
  justify-content: center;
}

.footer-links {
  display: flex;
  justify-content: end;
  align-items: center;
}
</style>
