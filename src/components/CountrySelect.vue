<template>
  <select
    @change="onChange"
    v-model="selected"
    class="form-select block w-full border p-3 rounded mt-10"
  >
    <option value="0">Select Country</option>
    <option
      v-for="country in countries"
      v-bind:key="country.ID"
      :value="country.ID"
    >
      {{ country.Country }}
    </option>
  </select>
</template>

<script>
export default {
  name: "CountrySelect",
  props: ["countries"],
  data() {
    console.log(this.Country);
    return {
      selected: 0,
    };
  },
};
</script>
