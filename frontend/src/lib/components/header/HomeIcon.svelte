<script lang="ts">
	import { writable } from 'svelte/store';

	const homeIconHover = writable(false);
</script>

<a
	href="/#intro"
	class="relative w-8 h-8"
	on:mouseover={() => homeIconHover.set(true)}
    on:focus={() => homeIconHover.set(true)}
	on:mouseout={() => homeIconHover.set(false)}
    on:blur={() => homeIconHover.set(false)}
>
	<svg class="w-full h-full" viewBox="0 0 483.86 483.86">
		<path
			class="fill-black/60 transition-colors duration-300 dark:fill-white"
			d="M483.86,112.345h-26.699c-6.952,0-25.143,7.552-25.143,13.981v233.467c0,6.445,18.191,11.729,25.143,11.729h26.699v51.835   H311.052v-51.835h34.57V129.615h-6.016L256.42,423.356h-64.406l-82.11-293.741h-6.219v241.906h34.555v51.835H0v-51.835h19.173   c7.527,0,15.383-5.283,15.383-11.729V126.326c0-6.43-7.855-13.981-15.383-13.981H0V60.504h179.155l58.496,207.342h1.574   l59.073-207.342H483.86V112.345z"
		/>
		<path
			class={$homeIconHover ? 'hover show' : 'hover'}
			d="M483.86,112.345h-26.699c-6.952,0-25.143,7.552-25.143,13.981v233.467c0,6.445,18.191,11.729,25.143,11.729h26.699v51.835   H311.052v-51.835h34.57V129.615h-6.016L256.42,423.356h-64.406l-82.11-293.741h-6.219v241.906h34.555v51.835H0v-51.835h19.173   c7.527,0,15.383-5.283,15.383-11.729V126.326c0-6.43-7.855-13.981-15.383-13.981H0V60.504h179.155l58.496,207.342h1.574   l59.073-207.342H483.86V112.345z"
		/>
	</svg>
</a>

<style lang="postcss">
	.hover {
		fill: rgb(76, 204, 204);
		clip-path: polygon(0 100%, 100% 100%, 100% 100%, 0% 100%);
		transition: clip-path 0.3s ease-in-out;
	}

	.hover.show {
		clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%);
	}
</style>
