<template>
  <q-page>
    <div class="row q-mb-md">
      <div class="col bg-primary"></div>
      <div class="col bg-secondary"></div>
      <div class="col bg-accent"></div>
    </div>

    <div class="row q-mb-md">
      <!--El row solo tiene 12 posiciones-->
      <div class="col bg-primary"></div>
      <div class="col-5 bg-secondary"></div>
      <div class="col-6 bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-center">
      <div class="col-4 bg-secondary"></div>
      <div class="col-4 bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="col-4 bg-secondary"></div>
      <div class="col-4 bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="col-4 bg-secondary"></div>
      <div class="col-4 bg-accent"></div>
    </div>

    <q-separator spaced></q-separator>

    <div class="row q-mb-md justify-between">
      <div class="col-12 col-md-4 col-sm-5 bg-secondary"></div>
      <div class="col-12 col-md-4 col-sm-5 bg-accent"></div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row q-mb-md justify-around">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column q-mb-md items-center bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column q-mb-md items-end bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div
      class="column custom-height q-mb-md items-center justify-center bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div
      class="column custom-height q-mb-md items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div
      class="column custom-height q-mb-md items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary"></div>
      <div class="square-box self-start bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "FlexPage",
});
</script>

<style scoped>
.col,
.col-4,
.col-6,
.col-12 {
  height: 50px;
}

.square-box {
  height: 50px;
  width: 50px;
}

.custom-height {
  height: 300px;
}
</style>
