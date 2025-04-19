<template>
  <div class="hello">
    <div>
      <input type="text" v-model="inputContent" placeholder="请输入内容" />
    </div>
    <div>
      <p>{{ inputContent }}</p>
    </div>
    <div>
      <button @click="clearInput">清空</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      inputContent: '' // 用于绑定输入框的内容
    };
  },
  methods: {
    // 清空输入框的内容
    clearInput() {
      this.inputContent = '';
    }
  }
}
</script>

<style scoped>
.hello {
  margin-top: 20px;
  text-align: center;
}
input {
  padding: 10px;
  margin-bottom: 10px;
  width: 200px;
}
button {
  padding: 5px 10px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #3b9a72;
}
</style>