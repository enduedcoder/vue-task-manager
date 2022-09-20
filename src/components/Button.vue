<template>
  <button
    @click="onClickHandler()"
    v-bind:style="{ background: color }"
    class="btn"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClickHandler() {
      this.$emit("btn-click");
    },
  },
};
</script>

<style></style>

<!-- 
    Notes:
    v-bind:style="{ background: color }" 
   (or)
    :style="{ background: color }" 


    v-bind:click="onClickHandler()"
    (or)
    @:click="onClickHandler()"
-->
