<template>
  <div ref="target">
    <div>Hello world unplugin-vue-router</div>
    <RouterLink to="/about">About</RouterLink>
    <RouterLink to="/">Home</RouterLink>
    <div>{{ msg }}</div>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
    <p>x: {{ x }}</p>
    <p>y: {{ y }}</p>
    <p>isOutside: {{ isOutside }}</p>
    <HelloWorld></HelloWorld>
    <UserComponent></UserComponent>
  </div>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
const msg = ref('Hello unplugin-auto-import')
const target = useTemplateRef('target')

const { x, y, isOutside } = useMouseInElement(target)
</script>

<style scoped></style>
