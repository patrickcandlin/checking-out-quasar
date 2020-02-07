<template>
  <q-page class="flex flex-center">
    <section
      class="qrcodes"
      v-for="(link, index) in essentialLinks"
      :key="index"
    >
      <QrCodeGenerator :link="link.link" />
    </section>
  </q-page>
</template>

<script>
import QrCodeGenerator from "../components/QrCodeGenerator.vue";
export default {
  name: "PageIndex",
  components: {
    QrCodeGenerator
  },
  data() {
    return {
      essentialLinks: [
        {
          title: "Docs",
          caption: "quasar.dev",
          icon: "school",
          link: "https://quasar.dev"
        },
        {
          title: "Github",
          caption: "github.com/quasarframework",
          icon: "code",
          link: "https://github.com/quasarframework"
        },
        {
          title: "Discord Chat Channel",
          caption: "chat.quasar.dev",
          icon: "chat",
          link: "https://chat.quasar.dev"
        },
        {
          title: "Forum",
          caption: "forum.quasar.dev",
          icon: "record_voice_over",
          link: "https://forum.quasar.dev"
        },
        {
          title: "Twitter",
          caption: "@quasarframework",
          icon: "rss_feed",
          link: "https://twitter.quasar.dev"
        },
        {
          title: "Facebook",
          caption: "@QuasarFramework",
          icon: "public",
          link: "https://facebook.quasar.dev"
        }
      ]
    };
  }
};
</script>
