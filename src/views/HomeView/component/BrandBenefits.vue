<script setup>
import { benefitsContent, buttonsLabel } from "@/@core/constants/home-view";
import SiteButton from "@/@core/components/SiteButton.vue";
</script>

<template>
  <section class="container py-20 2xl:py-26 md:px-10">
    <h4 class="text-2xl lg:text-3xl 2xl:text-4xl font-bold">
      {{ benefitsContent.heading }}
    </h4>
    <p class="text-lg 2xl:text-3xl pt-3 pb-5 md:pb-7 md::w-3/4">
      {{ benefitsContent.text }}
    </p>
    <div class="grid lg:grid-cols-2 gap-5 pb-6 lg:pb-0">
      <div class="pt-10 md:pt-16">
        <template v-for="benefit in benefitsContent.benefits" :key="benefit.title">
          <div class="flex items-start gap-5 md:gap-8 pb-10 md:pb-20">
            <div class="shrink-0 text-primary flex justify-center w-20 2xl:w-24">
              <span :class="`icon-${benefit.icon}`" class="text-6xl xl:text-8xl"></span>
            </div>
            <div>
              <h5 class="text-xl 2xl:text-3xl font-bold pb-2.5">{{ benefit.title }}</h5>
              <p class="text-lg 2xl:text-3xl">{{ benefit.description }}</p>
            </div>
          </div>
        </template>
        <div>
          <SiteButton border>
            {{ buttonsLabel.CTOBtn }}
          </SiteButton>
        </div>
      </div>
      <div class="flex items-center justify-center py-6">
        <img :src="benefitsContent.image" :alt="benefitsContent.alt">
      </div>
    </div>
  </section>
</template>
