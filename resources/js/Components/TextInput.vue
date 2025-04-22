<script setup>
import { onMounted, ref } from 'vue';
import InputText from "primevue/inputtext";

const model = defineModel({
    type: String,
    required: true,
});

const input = ref(null);

onMounted(() => {
    // if (input.value.hasAttribute('autofocus')) {
    //     input.value.focus();
    // }
});

defineExpose({ focus: () => input.value.focus() });
</script>

<template>
    <InputText
        v-model="model"
        ref="input"
    />
</template>
