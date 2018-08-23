<template>
  <div>
    <textarea v-model="theValue" @input="change"></textarea>
  </div>
</template>

<script>
export default {
  name: 'AlgaTextarea',
  props: {
    value: {
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
    change() {
      this.$emit('input', this.theValue);
    },
  },

  created() {
    // console.log('AlgaTextarea created');
  },
};
</script>

<style scoped>
  textarea {
    font-size: 2em;
  }
</style>
