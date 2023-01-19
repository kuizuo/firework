<script setup lang="ts">
import { loadFireworksPreset } from 'tsparticles-preset-fireworks'

const particlesInit = async (engine: any) => {
  await loadFireworksPreset(engine)
}

const particlesLoaded = async (container: any) => {
  console.log('Happy New Year 2023', container)
}

const particlesOptions = {
  preset: 'fireworks',
}
</script>

<template>
  <div id="app">
    <Particles
      id="tsparticles"
      :particlesInit="particlesInit"
      :particlesLoaded="particlesLoaded"
      :options="particlesOptions"
    />
    <div class="box">
      <h1>{{ new Date().getFullYear() }}🎉</h1>
    </div>
  </div>
</template>
