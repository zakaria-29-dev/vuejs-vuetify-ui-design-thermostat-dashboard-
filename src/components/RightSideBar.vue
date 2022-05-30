<template>
  <v-navigation-drawer app color="#EEEBF4" right width="290">
    <div class="d-block text-center">
      <v-btn class="mt-2" outlined
        >Add Equipment <v-icon right>fas fa-plus-circle</v-icon></v-btn
      >
    </div>
    <h3 class="ml-3">ROOMS</h3>
    <h5 class="grey--text ml-3 line">All</h5>
    <v-card
      flat
      class="rounded-br-pill rounded-tr-pill pa-4 mx-3"
      color="#51456B"
    >
      <v-row>
        <v-col cols="12" sm="8">
          <h4 class="white--text">29 Total</h4>
          <v-row>
            <v-col cols="12" sm="6">
              <span class="grey--text">11</span><br />
              <span class="grey--text">Active</span>
            </v-col>
            <v-col cols="12" sm="6">
              <span class="grey--text">13</span><br />
              <span class="grey--text">In Active</span>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="4">
          <v-progress-circular
            :size="60"
            :width="4"
            :value="70"
            color="#FE645B"
            class="mt-2"
          >
            220
          </v-progress-circular>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mx-3 mt-2 rounded-bl-xl rounded-tr-xl pa-2" height="90">
      <v-row>
        <v-col cols="12" sm="6" class="text-center">
          <v-icon color="#F7AFB0" large>fas fa-laptop</v-icon>

          <span class="grey--text">Computer</span><br />
          <span class="grey--text">4</span>
        </v-col>
        <v-col cols="12" sm="6">
          <v-progress-circular
            :size="60"
            :width="3"
            :value="60"
            color="#FE645B"
            class="mt-2 ml-12"
          >
            63
          </v-progress-circular>
          <v-badge
            bordered
            bottom
            color="green"
            dot
            offset-x="1"
            offset-y="-30"
          >
          </v-badge>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mx-3 mt-2 rounded-bl-xl rounded-tr-xl pa-2" height="90">
      <v-row>
        <v-col cols="12" sm="6" class="text-center">
          <v-icon color="#F7AFB0" large>fas fa-satellite</v-icon><br />

          <span class="grey--text">Satellite</span><br />
          <span class="grey--text">3</span>
        </v-col>
        <v-col cols="12" sm="6">
          <v-progress-circular
            :size="60"
            :width="3"
            :value="24"
            color="#FE645B"
            class="mt-2 ml-12"
          >
            24
          </v-progress-circular>
          <v-badge
            bordered
            bottom
            color="green"
            dot
            offset-x="1"
            offset-y="-30"
          >
          </v-badge>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="mx-3 mt-2 rounded-bl-xl rounded-tr-xl pa-2" height="90">
      <v-row>
        <v-col cols="12" sm="6" class="text-center">
          <v-icon color="#F7AFB0" large>fas fa-wifi</v-icon><br />

          <span class="grey--text">Wifi</span><br />
          <span class="grey--text">1</span>
        </v-col>
        <v-col cols="12" sm="6">
          <v-progress-circular
            :size="60"
            :width="3"
            :value="60"
            color="#FE645B"
            class="mt-2 ml-12"
          >
            63
          </v-progress-circular>
          <v-badge
            bordered
            bottom
            color="green"
            dot
            offset-x="1"
            offset-y="-30"
          >
          </v-badge>
        </v-col>
      </v-row>
    </v-card>
    <v-toolbar flat color="transparent" class="mt-n4">
      <span color="black--text" class="caption">+ 4 more</span>
      <v-spacer></v-spacer>
      <v-icon small color="black">fas fa-chevron-circle-right</v-icon>
    </v-toolbar>
    <h5 class="grey--text ml-3 mt-n6">Living Room</h5>
    <v-row>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
        >
          <v-badge bordered bottom color="green" dot>
            <v-icon color="#F7AFB0">fas fa-wifi</v-icon><br />
          </v-badge>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
        >
          <v-badge bordered bottom color="green" dot>
            <v-icon color="#F7AFB0">fas fa-camera</v-icon><br />
          </v-badge>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
        >
          <v-badge bordered bottom color="green" dot>
            <v-icon color="#F7AFB0">fas fa-lightbulb</v-icon><br />
          </v-badge>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
        >
          <v-badge bordered bottom color="green" dot>
            <v-icon color="#F7AFB0">fas fa-fan</v-icon><br />
          </v-badge>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
        >
          <v-badge bordered bottom color="green" dot>
            <v-icon color="#F7AFB0">fas fa-broadcast-tower</v-icon><br />
          </v-badge>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card
          class="d-block text-center mx-3 mt-3 rounded-bl-lg rounded-tr-lg pa-2"
          outlined
        >
          <v-icon color="black">fas fa-plus</v-icon><br />
        </v-card>
      </v-col>
    </v-row>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({}),
};
</script>

<style>
.line {
  text-decoration: underline #ff3028;
}
</style>
