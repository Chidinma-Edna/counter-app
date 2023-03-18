<template>
  <p className="result">Result: {{ count }}</p>
  <button type="button" className="plus" @click="handlePlus">+</button>
  <button type="button" className="minus" @click="handleMinus">-</button>
  <button type="button" className="reset" @click="handleReset">reset</button>
  <div class="col-6">
                <input v-model="quantity" v-on:input="$emit('input', quantity)" class="form-control" >
            </div>

            
</template>

<script>
export default {
  name: "Counter",
  props: {
    count: Number,
  
  },
  emits: ["plus", "minus", "reset"],
  methods: {
    handlePlus() {
      this.$emit("plus");
    },
    handleMinus() {
      this.$emit("minus");
    },
   
    handleReset() {
      this.$emit("reset");
    },
    
  },
};
</script>
    

<style>
.result{
   font-size: 30px;
   color: black;
}
.plus{
   width: 100px;
   border-radius: 12px;
   padding: 10px;
   background-color:yellow;
   box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
   //opacity: 0.6;
  cursor: pointer;
}

.plus:hover {
  background-color: black;
  color: white;
}

.minus{
   width: 100px;
   border-radius: 12px;
   padding: 10px;
   background-color:yellow;
   box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}

.minus:hover {
  background-color: black;
  color: white;
}



/* CSS */
.plus {
  align-items: center;
  background: #000;
  border: 0;
  border-radius: 8px;
  box-shadow: -10px -10px 30px 0 #fff,10px 10px 30px 0 #000;
  box-sizing: border-box;
  color: #2a1f62;
  cursor: pointer;
  display: flex;
  font-family: "Cascadia Code",Consolas,Monaco,"Andale Mono","Ubuntu Mono",monospace;
  font-size: 3rem;
  justify-content: center;
  line-height: 1.5rem;
  padding: 45px;
  position: relative;
  text-align: left;
  transition: .2s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: pre;
  width: max-content;
  word-break: normal;
  word-spacing: normal;
}

.plus:hover {
  background: blue;
  box-shadow: -15px -15px 30px 0 #fff, 15px 15px 30px 0 #1d0dca17;
}

@media (min-width: 768px) {
  .plus {
    padding: 24px;
  }
}


.minus {
  align-items: right;
  background: #000;
  border: 0;
  border-radius: 8px;
  box-shadow: -10px -10px 30px 0 #fff,10px 10px 30px 0 #000;
  box-sizing: border-box;
  color: #2a1f62;
  cursor: pointer;
  display: flex;
  margin-left:auto;
  font-family: "Cascadia Code",Consolas,Monaco,"Andale Mono","Ubuntu Mono",monospace;
  font-size: 3rem;
  justify-content: right;
  line-height: 1.5rem;
  padding: 45px;
  position: relative;
  text-align: right;
  transition: .2s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: pre;
  width: max-content;
  word-break: normal;
  word-spacing: normal;
  touch-action: manipulation
}

.minus:hover {
  background: blue;
  box-shadow: -15px -15px 30px 0 #fff, 15px 15px 30px 0 #1d0dca17;
  box-shadow: #FF 0 -6px 8px inset;
  transform: scale(1.125);
}

@media (min-width: 768px) {
  .minus {
    padding: 24px;
  }
}
        



/* CSS */
.reset {
  appearance: none;
  background-color: #ff;
  border-radius: 40em;
  border-style: none;
  box-shadow: #ADCFFF 0 -12px 6px inset;
  box-sizing: border-box;
  color: #000000;
  cursor: pointer;
  display: inline-block;
  font-family: -apple-system,sans-serif;
  font-size: 1.2rem;
  font-weight: 700;
  letter-spacing: -.24px;
  margin: 0;

  outline: none;
  padding: 2rem 2.4rem;
  quotes: auto;
  text-align: center;
  text-decoration: none;
  transition: all .15s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.reset:hover {
  background-color: #FFC229;
  box-shadow: #FF6314 0 -6px 8px inset;
  transform: scale(1.125);
}

.reset:active {
  transform: scale(1.025);
}

@media (min-width: 768px) {
  .reset {
    font-size: 1.5rem;
    padding: .75rem 2rem;
  }
}
</style>
