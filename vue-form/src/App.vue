<template lang="">
  <div>
    <form v-on:submit.prevent="submitForm">
      <div>
        <label for="username">ID : </label>
        <input id="username" type="text" v-model="username">
      </div>
      <div>
        <label for="password">PW : </label>
        <input id="password" type="password" v-model="password">
      </div>
      <button type="submit">login</button>
    </form>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  data: function() {
    return {
      username:'',
      password:''
    }
  },
  methods: {
    submitForm: function() {
      // event.preventDefault();
      console.log(this.username, this.password);
      let url = 'https://jsonplaceholder.typicode.come/users';
      axios.post(url, data)
      .then(function(response) {
        console.log(response);
      })
      .catch(function(error) {
        console.log(error);
      })
    }
  }
}
</script>
<style lang="">
  
</style>