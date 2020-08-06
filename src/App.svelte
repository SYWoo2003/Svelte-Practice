<script>
  let count = 0;
  let check = 0;
  let checktext = "on";

  const Clickevent = () => {
    count++;
  };

  const Checkchange = () => {
    if (check == 1) {
      check = 0;
      checktext = "on";
    } else {
      check = 1;
      checktext = "off";
    }
  };

  const Longincrease = () => {
    count += 30;
  };

  const Reset = () => {
    count = 0;
  };
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
</style>

<main>
  <p>{checktext}</p>
  <p>{count}</p>
  <button on:click={Clickevent}>click me</button>
  <button on:click={Checkchange}>checkchange</button>
  <button on:click={Longincrease}>+30</button>
  <button on:click={Reset}>reset</button>
</main>
