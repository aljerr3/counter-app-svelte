<script lang="ts">
  let counter: number = 0;

  const modifyCounter = (value: number): number => (counter += value);

  const reset = (): number => (counter = 0);

  //   const add = (): void => {
  //     counter++;
  //   };

  //   const diminish = (): void => {
  //     counter--;
  //   };

  //   const reset = (): void => {
  //     counter = 0;
  //   };
</script>

<main>
  <h1>Calculadora de Boletas</h1>
  <h3>Calcula el valor por el que debes hacer tu boleta de honorarios</h3>
  <hr />
  <h2 class={counter < 0 ? "negative" : "positive"}>Counter: {counter}</h2>
  <button class="add" on:click={() => modifyCounter(1)}>+1</button>
  <button class="diminish" on:click={() => modifyCounter(-1)}>-1</button>
  <button class="reset" on:click={reset}>Reset</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  h2 {
    font-size: 2rem;
  }

  button {
    font-size: 2rem;
    margin: 0 0.4rem;
    border-radius: 5px;
  }

  button:hover {
    cursor: pointer;
  }

  .add {
    background-color: #26d231;
    color: aliceblue;
  }

  .add:active {
    background-color: #118319;
  }

  .diminish {
    background-color: #3a9aea;
    color: aliceblue;
  }

  .reset {
    background-color: #b912c9;
    color: aliceblue;
  }

  .positive {
    color: #118319;
  }

  .negative {
    color: #963514;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
