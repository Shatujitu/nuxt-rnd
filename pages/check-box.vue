<template>
  <div class="container">
    <h1>Check Box</h1>
    <div class="form-check" v-for="item of allItems" :key="item.id">
      <input class="form-check-input" type="checkbox" :value="item.id" id="flexCheckDefault" v-model="arrayItemChecked">
      <label class="form-check-label" for="flexCheckDefault">
        {{ item.name }}
      </label>
    </div>
    <h1>Select</h1>
    <select class="form-select" v-model="selectedId">
      <option v-for="(item, i) of allItems" :value="item.id">{{ item.name}}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'checkBox',
  data() {
    return {
      allItems: [
        { name: 'Item 1', id: 1 },
        { name: 'Item 2', id: 2 },
        { name: 'Item 3', id: 3 },
        { name: 'Item 4', id: 4 },
        { name: 'Item 5', id: 5 },
      ],
      oneItemChecked: 2,
      arrayItemChecked: [2,3,5],
      selectedId: 3
    }
  }
}
</script>

<style scoped>

</style>
