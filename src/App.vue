<script setup>
import HelloWorld from './components/HelloWorld.vue'
import {ipcRenderer} from "electron";
import {onMounted, ref} from "vue";
const data = ref('');
onMounted(() => {
  ipcRenderer.on('update_already', function (){
    data.value = 'update_already';
  });
})
</script>

<template>
  4444
  {{ data }}
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
