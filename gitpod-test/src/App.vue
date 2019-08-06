<template>
  <div id="app">
    <toggle-case />
  </div>
</template>

<script>
import ToggleCase from './components/ToggleCase.vue';

export default {
  name: 'app',
  components: {
    ToggleCase
  }
}
</script>

<style lang="sass">
@import "~bulma/bulma.sass"
</style>
