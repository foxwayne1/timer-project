<template>
  <p>Reaction Time = {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank: null,
    }
  },
  mounted() {
    if (this.score < 300) {
      this.rank = 'Holy cow, that was impressive'
    } else if (this.score < 450) {
      this.rank = 'that was okay i suppose'
    } else {
      this.rank = 'Pretty pitiful'
    }
  },
}
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
