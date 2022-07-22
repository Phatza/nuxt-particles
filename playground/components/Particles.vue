<template>
  <Particles
    id="tsparticles"
    :particlesInit="particlesInit"
    :options="particlesOptions1"
  />
</template>

<script setup>
import { loadFull } from "tsparticles";
const particlesOptions1 = {
  fullScreen: {
    zIndex: -1,
  },
  particles: {
    color: {
      value: ["#5bc0eb", "#fde74c", "#9bc53d", "#e55934", "#fa7921"],
    },
    move: {
      direction: "top",
      enable: true,
      outModes: {
        bottom: "out",
        left: "out",
        right: "out",
        top: "out",
      },
      speed: 5,
    },
    number: {
      value: 100,
    },
    opacity: {
      random: {
        enable: true,
        minimumValue: 0.4,
      },
      value: {
        min: 0.4,
        max: 0.8,
      },
      animation: {
        speed: 1,
        minimumValue: 0.1,
      },
    },
    size: {
      random: {
        enable: true,
        minimumValue: 30,
      },
      value: {
        min: 30,
        max: 100,
      },
      animation: {
        enable: true,
        speed: 100,
        minimumValue: 30,
      },
    },
  },
}
const particlesInit = async (engine) => {
  await loadFull(engine);
}
</script>
