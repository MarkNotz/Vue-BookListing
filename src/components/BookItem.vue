<template>
  <li>{{book.title}}:&emsp;{{book.author}}</li>
</template>

<script>
export default {
  name: "BookItem",
  props: ["book"]
};
</script>

<style>

li {
  display: block;
  margin: 0 10px 0 0;
  }

</style>
