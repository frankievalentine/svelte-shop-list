<script>
	let items = [
		{ id: 1, name: "Milk", done: false },
		{ id: 2, name: "Bread", done: true },
		{ id: 3, name: "Eggs", done: false },
	]

	const remove = item => {
		items = items.filter(i => i !== item)
	}
</script>

<style>
 li button {
	 border: none;
	 background: transparent;
	 padding: 0;
	 margin: 0;
 }

 .done span {
	 opacity: 0.4;
 }
</style>

<div>
	<h1>Things to buy</h1>

	<ul>
	 {#each items as item}
	 	<li class:done={item.done}>
		 <span>{item.name}</span>
		 <button on:click={() => remove(item)}>❌</button>
		</li>
	 {/each}
	</ul>
</div>
