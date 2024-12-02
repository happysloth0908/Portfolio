<!-- App.vue -->
<template>
  <div class="min-h-screen bg-gray-100">
    <!-- Header -->
    <header class="bg-white shadow-lg">
      <div class="container mx-auto px-6 py-12">
        <h1 class="text-4xl font-bold mb-4">홍길동</h1>
        <p class="text-xl text-gray-600">Backend 개발자</p>
      </div>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto px-6 py-12">
      <!-- Skills Section -->
      <section class="mb-12">
        <h2 class="text-2xl font-bold mb-6">기술 스택</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <!-- Backend -->
          <div class="bg-white rounded-lg shadow p-6">
            <h3 class="text-xl font-bold mb-4">Backend (중)</h3>
            <ul class="list-disc pl-5 space-y-2">
              <li>Spring Boot를 활용한 REST API 구현</li>
              <li>Spring Security와 JWT 인증/인가</li>
              <li>JSP 기반 관리자 페이지 개발</li>
            </ul>
          </div>

          <!-- Frontend -->
          <div class="bg-white rounded-lg shadow p-6">
            <h3 class="text-xl font-bold mb-4">Frontend (하)</h3>
            <ul class="list-disc pl-5 space-y-2">
              <li>Vue.js 기반 반응형 웹 개발</li>
              <li>Node.js/npm 개발 환경 구성</li>
              <li>HTML5/CSS/JavaScript</li>
              <li>axios API 연동</li>
            </ul>
          </div>

          <!-- Database -->
          <div class="bg-white rounded-lg shadow p-6">
            <h3 class="text-xl font-bold mb-4">Database (중)</h3>
            <ul class="list-disc pl-5 space-y-2">
              <li>MySQL 데이터베이스 설계</li>
              <li>MyBatis 데이터 처리</li>
            </ul>
          </div>

          <!-- Tools -->
          <div class="bg-white rounded-lg shadow p-6">
            <h3 class="text-xl font-bold mb-4">Development Tools (중)</h3>
            <ul class="list-disc pl-5 space-y-2">
              <li>Figma - 와이어프레임 설계</li>
              <li>Git - 버전 관리</li>
            </ul>
          </div>
        </div>
      </section>

      <!-- Project Section -->
      <section>
        <h2 class="text-2xl font-bold mb-6">프로젝트</h2>
        <div class="bg-white rounded-lg shadow p-6">
          <div class="mb-6">
            <h3 class="text-xl font-bold">ETCO 운동 커뮤니티 웹 사이트</h3>
            <p class="text-gray-600">2023.10.23 ~ 2023.11.27 (2인 프로젝트)</p>
          </div>

          <div class="mb-6">
            <h4 class="font-bold mb-2">프로젝트 개요</h4>
            <p>비주류 스포츠를 즐기는 사람들을 위한 커뮤니티 플랫폼 개발. 관리자 페이지를 별도 구현하여 효율적인 커뮤니티 관리 시스템 구축</p>
          </div>

          <div class="mb-6">
            <h4 class="font-bold mb-2">주요 기능 구현</h4>
            <ul class="list-disc pl-5 space-y-2">
              <li>Spring Security/JWT 기반 인증 시스템</li>
              <li>게시판 CRUD 및 댓글 기능</li>
              <li>계층형 카테고리 사이드바</li>
              <li>JSP 기반 관리자 페이지</li>
              <li>ChatGPT API 연동 챗봇</li>
            </ul>
          </div>

          <div>
            <h4 class="font-bold mb-2">성과 및 배운점</h4>
            <ul class="list-disc pl-5 space-y-2">
              <li>체계적인 초기 설계의 중요성 인식</li>
              <li>팀 협업 시 명확한 의사소통과 코드 리뷰의 중요성 체득</li>
              <li>Git을 통한 효율적인 버전 관리 경험</li>
            </ul>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'Portfolio'
}
</script>