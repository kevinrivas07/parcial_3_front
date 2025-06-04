<template>
  <nav>
    <router-link to="/users" class="home">Agregar Usuarios</router-link> |
    <router-link to="/roles" class="home">Agregar Roles</router-link> |
    <router-link to="/mostrar" class="home">Vista General</router-link>
  </nav>
  <router-view />
</template>

<script setup lang="ts">
// No hay lógica adicional
</script>

<style>
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(90deg, #0f2027, #203a43, #2c5364);
  padding: 20px;
  box-shadow: 0 0 20px rgba(0, 255, 255, 0.3);
  border-radius: 0 0 20px 20px;
}

.home {
  font-size: 1.3rem;
  color: #00ffe0;
  font-weight: bold;
  text-decoration: none;
  margin: 0 15px;
  padding: 10px 15px;
  border-radius: 8px;
  transition: all 0.3s ease;
  position: relative;
}

.home::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: radial-gradient(circle, #00ffe0 0%, transparent 80%);
  opacity: 0;
  transition: opacity 0.4s ease;
  border-radius: 8px;
  z-index: -1;
}

.home:hover {
  color: #111;
  background-color: #00ffe0;
  box-shadow: 0 0 15px #00ffe0;
  transform: scale(1.05);
}

nav a.router-link-active {
  color: #fff;
  background-color: #ff4081;
  border-radius: 8px;
  box-shadow: 0 0 15px #ff4081;
}
</style>
