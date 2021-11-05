<template>
  <div class="app">
  <!-- <p>Hello, Hyrule {{name}}</p>
  <button @click="changeName('Zelda')">Change name</button> -->
  <p>{{jobs[0].location}}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import Job from './types/job';

export default defineComponent({
  name: 'App',
  components: {

  },
    setup() {
    // example using reactive
    // const state = reactive({
    //   name: 'Link',
    //   age: 25 as number | string
    // })

    // return {...toRefs(state)}

    //example using ref
    // const name = ref('Link')
    // const age = ref<string | number>(25)

    // return {name, age}

    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])
    return { jobs }
  },
  methods: {
    // changeName(name: string) {
    //   this.name = name
    // }
  }
});
</script>

<style>

</style>
