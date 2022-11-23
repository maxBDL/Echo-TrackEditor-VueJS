<script setup>
import { ref } from 'vue';

defineProps({
    color: String
});

const state = ref(false);

</script>

<template>
    <div @click="state = !state" class="button">
        <div v-if="state" class="note" :class="color"></div>
    </div>
</template>

<style>
.button {
    width: 50px;
    height: 50px;
    margin: 5px;
}

.note {
    z-index: 1;
    position: absolute;
    width: 20%;
    display: inline-block;
    padding-bottom: 20%;
    border-radius: 50%;
    cursor: pointer;
    width: 50px;
    height: 50px;

}

.note:after {
    content: "";
    position: absolute;
    display: block;
    border-radius: 50%;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: white;
    z-index: 1;
    background: radial-gradient(ellipse at top,
            rgba(0, 0, 0, 0) 40%,
            rgba(0, 0, 0, .2) 60%,
            rgba(0, 0, 0, .6) 95%,
            rgba(0, 0, 0, 1) 100%);
}

.color_blue {
    background-color: blue;
}


.color_yellow {
    background-color: yellow;
}

.color_red {
    background-color: red;
}

.color_green {
    background-color: green;
}
</style>