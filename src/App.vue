<template>
<div>paste a hash:</div>
<input v-model="hash" placeholder="hash" />
<div class='spacer' />
<Buraha v-if="hash" class="buraha" :hash="hash" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Buraha from '@/components/Buraha.vue';

const hash = ref('');
</script>

<style scoped>
input {
	width: 100%;
}
.buraha {
	display: block;
}
.spacer {
	height: 2em;
}
</style>
