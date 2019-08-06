<script>
	let items = [
		{ id: 1, name: "Milk", done: false },
		{ id: 2, name: "Bread", done: true },
		{ id: 3, name: "Eggs", done: false },
	]
</script>

<div>
	<h1>Things to buy</h1>

	<ul>
	 {#each items as item}
	 	<li>{item.name}</li>
	 {/each}
	</ul>
</div>
