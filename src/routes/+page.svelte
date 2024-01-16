<script>
	// import '../../app.pcss';
	import { onMount } from 'svelte';
	import pkg from '@googlemaps/js-api-loader';
	const { Loader } = pkg;

	// const PUBLIC_GOOGLEMAPS_API_KEY  = " - hidden -"

	// Bindings
	let mapElement;

	onMount(async function () {
		const loader = new Loader({
			apiKey: PUBLIC_GOOGLEMAPS_API_KEY,
			version: 'weekly'
		});

		const { Map } = await loader.importLibrary('maps');

		let map = new Map(mapElement, {
			center: { lat: -34.397, lng: 150.644 },
			zoom: 8
		});
        return 
	});
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<div bind:this={mapElement} style:height={'100%'} style:width={'100%'} />