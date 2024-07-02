<template>
  <v-app>
    <v-main>
      <HelloWorld />
      <CardComponent />
      <CardWithSparkline />
      <TableComponent />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CardWithSparkline from './components/CardWithSparkline.vue'
import CardComponent from './components/CardComponent.vue'
import TableComponent from './components/TableComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    CardComponent,
    CardWithSparkline,
    TableComponent
  },
}
</script>
