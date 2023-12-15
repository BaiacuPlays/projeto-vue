<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      operation: 'add',
    };
  },
  methods: {
    calculateResult() {
      switch (this.operation) {
        case 'add':
          return this.num1 + this.num2;
        case 'subtract':
          return this.num1 - this.num2;
        case 'multiply':
          return this.num1 * this.num2;
        case 'divide':
          return this.num1 / this.num2;
        default:
          return 0;
      }
    },
  },
};
</script>


<template>
   <div class="calculator">
    <input v-model="num1" type="number" placeholder="Número 1">
    <input v-model="num2" type="number" placeholder="Número 2">
    <select v-model="operation">
      <option value="add">+</option>
      <option value="subtract">-</option>
      <option value="multiply">*</option>
      <option value="divide">/</option>
    </select>
    <p>Resultado: {{ calculateResult() }}</p>
  </div>
</template>

<style scoped>
.calculator {
  text-align: center;
  width: 300px;
}

input {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  box-sizing: border-box;
}

select {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
  box-sizing: border-box;
}
</style>