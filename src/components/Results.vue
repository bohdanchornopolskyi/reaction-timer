<template>
    <h2>Your result is {{ score }} ms</h2>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        };
    },
    mounted() {
        if (this.score < 250) {
            this.rank = "Gosh you're fast!!!";
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes';
        } else {
            this.rank = 'Snail pace...';
        }
    },
};
</script>

<style>
.rank {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>
