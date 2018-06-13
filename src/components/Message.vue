<template>
  <li class="message-list-item">
    <h5 class="message-author-name">{{ message.authorName }}</h5>
    <div class="message-time">
      {{ message.timestamp | time }}
    </div>
    <div class="message-text">{{ message.text }}</div>
  </li>
</template>

<style lang="css" scoped>
</style>

<script>
export default {
  name: 'Message',
  props: {
    message: Object
  },
  data () {
    return {
    }
  }
}
</script>
