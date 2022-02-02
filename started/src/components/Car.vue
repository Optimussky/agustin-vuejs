<template>
  <h2>Coche</h2>

  <p>Marca: {{ brand }}</p>
  <p>Model: {{ model }}</p>
  <p>
    Color:
    <!--{{ colors[2] }}-->
    <span v-for="color in colors" :key="color">
      {{ color }}
    </span>
  </p>
  <p>Price: ${{ price }}</p>
  <p>Power: {{ power }}</p>
  {{ messaging.title }} - {{ messaging.text }}
</template>

<script>
export default {
  /*
data() {
    return {
      brand: "Audi",
      model: "A4",
      color: ["Gray", "Red", "Blue"],
      price: 38000,
      power: 180,
      messaging: {
        title: "Hola mundo",
        text: "Adiós",
      },
    };
  },
  */

  // Composition API
  setup() {
    const brand = "Audi";
    const model = "A4";
    const colors = ["Gray", "Red", "Blue"];
    const price = 45000;
    const power = 240;
    const messaging = {
      title: "Estoy bien",
      text: "Welcome",
    };
    return {
      brand,
      model,
      colors,
      price,
      power,
      messaging,
    };
  },
};
</script>

<style></style>
