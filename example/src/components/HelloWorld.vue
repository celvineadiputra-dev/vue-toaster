<script setup>
import { createToaster } from "@celvine/vue-toaster";

const toaster = createToaster({
  position: "top-right",
  duration: 4000,
});

const toast = (type = "default", dismissible = true) => {
  toaster.show("Hi! I'm a Toast", {
    dismissible,
    onClick: () => {
      console.log("clicked");
    },
  });
};
</script>

<template>
  <div>
    <button @click="toast">Click a button to show a Toast</button>
  </div>
</template>
