<template>
    <div class="calculator">
        <Display value="1000" />
        <Button label="AC" triple @onCalcButtonClick="clearMemory" />
        <Button label="/" operation @onCalcButtonClic="setOperation" />
        <Button label="7" @onClick="addDigit" />
        <Button label="8" @onClick="addDigit" />
        <Button label="9" @onClick="addDigit" />
        <Button label="*" operation/>
        <Button label="5" @onClick="addDigit" />
        <Button label="4" @onClick="addDigit" />
        <Button label="3" @onClick="addDigit" />
        <Button label="-" operation/>
        <Button label="1" @onClick="addDigit" />
        <Button label="2" @onClick="addDigit" />
        <Button label="3" @onClick="addDigit" />
        <Button label="+" operation/>
        <Button label="0" double @onClick="addDigit" />
        <Button label="." />
        <Button label="=" operation/>
    </div>

</template>

<script>
import Display from '../components/Display'
import Button from '../components/Button'

export default {
    components: { Button, Display },
    methods: {
        clearMemory() {
            console.log('Limpar Memoria')
        },
        setOperation(operation) {
            console.log('Operação' + operation)
        },
        addDigit(n) {
            console.log('Digito ' + n)
        }
    }
}
</script>
.calculator {

}

<style>
    .calculator {
        height: 320px;
        width: 235px;
        border-radius: 5px;

        display: grid;
        grid-template-columns: repeat(4, 25%);
        grid-template-rows: 1fr 48px 48px 48px 48px 48px;
    }
</style>