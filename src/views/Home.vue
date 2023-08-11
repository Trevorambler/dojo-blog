<template>
  <div class="home">
    <p>My name is {{ name }} my age is {{age }}</p>
    <button @click="handleClick">Click Me</button>
    <button @click="age++">add 1 to age </button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from 'vue'

// @ is an alias to /src


export default {
  name: 'Home',
  setup() {

   // const p = ref(null)

    const name = ref('mario')
    const age = ref(30)
    

    const handleClick = () => {
      name.value = 'luigi'
      age.value = 35
    }

    return { name, age, handleClick,}
    
  }
}
</script>
