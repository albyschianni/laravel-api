<script>

  import axios from 'axios';

  export default {

    mounted() {

      axios.get('http://127.0.0.1:8001/api/v1/movie/all')
        .then(res => {
          
          const data = res.data;
          const success = data.success;
          const movies = data.response;
        })
        .catch(err => console.error(err));
    }
  }

</script>

<template>
  <div>
    <h1>hello world</h1>
  </div>
</template>

<style scoped>

</style>
