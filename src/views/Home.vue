<template>
  <v-app
    id="inspire"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <SideBar />
    <RightSideBar />
    <v-container>
      <v-toolbar flat color="transparent" class="mt-n5">
        <v-icon color="grey" small>fas fa-chevron-left</v-icon>
        <span class="ml-2 caption grey--text">EQUIPMENTS</span>
      </v-toolbar>
      <v-toolbar flat color="transparent" class="mt-n8">
        <v-icon color="grey" small>far fa-snowflake</v-icon>
        <v-spacer></v-spacer>
        <v-icon color="grey" small>fas fa-hot-tub</v-icon>
        <span class="ml-2 caption grey--text">Swing</span>
        <v-switch color="green" v-model="on" class="mt-5 ml-2"></v-switch>
      </v-toolbar>
      <h1 class="grey--text text-darken-2 ml-3 mt-n5">Thermostat</h1>
      <span class="grey--text text-darken-2 ml-3 mr-2 caption"
        >Living Room</span
      >
      <v-icon small color="grey">fas fa-chevron-down</v-icon>
      <v-row class="mt-n10">
        <v-col cols="12" sm="9" align="center">
          <v-row>
            <v-col cols="12" sm="2" align="center">
              <v-btn fab color="#E2DEEC" class="top1"
                ><v-icon color="#827997">fas fa-chevron-left</v-icon></v-btn
              >
            </v-col>
            <v-col cols="12" sm="8">
              <v-btn fab color="#F2B7BD" class="top3"
                ><v-icon color="white">fas fa-power-off</v-icon></v-btn
              >
              <div class="box shadow">
                <v-progress-circular
                  :size="200"
                  :width="16"
                  :value="40"
                  color="#FE645B"
                  class=""
                >
                  <div class="box1">
                    <h6 class="white--text">25</h6>
                    <span class="caption white--text mt-n5 ml-1 mr-4">°C</span
                    ><br />
                    <v-icon color="white" small>fas fa-tint</v-icon
                    ><span class="caption white--text">%47</span>
                  </div>
                </v-progress-circular>
              </div>
            </v-col>
            <v-col cols="12" sm="2" align="center">
              <v-btn fab color="#E2DEEC" class="top2"
                ><v-icon color="#827997">fas fa-chevron-right</v-icon></v-btn
              >
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="3">
          <v-row>
            <v-col cols="12" sm="2">
              <span class="grey--text orientation">Fan Speed</span>
              <v-icon color="grey" small class="iconposi">fas fa-fan</v-icon>
            </v-col>
            <v-col cols="12" sm="10">
              <v-slider
                v-model="sld.val"
                :color="sld.color"
                track-color="#E2DEEC"
                vertical
                class="large-slider mtop"
              ></v-slider>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="12">
          <v-toolbar flat color="transparent" class="mt-n10">
            <span class="grey--text">Usage Pattern</span>
            <v-spacer></v-spacer>
            <span class="ml-2 caption grey--text">Daily</span>
            <span class="ml-2 caption grey--text">Weekly</span>
            <v-icon color="red" class="ml-2"
              >fab fa-creative-commons-sampling</v-icon
            >
          </v-toolbar>
          <v-sparkline
            class="mt-n16"
            fill="true"
            :labels="labels"
            :value="value"
            :gradient="gradients"
            line-width="1"
            padding="16"
            :smooth="16"
            auto-draw
            color="grey"
            stroke-linecap="round"
          ></v-sparkline>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
// @ is an alias to /src
import SideBar from "@/components/SideBar.vue";
import RightSideBar from "../components/RightSideBar.vue";
const gradients = ["#FC8D6D", "#F2B7BD", "#F1EDF3"];

export default {
  name: "Home",
  data: () => ({
    on: true,
    labels: ["12am", "3am", "6am", "9am", "12pm", "3pm", "6pm", "9pm"],
    value: [0, 7, 5, 9, 0, 10, 5, 1],
    gradients: gradients,
    sld: {
      val: 45,
      color: "#FE645B",
    },
  }),
  components: {
    SideBar,
    RightSideBar,
  },
};
</script>
<style scoped>
.box {
  position: relative;
  width: 250px;
  height: 250px;
  margin: 30px;
  background: #f1edf3;
  font-size: 2em;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  color: rgba(0, 0, 0, 0.1);
}
.box.shadow {
  box-shadow: -10px -10px 10px rgba(235, 112, 180, 0.11),
    15px 15px 15px rgba(0, 0, 0, 0.1),
    inset -10px -10px 10px rgba(255, 255, 255, 0.2),
    inset 15px 15px 15px rgba(0, 0, 0, 0.1);
}
.box1 {
  position: relative;
  width: 170px;
  height: 170px;
  margin: 30px;
  background: #f3b6b8;
  font-size: 2em;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  color: rgba(0, 0, 0, 0.1);
}
.top1 {
  margin-top: 120px;
  margin-left: 100px;
}
.top2 {
  margin-top: 120px;
  margin-left: -150px;
}
.top3 {
  position: absolute;
  margin-top: 260px;
  margin-left: -25px;
  z-index: 1000;
}
.large-slider >>> .v-slider {
  height: 300px;
}
.large-slider >>> .v-slider--vertical .v-slider__track-container {
  width: 8px;
}
.large-slider >>> .v-slider__thumb {
  width: 30px;
  height: 30px;
  left: -14px;
}
.orientation {
  writing-mode: vertical-lr;
  text-orientation: sideways;
  margin-top: 150px;
  margin-left: 80px;
}
.mtop {
  margin-top: -20px;
}
.iconposi {
  margin-top: 20px;
  margin-left: 85px;
}
</style>
