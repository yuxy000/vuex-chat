<template>
  <div class="chatapp">
    <thread-section></thread-section>
    <message-section></message-section>
  </div>
</template>

<script>
import ThreadSection from './components/ThreadSection'
import MessageSection from './components/MessageSection'
export default {
  name: 'App',
  components: {
    ThreadSection,
    MessageSection
  }
}
</script>

<style src="./css/chat.css"></style>
