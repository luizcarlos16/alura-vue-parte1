<template>
  <div>

    <h1 class="centralizado">Alurapic</h1>

    <input @input="filtro = $event.target.value" class="filtro" placeholder="filtre pelo título da foto" type="search">

    <ul class="lista-fotos">
      <li class="lista-fotos-item" v-for="foto of fotosComFiltro">
        <meu-painel :titulo="foto.titulo">
          <imagem-responsiva :titulo="foto.titulo" :url="foto.url"/>
          <meu-botao
            :confirmacao="true"
            @botaoAtivado="remove(foto)"
            estilo="perigo"
            rotulo="remover"
            tipo="button"/>
        </meu-painel>
      </li>
    </ul>
  </div>
</template>

<script>

  import Painel from '../shared/painel/Painel.vue';
  import ImagemResponsiva from '../shared/imagem-responsiva/ImagemResponsiva.vue';
  import Botao from '../shared/botao/Botao.vue';

  export default {

    components: {

      'meu-painel': Painel,
      'imagem-responsiva': ImagemResponsiva,
      'meu-botao': Botao
    },

    data() {
      return {

        fotos: [],

        filtro: ''
      }
    },
    methods: {

      remove(foto) {
        alert("remove foto");

      }
    },
    computed: {
      fotosComFiltro() {
        if (this.filtro) {
          let exp = new RegExp(this.filtro.trim(), 'i');
          return this.fotos.filter(foto => exp.test(foto.titulo));
        } else {
          return this.fotos;
        }
      }
    },

    created() {

      this.$http
        .get('http://localhost:3000/v1/fotos')
        .then(res => res.json())
        .then(fotos => this.fotos = fotos, err => console.log(err));
    }
  }
</script>
<style>

  .centralizado {
    text-align: center;
  }

  .lista-fotos {
    list-style: none;
  }

  .lista-fotos .lista-fotos-item {
    display: inline-block;
  }

  .filtro {
    display: block;
    width: 100%;
  }
</style>
