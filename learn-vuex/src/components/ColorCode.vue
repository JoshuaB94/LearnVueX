<template>
  <div>
    <input placeholder="Enter Color Code" type="text" v-model="colorCode" />
  </div>
</template>

<script>
export default {
  name: "ColorCode",
  computed: {
    colorCode: {
      get() {
        return this.$store.state.colorCode;
      },
      set(newValue) {
        this.$store.dispatch("setColorCode", newValue);
      },
    },
  },
};
</script>
