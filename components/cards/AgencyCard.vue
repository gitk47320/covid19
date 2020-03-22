<template>
  <v-col cols="12" md="6" class="DataCard">
  </v-col>
</template>

<script>
import agencyData from '@/data/agency.json'
import AgencyBarChart from '@/components/AgencyBarChart.vue'

export default {
  components: {
    AgencyBarChart
  },
  data() {
    const agencies = [
      this.$t('第一庁舎計'),
      this.$t('第二庁舎計'),
      this.$t('議事堂計')
    ]
    agencyData.datasets.map(dataset => {
      dataset.label = this.$t(dataset.label)
    })
    return {
      agencyData,
      agencies
    }
  }
}
</script>
