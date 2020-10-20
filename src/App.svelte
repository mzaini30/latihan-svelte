<h3 class="tengah">List teman</h3>
<hr>
<p>Ini adalah list teman-temanku...</p>
<ul>
	{#each list as x}
		<li>{x}</li>
	{/each}
</ul>
<form on:submit|preventDefault={tambahkan}>
	<input required type="" placeholder="Tambahkan teman" bind:value={baru} name="">
</form>
<style type="text/css">
	.tengah {
		text-align: center;
	}
</style>
<script type="text/javascript">
	let list = []
	let baru = ''
	const tambahkan = () => {
		list = [baru, ...list]
		baru = ''
	}
</script>