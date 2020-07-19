<script>
	import MyButton from './Button.svelte';
	let name = 'avi';
	let count = 0;
	export const increment = () => {
		count = count + 1;
	}
	const handleInutChange = (e) => {
		name = e.target.value;
	}
</script>

<h1>Hello {name}!</h1>
<button on:click={increment}>
	Counter: {count}
</button>

<!-- No Need to terminate tag -->
<input type='text' value={name} on:input={handleInutChange}>

<!-- Alternative way in svelte -->
<input type='text' bind:value={name}>

<!--Component Button, no need write count={count}-->
<MyButton {count} {increment}/>

<style>
	h1 {
	color: blue;
	font-style: italic;	
	}
	
	button {
		background: yellow;
		border: 2px solid blue;
	}
</style>