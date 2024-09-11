<div align="center">
	<a target="_blank" href="https://gitforcetalent.com">
        <picture>
            <source media="(prefers-color-scheme: dark)" srcset="https://gitforcetalent.com/_next/image?url=%2Fimages%2Flogo-light.png&w=1920&q=75">
            <source media="(prefers-color-scheme: light)" srcset="https://gitforcetalent.com/_next/image?url=%2Fimages%2Flogo.png&w=1920&q=75">
            <img alt="https://gitforcetalent.com" src="https://gitforcetalent.com/_next/image?url=%2Fimages%2Flogo.png">
        </picture>
	</a>
    <br />
    <br />
</div>

---

---

# Task: Dynamic Mood Board Creator

Create a Vue.js component that allows users to generate and manipulate a dynamic mood board with color swatches. The component should have the following features:

1. Add random color swatches to the board.
2. Remove color swatches by clicking on them.
3. Shuffle the existing color swatches.
4. Display the hex code of each color swatch.

Requirements:

1. Implement the `generateRandomColor` method to create random, visually appealing colors.
2. Complete the `addColor` method to add new colors to the `colors` array.
3. Implement the `removeColor` method to remove a color when clicked.
4. Create the `shuffleColors` method to randomly reorder the colors in the array.


```javascript
// MoodBoard.vue
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
  name: 'MoodBoard',
  data() {
    return {
      title: 'My Dynamic Mood Board',
      colors: [],
    }
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
}
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

```

