<template>
     <div :key = "task.id" v-for = "task in tasks" >
    <OnlyTask @toggle-reminder="$emit('toggle-reminder',task.id)"
    @delete-task="$emit('delete-task', task.id)" 
    :task="task" />

    </div>
</template>

<script>
import OnlyTask from "./OnlyTask.vue"

export default {
    name : "AddTasks",
    props :{
        tasks: {
            type: Array,
            default: () =>[]
        }
    },
    components: {
        OnlyTask
    },
    emits: ['delete-task', 'toggle-reminder']
}
</script>