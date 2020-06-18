<template>
  <ComponentWithSlot>
    <p class="red">I'm a p tag inside the slot</p>
    <FunctionalComp class="red" msg="I'm a component inside the slot"></FunctionalComp>
  </ComponentWithSlot>
  <p class="red">I'm a p tag outside the slot</p>
  <FunctionalComp class="red" msg="I'm a component outside the slot"></FunctionalComp>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FunctionalComp from './components/FunctionalComp.vue'
import ComponentWithSlot from './components/ComponentWithSlot.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ComponentWithSlot,
    FunctionalComp
  }
}
</script>

<style scoped>
.red {
  color: red;
}
/* ::v-deep(.functional) {
  color: red;
} */
</style>
