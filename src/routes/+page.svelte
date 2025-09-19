<!--<h1>Welcome to SvelteKit</h1>-->
<!--<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>-->

<h1>Sample transaction booking form</h1>

<br>
<form on:submit|preventDefault={handleSubmit}>
	<label>
		Account ID:
		<input type="number" bind:value={accountId} />
	</label>
	<br />

	<label>
		Amount:
		<input type="number" step="0.01" bind:value={amount} />
	</label>
	<br />

	<label>
		Date:
		<input type="date" bind:value={bookedAt} />
	</label>
	<br />

	<label>
		Description:
		<input type="text" bind:value={description} />
	</label>
	<br />

	<button type="submit">Save Transaction</button>
</form>


<!--Functions for home page-->

<script lang="">
	// Local state for the form fields
	// import { text } from '@sveltejs/kit';

	let accountId = 0;
	let amount= 0;
	let bookedAt = "";
	let description = "";

	function handleSubmit() {
		// For now, just log it to the console
		console.log({
			accountId,
			amount,
			bookedAt,
			description
		});
	}
</script>