<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <QrcodeVue :value="link" />
    </q-card>
  </div>
</template>
<script>
import QrcodeVue from "qrcode.vue";
export default {
  name: "QrCodeGenerator",
  components: {
    QrcodeVue
  },
  props: {
    link: String
  }
};
</script>
