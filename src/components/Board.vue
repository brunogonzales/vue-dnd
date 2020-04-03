<template>
  <div :id="id" class="board" @dragover.prevent @drop.prevent="drop">
    <slot />
  </div>
</template>

<script>
export default {
  name: "Board",
  props: ["id"],
  methods: {
    drop(e) {
      const cardId = e.dataTransfer.getData("cardId");
      const card = document.getElementById(cardId);
      card.style.display = "block";
      e.target.appendChild(card);
    },
  },
};
</script>
<style lang="scss">
.board {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 300px;
  background-color: #313131;
  padding: 15px;
}
</style>
