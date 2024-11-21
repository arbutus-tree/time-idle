<script>
  let timeAccumulated = 0;
  let money = 1;
  let haveAccumulator = false;

  let buyAccumulator = () => {
    haveAccumulator = true;
    money -= 1;
  }

  let accumulateTime = () => {
    if (haveAccumulator) timeAccumulated += 1;
  }

  setInterval(accumulateTime, 1000);

</script>

<h1>time idle</h1>
<h2>time is precious :)</h2>

<p>money: ${money}</p>

<button 
  on:click={buyAccumulator}
  disabled={money < 1}
  >$1 buy time accumulator</button>

<p>time accumulated: {timeAccumulated}</p>
