<template>
  <section class="pt-5">
    <div class="row container-md px-md-5 mx-md-4 mb-5">
      <h2>Skills</h2>
    </div>
    <div>
      <hr class="d-block d-md-none" />
      <experience-card
        :title="google.title"
        :diretory="google.diretory"
        :images="google.images"
        :textPosition="'right'"
        :heading="google.heading"
        :experience="google.experience"
        :description="google.description"
        data-aos="fade-left" data-aos-duration="1200"
      />
      <hr class="d-block d-md-none" />
      <experience-card
        :title="office.title"
        :diretory="office.diretory"
        :images="office.images"
        :textPosition="'left'"
        :heading="office.heading"
        :experience="office.experience"
        :description="office.description"
        :icon_size="office.icon_size"
        :disposition="office.disposition"
        data-aos="fade-right" data-aos-duration="1200"
      />
    </div>
    <hr class="d-block d-md-none" />
    <experience-card
      :title="frontend.title"
      :diretory="frontend.diretory"
      :images="frontend.images"
      :textPosition="'left'"
      :heading="frontend.heading"
      :experience="frontend.experience"
      :description="frontend.description"
      data-aos="fade-right" data-aos-duration="1200"
    />
    <hr class="d-block d-md-none" />
    <experience-card
      :title="development.title"
      :diretory="development.diretory"
      :images="development.images"
      :textPosition="'right'"
      :heading="development.heading"
      :experience="development.experience"
      :description="development.description"
      data-aos="fade-left" data-aos-duration="1200"
    />
  </section>
</template>

<script>
export default {
  name: "SkillsView",

  data() {
    return {
      google: {
        title: "Backend",
        diretory: "development",
        images: ["java", "spring", "quarkus"],
        heading: "Backend Development",
        experience: "3+ year of experience",
        description:
          "Specialized in Java enterprise applications using Spring Framework and Quarkus. Proficient in designing RESTful APIs with Swagger documentation, implementing business logic, and building high-performance, cloud-native services. Expert in dependency injection, transaction management, and microservices architecture.",
      },
      office: {
        title: "Database & ORM",
        diretory: "development",
        images: ["mysql", "postgresql", "mongodb"],
        heading: "Database Technologies",
        experience: "3+ year of experience",
        description:
          "Experienced with relational databases (MySQL, PostgreSQL) and NoSQL solutions (MongoDB). Proficient in Hibernate ORM for object-relational mapping, JPA specifications, and database design patterns. Skilled in query optimization, transaction management, and data persistence layers.",
        icon_size: "68",
        disposition: "between",
      },
      frontend: {
        title: "Frontend",
        diretory: "development",
        images: ["javascript", "typescript", "vue", "html", "css", "bootstrap"],
        heading: "Frontend Development",
        experience: "3+ year of experience",
        description:
          "Experienced with modern frontend technologies including JavaScript, TypeScript, and Vue.js. Proficient in building responsive user interfaces with HTML5, CSS3, and Bootstrap. Familiar with Angular framework and capable of creating dynamic, interactive web applications with component-based architecture.",
      },
        development: {
            title: "Tools & Practices",
            diretory: "development",
            images: ["git", "docker", "linux"],
            heading: "DevOps & Quality",
            experience: "3+ year of experience",
            description:
            "Proficient in version control with Git, containerization with Docker, and CI/CD practices. Experienced in JUnit 5 testing, design patterns (SOLID, Gang of Four), and code quality standards. Familiar with Swagger for API documentation, Jira for agile project management, and Linux environment management.",
        },
    };
  },

  components: {
    ExperienceCard: () => import("@/components/ExperienceCard.vue"),
  },
};
</script>

<style>
</style>
