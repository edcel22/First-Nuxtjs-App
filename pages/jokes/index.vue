<template>
	<div>
		<h1>Jokes</h1>
		<!-- Loop and output the jokes -->
		<Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
	</div>
</template>
<script>
	import axios from "axios";
	import Joke from "../../components/Joke";

	export default {
		components: {
			Joke
		},
		head() {
			return {
				title: 'Jokes',
				meta: [
                   {
                   	hid: "description",
                   	name: "description",
                   	content: "best place"
                   }         
				]
			}
		},
		data() {
			return {
				jokes: [
                   
				]
			}
		},
		async created() {
			const config = {
				headers: {
					'Accept': 'application/json'
				}
			}
			try {
               /*make a request to the api*/
			   const res = await axios.get('https://icanhazdadjoke.com/search', config);

			   /*console.log(res.data);*/
			   this.jokes = res.data.results;
			} catch(err) {
               console.log('err');
			}
		}
	}
</script>