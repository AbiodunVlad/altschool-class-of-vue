<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { ref, reactive } from "@vue/reactivity";
import actions from "../composables/actions";

const { message, matchColor } = actions(colors);

export default {
  setup() {
    const colors = ["green", "red", "blue", "purple"];

    return { colors };
  },
};
</script>

<style></style>
