<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="doSomething">test</button>
    <div>
      {{ test }}
    </div>
  </div>
</template>

<script>
import { ImplikationenGenerator } from "../lib/Implikationen";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      test: "test"
    };
  },
  methods: {
    doSomething() {
      let generator = new ImplikationenGenerator();
      this.test = generator.sampleMethod();
    }
  }
};
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
