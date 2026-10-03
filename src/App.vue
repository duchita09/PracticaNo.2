<script setup lang="ts">
import { ref } from 'vue'

const contador = ref(0)

function aumentar() {
  contador.value++
}

function disminuir() {
  contador.value--
}
</script>

<template>
  <main class="pagina">
    <div class="decoracion decoracion-1"></div>
    <div class="decoracion decoracion-2"></div>

    <section class="contador">
      <p class="etiqueta">PRÁCTICA NO. 2</p>

      <h1>Mi contador</h1>

      <p class="descripcion">
         @duchita09
      </p>

      <div class="numero">
        {{ contador }}
      </div>

      <div class="botones">
        <button
          class="boton"
          @click="disminuir"
          aria-label="Disminuir contador"
        >
          −
        </button>

        <button
          class="boton"
          @click="aumentar"
          aria-label="Aumentar contador"
        >
          +
        </button>
      </div>
    </section>
  </main>
</template>

<style scoped>
.pagina {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  overflow: hidden;
  background: linear-gradient(
    135deg,
    #eee6f7,
    #e4edf8,
    #f8e9ef
  );
}

.decoracion {
  position: absolute;
  border-radius: 50%;
  opacity: 0.5;
}

.decoracion-1 {
  width: 260px;
  height: 260px;
  background: #d9c2ff;
  top: -80px;
  left: -70px;
}

.decoracion-2 {
  width: 320px;
  height: 320px;
  background: #c9def5;
  bottom: -130px;
  right: -100px;
}


.contador {
  width: 350px;
  padding: 38px 30px;
  text-align: center;
  position: relative;
  z-index: 1;

  background: rgba(255, 255, 255, 0.92);
  border-radius: 22px;

  box-shadow:
    0 12px 30px rgba(80, 70, 100, 0.15);
}

.etiqueta {
  margin: 0 0 8px;
  font-size: 12px;
  letter-spacing: 2px;
  color: #9276b8;
  font-weight: bold;
}

h1 {
  margin: 0;
  font-size: 32px;
  color: #4c4554;
}

.descripcion {
  margin: 8px 0 25px;
  color: #88818d;
  font-size: 14px;
}

.numero {
  font-size: 70px;
  font-weight: bold;
  color: #6d5686;
  margin: 10px 0 25px;
}

.botones {
  display: flex;
  justify-content: center;
  gap: 18px;
}

.boton {
  width: 65px;
  height: 55px;

  border: none;
  border-radius: 14px;

  background-color: #d8c2f4;
  color: #51445e;

  font-size: 30px;
  cursor: pointer;

  transition: transform 0.2s;
}

.boton:hover {
  transform: translateY(-3px);
}

.boton:active {
  transform: scale(0.95);
}

.mensaje {
  margin: 25px 0 0;
  font-size: 13px;
  color: #99919e;
}
</style>