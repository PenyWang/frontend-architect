<template>
  <div class="hello">
    <h1>{{ test }} {{ b }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      a: 1,
      b: 2
    }
  },
  // beforeCreate() { // beforeCreate之前获取data的方式
  //   console.log(this.constructor.options.data());
  // },
  // created() {
  //   console.log(this._data);
  // },
  mounted() {
    setTimeout(() => {
      this.b = 7
      console.log(999);
    }, 1000)
  },
  computed: {
    test(){
      console.log(888);
      return this.a;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
