<script setup>
import { brandSelectionContent } from "@/@core/constants/home-view";
</script>

<template>
  <section id="whyUs" class="bg-primary/30">
    <div class="container text-start md:text-center py-20 md:py-28">
      <h2 class="text-2xl lg:text-3xl xl:text-4.5xl 3xl:text-5.5xl font-bold">
      {{ brandSelectionContent.heading }}
    </h2>
      <hr class="w-1/6 sm:w-[6%] md:mx-auto h-1.5 bg-primary my-6 lg:my-9 3xl:my-12">

      <template v-for="(content, i) in brandSelectionContent.descriptions" :key="i">
        <p class="text-lg 2xl:text-3xl pt-6">
          {{ content }}
        </p>
      </template>
    </div>
  </section>
</template>
