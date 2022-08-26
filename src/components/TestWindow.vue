<template>
  <div class="main">
    <div>
      <h1>Redactor</h1>
      <textarea v-model="text" cols="30" rows="10"></textarea>
    </div>
    <div>
      <h1>Preview</h1>
      <p class="main__text" v-html="markdownToHtml"></p>
    </div>
  </div>
</template>

<script>
import { marked } from "marked";
export default {
  data: () => ({
    text: "",
  }),
  mounted() {
    if (localStorage.text) {
      this.text = localStorage.text;
    }
  },
  computed: {
    markdownToHtml() {
      return marked(this.text);
    },
  },
  watch: {
    text(newText) {
      localStorage.text = newText;
    },
  },
};
</script>

<style>
.main {
  display: flex;
  justify-content: space-around;
}
.main__text {
  white-space: pre-line;
}
</style>
