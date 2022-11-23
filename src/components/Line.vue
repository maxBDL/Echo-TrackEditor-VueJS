<script setup>
import Button from './Button.vue';

defineProps({
    color: String
})
</script>

<template>
    <div class="flex flex-row divide-y divide-slate-200">
        <Button v-for="i in 15" :color="color"></Button>
    </div>
</template>

<style>

</style>