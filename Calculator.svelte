script>
  let a = 0;
  let b = 0;
  let result = '';

  function add()      { result = a + b; }
  function subtract() { result = a - b; }
	function multiple() {result = a * b;}
  function divide()   { result = b == 0 ? 'Cannot divide by zero' : a / b; }
</script>

<h1>Calculator</h1>

<input type="number" bind:value={a} placeholder="First number" />
<input type="number" bind:value={b} placeholder="Second number" />

<br/>
<button on:click={add}>Add</button>
<button on:click={subtract}>Subtract</button>
<button on:click={divide}>Divide</button>
<button on:click={multiple}>Multiple</button>

<h2>Result: {result}</h2>

<style>
  input  { padding: 6px; margin: 6px; }
  button { padding: 8px 14px; margin: 4px; background: #FF3E00; color: white; border: none; cursor: pointer; }
</style>
