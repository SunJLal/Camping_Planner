<template>
  <div class="q-pa-md">
    <p>
      Ideal Camping Temperature?
    </p>

    <p>
      {{ standard.min }}&#176; F to {{ standard.max }}&#176; F
    </p>

    <q-range
      v-model="standard"
      :min="0"
      :max="120"
      :left-label-value="'Low of ' + standard.min + '° F'"
      :right-label-value="'High of ' + standard.max + '° F'"
      label
      drag-range
    />

    <p>
      (Temperature range of {{ standard.max - standard.min }}&#176; F)
    </p>
  </div>
</template>

<script>
export default {
  name: 'Temperature',
  data () {
    return {
      standard: {
        min: 50,
        max: 90
      }
    }
  }
}
</script>
