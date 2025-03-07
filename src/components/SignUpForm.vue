<template>
  <div class="form-container">
    <form>
        <label>Email</label>
        <input type="email" v-model="email" required>

        <label>Password</label>
        <input type="text" v-model="password">
  </form>
  </div>
  <p>Email: {{ email }}</p>
  <p>Email: {{ password }}</p>

</template>

<script>
export default {
    data(){
        return {
            email: '',
            password: '',
        }
    },

}
</script>

<style>
body {
  background-color: #121212; /* Dark background */
  color: #ffffff; /* Light text color for contrast */
  font-family: Arial, sans-serif;
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-container {
  background-color: #1e1e1e; /* Slightly lighter dark background for the form */
  padding: 40px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

label {
  font-size: 16px;
  margin-bottom: 8px;
  color: #ffffff; /* Light text color for contrast */
}

input{
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #444444;
  border-radius: 4px;
  background-color: #2a2a2a; /* Dark input background */
  color: #ffffff; /* Light text color for contrast */
  outline: none;
  transition: border-color 0.3s;
}

input:focus {
  border-color: #6200ea; /* Highlight border color on focus */
}

input[type="email"]::placeholder {
  color: #bbbbbb; /* Light placeholder color */
}
</style>