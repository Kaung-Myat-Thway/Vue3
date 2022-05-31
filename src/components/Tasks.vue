<template>
  <div class="row">
  <div v-for="task in tasks" :key="task.id">
    <Task
      @delete-task="$emit('delete-task', task.id)"
      @toggle-reminder="$emit('toggle-reminder', task.id)"
      :task="task"
    />
  </div>
  </div>
</template>

<script>
import Task from "./Task.vue";
export default {
  name: "Tasks-list",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
  emits: ["delete-task", "toggle-reminder"], //sent data to parent
};
</script>

<style>
</style>