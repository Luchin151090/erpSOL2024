<template>
  <v-card>
    <NavigationDrawer />
    <v-app-bar :elevation="2" rounded>
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      </template>
      <v-app-bar-title>AGUA SOL ERP</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <div class="custom-icon">
          <MdiLogin />
        </div>
        <v-icon>mdi-bell</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-account-circle</v-icon>
      </v-btn>
      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item>
            <v-list-item-title>Option 1</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Option 2</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </v-card>
</template>

<script>
import MdiLogin from '@/components/MdiLogin.vue';
//import NavigationDrawer from './NavigationDrawer.vue';

export default {
  name: 'HelloWorld',
  components: {
    MdiLogin
    //NavigationDrawer,
  },
  methods: {
    toggleDrawer() {
      console.log('Drawer toggled');
    },
  },
};
</script>

<style scoped>
.custom-icon {
  margin-right: 15px;
}
</style>
