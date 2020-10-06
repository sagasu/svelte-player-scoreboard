<script>
	import Navbar from './Navbar.svelte';
	import Player from './Player.svelte';

	let players = [{
		name: "Matt",
		points: 3
	},
	{	name: "Aneta 'The Unicorn Queen'",
		points:12}
		,
	{
		name: "Noti",
		points: 5
	}];
</script>

<main>
	<Navbar></Navbar>
	<div class="container">
		{#if players.length === 0}
			<p>No Players</p>
		{:else}
			{#each players as player}
			<Player name={player.name} points={player.points}/>
			{/each}
		{/if}
	</div>
</main>

