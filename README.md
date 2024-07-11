---
difficulty: 1
training: true
chapter: "Chapter 1: Advanced Component Techniques"
tags: vue
---

# Form Component with v-model Challenge

Your task is to create a `LoginForm` component that works with v-model.

## Requirements

1. The v-model value should be an object with a username and password property
2. The data should ONLY be updated in the parent when the form is submitted
   - If the data in the parent updates as you're typing in the username or password input, you haven't met the objective.
3. The communication between the `LoginForm` and `App.vue` should ONLY be via the v-model directive
   - In other words, don't emit a `submit` event from the `LoginForm` component or any other separate event other than the event that is emitted to support the v-model syntactic sugar
4. When the data is updated in the parent it should flow down through the v-model and immediately update the value of the username/password fields in the form

> 💡 HINT: Feel free to use TypeScript to make your component type safe if you'd like. This is NOT required however.

![Screenshot of the solution](https://images.certificates.dev/csvd-training-code-challenge-2.gif)
