<template>
  <header class="header">
    <a href="#" class="logo">{{ title }}</a>
    <ul>
      <li v-for="(name, index) in names" :key="index" @click="$emit('send', name)">
        {{ name }}
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  props: {
    title: {
      typeof: String,
      default: "Hello",
    },
    names: {
      typeof: Array,
    },
  },
  // methods: {
  //   send(name) {
  //     this.$emit('send', name)
  //   },
  // },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-decoration: none;
}
ul {
  list-style: none;
  display: flex;
  gap: 30px;
  font-size: 30px;
}
a {
  font-size: 30px;
  color: red;
}
.header {
  background: #000;
  color: white;
  padding: 30px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>