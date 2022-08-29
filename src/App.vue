 <template>
  
     <input type="text" ref="input">
  <button @click="focusbtn">Focus</button>

 
</template>

<script >
  //using template reference
  export default{
   methods:{
    focusbtn() {
    this.$refs.input.focus();//template reference
  }
   } 
  }
 

  // import HelloWorldVue from './components/HelloWorld.vue';

</script>


}


<style>


button {
    margin: 8px 2;
    padding: 5px 10px;
    background-color: #1e90ff;
    color: #fff;
    font-size: 1rem;
    border: 1px solid dodgerblue;
}
input{
  font-size: large;
}
</style>
