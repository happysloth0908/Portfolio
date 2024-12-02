<!-- App.vue -->
<template>
  <div class="portfolio-wrapper">
    <nav class="navbar navbar-expand-lg navbar-light bg-white shadow-sm fixed-top py-3">
      <div class="container">
        <a class="navbar-brand fw-bold text-primary" href="#">Portfolio</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
          <ul class="navbar-nav">
            <li v-for="item in navItems" :key="item" class="nav-item">
              <a class="nav-link px-4 fw-semibold" :href="'#' + item.toLowerCase()">{{ item }}</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <section class="hero min-vh-100 bg-gradient d-flex align-items-center">
      <div class="container">
        <div class="row justify-content-center text-center">
          <div class="col-lg-8">
            <h1 class="display-3 fw-bold mb-4">김소운</h1>
            <p class="lead mb-5">Backend Developer</p>
            <div class="social-links">
              <a v-for="social in socials" 
                 :key="social.icon" 
                 :href="social.url" 
                 class="btn btn-light btn-lg rounded-circle mx-2 shadow-sm">
                <i :class="'fab fa-' + social.icon"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="py-6">
      <div class="container">
        <h2 class="display-6 text-center mb-5">Technical Skills</h2>
        <div class="row g-4 justify-content-center">
          <div v-for="skill in skills" :key="skill.title" class="col-md-6">
            <div class="card h-100 border-0 shadow-sm hover-card">
              <div class="card-body p-4">
                <div class="d-flex justify-content-between align-items-center mb-4">
                  <h3 class="h5 fw-bold mb-0">{{ skill.title }}</h3>
                  <span class="badge bg-primary px-3 py-2 rounded-pill">{{ skill.level }}</span>
                </div>
                <ul class="list-unstyled mb-0">
                  <li v-for="item in skill.items" :key="item" class="mb-3 d-flex align-items-center">
                    <i class="fas fa-check-circle text-primary me-2"></i>
                    {{ item }}
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="projects" class="bg-light py-6">
      <div class="container">
        <h2 class="display-6 text-center mb-5">Projects</h2>
        <div class="row g-4 justify-content-center">
          <div v-for="project in projects" :key="project.title" class="col-lg-8">
            <div class="card border-0 shadow-sm h-100 hover-card">
              <div class="card-body p-4">
                <h4 class="fw-bold mb-3">{{ project.title }}</h4>
                <p class="text-muted">{{ project.period }} | {{ project.type }}</p>
                <p>{{ project.description }}</p>
                <div class="mt-4">
                  <h6 class="fw-bold mb-3">Tech Stack:</h6>
                  <div class="d-flex flex-wrap gap-2">
                    <span v-for="tech in project.technologies" 
                          :key="tech" 
                          class="badge bg-primary bg-opacity-10 text-primary px-3 py-2">
                      {{ tech }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="py-6">
      <div class="container">
        <div class="text-center">
          <h2 class="display-6 mb-4">Contact Me</h2>
          <p class="lead mb-5">새로운 기회를 기다리고 있습니다</p>
          <a href="mailto:email@example.com" class="btn btn-primary btn-lg px-5 py-3 rounded-pill">
            <i class="fas fa-envelope me-2"></i>Get In Touch
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Portfolio',
  data() {
    return {
      navItems: ['Home', 'Skills', 'Projects', 'Contact'],
      socials: [
        { icon: 'github', url: 'https://github.com/happysloth0908' },
        // { icon: 'linkedin', url: '#' },
        // { icon: 'twitter', url: '#' }
      ],
      skills: [
        {
          title: 'Backend Development',
          level: '중급',
          items: [
            'Spring Boot - REST API 개발',
            'Spring Security & JWT 인증',
            'JSP 기반 관리자 페이지'
          ]
        },
        {
          title: 'Frontend Development',
          level: '초급',
          items: [
            'Vue.js & React',
            'HTML5/CSS/JavaScript',
            'RESTful API 연동'
          ]
        },
        {
   title: 'Database',
   level: '중급',
   items: [
     'MySQL 설계 및 쿼리 작성',
     '성능 최적화',
     'ERD 설계'
   ]
 }
      ],
      projects: [
        {
          title: 'ETCO 운동 커뮤니티',
          period: '2023.10 - 2023.11',
          type: '2인 프로젝트',
          description: '비주류 스포츠 동호회를 위한 커뮤니티 플랫폼',
          technologies: ['Spring Boot', 'MySQL', 'Vue.js', 'JWT', 'WebSocket']
        }
      ]
    }
  }
}
</script>

<style>
@import 'bootstrap/dist/css/bootstrap.min.css';
@import '@fortawesome/fontawesome-free/css/all.min.css';

.portfolio-wrapper {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow-x: hidden;
}

section {
  width: 100%;
  display: flex;
  justify-content: center;
}

nav, section {
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
}

.container {
  width: 100%;
  max-width: 1140px;
  margin: 0 auto;
  padding: 0 2rem;
}

@media (min-width: 1400px) {
  nav, section {
    padding: 0 2rem;
  }
}

.bg-gradient {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
}

.hover-card {
  transition: transform 0.3s ease;
}

.hover-card:hover {
  transform: translateY(-5px);
}

.navbar .nav-link {
  position: relative;
}

.navbar .nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #0d6efd;
  transition: width 0.3s ease;
}

.navbar .nav-link:hover::after {
  width: 100%;
}

.social-links .btn {
  width: 50px;
  height: 50px;
  padding: 0;
  line-height: 50px;
  transition: all 0.3s ease;
}

.social-links .btn:hover {
  transform: translateY(-3px);
  color: #0d6efd;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
}

.py-6 {
  padding-top: 6rem;
  padding-bottom: 6rem;
}

.container {
  max-width: 1140px;
  margin: 0 auto;
  padding: 0 1rem;
}
</style>