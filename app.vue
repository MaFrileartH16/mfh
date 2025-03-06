<template>
  <UContainer class="bg-white text-gray-900">
    <!-- Header -->
    <UHeader class="shadow-md bg-navy text-white">
      <div class="flex justify-between items-center p-4 max-w-6xl mx-auto">
        <h1 class="text-2xl font-bold">My Portfolio</h1>
        <div class="flex gap-4">
          <UButton as="a" href="#about" class="btn-lime">About</UButton>
          <UButton as="a" href="#projects" class="btn-lime">Projects</UButton>
          <UButton as="a" href="#contact" class="btn-lime">Contact</UButton>
        </div>
      </div>
    </UHeader>

    <!-- Hero Section -->
    <USection id="hero" class="min-h-screen flex flex-col justify-center items-center bg-navy text-center text-white">
      <h2 class="text-4xl font-bold">Hi, I'm Muhammad Fauzul Hanif</h2>
      <p class="text-lg mt-2 text-lime">Fullstack Developer | React.js & Laravel</p>
    </USection>

    <!-- About Section -->
    <USection id="about" class="min-h-screen flex flex-col justify-center items-center text-center bg-white px-6">
      <h2 class="text-3xl font-bold text-navy">About Me</h2>
      <p class="mt-4 max-w-2xl text-gray-700 leading-relaxed">
        I’m <span class="font-semibold text-navy">Muhammad Fauzul Hanif</span>, a
        <span class="font-semibold text-navy">third-year Informatics Engineering student</span>
        at Universitas Muhammadiyah Sukabumi.
        Passionate about <span class="text-lime">Fullstack Development</span>, I specialize in
        <span class="text-lime">React.js</span> and <span class="text-lime">Laravel</span> to build modern and scalable web applications.
      </p>
      <p class="mt-4 max-w-2xl text-gray-700 leading-relaxed">
        I enjoy solving real-world problems through software development and have worked on several projects,
        including web applications for e-commerce, portfolio websites, and backend API services.
      </p>
      <p class="mt-4 max-w-2xl text-gray-700 leading-relaxed">
        Currently, I am expanding my skills in cloud computing and DevOps, aiming to become a well-rounded software engineer.
        Let’s connect and collaborate on innovative projects! 🚀
      </p>
    </USection>


    <!-- Projects Section -->
    <USection id="projects" class="min-h-screen flex flex-col justify-center items-center bg-lime-light">
      <h2 class="text-3xl font-bold text-navy">Projects</h2>
      <UGrid :cols="3" class="mt-6">
        <UCard v-for="n in 3" :key="n" class="bg-white border border-gray-200 shadow-sm">
          <template #header>
            <h3 class="text-xl font-semibold text-navy">Project {{ n }}</h3>
          </template>
          <p class="text-gray-700">A short description of the project.</p>
        </UCard>
      </UGrid>
    </USection>

    <!-- Contact Section -->
    <USection id="contact" class="min-h-screen flex flex-col justify-center items-center text-center bg-white">
      <h2 class="text-3xl font-bold text-navy">Contact Me</h2>
      <p class="mt-4 text-gray-700">
        Feel free to reach out via email: <span class="font-semibold text-lime">your.email@example.com</span>
      </p>
    </USection>
  </UContainer>
</template>

<style scoped>
/* Warna utama */
.bg-navy {
  background-color: #000080;
}
.text-navy {
  color: #000080;
}
.text-lime {
  color: #BFFF00;
}
.bg-lime-light {
  background-color: #F0FFD0;
}

/* Button Style */
.btn-lime {
  background-color: #BFFF00;
  color: #000080;
  font-weight: bold;
  padding: 8px 16px;
  border-radius: 6px;
  transition: background 0.3s;
}
.btn-lime:hover {
  background-color: #A0E600;
}
</style>
