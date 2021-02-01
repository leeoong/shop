<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <div style="margin: 0px auto; max-width: 920px;">
        <q-toolbar>
          <q-btn
            flat
            dense
            round
            icon="o_menu"
            aria-label="Menu"
            @click="leftDrawerOpen = !leftDrawerOpen"
            style="z-index: 2;"
          />

          <div
            style="
              position: absolute; z-index: 1;
              left: 50%;
              transform: translateX(-50%);
              width: 100%; text-align: center;
            "
          ><img src="~assets/logo_head.png"/></div>
        </q-toolbar>
      </div>
      <div class="toolbar-line-bottom"></div>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label header class="text-grey-8" style="text-align: center;">
          <img src="~assets/logo_h_256.png" style="height: 64px;"/>
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    <div style="height: 50px;">&nbsp;</div>
    <div class="fast-contact flex">
      <a class="call" href="tel:080-546-9983" target="_blank">
        <span style="font-family: KanitRegular;"> CALL NOW</span><br/>
        <span>โทรคุยกับเรา</span>
      </a>
      <a class="line" href="https://line.me/ti/p/@leeoong" target="_blank">
        <span style="font-family: KanitRegular;">CHAT LINE</span><br/>
        <span>แชทไลน์</span>
      </a>
    </div>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Home',
    caption: 'หน้าแรก',
    icon: 'o_home',
    link: '/'
  },
  {
    title: 'Product',
    caption: 'สินค้าทั้งหมด',
    icon: 'o_category',
    link: '/catalog'
  },
  {
    title: 'Contact',
    caption: 'ติดต่อเรา',
    icon: 'o_contact_page',
    link: '/contact'
  }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
