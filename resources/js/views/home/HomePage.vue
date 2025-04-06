<template>
  <div class="p-12">
    <div class="text-center">
      <div class="mb-5 flex items-center justify-between">
        <img id="mjLight" alt="Bart Simpson" class="show-light text-center ml-auto mr-auto w-40" />
        <img id="mjDark" alt="Bart Simpson" class="show-dark text-center ml-auto mr-auto w-40" />
      </div>
      <h1 class="text-4xl mb-5 quicksand-font text-slate-500 dark:text-slate-300">
        {{ appName }}
      </h1>
    </div>
    <MichaelIpsum />
  </div>
</template>

<script>
import MichaelIpsum from '@components/ipsums/MichaelIpsum.vue';
import mjLight from '@img/logo/bart.png';
import mjDark from '@img/logo/bart.png';

export default {
  name: 'HomePage',
  components: { MichaelIpsum },
  computed: {
    appName() {
      return APP_NAME;
    },
  },
  mounted() {
    document.getElementById('mjLight').src = mjLight;
    document.getElementById('mjDark').src = mjDark;
  },
};
</script>
