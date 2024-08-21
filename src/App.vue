<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>
  <div v-if="showModal"> 
    <Modal theme="sale1" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>

      </template>
      <h1>Ninja Giveaway!</h1>
      <p>Grab your ninja swag for half price!</p>
    </Modal>
  </div>
  <button @click.alt="toggleModal">Open modal(option/alt)</button>
  
  <!-- <input type="text" ref="name">
  <button @click="handleClick">click me</button> -->
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal }, 
  data() {
    return {
      title: 'My First Vue App :)',
      header: 'Sign uo for the Giveaway!',
      text: 'Grab your ninja swag for half price!',
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
      }
    }
  }



// Emitting Custom Events - 触发的自定义事件(Tutorial 5)
// Custom Event: can be fired from a component and then it can be listen to from the parent component - 自定义事件：可由组件触发，然后由父组件监听
// Click Event Modifiers(Tutorial 5)
// Slot - 插槽(Tutorial 5): is really useful for passing custom templates into components
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>

