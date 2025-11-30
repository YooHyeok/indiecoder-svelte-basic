<script>
  let count = 0;
  function handleClick() {
    count += 1;
  }
</script>

<div>
  <div><h1>Part01_Ex01</h1></div>
  <button on:click={handleClick}>
    클릭수 {count}
  </button>
</div>
