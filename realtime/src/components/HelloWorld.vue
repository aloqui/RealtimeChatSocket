<template>
  <div class="hello">
   
  </div>
</template>

<script>

  export default {
    name: 'HelloWorld',
    data() {
      return {
        messages: {},
        message: null,
        user: {
          id: 1,
          name: 'Al Oquindo'
        }
      }
    },
    methods: {
      sendMsg() {
        console.log('Chat Message Sent')
      }
    },
    mounted() {
      this.$nextTick(function () {
        socket.on('connect', function () {
          console.log("Connected to the server.");
        })
      })
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
