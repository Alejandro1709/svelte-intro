<script>
	let todos = [
		{
			id: 1,
			title: 'Finish Physics Test',
			completed: false
		},
		{
			id: 2,
			title: 'Upload video to youtube',
			completed: false
		}
	];
</script>

<main>
	<ul>
		{#each todos as todo}
			<li>
				<h3>{todo.title}</h3>
				<button>{todo.completed ? 'Uncomplete' : 'Complete'}</button>
			</li>
		{/each}
	</ul>
	<form>
		<input type="text" placeholder="Add a new task" />
		<button type="submit">Add</button>
	</form>
</main>

<style>
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	ul {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	li {
		display: flex;
		justify-content: space-between;
		gap: 1rem;
		align-items: center;
		width: 100%;
		max-width: 500px;
		padding: 1rem;
		border: 1px solid #ccc;
		background-color: white;
		border-radius: 0.5rem;
		margin-bottom: 1rem;
	}

	button {
		padding: 0.5rem 1rem;
		border: none;
		border-radius: 0.5rem;
		background-color: #ccc;
		color: #fff;
		font-weight: bold;
		cursor: pointer;
	}

	button:hover {
		background-color: #aaa;
	}

	input {
		padding: 0.5rem 1rem;
		border: none;
		border-radius: 0.5rem;
		background-color: #e6e6e6;
		color: black;
		font-weight: bold;
		cursor: pointer;
	}
</style>
