<script>
  let tasks = [];
  let input = '';

  function add() {
    if (!input.trim()) return;
    tasks = [...tasks, input];
    input = '';
  }

  function remove(i) {
    tasks = tasks.filter((_, index) => index !== i);
  }
</script>

<h1>To-Do List</h1>

<input bind:value={input} placeholder="Enter task..." />
<button on:click={add}>Add</button>

{#each tasks as task, i}
  <p>{task} <button on:click={() => remove(i)}>Delete</button></p>
{/each}

{#if tasks.length === 0}
  <p>No tasks yet!</p>
{/if}

<style>
  input { padding: 6px; margin-right: 6px; }
  button { padding: 6px 12px; background: #FF3E00; color: white; border: none; cursor: pointer; }
</style>
