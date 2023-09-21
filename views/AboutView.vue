<template>
  <div>
    <div class="header">
      <h1>My Portfolio</h1>
    </div>
    <div class="container">
      <div class="section">
        <h2>Work Experience</h2>
        <ul>
          <li v-for="experience in workExperience" :key="experience.id">
            <h3>{{ experience.position }}</h3>
            <p>{{ experience.description }}</p>
          </li>
        </ul>
      </div>
      <div class="section">
        <h2>Education</h2>
        <ul>
          <li v-for="education in educationHistory" :key="education.id">
            <h3>{{ education.degree }}</h3>
            <p>{{ education.university }}</p>
            <p>{{ education.date }}</p>
            <p>{{ education.description }}</p>
          </li>
        </ul>
      </div>
      <div class="section">
        <h2>Sports</h2>
        <ul>
          <li v-for="sport in sports" :key="sport.id">
            <h3>{{ sport.name }}</h3>
            <p>{{ sport.description }}</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      workExperience: [
        {
          id: 1,
          position: 'Fresher',
          description: 'Designed and managed websites using updated technologies.',
        },
      ],
      educationHistory: [
        {
          id: 1,
          degree: 'Bachelor of Information Technology',
          university: 'Deakin University',
          date: '2023 - 2026',
          description: 'I am learning about computer programming and focusing on creating software programs.',
        },
      ],
      sports: [
        {
          id: 1,
          name: 'Cricket',
          description: 'Cricket is one of the most followed game in the world.',
        },
      ],
    };
  },
};
</script>

<style scoped>
/* CSS for Sections */
.section {
  margin: 20px 0;
  background-color: #fff;
  border-radius: 5px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.section h2 {
  font-family: 'Pacifico', cursive;
  color: #333;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 20px 0;
  padding: 10px;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 5px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

li h3 {
  font-family: 'Roboto', sans-serif;
  color: #333;
}

/* Additional Styling for Education and Sports Sections */
.education-section,
.sports-section {
  background-color: #f0f0f0;
}

/* Responsiveness */
@media (max-width: 768px) {
  .section {
    padding: 10px;
    margin: 10px 0;
  }
  li {
    padding: 5px;
    margin: 10px 0;
  }
}
</style>
