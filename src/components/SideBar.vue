<template>
  <v-navigation-drawer
    v-model="drawer"
    app
    color="#FFFFFF"
    mini-variant
    mini-variant-width="80"
  >
    <v-card
      class="d-block text-center mx-1 mt-4 my-10 rounded-bl-xl rounded-tr-xl pa-2"
    >
      <v-icon color="#F7AFB0" x-large>fas fa-book-open</v-icon>
    </v-card>

    <v-list flat class="mt-5">
      <v-list-item-group v-model="selectedItem">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          active-class="activeC"
          :ripple="false"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon" color="#F7AFB0"></v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <div
      style="
        position: absolute;
        bottom: 20px;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
      "
    >
      <v-icon class="mb-5" color="#F7AFB0">fas fa-tv</v-icon>

      <br />
      <v-icon color="#F7AFB0" class="mb-5">fas fa-people-arrows</v-icon>
      <br />
      <v-avatar size="30">
        <v-img
          src="https://cdn.vuetifyjs.com/images/lists/2.jpg"
          class="round"
        ></v-img>
      </v-avatar>
    </div>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    drawer: null,
    items: [
      { icon: "fas fa-home" },
      { icon: "fas fa-user-secret" },
      { icon: "fas fa-user-circle" },
      { icon: "fas fa-cog" },
    ],
  }),
};
</script>
<style>
.activeC {
  box-shadow: -10px -10px 10px rgba(255, 255, 255, 0.2),
    15px 15px 15px rgba(0, 0, 0, 0.1),
    inset -10px -10px 10px rgba(255, 255, 255, 0.2),
    inset 15px 15px 15px rgba(0, 0, 0, 0.1);
}
.v-list-item-group .v-list-item--active {
  color: white !important;
}
.round {
  border: 2px solid grey;
}
</style>
