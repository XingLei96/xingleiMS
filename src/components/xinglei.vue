<template>
  <div>
    <button @click="setValue">子传父值</button>

    <button>子组件接受父组件传过来的值 -------- {{ message }}</button>

  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: Array, //可指定接收类型，如:Array.
      default: [11,221,33], //可设置默认值
    },
  },
  data() {
    return {
      value: "sendValue子组件传过来的值",
    };
  },

  mounted() {
    this.setValue()
  },

  methods: {
    setValue() {
      this.$emit("getdata", this.value); //this.value为向父组件传递的数据
    },
  },
};
</script>
<style lang='scss' scoped>
</style>