<template>
  <div class="thread-section">
    <div class="thread-count">
      <span v-show="unreadCount">
        Unread threads {{ unreadCount }}
      </span>
    </div>
    <ul class="thread-list">
      <thread
        v-for="thread in threads"
        :key="thread.id"
        :thread="thread"
        :active="thread.id === currentThread.id"
        @switch-thread="switchThread">
      </thread>
    </ul>
  </div>
</template>

<style lang="css" scoped>
</style>

<script>
import Thread from './Thread'
import { mapActions, mapGetters } from 'vuex'
export default {
  name: 'ThreadSection',
  data () {
    return {
    }
  },
  components: {
    Thread
  },
  computed: mapGetters([
    'threads',
    'currentThread',
    'unreadCount'
  ]),
  methods: mapActions([
    'switchThread'
  ])
}
</script>
