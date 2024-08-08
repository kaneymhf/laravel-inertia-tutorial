<template>
    <Head title="Register" />

    <h1 class="title">Register a new account</h1>

    <div class="w-2/4 mx-auto">

        <form @submit.prevent="submit">

            <div class="mb-6">
                <label>Name</label>
                <input v-model="form.name" type="text">
            </div>
            <div class="mb-6">
                <label>Email</label>
                <input v-model="form.email" type="text">
            </div>
            <div class="mb-6">
                <label>Password</label>
                <input v-model="form.password" type="password">
            </div>
            <div class="mb-6">
                <label>Confirm Password</label>
                <input v-model="form.password_confirmation" type="password">
            </div>

            <div>
                <p class="text-slate-600 mb-2">
                    Already a user? <a href="#" class="text-link">Login</a>
                </p>
                <button class="primary-btn">Register</button>
            </div>

        </form>

    </div>
</template>

<script setup>
import { reactive } from 'vue';


const form = reactive({
    name: null,
    email: null,
    password: null,
    password_confirmation: null,
})

const submit = () => {
    console.log("submit")
}

</script>
