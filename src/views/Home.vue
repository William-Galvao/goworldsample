<script setup>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

function scrollToSection(event) {
    const id = event.target.getAttribute('href').substring(1);
    const targetSection = document.getElementById(id);

    if (targetSection) {
        event.preventDefault();

        
        const headerHeight = 120; 

        window.scrollTo({
            top: targetSection.offsetTop - headerHeight,
            behavior: 'smooth'
        });
    }
}


const itTraining = [
    'Artificial Intelligence and Machine Learning',
    'Internet Of Things',
    'Data Science and Big Data',
    'Cybersecurity',
    'Blockchain Technology',
    'Robotic Process Automation',
    'DevOps',
    'Cloud Technology'
]

const sapTraining = [
    'Financial Accounting (FI)',
    'Controlling (CO)',
    'Finance and Controlling (FICO)',
    'Logistic Execution (LE)',
    'Supplier Relationship Management (SRM)',
    'Customer Relationship Management (CRM)',
    'Human Resource (HR)',
    'Sales and Distribution (SD)',
    'Production Planning (PP)',
    'Materials Management (MM)',
    'Quality Management (QM)',
    'Human Capital Management (HCM)'
]

const businessConsultant = [
    'Vocational Training',
    'Business Development',
    'IT Consulting',
    'Cybersecurity Services',
    'Market Research',
    'Financial Advisory Services',
    'Hospitality Ventures',
    'Education Initiatives',
    'International Trade'
]


</script>

<template>
    <Navbar />
    <div class="bg-[#f2eee3] h-screen flex md:flex-row flex-col 2xl:px-80 md:px-20">

        <div
            class="md:w-1/2 h-1/3 md:h-full mt-24 md:mt-0 bg-[url('assets/images/pexels-jopwell-2422288.jpg')] bg-cover bg-center opacity-85 md:rounded-r-full animate__animated animate__fadeIn">

        </div>

        <div class="md:w-1/2 flex-1 flex flex-col gap-y-32 justify-center items-center text-[#5065a8]">
            <div class="flex flex-col text-end font-bold">
                <h1 class="md:text-7xl text-4xl animate__animated animate__fadeInDown">
                    Charting paths
                </h1>
                <h1 class="md:text-8xl text-5xl animate__animated animate__fadeInDown animate__delay-2s">
                    Shaping futures
                </h1>

                <a href="#solutions" @click.prevent="scrollToSection"
                    class="md:text-2xl  text-lg mt-16 px-8 py-4 rounded shadow-lg animate-pulse bg-[#5065a8] text-[#f2eee3] w-fit self-end flex items-center gap-x-4 cursor-pointer">
                    Explore our solutions
                    <fa icon="hand-pointer" />
                </a>
            </div>

        </div>

    </div>

    <div class="bg-[#f2eee3] h-fit flex flex-col 2xl:px-80 md:px-20" id="solutions">

        <div class="flex md:flex-row flex-col">
            <div
                class="2xl:w-1/3 md:w-1/2 bg-[#5065a8] md:rounded-r-full flex items-center 2xl:pl-20 text-[#f2eee3] gap-x-8 2xl:text-5xl md:text-4xl text-xl py-20 justify-center md:justify-start font-bold">
                <fa icon="computer" />IT <br> Training
            </div>
            <div
                class="w-2/3 flex flex-col px-10 md:items-end text-[#5065a8] md:pr-10 justify-center gap-y-4 2xl:text-2xl md:text-xl font-semibold py-10">
                <template v-for="item in itTraining">
                    <p class="flex items-center gap-x-4 transition duration-300 hover:scale-105">
                        <fa icon="circle" class="md:hidden" />
                        {{ item }}
                        <fa icon="circle" class="md:block hidden" />
                    </p>
                </template>
            </div>
        </div>

        <div class="flex md:flex-row flex-col">
            <div
                class="md:hidden 2xl:w-1/3 md:w-1/2 bg-[#5065a8] md:rounded-r-full flex items-center 2xl:pl-20 text-[#f2eee3] gap-x-8 2xl:text-5xl md:text-4xl text-xl py-20 justify-center md:justify-start font-bold">
                <fa icon="database" />SAP <br> Training
            </div>
            <div
                class="w-2/3 flex flex-col items-start text-[#5065a8] pl-10 justify-center gap-y-4 2xl:text-2xl md:text-xl font-semibold py-10">
                <template v-for="item in sapTraining">
                    <p class="flex items-center gap-x-4 transition duration-300 hover:scale-105">
                        <fa icon="circle" />{{ item }}
                    </p>
                </template>
            </div>
            <div
                class="hidden 2xl:w-1/3 md:w-1/2 bg-[#5065a8] rounded-l-full md:flex items-center justify-end  pr-20 text-[#f2eee3] gap-x-8 2xl:text-5xl md:text-4xl font-bold">
                <fa icon="database" />SAP <br> Training
            </div>
        </div>

        <div class="flex md:flex-row flex-col">
            <div
                class="2xl:w-1/3 md:w-1/2 bg-[#5065a8] md:rounded-r-full flex items-center 2xl:pl-20 text-[#f2eee3] gap-x-8 2xl:text-5xl md:text-4xl text-xl py-20 justify-center md:justify-start font-bold">
                <fa icon="user-tie" />Business <br> Consultant
            </div>
            <div
                class="w-2/3 flex flex-col px-10 md:items-end text-[#5065a8] md:pr-10 justify-center gap-y-4 2xl:text-2xl md:text-xl font-semibold py-10">
                <template v-for="item in businessConsultant">
                    <p class="flex items-center gap-x-4 transition duration-300 hover:scale-105">
                        <fa icon="circle" class="md:hidden" />
                        {{ item }}
                        <fa icon="circle" class="md:block hidden" />
                    </p>
                </template>
            </div>
        </div>



    </div>

    <div class="bg-[#f2eee3] h-screen 2xl:px-80 md:px-20">
        <div
            class="bg-[url('assets/images/pexels-monstera-production-7411982.jpg')] bg-cover bg-center w-full h-full flex flex-col gap-y-8 items-start py-20">
            <div class="flex flex-col gap-y-4 justify-center">
                <p
                    class="px-8 py-4 bg-[#5065a8] text-[#f2eee3] 2xl:text-4xl md:text-2xl text-xl font-semibold rounded-r-full transition duration-300 hover:scale-105">
                    we are</p>
                <p
                    class="px-8 py-4 bg-[#5065a8] text-[#f2eee3] 2xl:text-6xl md:text-4xl text-3xl font-bold rounded-r-full transition duration-300 hover:scale-105">
                    Go World</p>
            </div>


            <p
                class="bg-[#5065a8] text-[#f2eee3] px-8 py-8 2xl:w-1/2 md:w-2/3 w-5/6 rounded-lg 2xl:text-xl md:text-lg font-semibold transition duration-300 hover:scale-105">
                An innovative conglomerate business service operating across Canada, America, and Africa.
                <br>
                Our
                multifaceted expertise spans industries from technology to healthcare, offering bespoke consultancy,
                strategic investment guidance, and operational enhancement solutions.
                <br>
                Simultaneously, under SkillHub
                International, our vocational service division, we empower individuals with advanced training programs
                and skill development, preparing them for thriving careers in today's competitive landscape.
                <br>
                With a
                global footprint and a dedication to fostering growth, we seamlessly unite businesses and individuals,
                unlocking a realm of boundless opportunities.
            </p>


        </div>


    </div>

    <Footer />
</template>
