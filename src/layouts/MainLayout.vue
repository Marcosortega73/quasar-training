<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <NavBar />
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
    <q-dialog-wrapper>
      <DialogLogin />
    </q-dialog-wrapper>
  </q-layout>
</template>

<script setup>
import NavBar from "./components/NavBar.vue";
import DialogLogin from "../components/DialogLogin.vue";
import { defineComponent, ref } from "vue";

const leftDrawerOpen = ref(false);

const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};
</script>
