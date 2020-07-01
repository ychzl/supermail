<template>
  <div class="tabItem" @click="itemClick">
      <slot name="icon"></slot>
      <div :class="{'active-item' : isactive, 'item-bar': true}">
          <slot name="text"></slot>
      </div>
  </div>
</template>

<script>
export default {
  name: 'tabItem',
  props: {
    path: {
      type: String,
      default: '/home'
    }
  },
  data() {
    return {
      // isactive: false
    }
  },
  computed: {
    isactive() {
      return this.$route.path.indexOf(this.path) !== -1
      // return true
    }
  },
  mounted() {
  },
  methods: {
    itemClick() {
      if(this.$route.path.indexOf(this.path) !== -1) return false;
      this.$router.replace(this.path)
    }
  }
}
</script>

<style>
.active-item {
  color: red;
}
</style>
