<script setup>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
const items = ref([{ title: "Audífonos" }, { title: "Bocinas" }]);
</script>

<template>
  <v-responsive>
    <body style="background-color: #e5e5e5">
      <div class="promo">
        <v-icon class="icon-box">mdi-package-variant-closed</v-icon>
        <p class="envio">Envío gratis en compras de más de $499</p>
        <a class="acerca" href="">Acerca de</a>
        <a class="contacto" href="">Contacto</a>
        <a class="asistencia" href="">Asistencia</a>
        <a class="telefono" href="">Llama +52-1-33-12345678</a>
      </div>
      <v-toolbar
        class="toolbar"
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
            class="toolbar-title"
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
        <div class="icons">
          <v-icon size="30">mdi-account-circle</v-icon>
          <a class="entrar" href="">Entrar</a>
          <v-icon style="margin-left: 20px" size="30">mdi-heart-outline</v-icon>
          <a class="fav" href="">Favoritos</a>
          <v-icon style="margin: 0 20px" size="30">mdi-cart-outline</v-icon>
        </div>
      </v-toolbar>
      <div class="menu">
        <a href="">Comprar todo</a>
        <a href="">Computadoras</a>
        <a href="">Tabletas</a>
        <a href="">Drones y cámaras</a>
        <v-menu open-on-hover>
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

      <div class="carrusel">
        <v-carousel
          :show-arrows="false"
          cycle
          :interval="5000"
          hide-delimiters
          style="position: relative"
        >
          <v-carousel-item
            src="../public/img/apple.jpg"
            cover
          ></v-carousel-item>

          <v-carousel-item
            src="../public/img/cells.jpg"
            cover
          ></v-carousel-item>

          <v-carousel-item src="../public/img/kit.jpg" cover></v-carousel-item>

          <v-carousel-item
            src="../public/img/laptops.jpg"
            cover
          ></v-carousel-item>
          <v-carousel-item
            src="../public/img/relojes.jpg"
            cover
          ></v-carousel-item>
        </v-carousel>
        <span>Mejores Precios</span>
        <h1>
          Súper precios <br />
          en tus artículos <br />
          favoritos
        </h1>
        <p>Gana más por tu dinero</p>
        <button>Comprar ahora</button>
      </div>
      <div class="imagered">
        <img
          src="../public/img/telefono-rojo.jpg"
          alt=""
          class="telefonorojo"
        />
        <span>Ofertas de temporada</span>
        <h2>
          Hasta <br />
          30% menos
        </h2>
        <p>En Smartphones seleccionados</p>
        <button>Tienda</button>
      </div>
      <div class="imagevioleta">
        <img src="../public/img/audifono-violeta.jpg" alt="" class="audifono" />
        <span>Recién llegados</span>
        <h2>
          Lleva tu <br />
          sonido <br />
          dondequieras
        </h2>
        <p>Mejores marcas de audífonos</p>
        <button>Comprar</button>
      </div>

      <div class="promocion">
        <div class="promocion-item">
          <v-icon>mdi-bicycle-basket</v-icon>
          <p>Recogida en la acera</p>
        </div>
        <div class="promocion-item">
          <v-icon>mdi-package-variant-closed</v-icon>
          <p>Envíos gratis en compras de más de $499</p>
        </div>
        <div class="promocion-item">
          <v-icon>mdi-cash-multiple</v-icon>
          <p>Precios bajos garantizados</p>
        </div>
        <div class="promocion-item">
          <v-icon>mdi-clock-check-outline</v-icon>
          <p>Disponibles para ti 24/7</p>
        </div>
      </div>
      <div class="masvendido">
        <h3>Más vendido</h3>
        <div class="v-cards">
          <v-card class="item1card" max-width="150" max-height="400">
            <v-img height="180" src="../public/img/fitboot.jpeg" cover></v-img>
            <v-card-text>
              <div>Fitboot fitness con seguimiento del ritmo cardíaco</div>
              <p>$ 984.00</p>
            </v-card-text>
          </v-card>

          <v-card class="item1card" max-width="150" max-height="400">
            <v-img height="180" src="../public/img/laptopJP.jpeg" cover></v-img>
            <v-card-text>
              <div>JP laptop para juegos de 15,6" de 256GB</div>
              <p>$ 984.00</p>
            </v-card-text>
          </v-card>

          <v-card class="item1card" max-width="150" max-height="400">
            <v-img height="180" src="../public/img/drone.jpeg" cover></v-img>
            <v-card-text>
              <div>HKI Tech drone cuadricóptero con cámara y mando 360</div>
              <p>$ 999.00</p>
            </v-card-text>
          </v-card>
          <v-card class="item1card" max-width="150" max-height="400">
            <v-img
              height="180"
              src="../public/img/smartphoneZ.jpeg"
              cover
            ></v-img>
            <v-card-text>
              <div>Smartphone Z Pixel Max 128GB desbloqueado</div>
              <p>$ 984.00</p>
            </v-card-text>
          </v-card>

          <v-card class="item1card" max-width="150" max-height="400">
            <v-img
              height="180"
              src="../public/img/audifonosInalambricos.jpeg"
              cover
            ></v-img>
            <v-card-text>
              <div>Audífonos inalámbricos con cancelación de ruido</div>
              <p>$ 984.00</p>
            </v-card-text>
          </v-card>

          <v-card class="item1card" max-width="150" max-height="400">
            <v-img
              height="180"
              src="../public/img/realidadVirtual.jpeg"
              cover
            ></v-img>
            <v-card-text>
              <div>
                Gafas de realidad virtual Safay Gen 2 de 256GB con mando
                táctiles
              </div>
              <p>$ 984.00</p>
            </v-card-text>
          </v-card>
        </div>
        <button>Ver todo</button>
      </div>
      <div class="comprarCategoria">
        <h3>Comprar por categoría</h3>
        <div class="images">
          <div class="categoria-item">
            <img src="../public/img/laptopJP.jpeg" alt="" />
            <a href="">Computadoras</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/smartphoneZ.jpeg" alt="" />
            <a href="">Celulares</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/drone.jpeg" alt="" />
            <a href="">Drones y camáras</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/oferta.jpeg" alt="" />
            <a href="">Ofertas</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/tablets.jpeg" alt="" />
            <a href="">Tabletas</a>
          </div>
        </div>
        
        
        <div class="images">
          <div class="categoria-item">
            <img src="../public/img/masvendido.jpeg" alt="" />
            <a href="">Más vendido</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/smartv.jpeg" alt="" />
            <a href="">T.V. y cine en casa</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/tecnoportatil.jpeg" alt="" />
            <a href="">Tecnología portátil</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/bocinas.jpeg" alt="" />
            <a href="">Bocinas</a>
          </div>
          <div class="categoria-item">
            <img src="../public/img/audifonoscable.jpeg" alt="" />
            <a href="">Audífonos</a>
          </div>
        </div>  
      </div>
    </body>
  </v-responsive>
  <RouterView />
</template>
