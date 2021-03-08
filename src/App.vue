<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
          </v-app-bar>

    <v-main>
        <v-container>
          <v-row class="text-center">
            <v-col cols="6">
              
              <extraction-card outlined class="mx-auto card-shadow" style="max-width: 500px">
                <v-list-item three-line>
                  <v-list-item-content>
                    <div class="overline mb-4">
                      OVERLINE
                    </div>
                    <v-list-item-title class="headline mb-1">
                      Headline 5
                    </v-list-item-title>
                    <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
                  </v-list-item-content>

                  <v-list-item-avatar
                    tile
                    size="80"
                    color="grey"
                  ></v-list-item-avatar>
                </v-list-item>

                <v-card-actions>
                  <IdxButton outlined title="submit" class="home-btn" />
                </v-card-actions>


              </extraction-card>

            </v-col>
            <v-col cols="6">
              <overview-card style="max-height: 400px; max-width: 450px;">
                <v-card-text>
                  <div>Word of the Day</div>
                  <p class="display-1 text--primary">
                    el·ee·mos·y·nar·y
                  </p>
                  <p>adjective</p>
                  <div class="text--primary">
                    relating to or dependent on charity; charitable.<br>
                    "an eleemosynary educational institution."
                  </div>
                </v-card-text>
                <v-card-actions>
                  <v-btn
                    text
                    color="teal accent-4"
                    @click="reveal = true"
                  >
                    Learn More
                  </v-btn>
                </v-card-actions>

                <v-expand-transition>
                  <v-card
                    v-if="reveal"
                    class="transition-fast-in-fast-out v-card--reveal"
                    style="height: 100%;"
                  >
                    <v-card-text class="pb-0">
                      <p class="display-1 text--primary">
                        Origin
                      </p>
                      <p>late 16th century (as a noun denoting a place where alms were distributed): from medieval Latin eleemosynarius, from late Latin eleemosyna ‘alms’, from Greek eleēmosunē ‘compassion’ </p>
                    </v-card-text>
                    <v-card-actions class="pt-0">
                      <v-btn
                        text
                        color="teal accent-4"
                        @click="reveal = false"
                      >
                        Close
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-expand-transition>
              </overview-card>
            </v-col>
          </v-row>
        </v-container>
    </v-main>
  </v-app>
</template>

<script>
import ExtractionCard from './assets/idxUILib/extractionCard.vue';
import IdxButton from './assets/idxUILib/IdxButton';
import OverviewCard from './assets/idxUILib/overviewCard.vue';


export default {
  name: 'App',

  components: {
    IdxButton,
    ExtractionCard,
    OverviewCard
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.v-main__wrap .v-btn:not(.v-btn--round).v-size--default{
  margin: 10px 0;
}
.v-input.v-input--dense.theme--light.v-text-field.v-text-field--is-booted.v-text-field--enclosed.v-text-field--outlined{
  margin-top: 30px;
}
</style>