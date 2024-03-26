<script setup>
import { ref } from 'vue'
import Button from 'primevue/button';
import Card from 'primevue/card';
import Calendar from 'primevue/calendar';
const buttondisplay = ref();
const icondisplay = ref();
</script>

<template>
  <main class="my-0 mx-auto max-w-3xl text-center">
    <h2 class="p-6 text-4xl">Hello</h2>

    <p class="px-10 pb-10 text-left">
    <div class="card flex items-center justify-center">
      <Card style="width: 25em">
        <template #title> Simple Card </template>
        <template #content>
          <p class="m-0">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore sed consequuntur error repudiandae
            numquam
            deserunt quisquam repellat libero asperiores earum nam nobis, culpa ratione quam perferendis esse,
            cupiditate
            neque
            quas!
          </p>
        </template>
      </Card>
    </div>
    </p>
    <div class="card flex justify-center flex-wrap gap-3">
      <Button label="Primary" />
      <Button label="Secondary" severity="secondary" />
      <Button label="Success" severity="success" />
      <Button label="Info" severity="info" />
      <Button label="Warning" severity="warning" />
      <Button label="Help" severity="help" />
      <Button label="Danger" severity="danger" />
    </div>
    <div class="card flex flex-wrap gap-4 p-fluid">
      <div>
        <label for="buttondisplay" class="font-bold block mt-2"> Button Display </label>
        <Calendar v-model="buttondisplay" showIcon inputId="buttondisplay" />
      </div>
      <div>
        <label for="icondisplay" class="font-bold block mt-2"> Icon Display </label>
        <Calendar v-model="icondisplay" showIcon iconDisplay="input" inputId="icondisplay" />
      </div>
    </div>
  </main>

</template>