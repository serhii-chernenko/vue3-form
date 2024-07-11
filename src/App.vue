<script setup>
import { ref } from "vue";
import { faker } from "@faker-js/faker";

import LoginForm from "./components/LoginForm.vue";
const userData = ref({
  username: "",
  password: "",
});

function randomize() {
  userData.value = {
    username: faker.internet.userName(),
    password: faker.internet.password(),
  };
}
</script>

<template>
  <div class="page">
    <div></div>
    <LoginForm v-model="userData" />

    <div class="result">
      <h2>userData in Parent</h2>
      <pre>{{ userData }}</pre>
      <button @click="randomize">Change userData from Parent</button>
      <div class="mt-3">
        <small
          >Setting the data in the parent should immediately pass the updated
          values down to the form</small
        >
      </div>
    </div>
  </div>
</template>
