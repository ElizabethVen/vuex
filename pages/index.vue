<template>
  <div class="container">
    <button @click="increment">
      Incrementar
    </button>
    {{ $store.state.counter }}
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  methods: {
    ...mapMutations(['increment'])
  }
}
</script>
