<script setup>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
 const items=ref( [
        { title: 'Audífonos' },
        { title: 'Bocinas' },
      ])
</script>

<template>
  <v-responsive>
    <div class="promo">
      <v-icon class="icon-box">mdi-package-variant-closed</v-icon>
      <p class="envio">Envío gratis en compras de más de $499</p>
      <a class="acerca" href="">Acerca de</a>
      <a class="contacto" href="">Contacto</a>
      <a class="asistencia" href="">Asistencia</a>
      <a class="telefono" href="">Llama +52-1-33-12345678</a>
    </div>
    <v-toolbar
      color="white"
      style="
        height: 100px;
        display: flex;
        justify-content: center;
        align-items: center;
      "
    >
      <v-toolbar-title style="font-size: 30px"
        ><a
          style="
            text-decoration: none;
            color: black;
            font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS',
              sans-serif;
            font-size: 42px;
            font-weight: 600;
          "
          href="/index.html"
          >Perez TEc</a
        ></v-toolbar-title
      >
      <div class="search-container">
        <input type="text" placeholder="   Buscar..." class="search-input" />
        <button @click="search" class="search-button">
          <v-icon>mdi-magnify</v-icon>
        </button>
      </div>
      <v-icon size="30">mdi-account-circle</v-icon>
      <a class="entrar" href="">Entrar</a>
      <v-icon style="margin-left: 20px" size="30">mdi-heart-outline</v-icon>
      <a class="fav" href="">Favoritos</a>
      <v-icon style="margin: 0 20px" size="30">mdi-cart-outline</v-icon>
    </v-toolbar>
    <div class="menu">
      <a href="">Comprar todo</a>
      <a href="">Computadoras</a>
      <a href="">Tabletas</a>
      <a href="">Drones y cámaras</a>
      <v-menu
      open-on-hover
    >
      <template v-slot:activator="{ props }">
        <buttom
          color="black"
          v-bind="props"
          variant="plane"
          class="custom-button"
        >
         Audio
        </buttom>
      </template>

      <v-list>
        <v-list-item
        class="listmenu"
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
    <a href="">Celulares</a>
    <a href="">T.V. y cine en casa</a>
    <a href="">Tecnología Portátil</a>
    <a href="">Oferta</a>
    </div>
  </v-responsive>
  <RouterView />
</template>
