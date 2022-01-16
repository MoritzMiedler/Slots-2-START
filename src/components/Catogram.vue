<template>
  <div>
    <h3 class="fw-bold mb-5">Charlie Inc. feat. Miedler</h3>
    <h3 class="fw-bold">Boss</h3>
    <slot name="boss" :item="boss"> </slot>
    <div class="mt-5">
      <h3 class="fw-bold">Employees</h3>
      <div class="d-flex flex-row">
        <slot name="employees" v-for="emp of employees" :item="emp"> </slot>
      </div>
    </div>
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
