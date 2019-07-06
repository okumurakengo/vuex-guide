<template>
  <div>
    <p>Clicked {{ count }} times! Count is {{ parity }}.</p>

    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
    <button @click="incrementIfOdd">Increment if Odd</button>
    <button @click="incrementAsync">Increment Async</button>
  </div>
</template>

<script>
import { mapState, mapGetters, mapActions } from "vuex";

export default {
  name: "Counter",
  computed: {
    ...mapState(["count"]),
    ...mapGetters(["parity"])
  },
  methods: mapActions([
    "increment",
    "decrement",
    "incrementIfOdd",
    "incrementAsync"
  ])
};
</script>
