<script setup lang="ts">
import type { UserData } from "@/types/user.d";

const userData = defineModel<UserData>({ required: true });
</script>

<template>
  <form>
    <h1>Login</h1>
    <label>
      <span>Username</span>
      <input v-model="userData.username" type="text" />
    </label>

    <label>
      <span>Password</span>
      <input v-model="userData.password" type="password" />
    </label>

    <button>Login</button>
  </form>
</template>
