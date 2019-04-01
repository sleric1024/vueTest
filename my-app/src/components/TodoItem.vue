<template>
  <li class="item">
    <input type="checkbox" v-model="checked">
    <slot name="itemSlot" v-bind="{checked}"></slot>
    <span>{{ testprop }}</span>
  </li>
</template>

<script>
export default {
  props: ['testprop'],
  data() {
    return {
      checked: false
    }
  }
}
</script>

<style scoped>
.item {
    color: red;
}
</style>