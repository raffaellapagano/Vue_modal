<template>
  <div>
    <h1 :class="{'d-none': !display}">Heu tancat el Modal</h1>
    <ModalBootstrap :class="{'d-none': display}">

        <template v-slot:header>
            <h5>Hola Mundo</h5>
        </template>

        <template v-slot:body>
            <h5 class="card-title">Cambio de Moneda</h5>
            <input type="text" v-model='euro'>
            <p class="card-text mt-2">El cambio de {{euro}}€ en dolares es {{ euro | convertir}}$</p>
        </template>

        <template v-slot:footer>
        <button type="button" class="btn btn-primary" @click="display = !display">Cerrar</button>
        </template>
   

    </ModalBootstrap>
  </div>
</template>

<script>
import ModalBootstrap from './ModalBootstrap.vue'
export default {
  name: 'Pare',
  components: {
    ModalBootstrap
  },
  data(){
      return{
          euro: 0,
          display : false
      }
  },
  filters:{
      convertir: function(value){
          return value * 1.23;
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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