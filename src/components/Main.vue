<template>
  <v-row> Plain Bild oder so </v-row>
  <v-row>
    <v-col class="ma-10">
      <v-tabs v-model="tab" color="primary" grow inset align-tabs="center">
        <v-tab value="one">Fähigkeiten</v-tab>
        <v-tab value="two">Fertigkeiten</v-tab>
        <v-tab value="three">Über mich</v-tab>
      </v-tabs>
      <v-divider class="mt-2"></v-divider>
    </v-col>
  </v-row>
  <v-row>
    <v-col class="width=20%"></v-col>
    <v-col class="width=60%">
      <v-card>
        <v-tabs-window v-model="tab">
          <v-tabs-window-item value="one">
            <v-sheet>Inhalt 1</v-sheet>
          </v-tabs-window-item>
          <v-tabs-window-item value="two">
            <v-sheet>Inhalt 2</v-sheet>
          </v-tabs-window-item>
        </v-tabs-window>
      </v-card>
    </v-col>
    <v-col></v-col>
  </v-row>
</template>

<script setup lang="ts">
import { ref } from "vue";

const tab = ref("one");
</script>
