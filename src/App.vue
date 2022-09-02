
<template> 
  <div class="main">
    <h2>VueJs Ex2</h2>
    <input type="text" ref="input">
    <button @click="focusBtn">Focus</button>
    <br />
    <!-- <h1 v-if="show">Priya modal</h1> -->
     <button v-if="show">Modal</button> 
      <button @click="show = !show">Modal</button> 
    <!-- <div class="prompt" v-if="show" @click="show = !show">
            <div id="modal-box" :class="{ sale: isValid }" @click.prevent="show = !show"> -->
    <ModalBox title="Sign up for the giveaway!" content="Grab your ninja swag for half price!" theme="sale" ref="modal" :show="show">
      <template v-slot:links >
        <a href="#" id="slot-link">Close</a>
      </template>
    </ModalBox> 

  </div>
  <!-- </div>
  </div> -->



</template>

<script>
import ModalBox from './components/ModalBox.vue'
export default {
  components: {
    ModalBox
  },
  data() {
    return {
      show: false
    }
  },
  methods: {
    focusBtn() {
      this.$refs.input.focus();
      console.log("focus");
    },
  }
}
</script>


<style>
* {
  margin: 0px;
  padding: 0;
}

.main {
  position: relative;
  height: 100%;
  padding: 20px;
}

button {
  margin: 5px 0px;
  padding: 5px 10px;
  background-color: dodgerblue;
  color: white;
  font-size: 1rem;
  border: 1px solid dodgerblue;
}

input {
  font-size: 1rem;
  padding: 5px;
}

#slot-link {
  text-align: center;
  color: white;
  background-color: black;
  padding: 4px 20px;
  text-decoration: none;
  font-size: 1.1rem;
  width: 80px;
  white-space: nowrap;
}
</style>




