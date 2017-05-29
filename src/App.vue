<template>
  <div id="app">
    <p>Count: {{ count }}</p>
  </div>
</template>

<script>
  import { Observable } from 'rxjs/Observable'

  export default {
    name: 'app',
    data () {
      return {
        count: 0
      }
    },
    created () {
      const obs = Observable.interval(1000)
      obs.subscribe(
        (value) => this.count = value
      )
    }
  }
</script>

<style lang="scss">

</style>
