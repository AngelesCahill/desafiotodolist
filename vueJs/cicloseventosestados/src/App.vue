<template>
  <div id="app">
    <div>
      <h4>{{header}}</h4>
      <ul>
      <li v-for="(item, index) in items" :key="index" class="default" :style="[styleObject, another]"
      :class="{strikeout: item.comprado}">{{item.elemento}}</li>
      </ul>
<hr>
<h1>{{message}}</h1>

</div>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      header: "Lista cumpleaños",
      items: [
      {
      elemento: "20 palitos de fósforos",
      comprado: true
      },
      {
      elemento: "10 Velas",
      comprado: true
      },
      {
      elemento: "1 Torta",
      comprado: false
      }
      ],
      styleObject: {
        color: 'red',
        fontSize: '13px',
      },
      another: {
        background: 'black',
      },
      message: 'Hola Ñ!!!',

    }
  },
  

}
</script>

<style>
.default {
 color: royalblue;
}
.strikeout {
 text-decoration: line-through;
 color: gray;
}
</style>
