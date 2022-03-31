<template>
    <button @click="onClick()" :style="{background: color}">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        onClick() {
            this.$emit('toggle-add-task')
        }
    },
}
</script>

<style scoped>
    button {
        border-radius: 10px;
        padding: 10px 20px;
        color: #fff;
        border: none;
        cursor: pointer;
    }
</style>