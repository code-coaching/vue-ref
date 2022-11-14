<template>
  <p>{{ title }}</p>
  <p>{{ persoon }}</p>
  <p>{{ samson }}</p>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const samson = ref('Samson');
    /*
    {
      value: 'Samson'
    }
    */

    const title = ref('Ref uitleg!');
    const persoon = ref('John Duck');

    setTimeout(() => {
      console.log('title', title.value);
      title.value = 'Ref uitleg is veranderd!';
      persoon.value = 'Janine Duck';
      samson.value = 'Samson is veranderd!';
      console.log('title', title.value);
    }, 5000);

    return {
      title,
      persoon,
      samson,
    };
  },
});
</script>
