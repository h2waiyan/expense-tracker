<template>
  <MyHeader />
  <div class="container">
    <MyBalance :total="total" />
    <IncomeExpense />
    <TranscationList :transactions="transactions"/>
    <AddTransaction />
  </div>
</template>

<script setup>
import MyHeader from '@/components/MyHeader.vue';
import MyBalance from '@/components/MyBalance.vue';
import IncomeExpense from '@/components/IncomeExpense.vue';
import TranscationList from '@/components/TranscationList.vue';
import AddTransaction from './components/AddTransaction.vue';

import { ref,computed } from 'vue';

const transactions = ref([
  { id: 1, text: "Flowers", amount: -19.99 },
  { id: 2, text: "Salary", amount: 300.00 },
  { id: 3, text: "Book", amount: -10.00 },
  { id: 4, text: "Laptop", amount: 150.00 }
])

const total = computed(() => {
  return transactions.value.reduce((acc, item) => (acc += item.amount), 0).toFixed(2);
});

</script>

<style lang="scss">

</style>
