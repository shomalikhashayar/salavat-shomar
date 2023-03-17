<template>
  <q-page class="q-pa-md">
    <q-btn
      @click="increment"
      color="deep-orange"
      filled
      :label="counter"
      size="xl"
      class="full-width q-mb-lg"
    />
    <div class="row">
      <div class="col text-center">
        <q-btn
          @click="decrement"
          filled
          rounded
          color="deep-orange"
          size="md"
          flat
          icon="remove"
          class="bg-orange-2"
        />
      </div>
      <div class="col text-center">
        <q-btn
          @click="reset"
          filled
          rounded
          color="deep-orange"
          size="md"
          flat
          icon="restart_alt"
          class="bg-orange-2"
        />
      </div>
      <div class="col text-center">
        <q-btn
          @click="increment"
          filled
          rounded
          color="deep-orange"
          size="md"
          flat
          icon="add"
          class="bg-orange-2"
        />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";

const counter = ref(0);

const increment = () => {
  counter.value++;
};
const decrement = () => {
  counter.value--;
};
const reset = () => {
  counter.value = 0;
};
</script>
