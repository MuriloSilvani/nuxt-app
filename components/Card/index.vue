<template>
  <div class="column">
    
    <div
      v-for="row in 3"
      :key="`row-${row}`"
      :class="['row', `row-${row}`]"
    >
      <div
        v-for="card in 3"
        :key="`card-${card}`"
        :class="['card', `card-${card}`]"
      >
        <div class="title">Title {{ card }}</div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum reprehenderit, non eum voluptas corporis consequuntur aut quisquam ab velit eius exercitationem natus itaque dolorum soluta optio? Optio blanditiis expedita repellat?
      </div>
    </div>

  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.row {
  .card {
    .title {
      color: var(--primary);
      font-size: var(--font);
      font-family: Quicksand-bold, sans-serif;
    }
  }
  .card-1 {
    background: var(--background-light);
    font-family: Quicksand-light, sans-serif;
    border: 1px solid var(--border-light);
    box-shadow: 0 0 var(--shadow-size-small) var(--shadow-light);
  }
  .card-2 {
    background: var(--background);
    font-family: Quicksand, sans-serif;
    border: 1px solid var(--border);
    box-shadow: 0 0 var(--shadow-size) var(--shadow);
  }
  .card-3 {
    background: var(--background-dark);
    font-family: Quicksand-bold, sans-serif;
    border: 1px solid var(--border-dark);
    box-shadow: 0 0 var(--shadow-size-large) var(--shadow-dark);
  }
}
.row-1 {
  gap: var(--gap-small);
  .card {
    color: var(--text-light);
    font-size: var(--font-small);
    padding: var(--padding-small);
    border-radius: var(--border-radius-small);
  }
}
.row-2 {
  gap: var(--gap);
  .card {
    color: var(--text);
    font-size: var(--font);
    padding: var(--padding);
    border-radius: var(--border-radius);
  }
}
.row-3 {
  gap: var(--gap-large);
  .card {
    color: var(--text-dark);
    font-size: var(--font-large);
    padding: var(--padding-large);
    border-radius: var(--border-radius-large);
  }
}
</style>
