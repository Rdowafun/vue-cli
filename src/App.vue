<template>
  <div class="wrapper">
    <Header :title="logo" :names="names" @send="title = $event" />
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  components: {
    Header,
  },
  data() {
    return {
      title: "Vuejs Init",
      logo: "Мы используем props",
      names: ["кнопка 1", "кнопка 2", "кнопка 3"],
    };
  },
  // methods: {
  //   getTitle(name) {
  //     this.title = name;
  //   },
  // },
};
</script>

<style>
</style>
