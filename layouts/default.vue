<template>
  <div>
    <TheHeader />
    <main
      class="lg:block relative pt-16 lg:pt-24 bg-light-elevatedSurface dark:bg-dark-elevatedSurface transition-colors duration-300 ease-linear"
    >
      <Nuxt />
    </main>
    <TheFooter />
    <TheMobileBottomNav />
  </div>
</template>

<script>
export default {
  head() {
    const i18nSeo = this.$nuxtI18nSeo()

    // let canonical = `https://nuxtjs.org${this.$route.path}`
    // if (this.$store.state.locale !== 'en') {
    //   canonical = `https://${this.$store.state.locale}.nuxtjs.org${this.$route.path}`
    // }
    // const link = [
    //   { rel: 'canonical', href: canonical },
    //   { rel: 'alternate', hreflang: 'en', href: `https://nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'zh', href: `https://zh.nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'ru', href: `https://ru.nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'ja', href: `https://ja.nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'ko', href: `https://ko.nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'fr', href: `https://fr.nuxtjs.org${this.$route.path}` },
    //   { rel: 'alternate', hreflang: 'id', href: `https://id.nuxtjs.org${this.$route.path}` }
    // ]
    // link.forEach((l) => {
    //   if (l.href.slice(-1) !== '/') {
    //     l.href = l.href + '/'
    //   }
    // })
    return {
      // htmlAttrs: { lang: this.$store.state.locale },
      // link,
      meta: [
        // Open Graph
        {
          hid: 'og:title',
          property: 'og:title',
          content: this.$i18n.t('homepage.meta.title')
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: this.$i18n.t('homepage.meta.description')
        },
        {
          hid: 'twitter:title',
          name: 'twitter:title',
          content: this.$i18n.t('homepage.meta.title')
        },
        {
          hid: 'twitter:description',
          name: 'twitter:description',
          content: this.$i18n.t('homepage.meta.description')
        }
      ],
      ...i18nSeo
    }
  }
}
</script>
