<template>
    <div class="results">
        <p class="rank">{{ rank }}</p>
        <p>Reaction time: {{ score }} ms</p>
    </div>
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
        if (this.score < 250) {
            this.rank = 'Ninja Fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflexes'
        } else {
            this.rank = 'Snail pace...'
        }
    },
}
</script>

<style lang="scss" scoped>
.results {
    margin: 60px auto;
    padding: 60px;
    color: #0faf87;
    border: 2px solid #0faf87;
    border-radius: 20px;
    width: 400px;
}
.rank {
    font-size: 1.4em;
    font-weight: bold;
}
</style>
