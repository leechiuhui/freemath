<template>
  <div class="hello">
    <br/>
    <div class="ui left aligned segment container no-print">
      <h1>攀岩式學習地圖</h1>
      <h3 class="ui header">如何使用：</h3>
      <div class="ui large ordered list">
        <div class="item">
          選擇適合年段的地圖下載印出
        </div>
        <div class="item">
          用筆圈出己經會的單元
        </div>
        <div class="item">
          用筆圈出不太會的單元(可打問號)
        </div>
        <router-link class = 'item' to='/trace' exact=''>
          <i class="sort amount icon" />下載相關教材
        </router-link>
        <div class="item">
          遇到問題可上
          <a class="item" href="https://www.facebook.com/groups/156709241062806/" target="_blank">
            <i class="facebook icon" />自學數學團
          </a>提問
        </div>
      </div>

      <div class="ui divider"></div>

      <div class="ui grid no-print">
        <label>選擇年段：
          <br class="thin-only" /></label>
        <div class="ui stackable row">
          <div class="four wide column" v-for="(r, l) in ranges" :key="'range' + l">
            <div class="ui radio checkbox">
              <input type="radio" name="year" v-bind:value="r" v-model = "myRange">
              <label class="clickable" @click = "myRange = r">{{r.t}}</label>
            </div>
          </div>
        </div>
        <div class="ui row text-center">
          <button class = "ui large green button" id = "doPrint" @click = "printUrl(myRange.t,'.pdf')"> 友善列印
          </button>
        </div>
      </div>
    </div><!-- Segment END -->

   <ul class = "print">
      <li v-for = "i in [1,2,3,4,0,5]" :key="'print' + i">
        <a :href="'/static/maps/'+myRange.t+'/p'+i+'.jpg'" target="_blank">
          <img :src ="'/static/maps/'+myRange.t+'/p'+i+'.jpg'" style="max-width:75vw" alt = ""/>
        </a>
      <div class="divider"></div></li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'maps',
  data () {
    return {
      index: undefined,
      myRange: {t: '小學數學地圖', p: 6},
      ranges: [
        {t: '小學數學地圖', p: 6},
        {t: '國中數學地圖', p: 6},
        {t: '高中數學地圖', p: 6}
      ],
      images: [
        '/static/maps/小學數學地圖/p0.jpg',
        '/static/maps/小學數學地圖/p1.jpg',
        '/static/maps/小學數學地圖/p2.jpg',
        '/static/maps/小學數學地圖/p3.jpg',
        '/static/maps/小學數學地圖/p4.jpg',
        '/static/maps/小學數學地圖/p5.jpg',
        '/static/maps/國中數學地圖/p0.jpg',
        '/static/maps/國中數學地圖/p1.jpg',
        '/static/maps/國中數學地圖/p2.jpg',
        '/static/maps/國中數學地圖/p3.jpg',
        '/static/maps/國中數學地圖/p4.jpg',
        '/static/maps/國中數學地圖/p5.jpg',
        '/static/maps/高中數學地圖/p0.jpg',
        '/static/maps/高中數學地圖/p1.jpg',
        '/static/maps/高中數學地圖/p2.jpg',
        '/static/maps/高中數學地圖/p3.jpg',
        '/static/maps/高中數學地圖/p4.jpg',
        '/static/maps/高中數學地圖/p5.jpg'
      ]
    }
  },
  methods: {
    printUrl: function (title, tail) {
      window.open(
        '/static/maps/' + title + tail,
        '_blank'
      )
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #35495E;
}

.image {
  cursor: pointer;
  width: 16%
}

</style>
