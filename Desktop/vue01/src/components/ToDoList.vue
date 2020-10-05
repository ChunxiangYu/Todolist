<template>
  <div id="ToDoList" class="ToDoList">
    <h1 v-html="title"></h1>
    <div>
      <input type="text" v-model="newItem">
      <button @click="addNewItem">Add</button>
    </div>
    <ul>
      <li v-for="item in items" :key="item.id">
        <!-- 待办事项 -->
        <span v-text="item.title"></span>
        <!-- 完成按钮 -->
        <button v-on:click="toggleFinish(recycleItem)">Done</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ToDoList',
  data () {
    return {
      title: 'ToDoList',
      items: [],
      id: 0
    }
  }
}
</script>
