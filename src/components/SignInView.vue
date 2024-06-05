<template>
    <div>
        <h1>
            チケカリ！
        </h1>
    </div>
    <div class="flex flex-col gap-8">
        <AtomInput id="email"/>
        <AtomInput id="password"/>
    </div>
</template>

<script setup lang="ts">
import AtomInput from './atom/AtomInput.vue';
</script>