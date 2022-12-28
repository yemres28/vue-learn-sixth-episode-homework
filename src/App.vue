<template>
  <div>
    <p>Seçili Component : {{ componentSelected }}</p>
    <br />
    <button
      class="btn-sm btn btn-primary"
      @click="componentSelected = 'BlueTheme'"
    >
      Blue Theme
    </button>
    <button
      class="btn-sm btn btn-primary"
      @click="componentSelected = 'RedTheme'"
    >
      Red Theme
    </button>
    <button
      class="btn-sm btn btn-primary"
      @click="componentSelected = 'GreenTheme'"
    >
      Green Theme
    </button>
    <br /><br />
    <component :is="componentSelected"></component>
  </div>
</template>
<script>
import BlueTheme from "@/views/BlueTheme.vue";
import RedTheme from "@/views/RedTheme.vue";
import GreenTheme from "@/views/GreenTheme.vue";

export default {
  components: {
    BlueTheme,
    RedTheme,
    GreenTheme,
  },
  data() {
    return {
      componentSelected: "BlueTheme",
    };
  },
};
</script>

<style scoped>
button {
  margin-left: 5px;
}
</style>
