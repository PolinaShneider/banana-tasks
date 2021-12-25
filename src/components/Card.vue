<template>
<div class="card" :class="isActive ? 'card-active' : ''">
  <h2>{{title}}</h2>
  <p>{{description}}</p>
  <span>{{cost}}</span>
</div>

</template>

<script>
    export default {
        name: "Card",
        props: {
            title: String,
            description: String,
            cost: String,
            isActive: Boolean
        }
    }
</script>

<style scoped>
  .card {
    text-align: initial;
    border-radius: 8px;
    border: 1px solid black;
    padding: 10px;
    background: blanchedalmond;
    box-sizing: border-box;
    margin: 10px;
    flex-basis: calc(50% - 20px);
  }

  .card h2 {
    margin: 10px 0;
  }

  .card span {
    font-style: italic;
  }

  .card.card-active {
    background: aquamarine;
  }
</style>
