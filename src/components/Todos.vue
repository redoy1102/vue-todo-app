<template>
  <div>
    <div v-for="(todo,id) in todos" :key="id">
      <TodoItem v-bind:todo="todo"
                v-on:del-todo="$emit('del-todo', todo.id)"
      />
      <!--    first todo is props name and second is data-->

    </div>
  </div>
</template>

<script>
import TodoItem from "@/components/TodoItem";

export default {
  props: ["todos"],
  components: {
    TodoItem
  }
}
</script>

<style scoped>

</style>