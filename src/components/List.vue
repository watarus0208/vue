<template>
  <ul class="List">
    <li
      v-for="childListItem in childListData"
      :key="childListItem.id"
      class="ListItem"
    >
      <p class="ListItemNumber">番号：{{ childListItem.id }}</p>
      <p class="ListItemName">名前：{{ childListItem.name }}</p>
    </li>
  </ul>
</template>

<script>
import { ref } from "@vue/composition-api";

export default {
  props: {
    childListData: {
      default: [],
      required: true,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style scoped>
.List {
  border: solid 1px black;
  padding: 16px;
}

.ListItem {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  list-style: none;
  width: 300px;
  height: 80px;
  background-color: #E0FFC1;
  margin-bottom: 16px;
  padding: 16px;
}
</style>