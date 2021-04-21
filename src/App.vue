<template>
  <div>
    <!-- Encapsular el nav en un componente e importarlo -->
    <nav class="navbar navbar-light navbar-expand-lg fixed-top" id="mainNav">
      <div class="container">
        <a class="navbar-brand">V8</a
        ><button
          data-toggle="collapse"
          data-target="#navbarResponsive"
          class="navbar-toggler"
          aria-controls="navbarResponsive"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fa fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <!-- MENU DE NAVEGACION -->
          <ul class="nav navbar-nav ml-auto" id="menu-v8">
            <li class="nav-item" role="presentation">
              <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA NOMBRADA -->
              <!-- <a href="/">portada</a> -->
              <router-link to="/"> Portada </router-link>
            </li>
            <li class="nav-item" role="presentation">
              <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA NOMBRADA -->
              <!-- <a href="/sobremi">sobre mí</a> -->
              <router-link to="/sobremi"></router-link>
            </li>
            <li class="nav-item" role="presentation">
              <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA ESTÁTICA -->
              <a href="/">contacto</a>
            </li>
            <li class="nav-item" role="presentation">
              <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A RUTA ESTÁTICA -->
              <a href="/post/1">último post</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- Encapsular el nav en un componente e importarlo -->

    <!-- ROUTER VIEW QUE CARGARÁ LAS VISTAS (INICIO, SOBRE MÍ, CONTACTO, ETC.) -->
    <router-view></router-view>

    <!-- Footer -->
    <FooterV8 />
  </div>
</template>

<script>
import FooterV8 from "@/components/FooterV8.vue";

export default {
  name: "App",
  components: {
    FooterV8,
  },
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#menu-v8 a {
  text-shadow: 1px 1px #000;
}
</style>
