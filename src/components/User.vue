<template>
<button type="button" @click="onClickAgeUp">Update Age Up</button>
<!-- <button type="button" @click="onClickAgeDown">Update Age Down</button> -->
<p>The user is {{ age }} years old</p>
</template>

<script>
export default {
    name: "User",
    props: ["age"],
    emits:['age-change'],
    methods: {
        onClickAgeUp() {
         this.$emit('age-change-up', 3)
        }
        // onClickAgeDown() {
        //     this.$emit('age-change-down')
        // },
    }
}

</script>

<style lang="scss" scoped>

</style>
