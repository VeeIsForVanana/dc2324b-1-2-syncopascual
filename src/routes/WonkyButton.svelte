<script>
	export let value = 0;

	function increment() {
		value += Math.floor(Math.random() * 9);
	}
</script>

{#if value % 15 == 0}
	<button on:click={increment}>
		FizzBuzz {value}
	</button>
{:else if value % 3 == 0}
	<button on:click={increment}>
		Fizz {value}
	</button>
{:else if value % 5 == 0}
	<button on:click={increment}>
		Buzz {value}
	</button>
{:else}
	<button on:click={increment}>
		{value}
	</button>
{/if}
