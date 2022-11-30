<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import Home from '../components/Home.vue'
import { ref, onMounted } from 'vue'

const el = ref()

onMounted(() => {
  el.value // <div>
  console.log('el.value =>',el.value);
})

</script>

<template>
  <main>
    <Home />
    <div ref="el"></div>
    {{msg}}
  </main>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello world!'
    }
  },
  mounted(){
    console.log('this mounted');
  }
}
</script>
