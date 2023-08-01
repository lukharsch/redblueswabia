<template>
  <span class="text-h3"> {{ title }} </span>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: "Red-Blue Swabia 1846",
  },
});
</script>

<style scoped>
span {
  padding: 0 0 8px;
  position: relative;
  z-index: 1;
}
span::before {
  content: "";
  position: absolute;
  bottom: 12px;
  width: 105%;
  height: 15px;
  background: rgba(var(--v-theme-secondary), 0.7);
  z-index: -1;
}
</style>
