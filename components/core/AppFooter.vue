<template>
  <v-footer
    id="core-footer"
    absolute
    height="82"
  >
    <div class="footer-items">
      <span
        v-for="link in links"
        :key="link.name"
      >
        <a
          :href="link.Link"
          class="tertiary--text footer-links">{{ link.name }}</a>
      </span>
    </div>
    <v-spacer/>
    <span class="font-weight-light copyright">
      &copy;
      {{ (new Date()).getFullYear() }}
      <a
        href="https://www.creative-tim.com/"
        target="_blank">Htin Lynn</a>, made with
      <v-icon
        color="tertiary"
        size="17">mdi-heart</v-icon>
      for a better web
    </span>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    links: [
      { name: 'Dashboard', Link: '/dashboard' },
      { name: 'Htin Lynn', Link: 'https://mghtinlynn.github.io/HtinLynn/' }
    ]
  })
}
</script>

<style>
#core-footer {
  z-index: 0;
}
</style>
