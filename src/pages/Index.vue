<template>
  <div style="margin: 0px auto; max-width: 920px;">
    <div class="row">
      <div class="section-1 col-12">
        <q-carousel
          swipeable
          animated
          v-model="slide"
          navigation
          infinite
          :autoplay="autoplay"
          arrows
          transition-prev="slide-right"
          transition-next="slide-left"
          @mouseenter="autoplay = false"
          @mouseleave="autoplay = true"
        >
          <q-carousel-slide :name="1" img-src="~assets/banner/AW-1.jpg" />
          <q-carousel-slide :name="2" img-src="~assets/banner/ad_serum.jpg" />
          <q-carousel-slide :name="3" img-src="~assets/banner/AW-2.jpg" />
          <q-carousel-slide :name="4" img-src="~assets/banner/S__65519787.jpg" />
        </q-carousel>
      </div>
    </div>
    <div class="gold-line"></div>
    <div class="main-title q-pa-sm">
      ยินดีต้อนรับเข้าสู่<br/>
      HIRABLUE SHOP+<br/>
    </div>
    <div class="gold-line"></div>
    <div class="q-pa-sm">
      <div class="row">
        <div class="col-12 q-pa-sm">
          <div style="font-size: 24px; text-align: center;">HIRA BLUE ไฮร่าบลู</div>
          <div style="text-indent: 1.5em;">
            NO.1 นวัตกรรมใหม่จากญี่ปุ่น HIRA BLUE ผลิตภัณฑ์ใหม่ ไฉไลกว่าเดิม นอกจากจะเป็นสุดยอดสกินแคร์ที่อุดมไปด้วย Hyaluron ถึง 4 อนุพันธ์ุ และ มอส MossCelltecTM
            อ่อนโยนต่อผิว ผิวแพ้ง่าย คนท้องก็ใช้ได้ มั่นใจ ด้วยสารสกัดจากธรรมชาติ
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-12 col-md-6 q-pa-sm"><img class="rounded-borders shadow-5" src="~assets/promo/AW-5.jpg" style="width: 100%;"/></div>
        <div class="col-12 col-md-6 q-pa-sm"><img class="rounded-borders shadow-5" src="~assets/promo/AW-7.jpg" style="width: 100%;"/></div>
        <div class="col-12 col-md-6 q-pa-sm"><img class="rounded-borders shadow-5" src="~assets/promo/AW-6.jpg" style="width: 100%;"/></div>
        <div class="col-12 col-md-6 q-pa-sm"><img class="rounded-borders shadow-5" src="~assets/promo/AW-8.jpg" style="width: 100%;"/></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  meta: {
    title: 'Hira Blue Shop'
  },
  name: 'PageIndex',
  data () {
    return {
      slide: 1,
      autoplay: true
    }
  }
}
</script>
