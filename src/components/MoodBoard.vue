<template>
    <div class="mood-board">
        <h1>{{ title }}</h1>
        <div class="controls">
            <button @click="addColor">Add Color</button>
            <button @click="shuffleColors">Shuffle</button>
        </div>
        <div class="color-grid">
            <div
                v-for="(color, index) in colors"
                :key="index"
                class="color-item"
                :style="{ backgroundColor: color }"
                @click="removeColor(index)"
            >
                {{ color }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "MoodBoard",
    data() {
        return {
            title: "My Dynamic Mood Board",
            colors: [],
        };
    },
    methods: {
        addColor() {
            // TODO: Implement color generation
        },
        removeColor(index) {
            // TODO: Implement color removal
        },
        shuffleColors() {
            // TODO: Implement color shuffling
        },
        generateRandomColor() {
            // TODO: Implement random color generation
        },
    },
};
</script>

<style scoped>
.mood-board {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

.controls {
    margin-bottom: 20px;
}

.controls button {
    margin-right: 10px;
    padding: 8px 16px;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.controls button:hover {
    background-color: #45a049;
}

.color-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
    gap: 10px;
}

.color-item {
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    cursor: pointer;
    transition: transform 0.2s ease-in-out;
}

.color-item:hover {
    transform: scale(1.05);
}
</style>
