<template>
    <section v-show="completedAssigments.length">
        <!-- <h2>Assignment undone({{ assignments.filter(a=>!a.completed).length}}) </h2> -->
        <h2>Assignment undone({{ completedAssigments.length }}) </h2>
        <ul>
            <!-- <li v-for="ret in assignments.filter(a=>!a.completed)" :key="ret.id">{{ ret.name }} -->
            <li v-for="ret in completedAssigments" :key="ret.id">{{ ret.name }}

                <input type="checkbox" v-model="ret.completed">
            </li>
        </ul>
    </section>
    <br>
    <section v-if="unCompletedAssigments.length > 0">
        <h2>Assignment done({{ unCompletedAssigments.length }})</h2>
        <ul>
            <li v-for="ret in unCompletedAssigments" :key="ret.id">{{ ret.name }}
                <input type="checkbox" v-model="ret.completed">
            </li>
        </ul>
    </section>
</template>
  
<script >
export default {
    data() {
        return {
            assignments: [
                { id: 1, name: 'Chan', completed: false },
                { id: 2, name: 'Panha', completed: false },
                { id: 3, name: 'Pich', completed: false },
                { id: 4, name: 'Tye', completed: false },
            ]
        }
    },
    computed: {
        completedAssigments() {
            return this.assignments.filter(a => a.completed)
        },
        unCompletedAssigments() {
            return this.assignments.filter(a => !a.completed)
        }
    }
}
</script>