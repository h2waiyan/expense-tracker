<template>
  <MyHeader />
  <div class="container">
    <MyBalance />
    <IncomeExpense />
    <TranscationList />
    <AddTransaction />
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue';
import MyBalance from '@/components/MyBalance.vue';
import IncomeExpense from '@/components/IncomeExpense.vue';
import TranscationList from '@/components/TranscationList.vue';
import AddTransaction from './components/AddTransaction.vue';

export default {
  components: {
    MyHeader,
    MyBalance,
    IncomeExpense,
    TranscationList,
    AddTransaction,
  },
};
</script>

<style lang="scss">

</style>
