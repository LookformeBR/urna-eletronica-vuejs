<template>
  <div class="urna-teclado">
    <div class="urna-teclado-numerico">
      <!-- BOTÕES -->
      <div class="urna-teclado-numerico-linha">
        <button v-on:click="adicionarNumero(1)">1</button>
        <button v-on:click="adicionarNumero(2)">2</button>
        <button v-on:click="adicionarNumero(3)">3</button>
      </div>

      <div class="urna-teclado-numerico-linha">
        <button v-on:click="adicionarNumero(4)">4</button>
        <button v-on:click="adicionarNumero(5)">5</button>
        <button v-on:click="adicionarNumero(6)">6</button>
      </div>

      <div class="urna-teclado-numerico-linha">
        <button v-on:click="adicionarNumero(7)">7</button>
        <button v-on:click="adicionarNumero(8)">8</button>
        <button v-on:click="adicionarNumero(9)">9</button>
      </div>
      <!-- BOTÕES -->

      <!-- BOTÕES -->
      <div class="urna-teclado-numerico-linha">
        <button v-on:click="adicionarNumero(0)">0</button>
      </div>
      <!-- BOTÕES -->
    </div>

    <div class="urna-teclado-acoes">
      <button   v-on:click="votarEmBranco()" class="btn-branco">Branco</button>
      <button v-on:click="corrigir()" class="btn-corrige">Corrige</button>
      <button v-on:click="confirmar()" class="btn-confirma">Confirma</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Teclado",
  props: {
    adicionarNumero: Function,
    corrigir: Function,
    confirmar: Function,
    votarEmBranco: Function,
  },
};
</script>

<style>
.urna-teclado {
  width: 40%;
  height: 100%;
  background-color: var(--ballot-box-keyboard-color);
  border-radius: 5px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.urna-teclado-numerico {
  width: 100%;
}

.urna-teclado-numerico-linha {
  display: flex;
  justify-content: space-around;
  margin-bottom: 20px;
}

.urna-teclado-numerico button {
  background-color: var(--ballot-box-keyboard-button-color);
  color: var(--light-text-color);
  font-size: 30px;
  border-radius: 5px;
  width: 80px;
  height: 50px;
}
.urna-teclado-acoes {
  width: 100%;
  display: flex;
  justify-content: space-around;
}
.urna-teclado-acoes button {
  color: var(--dark-text-color);
  font-size: 15px;
  border-radius: 10px;
  width: 30%;
  height: 50px;
}

.btn-branco {
  background-color: var(--ballot-box-white-button-color);
}

.btn-corrige {
  background-color: var(--ballot-box-correct-button-color);
}

.btn-confirma {
  background-color: var(--ballot-box-confirm-button-color);
}
</style>