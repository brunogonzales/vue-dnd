<template>
  <div id="app">
    <main class="container">
      <Board id="board-1">
        <Card id="card-1" draggable="true"><p>Card one</p></Card>
      </Board>

      <Board id="board-2">
        <Card id="card-2" draggable="true"><p>Card two</p></Card>
      </Board>
    </main>
  </div>
</template>

<script>
import Board from "@/components/Board";
import Card from "@/components/Card";

export default {
  name: "App",
  components: { Board, Card },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 768px;
  height: 100vh;
  overflow: hidden;
  margin: 0 auto;
  padding: 15px;
}
</style>
