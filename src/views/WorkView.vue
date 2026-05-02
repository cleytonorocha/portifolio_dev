<template>
    <section class="pt-5">
        <div class="row container-md px-md-5 mx-md-4 mb-5">
            <h2>Featured Works</h2>
            <project-card
                v-for="(project, index) in projects"
                :key="index"
                :project="project"
                :imagem="project.imageSrc"
                data-aos="fade-right" data-aos-duration="1200"
            />
        </div>
    </section>
</template>

<script>
export default {
    name: "WorkView",

    components: {
        ProjectCard: () => import("@/components/ProjectCard.vue"),
    },

    data() {
        return {
            projects: [
                {
                    title: "Hospital ERP System - Saúde Agora",
                    year: "2025",
                    category: "Full-Stack Java/Vue",
                    description:
                        "ERP system for hospital and clinical management. Development of medical scheduling modules, reception, electronic health records and TUSS/TISS procedure coding. Integration with RESTful APIs, JasperReports and Docker containerization.",
                    imageSrc: "img1",
                    projectLink: "https://saudeagora.com.br",
                },
                {
                    title: "Integration System - eSocial MG",
                    year: "2024-2025",
                    category: "Backend Java",
                    description:
                        "Asynchronous messaging integration platform between state and federal systems. Implementation of retry strategies, idempotency and consistency in distributed flows. Failure handling and guarantee of critical message delivery.",
                    imageSrc: "img2",
                    projectLink: "https://www.mg.gov.br",
                },
                {
                    title: "Python Automations - Brazilian Air Force",
                    year: "2023-2024",
                    category: "Automation",
                    description:
                        "Development of automations with Python and Selenium for document classification. Tools for data extraction and batch processing. Integration with internal systems for administrative process optimization.",
                    imageSrc: "img3",
                    projectLink: "#",
                },
                {
                        title: "Internal Portal GSD-LS",
                        year: "2022-2023",
                        category: "Backend Java",
                        description:
                                "Web application developed in Java with Spring Framework for the internal website of the Security and Defense Group of Lagoa Santa. Personnel control dashboards, data management and operational reports.",
                        imageSrc: "img4",
                        projectLink: "#",
                }
            ],
        };
    },
};
</script>

<style>
</style>
