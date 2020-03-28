<template>
    <p class="copyright">{{ copyright }}</p>
</template>

<script>
export default {
  data () {
    return {
      copyright: 'ⒸAnime Movbay'
    }
  },
  year () {
    var d = new Date()
    d.getFullYear()
  }
}

</script>

<style>
    .copyright
    {
        font-style: italic;
        font-size: 10px;
    }
</style>
