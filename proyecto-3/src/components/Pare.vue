<template>
  <div>
    <modal-bootstrap>

      <template v-slot:footer>
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
        </template>

        <template v-slot:header>
            <h5 class="modal-title">Modal title</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
            </button>
        </template>

        <template v-slot:body>
            <p>Modal body text goes here.</p>
        </template>

    </modal-bootstrap>
  </div>
</template>

<script>
import ModalBootstrap from './ModalBootstrap.vue'
export default {
  name: 'Pare',
  components: {
    ModalBootstrap
  },
  props: {
    msg: String
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