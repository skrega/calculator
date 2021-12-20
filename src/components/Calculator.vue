<template>
    <div>
        <div class="dispaly">
            <input v-model.number="operand1" type="number" class="dispaly-input mr">
            <input v-model.number="operand2" type="number" class="dispaly-input">
            = <span class="result"> {{ result }}</span>

        </div>
        <div class="keyboard">
            <button @click="addition"><i class="fas fa-plus"></i></button>
            <button @click="subtraction"><i class="fas fa-minus"></i></button>
            <button @click="divide"><i class="fas fa-divide"></i></button>
            <button @click="multiply(operand1, operand2)"><i class="fas fa-times"></i></button>
            <button @click="exponentiation"><strong>x<sup>2</sup></strong></button>
        </div>
      
       
    </div>
</template>

<script>
export default {
    name: "Calculaator",
    data(){
        return{
            operand1: 0,
            operand2: 0,
            result: 0
        }
    },
    methods: {
        addition(){
            this.result = this.operand1 + this.operand2
        },
        subtraction(){
            this.result = this.operand1 - this.operand2
        },
        divide(){
            this.result = this.operand1 / this.operand2
        },
        multiply(operand1,operand2){
            this.result = operand1 * operand2
        },
        exponentiation(){
            this.result = Math.pow(this.operand1, this.operand2)
        }
    }
}
</script>

<style scoped lang="sass">

.dispaly
    margin-bottom: 12px
    font-size: 20px
    line-height: 22px
    &-input
        height: 32px
        font-size: 20px
        line-height: 22px
        width: 100px
        &.mr 
            margin-right: 12px

.keyboard 
    display: flex
    justify-content: center
    align-items: center
    button
        display: flex
        align-items: center
        justify-content: center
        width: 40px
        height: 40px
        font-size: 20px
        line-height: 20px
        margin-right: 10px
        border: none
        background-color: #ccc
        border-radius: 9px
        cursor: pointer
        transition: all .3s
        &:active
            transform: translateY(3px)
        &:hover
            background-color: #ccc - #111
</style>