<template>
    <section>
        Filter
    </section>
    <section>
        <div class="controls">
            <button>Refresh</button>
            <button to="/register">Register as coaach</button>
        </div>
        <ul v-if="hasCoaches">
          <li v-for="coach in filteredCoaches" :key="coach.id">
            {{ coach.firstName}}
          </li>
        </ul>
        <h3 v-else>No coaches found</h3>
    </section>
</template>

<script>
export default {
    computed: {
        filteredCoaches() {
            return this.$store.getters['coaches/coaches'];
        },
        hasCoaches() {
            return this.$store.getters['coaches/coaches'];
        }
    }
}
</script>