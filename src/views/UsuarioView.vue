<template>
  <div class="usuario">
    <h1 v-if="nome.length > 5">{{nome}}</h1>
    <input type="text" v-model="nome">
    <ul>
        <li v-for="nota in notas" :key="nota">
            <h2>{{nota}}</h2>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "usuarioView",
  data() {
    return {
      nome: "Marcus",
      notas: ['oi', 'tchau']
    };
  },
};
</script>