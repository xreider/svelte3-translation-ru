<script>
	import Thing from './Thing.svelte';

	let things = [
		{ id: 1, color: 'darkblue' },
		{ id: 2, color: 'indigo' },
		{ id: 3, color: 'deeppink' },
		{ id: 4, color: 'salmon' },
		{ id: 5, color: 'gold' }
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<button on:click={handleClick}>
	Удалить первый элемент
</button>

{#each things as thing}
	<Thing current={thing.color}/>
{/each}