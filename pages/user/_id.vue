<template>
  <div>/user/{{ userId }}</div>
</template>

<script>
export default {
  name: 'UserDetail',
  validate({ params }) {
    // 数値でなければならない
    return /^\d+$/.test(params.id)
  },
  computed: {
    userId() {
      return this.$route.params.id
    }
  }
}
</script>

<style scoped></style>
