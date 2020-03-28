<template>
  <div class="container">
    <div class="form">
      <h2>学生登录</h2>
      <br />
      <label for="id">学号：</label>
      <input type="text" id="id" v-model="id"/>
      <br />
      <br />
      <label for="psw">密码：</label>
      <input type="password" id="psw" v-model="psw"/>
      <br />
      <br />
      <br />
      <button type="button" @click="submit">登录</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      id: '',
      psw: ''
    }
  },
  methods: {
    submit: function () {
      if (this.id === '' || this.psw === '') {
        alert('请输入完整信息')
      } else {
        this.$router.push({path: '/home'})
      }
    }
  }
}
</script>

<style scoped>
.container {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.form {
  margin: 0 auto;
  padding: 2rem 3rem;
  border: 1px solid #075f5f;
  background: #0c8484;
  color: white;
  text-align: center;
}
a{
    padding: .5rem 1rem;
    background: #075f5f;
    box-shadow: 1px 1px 2px #075f5f;
}
a:hover{
    outline: 2px solid rgb(196, 196, 196);
}
button{
  padding: .5rem 1rem;
  font-size: 1rem;
}
</style>
