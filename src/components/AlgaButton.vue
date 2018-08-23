<template>
  <button @click="click">{{ title }}</button>
</template>

<script>
export default {
  name: 'AlgaButton',
  props: {
    title: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      theValue: this.value,
      va: false,
    };
  },
  methods: {
    click() {
      this.$emit('click');
    },
  },

  created() {
    // console.log('AlgaButton created');
  },
};
</script>

<style></style>
