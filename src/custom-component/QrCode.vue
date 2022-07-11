<template>
    <div class="qrcode">
        <vue-qr
            style="width: 100%;height: 100%"
            :text="element.propValue"
            :margin="element.style.qrcodeMargin"
            :size="element.style.qrcodeSize"
            :logoSrc="element.style.qrcodeLogoSrc"
            :logoScale="element.style.qrcodeLogoScale"
            :colorDark="element.style.colorDark"
            :colorLight="element.style.colorLight"
            :autoColor="element.style.autoColor"
        ></vue-qr>
    </div>
</template>

<script>

import vueQr from 'vue-qr'

export default {
    components: {
        vueQr,
    },
    props: {
        propValue: {
            type: String,
            require: true,
            default: '',
        },
        element: {
            type: Object,
            default: () => {},
        },
    },
}
</script>

<style lang="scss" scoped>
.qrcode {
    width: 100%;
    height: 100%;
    overflow: hidden;
}
</style>
