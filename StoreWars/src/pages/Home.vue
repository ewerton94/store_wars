<template>
  <q-page class="WAL__layout " >
    <div class="row q-ma-md">
      <div class="full-width">
        <Breadcrumbs :pages="pages"  />
        <div class="row justify-end">

        <q-btn flat align="right" to="/new-order" class="bg-grey-9 q-px-sm text-white " dense label="Novo pedido" icon="add" />
        </div>
      </div>

      <div  class="full-width">
        <ListOrders />
      </div>
    </div>
  </q-page>
</template>

<script>
import Breadcrumbs from 'components/Home/BreadCrumbs.vue'
// import FilterBlock from 'components/Home/FilterBlock.vue'
import ListOrders from 'components/Home/ListOrders.vue'

export default {
  name: 'PageIndex',
  data: function () {
    return {
      pages: [
        { name: 'Pedidos', icon: 'store', href: '/' }
      ]
    }
  },
  components: {
    Breadcrumbs,
    // FilterBlock,
    ListOrders
  }
}
</script>
<style  lang="sass">
.WAL
  &__layout
    margin: 0 auto
    height: 100%
    width: 90%
    max-width: 1050px
    border-radius: 5px
@media (max-width: 850px)
  .WAL
    padding: 0
    &__layout
      width: 100%
      border-radius: 0
@media (min-width: 691px)
  .WAL
    &__drawer-open
      display: none
</style>
