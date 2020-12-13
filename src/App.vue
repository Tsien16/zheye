<template>
  <div class="container">
    <global-header :user="currentUser"></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import "bootstrap/dist/css/bootstrap.min.css";

import ColumnList, { ColumnProps } from "@/components/ColumnList.vue";
import GlobalHeader, { UserProps } from "@/components/GlobalHeader.vue";

const currentUser: UserProps = {
  isLogin: true,
  name: "tsien"
};

const testData: ColumnProps[] = [
  {
    id: 1,
    title: "test1的专栏",
    description: "这是test1的专栏",
    avatar:
      "https://pic1.zhimg.com/v2-43259f6435eb8096750388fc002bd812_1440w.jpg?source=172ae18b"
  },
  {
    id: 2,
    title: "test2的专栏",
    description: "这是test2的专栏"
  },
  {
    id: 3,
    title: "test3的专栏",
    description: "这是test3的专栏",
    avatar:
      "https://pic1.zhimg.com/v2-43259f6435eb8096750388fc002bd812_1440w.jpg?source=172ae18b"
  },
  {
    id: 4,
    title: "test4的专栏",
    description: "这是test4的专栏",
    avatar:
      "https://pic1.zhimg.com/v2-43259f6435eb8096750388fc002bd812_1440w.jpg?source=172ae18b"
  }
];

export default defineComponent({
  name: "App",
  components: {
    GlobalHeader,
    ColumnList
  },
  setup() {
    return {
      list: testData,
      currentUser
    };
  }
});
</script>

<style></style>
