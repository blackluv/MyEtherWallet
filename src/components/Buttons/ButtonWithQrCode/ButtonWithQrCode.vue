<template>
  <div class="modal-container">
    <div class="wrap">
      <div class="the-button large-round-button-green-filled">{{ buttonname }}</div>
      <div class="qrcode-container">
        <img
          :src="qrcodeIconImage"
          class="dummy-qrcode">
        <div class="real-qrcode">
          <img src="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QrcodeIcon from '@/assets/images/icons/qr-code.svg';

export default {
  props: {
    qrcode: {
      type: String,
      default: ''
    },
    buttonname: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      qrcodeIconImage: QrcodeIcon
    };
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
@import 'ButtonWithQrCode.scss';
</style>
