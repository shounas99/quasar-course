<template>
  <q-page class="flex column q-pa-md">
    <span class="text-h1">Headline 1</span>
    <span class="text-h2">Headline 2</span>
    <span class="text-h3">Headline 3</span>
    <span class="text-h4">Headline 4</span>
    <span class="text-h5">Headline 5</span>
    <span class="text-h6">Headline 6</span>

    <q-separator />

    <span class="text-subtitle1">Subtitle 1</span>
    <span class="text-subtitle2">Subtitle 2</span>

    <p class="text-body1">
      Laboris id minim incididunt deserunt ullamco reprehenderit officia mollit
      dolore eiusmod. Consequat est sunt consectetur ut qui dolor. Id amet
      deserunt esse nostrud velit. Sunt amet aliqua adipisicing nostrud qui
      tempor laborum. Magna ad aute id exercitation nulla ut et sunt sit
      reprehenderit velit.
    </p>
    <p class="text-body2">
      Laboris id minim incididunt deserunt ullamco reprehenderit officia mollit
      dolore eiusmod. Consequat est sunt consectetur ut qui dolor. Id amet
      deserunt esse nostrud velit. Sunt amet aliqua adipisicing nostrud qui
      tempor laborum. Magna ad aute id exercitation nulla ut et sunt sit
      reprehenderit velit.
    </p>

    <q-separator />
    <span class="text-weight-thin"
      >Commodo exercitation cillum eu Lorem aliqua consequat sunt.</span
    >
    <span class="text-weight-light"
      >Do adipisicing dolore sint do deserunt do qui.</span
    >
    <span class="text-weight-regular"
      >Proident magna Lorem labore eu eiusmod ullamco laboris esse ullamco
      magna.</span
    >
    <span class="text-weight-medium"
      >Mollit laboris non ipsum aliquip dolore quis consectetur enim ex
      culpa.</span
    >
    <span class="text-weight-bold"
      >Cillum quis aute deserunt velit id anim eu laboris et.</span
    >
    <span class="text-weight-bolder">Anim sunt esse deserunt mollit sint.</span>

    <q-btn color="primary" label="Abrir menù lateral" class="q-mt-md"> </q-btn>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "TipographyPage",
});
</script>
