<template>
  <div>
   <!-- Add your code here -->
  </div>
</template>

<script>
export default {
  props: {
    cats: {
      type: Array,
    },
  },
  data() {
    return {
      boss: this.cats.find((el) => el.role == 'Boss'),
      employees: this.cats.filter((el) => el.role != 'Boss'),
    };
  },
};
</script>

<style lang="scss" scoped></style>
