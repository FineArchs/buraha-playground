<template>
<canvas ref="canvas" />
</template>

<script lang="ts" setup>
import { render } from 'buraha';
import { shallowRef, watch } from 'vue';

const props = defineProps<{
	hash: string;
}>();
const canvas = shallowRef<HTMLCanvasElement>();

watch([canvas, () => props.hash], () => canvas.value && render(props.hash, canvas.value));
</script>
