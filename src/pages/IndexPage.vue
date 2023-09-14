<template>
  <q-page class="q-pa-md">
    <q-btn class="full-width q-py-xl" size="32px" @click="updateCounter(1)" color="grey-7" outline :label="counter" />
    <div class="row q-gutter-x-md items-center justify-center q-mt-xl">
      <q-btn @click="reset" outline rounded color="negative" size="md" icon="restart_alt" />
      <q-btn @click="updateCounter(1)" filled unelevated rounded color="green" size="md" icon="add" />
    </div>
  </q-page>
</template>

<script setup>
import { ref } from "vue";
import { useQuasar } from 'quasar'

const $q = useQuasar()

const counter = ref(0);

const updateCounter = (value) => {
  counter.value += value;
  $q.notify({
    message: 'ایشالا اجرت با بی بی رقیه',
    color: 'green',
    position: 'center',
  })

}

const reset = () => {
  counter.value = 0;
};

</script>
