<template>
  <div id="app">
    <span v-on:click="change" class="quote">{{ quotes[counter] }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 4,
      quotes: [
        "Repeat question in own words",
        "Check Assumptions",
        "Use real examples",
        "Brainstorm solution and big O",
        "Write working code",
        "Test code"
      ]
    };
  },
  methods: {
    change() {
      let randomIndex = Math.floor(Math.random() * this.quotes.length + 0);
      this.counter = randomIndex;
    }
  }
};
</script>
