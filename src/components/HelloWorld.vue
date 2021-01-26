<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
  <div>{{computedCount}}===计算属性 </div>
  <input type="button" @keyup.enter="onSay" value="按键">
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0
    }
  },
  computed: {
    computedCount() {
      return this.count * 2;
    }
  },
  methods: {
    onSay() {
      console.log("鼠标时间")
    }
  }
}
</script>
