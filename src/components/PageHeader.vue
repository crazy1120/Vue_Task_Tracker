<template>
    <header>
        <h1> {{ title }} </h1>
        <ToggleButton 
        @btn-click="$emit('toggle-add-task')" 
        :text="showAddTask ? 'close' : 'Add Task'" 
        :color="showAddTask ? 'red' : 'green'"/>
    </header>
</template>

<script>
import ToggleButton from './ToggleButton.vue';

export default {
    name: 'PageHeader',
    props: {
        title:  String,
        showAddTask: Boolean
        },
    components : {
        ToggleButton
    }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>