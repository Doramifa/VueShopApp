<template>
  <div class="listview">
    <ul v-for="(listItem, index) in listDataShow" :key="index"
      :is="listItem.type" :ownprop="listItem">
    </ul>
  </div>
</template>

<script>
import Item from './Item'
import Shop from './Shop'
import Dummy from './Dummy'

export default {
  name: 'listview',
  props: [],
  components: {
    'item': Item,
    'shop': Shop
  },
  data () {
    return {
      start: 0,
      end: 6,
      listData: [
        {type: 'shop', name: '店铺名长长长长长长长长长长长长', imgUrl: Dummy.prototype.get(), assess: [3, 5, 4.4], shopUrl: 'dianpuURL'},
        {type: 'shop', name: '店铺名长长', imgUrl: Dummy.prototype.get(), assess: [3.5, 4.3, 2.1], shopUrl: 'dianpuURL'},
        {type: 'shop', name: '水果手机专卖店', imgUrl: Dummy.prototype.get(), assess: [5, 4.6, 3.9], shopUrl: 'dianpuURL'},
        {type: 'item', name: '商品名长长长长长长长长长长长长', imgUrl: Dummy.prototype.get(), price: 6.66, itemUrl: 'dianpuURL', volume: 5, discount: 10},
        {type: 'item', name: '商品名长长', imgUrl: Dummy.prototype.get(), price: 23.33, itemUrl: 'dianpuURL', volume: 780, discount: 10},
        {type: 'item', name: '商品名长', imgUrl: require('./assets/S.png'), price: 8088.00, itemUrl: 'dianpuURL', volume: 123102, discount: 10},
        {type: 'shop', name: '店铺名长长长长长长长长长长长长', imgUrl: Dummy.prototype.get(), assess: [3, 5, 4.4], shopUrl: 'dianpuURL'},
        {type: 'shop', name: '店铺名长长', imgUrl: Dummy.prototype.get(), assess: [3.5, 4.3, 2.1], shopUrl: 'dianpuURL'},
        {type: 'shop', name: '水果手机专卖店', imgUrl: Dummy.prototype.get(), assess: [5, 4.6, 3.9], shopUrl: 'dianpuURL'},
        {type: 'item', name: '商品名长长长长长长长长长长长长', imgUrl: Dummy.prototype.get(), price: 6.66, itemUrl: 'dianpuURL', volume: 5, discount: 10},
        {type: 'item', name: '商品名长长', imgUrl: Dummy.prototype.get(), price: 23.33, itemUrl: 'dianpuURL', volume: 780, discount: 10},
        {type: 'item', name: '商品名长', imgUrl: require('./assets/S.png'), price: 8088.00, itemUrl: 'dianpuURL', volume: 123102, discount: 10}
      ]
    }
  },
  computed: {
    listDataShow: function () {
      return this.listData.slice(this.start, this.end)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  margin: 0;
}

a {
  color: #42b983;
}

.listview {
  position: relative;
  width: 100%;
  background-color: #EEEEEE;
}
</style>
