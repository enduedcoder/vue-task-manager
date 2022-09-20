<template>
  <div :key="task.id" v-for="task in tasks">
    <h3>
      <SingleTask
        @toggle-reminder="$emit('toggle-reminder', task.id)"
        @delete-task="$emit('delete-task', task.id)"
        :task="task"
      />
    </h3>
  </div>
</template>

<script>
import SingleTask from "./SingleTask";
export default {
  name: "Tasks",
  components: { SingleTask },
  props: {
    tasks: Array,
  },
  emits: ["delete-task", "toggle-reminder"],
};
</script>
