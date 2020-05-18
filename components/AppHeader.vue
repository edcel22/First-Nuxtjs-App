<template>
	<div>
		<header id="header" class="">
			<h1>Dad Jokes</h1>
			<ul>
				<li><nuxt-link to="/">Home</nuxt-link></li>
				<li><nuxt-link to="/jokes">Jokes</nuxt-link></li>
				<li><nuxt-link to="/about">About</nuxt-link></li>
			</ul>	
		</header><!-- /header -->
	</div>
</template>
<script>
	export default {
		name: 'AppHeader'
	}
</script>
<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 10px;
		border-bottom: 1px solid black;
	}
	header h1 {
		margin: 0;
	}
	header ul {
		display: flex;
		margin: 0;
	}
	header li {
		list-style-type: none;
		padding: 5px 10px;
	}
	header li a {
		text-decoration: none;
		margin: 0;
	}
	
</style>