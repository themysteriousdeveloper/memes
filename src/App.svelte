<script>
	// Materialize
	import '../node_modules/materialize-css/dist/css/materialize.min.css';
	import '../node_modules/materialize-css/dist/js/materialize.min.js';

	// Router from "svelte routing"
	import { Router, Route } from "svelte-routing";

	// Navbar import
	import Navbar from './layouts/navbar.svelte';
	import Footer from './layouts/footer.svelte';
	import Socials from './layouts/socials.svelte';

	// Pages import
	import Home from './pages/Home.svelte';
	import Meme from './pages/Memes.svelte';

</script>

<style>
body {
	display: flex;
	min-height: 100vh;
	flex-direction: column;
}

main {
	flex: 1 0 auto;
}

</style>

<Router>
	<Navbar />
	<Socials />
	<div class="container">
		<Route path="/" component={Home} />
		<Route path="/memes" component={Meme} />
	</div>
	<Footer />
</Router>
