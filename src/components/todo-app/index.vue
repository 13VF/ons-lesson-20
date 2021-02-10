<template>
  <div class="mainWrapper">
    <h1 class="mainTitle">Мой список дел :)</h1>

    <div class="todoControls">
      <select name="" id="" class="todoControls__prioritySelect">
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
      </select>
      <input type="text" placeholder="Введите текст" class="todoControls__textInput">
      <input type="text" placeholder="Введите deadline" class="todoControls__dateInput">
      <button class="todoControls__addButton">+</button>
    </div>

    <div class="todoList">
      <TodoAppItem
        v-for="todoItem of tasks"
        :key="todoItem.id"
        :item="todoItem"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import TodoAppItem from './todo-item.vue';

export default Vue.extend({
  name: 'TodoApp',

  components: {
    TodoAppItem,
  },

  props: {
    tasks: {
      type: Array,
      default: () => [],
    },
  },
});
</script>

<style scoped>
  .mainWrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 500px;
  }

  .todoControls {
    margin: 16px 0;
  }

  .todoList {
    width: 100%;
    max-width: 800px;
    padding: 16px;
    box-sizing: border-box;
  }
</style>
