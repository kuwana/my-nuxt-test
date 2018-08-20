<template>
  <section class="container">
    <table>
      <tr>
        <td>{{ name }}</td>
        <td class="test">
          <input v-model="firstName">
          <input v-model="lastName">
        </td>
        <td class="test">
          <div>{{ firstName }}</div>
          <div>{{ lastName }}</div>
          <div><button @click="送信()">送信</button></div>
        </td>
      </tr>
    </table>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import fullName from '~/components/fullName'

export default {
  components: {
    AppLogo,
    fullName
  },
  data () {
    return {
      firstName: 'takuya',
      lastName: 'kuwana',
      age: 32
    }
  },
  methods: {
    fullName () {
      return this.firstName + this.lastName
    },
    送信 () {
      window.alert(this.firstName +this.lastName)
    }
  }
}
</script>

<style scoped>
.test {
  font-weight: bold;
}
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

