<template>
  <section>
    Name: {{ fullName }}<br>
    Message: {{ message }}
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

interface User {
    firstName: string
    lastName: string
}

export default Vue.extend({
  name: 'IndexPage',

  data () {
    return {
      name: {
        firstName: 'Buddy',
        lastName: 'Williams'
      } as User,
      message: 'Hello, world!' as string
    }
  },

  computed: {
    fullName (): string {
      return `${this.name.firstName} ${this.name.lastName}`
    }
  }
})
</script>
