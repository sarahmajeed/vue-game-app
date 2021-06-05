<template>
  <div class="modal">
    <h2>You {{ uiState }}</h2>
    <img src="../assets/face.svg" alt="face" /> <br />
    <button @click="handleReset">Play Again!</button>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["uiState"]),
  },
  methods: {
    handleReset() {
      console.log("handling reset");
      this.$store.commit("handleReset");
    },
  },
};
</script>

<style lang="scss" scoped></style>
