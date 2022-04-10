<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @toggle-add-task="$emit('btn-click')" :text="showAddTask ? 'close' : 'Add Task'" color="green" />
    </header>
</template>

<script>
import Button from './Button'

export default  {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean
    },
components: {
    Button,
},
}
</script>

<style scoped>
    header  {
        display: flex;
        justify-content: space-between;
        align-content: center;
        margin-bottom: 20px;
    }
</style>