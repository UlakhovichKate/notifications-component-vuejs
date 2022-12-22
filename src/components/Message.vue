<template>
  <div class="col-12" v-if=isActive>
    <div :class="['alert-'+info.type]" class="row alert" role="alert">
      <div class="col-11">{{ info.msg }}</div>
      <button type="button" class="col-1 btn-close" aria-label="Close" v-on:click="closeAlert"></button>
    </div>
  </div>
</template>

<script>

export default {
  name: "Message",
  props: ['info'],
  data() {
    return {
      isActive: true
    }
  },
  methods: {
    closeAlert() {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style scoped>

</style>
