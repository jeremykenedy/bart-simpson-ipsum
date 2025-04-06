<template>
  <div
    class="flex flex-col-reverse items-center justify-center gap-16 px-4 py-24 md:gap-28 md:py-20 md:px-44 lg:flex-row lg:px-24 lg:py-24"
  >
    <div class="relative w-full pb-12 lg:pb-0 xl:w-1/2 xl:pt-24">
      <div class="relative">
        <div class="">
          <div class="text-center md:text-left">
            <h1 class="my-2 text-2xl font-bold text-gray-800 dark:text-white">¡Ay Caramba!</h1>
            <p class="my-7 text-gray-800 dark:text-white">I'm bart simpson, who the hell are you?</p>
            <router-link :to="{ name: 'home' }">
              <AppButton secondary text="Go Home" class="py-4 px-8 w-full lg:w-auto" />
            </router-link>
          </div>
        </div>
      </div>
    </div>
    <div>
      <img id="light" alt="Bart Simpson" class="show-light text-center ml-auto mr-auto w-40" />
      <img id="dark" alt="Bart Simpson" class="show-dark text-center ml-auto mr-auto w-40" />
      <img id="fourZeroFour" alt="404" class="show-dark w-40" />
      <img id="fourZeroFourLight" alt="404" class="show-light w-40" />
    </div>
  </div>
</template>

<script lang="ts">
import fourZeroFour from '@img/404.png';
import fourZeroFourLight from '@img/404-light.png';
import light from '@img/logo/bart.png';
import dark from '@img/logo/bart.png';

export default {
  name: 'NotFound',
  mounted() {
    document.getElementById('light').src = light;
    document.getElementById('dark').src = dark;
    document.getElementById('fourZeroFour').src = fourZeroFour;
    document.getElementById('fourZeroFourLight').src = fourZeroFourLight;
  },
};
</script>
