<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @toggle-add-task="$emit('toggle-add-task')"  :text="showToggle? 'CLOSE' :'ADD TASK'" :color="showToggle? 'red' :'blue'" />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header-area",
  props: {
    title: String,
    showToggle : Boolean
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>