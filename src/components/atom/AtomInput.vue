<template>
<input
	v-model="modelValue"
	@blur="onBlur"
	class="base-input"
/>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const modelValue = defineModel<string | number>({default: ''})
defineProps<{
    id: string;
    error?: string
}>()

const inputEl = ref<HTMLInputElement>()

const onBlur = () => {
	if (!inputEl.value) return
	inputEl.value.value = modelValue.value.toString()
}
</script>

<style scoped>
.base-input {
	@apply h-12 w-full appearance-none rounded border border-slate-900
}
</style>

