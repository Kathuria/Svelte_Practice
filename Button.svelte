<script>
	import MyApp from './App.svelte';
	export let count = 10;
	export let increment = () => {}
</script>


<button on:click={increment}>
	Double Counter: {count*2}
</button>