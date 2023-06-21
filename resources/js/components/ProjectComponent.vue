<template>
    <div>
        <h2>Project Management</h2>
        <!-- Create Form -->
        <form @submit.prevent="addProject">
            <input type="text" v-model="newProject" placeholder="Add new project" />
            <button type="submit">Add</button>
        </form>

        <!-- Project List -->
        <div v-for="project in projects" :key="project.id">
            {{ project.name }}
        </div>

        <!-- TODO: Add edit and delete functionality -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            newProject: "",
            projects: [], // this will be loaded from backend
        };
    },
    methods: {
        addProject() {
            // TODO: Implement this method to add new project to the list (POST request to the backend)
        },
    },
};
</script>
