<template>
    <div>
        <h2>Task Management</h2>
        <!-- Create Form -->
        <form @submit.prevent="addTask">
            <input type="text" v-model="newTask" placeholder="Add new task" />
            <button type="submit">Add</button>
        </form>

        <!-- Draggable List -->
        <draggable v-model="tasks" @end="updatePriority">
            <div v-for="task in tasks" :key="task.id">{{ task.name }} - {{ task.priority }}</div>
        </draggable>

        <!-- TODO: Add edit and delete functionality -->
    </div>
</template>

<script>
import draggable from "vuedraggable";

export default {
    components: {
        draggable,
    },
    data() {
        return {
            newTask: "",
            tasks: [], // this will be loaded from backend
        };
    },
    methods: {
        addTask() {
            // TODO: Implement this method to add new task to the list (POST request to the backend)
        },
        updatePriority(event) {
            // TODO: Implement this method to update task priority based on the new order (PATCH request to the backend)
        },
    },
};
</script>
