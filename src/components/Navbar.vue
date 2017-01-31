<template>
  <nav class="nav has-shadow">
    <div class="nav-left">
      <router-link to="/" class="nav-item is-brand">
        Vue Project
      </router-link>
      <router-link to="/dashboard" class="nav-item">
        <i class="fa fa-dashboard"></i> Dashboard
      </router-link>
      <router-link to="/projects" class="nav-item">
        <i class="fa fa-list-alt"></i> Project List
      </router-link>
    </div>
    <div class="nav-right">
      <span class="nav-item">
        <a class="button">Logout</a>
      </span>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'navbar'
  }
</script>
