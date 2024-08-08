<template lang="pug">
div(v-html="md")
</template>
<script setup>
// data
const route = useRoute()
const { theme } = useData()
const fileKey = `docs/${route.data.filePath}`
const templateMap = theme.value.docsTemplate

const md = computed(() => templateMap[fileKey])
// methods
// lifecycle
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped></style>
