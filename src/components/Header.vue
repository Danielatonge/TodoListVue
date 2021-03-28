<template>
  <header>
    <h2>Task Tracker</h2>
    <Button
      :text="!toggle ? 'Add Task' : 'Close'"
      :color="!toggle ? 'green' : 'red'"
      @btn-click="$emit('toggle-add-task')"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  components: { Button },
  name: "Header",
  methods: {},
  props: {
    toggle: Boolean,
  }
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