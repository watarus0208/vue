<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <List :childListData="listData" />
  </div>
</template>

<script>
import { ref } from "@vue/composition-api";
import List from "./components/List";

export default {
  name: "App",
  components: {
    List,
  },
  setup() {
    const message = ref("Hello World");
    const listData = [
      {
        id: 1,
        name: "りんご",
      },
      {
        id: 2,
        name: "メロン",
      },
      {
        id: 3,
        name: "ぶどう",
      },
    ];
    return {
      message,
      listData,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
