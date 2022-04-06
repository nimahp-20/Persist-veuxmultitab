<template>
  <div>
    <h6>These will be updated in every window or tab</h6>
    <div>
      <p>🍊: {{ $store.state.fruits.oranges }}</p>
      <button @click="$store.dispatch('fruits/commitAddOrange')">
        Add orange
      </button>
    </div>
    <div>
      <p>🐧: {{ $store.state.animals.penguins }}</p>
      <button @click="$store.dispatch('animals/commitAddPenguin')">
        Add penguin
      </button>
    </div>

    <h6>These won't be updated in every tab or window</h6>
    <!-- Apples -->
    <div>
      <p>🍎: {{ $store.state.fruits.apples }}</p>
      <button @click="$store.dispatch('fruits/commitAddApple')">
        Add apple
      </button>
    </div>
    <div>
      <p>🐺: {{ $store.state.animals.wolfs }}</p>
      <button @click="$store.dispatch('animals/commitAddWolf')">
        Add wolf
      </button>
    </div>
  </div>
</template>

<script>
import { useStore } from "vuex";
export default {
  name: "App",
  setup() {
    const $store = useStore();
  },
};
</script>
