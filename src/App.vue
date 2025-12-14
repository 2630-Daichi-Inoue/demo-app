<script setup>
  import { ref } from 'vue'
  import FoodCard from './components/FoodCard.vue'
  const foods = ref([
    { name: '寿司', emoji: '🍣' },
    { name: 'ハンバーガー', emoji: '🍔' },
    { name: 'カツ丼', emoji: '🐖' },
    { name: 'ラーメン', emoji: '🍜'},
    { name: 'ピザ', emoji: '🍕' },
    { name: 'サラダ', emoji: '🥗' },
    { name: '鍋', emoji: '🍲' }
  ])
</script>

<template>
  <main>
    <h1 class="title">今日何食べる？</h1>
    <FoodCard :name="foods[0].name" :emoji="foods[0].emoji"/>
    VS.
    <FoodCard :name="foods[1].name" :emoji="foods[1].emoji"/>
  </main>
</template>

<style scoped>
  main {
    width: 350px;
    margin: 100px auto;
    text-align: center;
  }

  .title {
    margin-bottom: 60px;
  }
</style>
