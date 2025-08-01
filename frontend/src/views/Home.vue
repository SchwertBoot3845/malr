<template>
  <div class="home">
    <h1>Welcome to MALR 👾</h1>
    <p>Your Geometry Dash community rating hub.</p>

    <section>
      <h2>Featured Levels</h2>
      <!-- For now, static example cards -->
      <div class="level-list">
        <div class="level-card" v-for="level in featuredLevels" :key="level.id">
          <h3>{{ level.name }}</h3>
          <p>Creator: {{ level.creator }}</p>
          <p>Average Rating: {{ level.avgRating }}/20</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// static sample data for now
const featuredLevels = ref([
  { id: 1, name: 'Super Crazy Level', creator: 'Theodor', avgRating: 18 },
  { id: 2, name: 'Insane Demon Rush', creator: 'ArcLia', avgRating: 19.5 }
])
</script>

<style scoped>
.home {
  max-width: 800px;
  margin: auto;
  padding: 1rem;
  text-align: center;
}

.level-list {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.level-card {
  border: 2px solid #0dff9a;
  border-radius: 8px;
  padding: 1rem;
  width: 200px;
}
</style>