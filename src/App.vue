//app

<template>
  <Counter :count="count" @plus="handlePlus" @minus="handleMinus" @reset="handleReset" @input="inputQuantity" />
  
</template>

<script>
import Counter from "./components/Counter.vue";
export default {
  name: "App",
  components: {
    Counter,
    
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    handlePlus() {
      this.count++;
    },
    handleMinus() {
      this.count--;
    },

     handleReset() {
      this.reset;
    },

    handleQuantity() {
      this.inputQuantity;
    },
  },
};
</script>
