<script lang="ts">
	export let screens: any[] = [];
	export let startScreen = 0;
	export let currentScreen = startScreen;
</script>

<!-- markup (zero or more items) goes here -->
<svelte:component this={screens[currentScreen]} />

<style>
	/* your styles go here */
</style>
