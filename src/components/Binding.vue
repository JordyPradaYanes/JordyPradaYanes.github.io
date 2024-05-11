<script setup>

import { ref } from "vue";
const val = ref(false);

const items = ["Opcion 1", "Opcion 2"];
const colores = { "Opcion 1": "bg-red-500", "Opcion 2": "bg-green-500"}

</script>

<template>
    <ul v-show="val" class="absolute top-0 -translate-y-full">
        <li v-for="(item, index) in items">
            <button class="flex justify-center items-center size-10 rounded-full text-white" :class=colores[item]
                @click="val = !val">
            </button>
        </li>
    </ul>
    <button class="flex justify-center items-center size-10 rounded-full bg-red-500 text-white" @click="val = !val">
    </button>
</template>