<script setup>
import { ref } from "vue";
import coracaoCheio from "../src/assets/coracaoCheio.png"
import coracaoVazio from "../src/assets/coracaoVazio.png"


const formatDate = (date) => {
  const options = { year: 'numeric', month: 'long', day: 'numeric' };
  return new Date(date).toLocaleDateString('pt-BR', options);
};

const imagens = ref([
  { id: 1, src: coracaoVazio, cheio: false, data: '2024-12-02'},
  { id: 2, src: coracaoVazio, cheio: false, data: '2024-11-31'},
  { id: 3, src: coracaoVazio, cheio: false, data: '2024-08-10'},
  { id: 4, src: coracaoVazio, cheio: false, data: '2024-08-10'},

]);

const alterarImagem = (id) => {
  const imagem = imagens.value.find((img) => img.id === id);
  if (imagem) {
    imagem.cheio = !imagem.cheio;
    imagem.src = imagem.cheio ? coracaoCheio : coracaoVazio;
  }
};

</script>

<template>
 <header>
  <h1>Vue</h1>
  <input type="text" placeholder="Pesquisar no blog">
 </header>
 <main>
  <section v-for="imagem in imagens" :key="imagem.id">
    <div>
      <p>{{ formatDate(imagem.data) }}</p>      
        <!-- Como trazer dados de forma dinamica ?-->
        <!-- dentro de Tags, usamos o {} ex: <p {} </p>  -->
        <!-- para inserir em atributos, usamos o v-bind
        : atalho para o v-bind -->
        <img :src="imagem.src" :alt="'Coração ' + (imagem.cheio ? 'cheio' : 'vazio')" @click="alterarImagem(imagem.id)"/>
    <h3>O que é linguagem de programação? Conheça as principais:</h3>
    <h4>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</h4>
  </div>
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
    padding: 8px 8px;
    color: #FFFFFF;l

    &::placeholder{
        padding-left: 10px;
        color: #AFABB6;      
    }
  }
}


main {
  display: flex;
  flex-direction: column;
  padding: 0 20%;
  justify-content: center;
  background-color: black;
  font-family: "Space Grotesk", sans-serif;
}

div {
  width: 60vw;
  background-color: #202024;
  border: none;
  padding: 40px 40px;
  margin: 40px 20px;

  &:hover{
    border: #E07B67 solid;
  
  }

}

img{
 margin: 0 90%;
 padding: 0% 8%;
}

p{
  color: #E07B67;

}

h3 {
  color: #FFFFFF;
  padding: 5px;
}


h4{
  padding: 5px;
  color: #AFABB6;
}
</style>