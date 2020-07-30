<template>
    <div>
        <h1>Calculator</h1>
        <Calculator />
    </div>
</template>

<script>
    import Calculator from './main/Calculator'
    export default {
        components: { Calculator }
    }
</script>

<style>
    body {
        margin: 0;
    }

    #app {
        display: flex;
        flex-direction: column;
        height: 100vh;
        justify-content: center;
        align-items: center;
        text-align: center;

        color: #FFF;
    }
</style>