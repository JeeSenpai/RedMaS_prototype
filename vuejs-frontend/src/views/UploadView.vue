<template>
  <div class="about">
    <NavBar></NavBar>
    <h1>This is an about page</h1>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'

export default {
    components: { NavBar },

    mounted() {
    const token = localStorage.getItem('access_token');
		if (!token) {
			this.$router.push("/login");
		}
	}
}
</script>