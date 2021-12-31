<template>
  <div class="hello">
    <h1>Bem vindo {{ msg }}</h1>
    <button v-on:click="mudarCor">Mudar Cor</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      cores: ['blue', 'red', 'yellow', 'pink', 'green', 'wheat'],
    }
  },
  methods: {
    mudarCor() {
      var el = document.body;
      var proximoIndex = Math.floor(Math.random() * this.cores.length);
      var cor = this.cores[proximoIndex];
      el.style.backgroundColor = cor;
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    min-height: 80vh;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
