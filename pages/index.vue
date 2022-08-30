<template>
  <span class="flex w-screen h-screen">
    <link href="https://fonts.googleapis.com/css2?family=Material+Icons" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css" rel="stylesheet">
    <Sidebar />
    <Dashboard />
  </span>
</template>

<script lang="ts">
import Vue from 'vue'
import Dashboard from '~/components/Dashboard.vue'

export default Vue.extend({
    name: "IndexPage",
    components: { Dashboard }
})
</script>
