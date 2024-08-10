<template>
    <div class="mb-6">
        <label>{{ name }}</label>
        <input v-model="model" :type="type" :class="{'!ring-red-500': message}">
        <small class="error" v-if="message">
            {{ message }}
        </small>
    </div>
</template>

<script setup>

const model = defineModel({
    type: null,
    required: true
})

defineProps({
    name: {
        type: String,
        required: true
    },
    type: {
        type: String,
        default: 'text'
    },
    message: String
})
</script>
