<template lang="pug">
  .hello
    br.fat-only
    h1 {{ sify('三、具體經驗') }}
    .ui.grid
      .one.column.row
        .column
          .ui.segment.container
            h3 {{ sify('『太上，不知有之；其次，親之譽之。』-- 老子《道德經》') }}

            p {{ sify('前兩節談到了倒溯法和前推法。') }}
            p {{ sify('把它們交互運用，可以在知識體系中織起密實的網子，搭起堅固的鷹架，補舊的破洞、做新的拓展。') }}
            br
            p {{ sify('不過，知識環節只是數學的骨架，而不是血肉。') }}
            br
            p {{ sify('有時候會遇到這樣的情況：') }}
            br
            p {{ sify('『7乘以6是多少？』『七六...七六...不知道。』') }}
            p {{ sify('『那你知道6乘以7是多少嗎？』『六七...六七...42。』')}}
            p {{ sify('『7乘以6和6乘以7會一樣嗎？』『會。』') }}
            p {{ sify('『為什麼？』『7個6和6個7一樣啊。』') }}
            br
            p {{ sify('在知識上，這個小孩懂得乘法的意義和交換性，但是這個知識並沒有內化、變成一種自然而然的感覺。') }}
            p {{ sify('所以當他背不出『七六』的時候，不會想到用『六七』來替代。') }}
            br
            p {{ sify('或者像是：') }}
            br
            p {{ sify('『半斤是8兩，那麼一兩是幾斤呢？』『8斤。』') }}
            p {{ sify('『8斤？8斤比半斤多還是少？』『多。』') }}
            p {{ sify('『那怎麼會是8斤呢？再想想。』『嗯...要先除2再乘8嗎？』') }}
            br
            p {{ sify('這是量感的問題。') }}
            p {{ sify('如果幫他把圖畫出來，他多半會算。但是他對單位之間的關係沒有感覺。') }}
            br
            p {{ sify('數學能力的血肉，就是這種「感覺」。對數字的感覺 ; 對長度、重量、時間、面積的感覺 ; 均分的經驗 ; 機率感、策略運用等等。') }}
            br
            p {{ sify('在國中小和學齡前，這種感覺主要是靠遊戲和具體活動來建立的。') }}
            br
            p {{ sify('任何遊戲，只要用到策略，就和數學經驗有關。') }}
            p {{ sify('不只是樸克牌、圍棋、魔法牌，連紅綠燈、大風吹、桌球、籃球，都是豐富策略經驗的來源。') }}
            p {{ sify('單車、爬竿、捉蟲，用身體得到的經驗，也是相當寶貴的。') }}
            br
            p {{ sify('數學並不是加、減、乘、除、算一算答案，那叫算術；也不是公理、定義、定理，那叫公理系統。') }}
            p {{ sify('數學是在尋找變動的世界背後，不變的秩序，並且把它用符號表現出來，讓大家都能理解、運用。') }}
            p {{ sify('因此，很多看起來不是數學的東西，都能提供富豐的數學經驗。') }}
            br
            p {{ sify('以廚藝為例。') }}
            br
            p {{ sify('看食譜、考慮人數，是比例的經驗；不同大小的匙、量杯一杯和一格的區別，是單位的經驗；切菜、切蛋糕，是分數的經驗；火候的調控，是時間與函數的經驗。') }}
            br
            p {{ sify('在測量麵粉重量的時候、在目測茸絲長度的時候，就經驗到了數學；在設定烤箱溫度的時候、在把蛋汁打均的時候，就經驗到了數學。') }}
            br
            p {{ sify('每一種工藝，每一樣文明的產物，都有它的秩序、策略和條理。') }}
            br
            p {{ sify('小孩在從事它們的時候，並不會說『啊！這是分數』、『啊！這是比例』、『酷！座標變換！』。') }}
            p {{ sify('但是，無論是廚藝、武術、縫紉、繪畫、魔術，這些動手又動腦的經驗，都會使小孩的數學感變得豐富。') }}
            br
            p {{ sify('豐富的數學感，有助於學習數學、有助於內化數學、有助於把數學應用到生活。') }}
            p {{ sify('如此，小孩才能用其所學，不會一直追問：數學有什麼用？') }}

            h3 {{ sify('練習') }}
            ol.ui.ordered.list
              li.item {{ sify('請舉出生活中會應用到的「除法」概念') }}
              li.item {{ sify('請舉出生活中會應用到的「比例」概念') }}
              li.item {{ sify('請舉出生活中會應用到的「負數」概念') }}
    .ui.grid.container
      .three.column.doubling.row
        .column
          router-link(to = "/one1") {{ sify('一、倒溯法')}}
        .column
          router-link(to = "/one2") {{ sify('二、前推法')}}
        .column
          router-link(to = "/one3") {{ sify('三、具體經驗')}}
        .column
          router-link(to = "/one4") {{ sify('四、繞道法--渡過心理障礙')}}
        .column
          router-link(to = "/one5") {{ sify('五、主客易位法')}}
        .column
          router-link(to = "/one6") {{ sify('六、面對錯誤')}}
        .column
          router-link(to = "/one7") {{ sify('七、適度的練習')}}
        .column
          router-link(to = "/one8") {{ sify('八、互為主體、交互佈題法')}}
        .column
          router-link(to = "/one9") {{ sify('數學學習診斷是什麼？')}}

</template>

<script>

import {sify} from 'chinese-conv'

export default {
  name: '具體經驗',
  props: ['si'],
  data () {
    return {
    }
  },
  methods: {
    sify (t) {
      if (this.si) {
        return sify(t)
      } else {
        return t
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.column {
  text-align: left;
}
</style>
