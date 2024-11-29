<script setup>
import coracaoCheio from "../src/assets/coracaoCheio.png"
import coracaoVazio from "../src/assets/coracaoVazio.png"

</script>

<template>
 <header>
  <h1>Vue</h1>
  <input type="text" placeholder="Pesquisar no blog">
 </header>
 <main>
  <section>
    <div>
      <p>17 de ago, 2024</p>
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
      <img v-bind:src="coracaoCheio" alt="coração cheio">
    </div>
    <h3>O que é linguagem de programação? Conheça as principais</h3>
    <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
  </section>
  <section>
    <div>
      <p>17 de ago, 2024</p>
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
      <img v-bind:src="coracaoCheio" alt="coração cheio">
    </div>
    <h3>O que é linguagem de programação? Conheça as principais</h3>
    <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
  </section>
  <section>
    <div>
      <p>17 de ago, 2024</p>
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
      <img v-bind:src="coracaoCheio" alt="coração cheio">
    </div>
    <h3>O que é linguagem de programação? Conheça as principais</h3>
    <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
  </section>
  <section>
    <div>
      <p>17 de ago, 2024</p>
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
      <img v-bind:src="coracaoVazio" alt="coração vazio">
    </div>
    <h3>O que é linguagem de programação? Conheça as principais</h3>
    <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
  </section>
  <section>
    <div>
      <p>17 de ago, 2024</p>
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
      <img v-bind:src="coracaoVazio" alt="coração vazio">
    </div>
    <h3>O que é linguagem de programação? Conheça as principais</h3>
    <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
  </section>
 </main>
</template>

<style scoped lang="scss">

header{
  background-color: #17171A;
  color: #E07B67;
  font-family: "Space Grotesk", sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 20vh;


  input{
    width: 60vw;
    margin-top: 1rem;
    background-color: #202024;
    border: none;
    padding: 8px 0;

    &::placeholder{
        padding-left: 10px;
        color: red;
    }
  }
}
</style>