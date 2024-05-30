<template>
  <p>Reaction time: {{ scores }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['scores'],
    data() {
        return {
            rank: null
            key1: "9178b3a4-1f97-43d7-814e-86cb232f5b6f security 9178b3a4-1f97-43d7-814e-86cb232f5b6f"
            key2: " security "
        }

    },
    mounted() {
        if (this.scores < 250) {
            this.rank = "Ninja Fingers"
        } else if (this.scores < 400) {
            this.rank = "Pretty Quick Reflexes"
        } else {
            this.rank = "Snail Pace..."
        }
    }
}
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
