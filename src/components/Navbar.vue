<script setup>
import { ref } from 'vue'

const mobileMenuActive = ref(false)


</script>

<template>
    <header class="fixed top-0 z-40 w-full flex justify-between items-center 2xl:px-80 md:px-20 bg-[#f2eee3]">
        <img src="../assets/logo/gw.png" class="md:h-48 h-24" />
        <nav class="text-[#5065a8] hidden md:flex items-center gap-x-8 text-xl font-semibold">
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Meet the Team</a>
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Venture Lab</a>
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Management Hub</a>
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Work With Us</a>
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Terms & Policies</a>
            <a class="transition duration-300 hover:scale-105 cursor-pointer">Get in Touch</a>
        </nav>

        <fa @click="mobileMenuActive = !mobileMenuActive" class="block lg:hidden text-2xl p-8 z-50"
            :icon="mobileMenuActive ? 'x' : 'bars'" :class="mobileMenuActive ? 'text-[#f2eee3]' : 'text-[#5065a8]'" />

        <Transition enter-active-class="animate__animated animate__fadeInDown"
            leave-active-class="animate__animated animate__fadeOutUp">
            <nav v-if="mobileMenuActive"
                class="bg-[#5065a8] fixed top-0 pt-24 w-full h-screen z-40 lg:hidden flex flex-col gap-y-2 items-start">

                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Meet the Team
                </button>
                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Venture Lab
                </button>
                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Management Hub
                </button>
                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Work With Us
                </button>
                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Terms & Policies
                </button>
                <button class="cursor-pointer text-white text-xl p-4 border-b border-white w-full">
                    Get in Touch
                </button>
            </nav>
        </Transition>
    </header>
</template>