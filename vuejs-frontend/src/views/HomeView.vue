<template>
  <div class="home">
    <NavBar></NavBar>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import NavBar from '@/components/NavBar.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    NavBar
  },

  mounted() {
    const token = localStorage.getItem('access_token');
		if (!token) {
			this.$router.push("/login");
		}
	}
  
}
</script>
