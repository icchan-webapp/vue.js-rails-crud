<template>
  <div>
    <router-view></router-view>
  </div>
</template>

<script>
import { createRouter, createWebHashHistory } from 'vue-router'
import EmployeeIndexPage from 'EmployeeIndexPage.vue'
import EmployeeDetailPage from 'EmployeeDetailPage.vue'
import EmployeeNewPage from 'EmployeeNewPage.vue'

const router = createRouter({
  history: createWebHashHistory(),
  routes: [
    { path: '/',
      component: EmployeeIndexPage },
    { path: '/employees/:id(\\d+)',
      name: 'EmployeeDetailPage',
      component: EmployeeDetailPage },
    { path: '/employees/new',
      name: 'EmployeeNewPage',
      component: EmployeeNewPage }
  ]
})

export default router
</script>

<style scoped>
</style>