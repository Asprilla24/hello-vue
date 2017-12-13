<template>
  <div class="row">
    <h1>{{ msg }}</h1>
    <div>
      <ul>
        <li v-for="comment in comments">
          {{comment}}
        </li>
      </ul>
    </div>
    <div class="col-md-12">
      <input type="text" v-model="input_comment">
    </div>
    <div class="row">
      <div class="col-md-12">

      <button class="btn btn-primary" v-on:click="addComment(input_comment)">Post</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      comments: ['Alde Ganteng'],
      input_comment: ''
    }
  },

  methods: {
    addComment: function($data) {
      this.comments.push($data)
      this.input_comment = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-position: inside;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
