<template lang="pug">
  .dashboard-page.pa-0.ma-0.fill-width
    upper-title.ma-0(:title="'Employee'" :titleClass="'dark-background'" :icon="'bell'" :rightIconColor="$vuetify.theme.themes.light.tertiary")
    v-row.ma-0.pt-8.fill-width
      v-col(cols="12")
        //- company-details-vue.align-center.pl-4.pb-4.mb-5.ml-5
        //- company-overview-vue.pb-8.align-center.pl-4.mb-5.ml-5
        //- line-chart-vue.pb-8.align-center.pl-4.mb-5.ml-5
        invoice-details-vue.mt-10.pb-8.align-center.pl-4.mb-5.ml-5.mr-5

  </template>

<script>
import { mapGetters } from 'vuex'
import CompanyStatusVue from '~/components/company/CompanyStatus.vue'
import CompanyDetailsVue from '~/components/company/CompanyDetails.vue'
import UpperTitleVue from '~/components/UpperTitle.vue'
import CompanyOverviewVue from '~/components/company/CompanyOverview.vue'
import InvoiceDetailsVue from '~/components/invoice/InvoiceDetails.vue'

export default {
  name: 'InvoicePage',
  components: {
    CompanyStatusVue,
    CompanyDetailsVue,
    CompanyOverviewVue,
    UpperTitleVue,
    InvoiceDetailsVue
  },
  layout: 'default',
  data () {
    return {
      // search: null
    }
  },
  computed: {
    ...mapGetters({
    })
  },
  methods: {
  }
}
</script>

  <style lang="scss" scoped>
  .fill-height {
    height: 100% !important;
  }
  </style>
