<script>
	let name = "Rasyid";
	let beltColour = 'black';

	const handleClick = () => {
		beltColour = beltColour === 'black' ? 'white' : 'black';
	};

	const handleInput = (e) => {
		beltColour = e.target.value
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p style="color: {beltColour}" >{beltColour} belt</p>
	<button on:click={handleClick}>update belt colour</button>
	<!--<input type="text" on:input={handleInput} value={beltColour}>-->
	<!--this is same away like above-->
	<input type="text" bind:value={beltColour}> 
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>