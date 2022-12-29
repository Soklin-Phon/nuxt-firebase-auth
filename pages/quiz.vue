<template>
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step
        :complete="e1 > 1"
        step="1"
      >
        Question 1
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step
        :complete="e1 > 2"
        step="2"
      >
        Question 2
      </v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3">
        Question 3
      </v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">     
       asyncData is called every time before loading the page component.
          <v-checkbox
          v-model="checkbox1"
          :label="`True`"
        ></v-checkbox>
        <v-checkbox
          v-model="checkbox2"
          :label="`False`"
        ></v-checkbox>

        <v-btn
          color="primary"
          @click="e1 = 2"
        >
          Continue
        </v-btn>

        <v-btn text>
          Cancel
        </v-btn>
      </v-stepper-content>

      <v-stepper-content step="2">
        Nuxt.js is a free and open source JavaScript library based on React Js
        <v-checkbox
        v-model="checkbox1"
        :label="`True`"
      ></v-checkbox>
      <v-checkbox
        v-model="checkbox2"
        :label="`False:`"
      ></v-checkbox>

        <v-btn
          color="primary"
          @click="e1 = 3"
        >
          Continue
        </v-btn>

        <v-btn text>
          Cancel
        </v-btn>
      </v-stepper-content>

      <v-stepper-content step="3">
    Nuxt js is a frontend framework built upon Vue.
        <v-checkbox
        v-model="checkbox1"
        :label="`True`"
      ></v-checkbox>
      <v-checkbox
        v-model="checkbox2"
        :label="`False:`"
      ></v-checkbox>
        <v-btn
          color="primary"
          @click="e1 = 1"
        >
          Continue
        </v-btn>

        <v-btn text>
          Cancel
        </v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
</template>

<script>
  export default {
    data () {
      return {
        e1: 1,
        checkbox1: true,
        checkbox2: false,
      }
    },
  }
</script>