<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import SmartContract from './components/SmartContract.vue' 
// import {GridProps} from "naive-ui"
import { onMounted } from 'vue'

onMounted(() => {
  setTimeout(() => {
    const script = document.createElement('script')
    script.src = '/onboarding_prettismart.js'
    script.onload = () => console.log('✅ onboarding script loaded')
    script.onerror = (e) => console.error('❌ failed to load script', e)
    document.body.appendChild(script)
  }, 1000)
})
</script>

<template>
  <SmartContract />
  <!-- <hello-world/> -->
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 0px;
}
</style>
