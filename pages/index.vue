<template>
  <div>
    <h1>{{ page.heading }}</h1>
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {

  async asyncData({$content}) {

    const page = await $content('homepage').fetch()

    return {
      page,
    }
  },

}
</script>
