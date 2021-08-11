<template>
  <div class="container mb-5">
    <h1 v-if="flag">Login Page</h1>
    <h1 v-else>Sign Up Page</h1>
    <!-- SECTION for Login Page -->
    <div v-if="flag">
      <div class="form-group">
        <label for="Email">Email:</label>
        <input type="email" class="form-control" />
      </div>
      <div class="form-group mb-3">
        <label for="password">Password:</label>
        <input type="password" class="form-control" />
      </div>
      <button class="btn btn-primary me-3" @click="btnClick('login')">Login</button>
      <button class="btn btn-primary" @click="btnClick('signup')">Sign Up</button>
    </div>
    <div v-else>
      <div class="form-group">
        <label for="fname">First Name:</label>
        <input type="text" class="form-control" />
      </div>
      <div class="form-group">
        <label for="fname">Last Name:</label>
        <input type="text" class="form-control" />
      </div>
      <div class="form-group">
        <label for="password">Password:</label>
        <input type="password" class="form-control" />
      </div>
      <div class="form-group mb-3">
        <label for="rpassword">Retype-Password:</label>
        <input type="password" class="form-control" />
      </div> 
      <button class="btn btn-primary me-3" @click="btnClick('login')">Log In</button>
      <button class="btn btn-primary" @click="btnClick('signup')">Sign Up</button>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return { 
      flag: true,
    }
  },
  methods: {
    btnClick: function(value) {
      if (value == 'login') {
        this.flag = true;
      } else {
        this.flag = false;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
