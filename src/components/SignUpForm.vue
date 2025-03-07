<template>
  <div class="form-container">
    <form>
        <label>Email</label>
        <input type="email" v-model="email" required placeholder="johndoe@gmail.com">

        <label>Password</label>
        <input type="text" v-model="password">

        <label>Role</label>
        <select v-model="role">
            <option value="Developer">Web Developer</option>
            <option value="Designer">Designer</option>
        </select>
        <div class="terms">
            <input type="checkbox" required v-model="terms"></input>
            <label>Accept terms and conditions</label>
        </div>
        <div>
            <input value="vin" type="checkbox" v-model="names"></input>
            <label>Vin</label>
        </div>
        <div>
            <input type="checkbox" value="emma" v-model="names"></input>
            <label>Emma</label>
        </div>
        <div>
            <input type="checkbox" value="kian" v-model="names"></input>
            <label>Kian</label>
        </div>
  </form>
  </div>
  <p>Email: {{ email }}</p>
  <p>Email: {{ password }}</p>
  <p>Email: {{ role }}</p>
  <p>Terms: {{ terms }}</p>
  <p>Names: {{ names }}</p>





</template>

<script>
export default {
    data(){
        return {
            email: '',
            password: '',
            role: 'Designer',
            terms: false,
            names: [],
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

input, select{
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
input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0px 10px 0 0;
    position: relative;
    top: 2px;
}
input:focus {
  border-color: #6200ea; /* Highlight border color on focus */
}

input[type="email"]::placeholder {
  color: #bbbbbb; /* Light placeholder color */
}
</style>