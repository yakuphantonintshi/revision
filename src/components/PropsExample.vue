<template>
  <div>

    <p>
        <span v-if="numb1>0">Numb1: {{ numb1 }}</span>
        <span v-else>Enter numb1 value</span>
    </p>

    <p>
        <span v-if="numb2 > 0">Numb2: {{ numb2 }}</span>
        <span v-else>Enter a valid numb2 value</span>
    </p>
    <p>Sum: {{ addition }} </p>
  </div>
</template>

<script>
export default {
    props: ["numb1", "numb2"],
    computed:{
        addition(){
            return +this.numb1 + +this.numb2
        }
    }

}
</script>

<style scoped>

</style>