<template>
  <form v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" class="" action="#" method="post">
    <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title"><br>
    <br>
    <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author"><br>
    <br>
    <button type="submit" name="button">Add Book</button>
  </form>
</template>

<script>
export default {
  name: 'BookForm',
  props: ['books'],
  data() {
    return {
      bookTitle: '',
      bookAuthor: ''
    }
  },
  methods: {
    bookSubmit(bookTitle, bookAuthor) {
      this.$emit('addBook', bookTitle, bookAuthor)
    }
  }
}
</script>

<style>
input {
    border-color: green;
    font-style: italic;
}

form {
    padding-top: 1em;
}
</style>


