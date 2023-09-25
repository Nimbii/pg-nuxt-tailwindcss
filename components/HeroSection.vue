<script setup lang="ts">
  import { pg_background_urls } from '~~/themes/pg-tailwindcss/tokens.mjs'

  const heroImageUrl =
    pg_background_urls['design-image-large'] ||
    pg_background_urls['design-image']

  const { optimizeImage } = useOptimizeImage()
  const { bgStyles } = optimizeImage(heroImageUrl)
</script>
<template>
  <section>
    <div
      class="bg-center bg-cover bg-no-repeat blur-none z-0 bg-design-image lg:bg-design-image-large"
    >
      <div
        class="pb-36 pt-2 px-6 relative rounded-3xl md:pb-48 lg:pb-72 lg:px-12"
      >
        <div
          class="-mx-4 flex flex-wrap items-center justify-center lg:space-y-0 mt-24 space-y-6"
        >
          <div class="px-4 text-center w-full md:w-8/12 xl:w-6/12">
            <h4
              class="font-bold font-serif mb-1 text-secondary-600 dark:text-secondary-200 uppercase"
            >
              Welcome to
            </h4>
            <h1 class="capitalize leading-tight mb-2 text-white">
              Vue Designer
            </h1>
            <h5 class="mb-6 text-gray-300">
              A desktop drag-and-drop editor for Mac, Windows and Linux that
              lets you visually design your Vue apps.
            </h5>
            <BaseButton
              class="!rounded-3xl px-6 py-4"
              to="https://vuedesigner.com"
              trailing
              target="_blank"
              trailing-icon="i-material-symbols-open-in-new"
              size="xl"
              label="Learn More!"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped></style>
