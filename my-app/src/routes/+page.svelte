<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<script>
	let hereKitty = false;

  // Mouse entra
	const handleMouseenter = () => hereKitty = true;
  // Mouse sai
	const handleMouseleave = () => hereKitty = false;
</script>

<svelte:body
	on:mouseenter={handleMouseenter}
	on:mouseleave={handleMouseleave}
/>

<!-- creative commons BY-NC http://www.pngall.com/kitten-png/download/7247 -->
<!-- !hereKitty nega a função, sendo assim, o que era True vira False e o que era False vira True -->
<img
	class:curious={!hereKitty}
	alt="Kitten wants to know what's going on"
	src="https://www.greenmangaming.com/blog/wp-content/uploads/2022/06/teenage-mutant-ninja-turtles-characters-ranked-890x606.jpg"
>

<style>
	img {
		position: absolute;
		left: 0;
		bottom: -60px;
		transform: translate(-80%, 0) rotate(-30deg);
		transform-origin: 100% 100%;
		transition: transform 0.4s;
	}

	.curious {
		transform: translate(-15%, 0) rotate(30deg);
	}

	:global(body) {
		overflow: hidden;
	}
</style>
