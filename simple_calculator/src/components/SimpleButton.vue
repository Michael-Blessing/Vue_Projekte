<template>
  <button @click="calculate">
    {{beschriftung}}
  </button>
</template>

<script>


export default {
  emits: ['calculate'],
  name:'SimpleButton',
  props: {
    beschriftung: String
  },
  data() {
    return [];
  },
  methods: {
    calculate() {
      this.$emit('calculate', this.beschriftung);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.button {
  width:100px;
  padding:10px;
  border-radius: 10px;
}
</style>
