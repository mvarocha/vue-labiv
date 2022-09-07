<template>
  <div class="usuario">
    <h1 v-if="nome.length > 5">{{ nome }}</h1>
    <form action="">
      <input type="text" v-model="nome" />
      <button @click="inserirUsuario">Ok</button>
    </form>
    <ul>
      <li v-for="nota in notas" :key="nota">
        <h2>{{ nota }}</h2>
      </li>
    </ul>
  </div>
</template>

<style>
    form{
        display: flex;
        flex-direction: column;
        width: 100%;
        align-items: center;
    }
    input{
        width: 200px;
    }
    button{
        margin-top: 10px;
        width: 100px;
        border-radius: 100px;
        cursor: pointer;
    }
</style>

<script>
export default {
  name: "usuarioView",
  data() {
    return {
      nome: "Marcus",
      notas: ["oi", "tchau"],
    };
  },
  methods:{
    inserirUsuario(){
        this.notas.push(this.nome)
        this.nome = ''
    }
  }
};
</script>