<script setup>
import ImageGallery from "../components/common/ImageGallery.vue";
import MainHeading from "../components/common/MainHeading.vue";
import MinorHeading from "../components/common/MinorHeading.vue";
import PrevNextNav from "../components/common/PrevNextNav.vue";
import SideImage from "../components/common/SideImage.vue";

const prevNextNavData = {
    prevHref: "/glossary",
    prevLabel: "Glossary",
    nextHref: "/",
    nextLabel: "Home",
};

const cpuLinks = [
    {
        url: "https://en.wikipedia.org/wiki/Microprocessor_chronology",
        title: "Microprocessor Chronology",
        website: "wikipedia.org",
        description:
            "A timeline of microprocessors from the 70s to modern day.",
    },
    {
        url: "https://embeddedprep.com/popular-cpu-architectures-in-2025/",
        title: "Popular CPU Architectures in 2026",
        website: "embeddedprop.com",
        description:
            "An overview of common CPU architectures and the ways they can differ.",
    },
    {
        url: "https://codefinity.com/blog/Assembler-Programming",
        title: "Assembler Programming",
        website: "codefinity.com",
        description: "An introduction to assembly language concepts.",
    },
    {
        url: "https://www.baeldung.com/cs/fetch-execute-cycle",
        title: "Introduction to the Fetch-Execute Cycle",
        website: "baeldung.com",
        description: "An alternative overview of the fetch-execute cycle.",
    },
];
</script>

<template>
    <section class="section wrapper">
        <PrevNextNav :data="prevNextNavData" />

        <MainHeading>Resource Links</MainHeading>

        <MinorHeading id="cpu">CPU</MinorHeading>

        <ul class="list">
            <li v-for="(item, index) in cpuLinks" :key="index">
                <a :href="item.url" class="link" target="_blank">{{
                    item.title
                }}</a>
                - <b>{{ item.website }}</b
                ><br />
                {{ item.description }}
            </li>
        </ul>

        <PrevNextNav :data="prevNextNavData" />
    </section>
</template>

<style scoped></style>
