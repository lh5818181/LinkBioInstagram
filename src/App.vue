<template>
  <div id="app">
    <div class="container">
      <img src="../public/profile.jpg" alt="Foto de perfil" class="profile-picture" />
      <h1>Meus Links</h1>
      <p class="professional-name">@devriqueoliver</p>
      <LinksList :links="links" />
    </div>
    <footer class="container footer">
      &copy; 2024 Todos os direitos reservados | Luis Henrique Vieira de Oliveira
    </footer>
  </div>
</template>

<script lang="ts" setup>
import LinksList from "./components/LinksList.vue";

// Tipagem para os Links
interface Link {
  id: number;
  label: string;
  url: string;
}

// Lista de links
const links: Link[] = [
  { id: 1, label: "Portfolio Web", url: "https://portfolio-home-ten.vercel.app/" },
  { id: 2, label: "GitHub", url: "https://github.com/lh5818181" },
  { id: 3, label: "LinkedIn", url: "https://www.linkedin.com/in/luis-henrique-76245231a/" },
  { id: 4, label: "Whatsapp", url: "https://wa.me/qr/XOOHIGLGNEOCA1" }
];
</script>

<style src="./styles/global.css"></style>
