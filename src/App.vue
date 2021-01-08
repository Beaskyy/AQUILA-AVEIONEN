<template>
  <div id="app">



      <Foundation
      :name="name"
      :social_media="social_media"
      />



  </div>
</template>

<script>
import Foundation from './components/Foundation.vue'


export default {
  name: 'App',
  components: {
    Foundation
  },
  data() {
    return {
      name: '',
      social_media: ''
    }
  },
  mounted() {
    fetch('https://hirng-x2021.glitch.me/api', {
      method: 'get'
    })
    .then((response) => {
      return response.json()
    })
    .then((jsonData) => {
      console.log(jsonData)


      this.name = jsonData.name
      this.social_media = jsonData.social_media
      console.log(this.name)
      console.log(this.social_media)
    })
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 60px;
}
</style>
