

<template>
  <button @click="addVideo">UPLOAD VIDEO</button>
</template>

<script lang="ts" setup>
import {FilePicker} from "@capawesome/capacitor-file-picker";

async function addVideo() {
  try {
    console.log("SUCCESS: ", (await FilePicker.pickVideos({skipTranscoding: true})).files)
  } catch (e) {
    console.log("ERR: ", e)
  }
}
</script>
