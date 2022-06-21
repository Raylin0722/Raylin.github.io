<script setup>
import Typing from "../components/Typing.vue";
import Project from "../components/Project.vue";

const Projects = [
    {
        title : "AAAA",
        d : "AAA",
        i : "https://i.imgur.com/7Je16BU.jpg"
    },
    {
        title : "BBBB",
        d : "BBB",
        i : "https://i.imgur.com/7Je16BU.jpg"
    },
    {
        title : "CCCC",
        d : "CCC",
        i : "https://i.imgur.com/7Je16BU.jpg"
    },

];

</script>
<template>
    <div class="h-full w-full px-8 pt-16 sm:px-12 sm:pt-20 lg:px-16 lg:pt-24">
        <Typing text="My Projects" class="block text-2xl sm:text-3xl lg:text-4xl" />
        <div class="py-2">
            <Project
                v-for="i in Projects"
                :key="i"
                :name="i.title"
                :description="i.d"
                :image="i.i"
                class="my-2 w-full rounded-md bg-white bg-opacity-50 p-4 shadow-md shadow-indigo-200"
            >
            </Project>
        </div>
    </div>
</template>
