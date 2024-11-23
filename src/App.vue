<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <v-responsive>
  <div class="promo">
    <v-icon class="icon-box">mdi-package-variant-closed</v-icon>
    <p class="envio">Envío gratis en compras de más de $499</p>
    <a class="acerca" href="">Acerca de</a>
    <a class="contacto" href="">Contacto</a>
    <a class="asistencia">Asistencia</a>
    <a class="telefono" href="">Llama +52-1-33-12345678</a>
  </div>
  <v-toolbar color="white" style="height: 100px;display: flex; justify-content: center; align-items: center;">
    <v-toolbar-title style="font-size: 30px;"><a style="text-decoration: none;color: black;" href="/index.html">Perez TEc</a></v-toolbar-title>
    
    <div class="textfield" style="margin-right: 20px;"><v-text-field style="margin-top: 25px; margin-right: 80px;"
            label="Buscar..."
            variant="outlined"
            width="290px"
            append-inner-icon="mdi-magnify"
            rounded
          ></v-text-field></div>
    <v-icon>mdi-account-circle</v-icon> <a class="entrar" href="">Entrar</a>
    <v-icon style="margin-left: 20px;">mdi-heart-outline</v-icon> <a class="fav" href="">Favoritos</a>
    <v-icon style="margin:0 20px;">mdi-cart-outline</v-icon>
  </v-toolbar>
  <div style="padding: 20px; background-color:#e5e5e5;"></div>
  </v-responsive>
  <RouterView />
</template>

