<script>
	import '../app.css';
	import Navbar from '../components/navbar.svelte';
</script>

<div class="flex flex-col h-screen">
	<Navbar />
	<div class="flex flex-grow">
		<slot />
	</div>
</div>
