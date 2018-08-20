<template>
  <h1>{{ fullName() }}</h1>
</template>

<script>
export default {
  props: ['firstName', 'lastName'],
  methods: {
    fullName () {
      return this.firstName + this.lastName
    }
  }
}

</script>
