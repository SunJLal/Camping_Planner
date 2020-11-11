<template>
  <q-page class="text-center q-pa-md question-form q-page doc-page">
    <p>Hello Camper!</p>

    <p>Where would you like to camp?</p>
      <div class="q-my-md">
        <q-input outlined v-model="city" label="City" />
      </div>
      or
      <div class="q-my-md">
        <q-input outlined v-model="zip" label="Zip" />
      </div>
    <p>When are you free to camp?</p>
    <q-date v-model="days"
    subtitle="Camping Window"
    range
    multiple />

    <!-- <div class="q-pb-sm">
      Model: {{ days }}
    </div> -->

    <Temperature> </Temperature>

  </q-page>
</template>

<script>
import Temperature from 'components/Temperature'

export default {
  name: 'PageIndex',
  components: { Temperature },
  data () {
    return {
      days: null,
      city: null,
      zip: null
    }
  }
}
</script>

<style scoped>
.question-form {
  padding: 16px 46px;
  font-weight: 300;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}
</style>
