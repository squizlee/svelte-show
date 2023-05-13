<script lang="ts">
	import { onMount } from 'svelte';

	import Home from '../mock_screens/Home.svelte';
	import Account from '../mock_screens/Account.svelte';
	import Show from '$lib/Show.svelte';

	const screens: any[] = [Home, Account];
	let ShowRef: any;

	onMount(() => {
		console.log(ShowRef);
	});
</script>

<!-- markup (zero or more items) goes here -->
<h1>Svelte Show</h1>
<p>
	This is a component that makes it easier for you to navigate between different 'screens' or
	components like a state machine. For example we have the following flow
</p>

<img width="400" height="400" src="/structure.png" alt="" />

<section class="show-container">
	<Show bind:this={ShowRef} {screens} startScreen={0} />
</section>

<style>
	.show-container {
		border: 1px solid gray;
		height: 50vh;
	}

	img {
		display: block;
		margin: 0 auto;
	}
</style>
