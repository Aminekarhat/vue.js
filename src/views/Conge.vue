<template>
    <div>
      <h2>Register</h2>
      <form @submit.prevent="submitForm">
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div>
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <div>
          <label for="nickname">Nickname:</label>
          <input type="text" id="nickname" v-model="nickname" required>
        </div>
        <button type="submit">Submit</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: "",
        password: "",
        nickname: "",
      };
    },
    methods: {
      submitForm() {
        // Here you can add your registration logic, such as sending a request to your API or submitting a form
        console.log("Registration form submitted!");
      },
    },
  };
  </script>
  