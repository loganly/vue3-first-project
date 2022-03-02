<template>
  <h1>这是首页</h1>
  <Todolist />
  <Rate v-model="score" @update-rate="update" />
</template>

<script setup>
import { ref } from 'vue';
import Todolist from '../components/Todolist.vue';
import Rate from '../components/Rate.vue';

let score = ref(3.5);
function update(num) {
  score.value = num;
}
</script>
