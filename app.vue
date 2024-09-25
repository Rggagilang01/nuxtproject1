<template>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

  <div class="bg-gray-100 min-h-screen" @scroll="handleScroll">
    <!-- Hero Section -->
    <section
      class="hero bg-gradient-to-br from-teal-100 to-blue-400 text-white py-56 text-center relative overflow-hidden"
      :style="{ backgroundImage: `url(${heroBackground})`, backgroundPositionY: `${scrollY * 0.5}px` }"
    >
      <div class="absolute inset-0 bg-black opacity-50"></div> <!-- Dark overlay for better visibility -->
      <div class="container mx-auto relative z-10">
        <h2 class="text-5xl font-extrabold mb-4">Curriculum Vitae</h2>
        <p class="text-2xl italic mb-6">Information Technology | Web Developer</p>

        <!-- Scroll Down Button -->
        <button 
          @click="scrollToSection('about')" 
          class="bg-[#84cc16] text-white px-6 py-3 rounded-full mt-4 font-semibold hover:bg-[#74b615] transition duration-300"
        >
          Scroll Down
        </button>
      </div>

      <!-- Navigation Buttons moved to the top right -->
      <nav class="absolute top-8 right-8 z-20">
        <ul class="flex space-x-6">
          <li><a href="#about" class="text-lg font-bold hover:text-yellow-400">About Me</a></li>
          <li><a href="#education-skills" class="text-lg font-bold hover:text-yellow-400">Education & Skills</a></li>
          <li><a href="#hobbies" class="text-lg font-bold hover:text-yellow-400">Hobbies</a></li>
          <li><a href="#contact" class="text-lg font-bold hover:text-yellow-400">Contact</a></li>
        </ul>
      </nav>
    </section>

   <!-- About Section -->
<section id="about" class="py-16 bg-gray-100 text-gray-800 relative overflow-hidden">
  <div class="absolute inset-0 bg-[#84cc16] opacity-30"></div> <!-- Light green overlay -->
  <div class="container mx-auto text-center relative z-10">
    <h3 class="text-4xl font-bold mb-6 about-title">Hello, I'm Rangga</h3>
    <p class="text-xl mb-4">Hallo Perkenalkan Nama Saya TB Rangga Gilang Yanuari</p>
    <p class="text-lg mb-8 about-description"> Saya seorang mahasiswa berusia 19 tahun yang tinggal di Banten. Saat ini, saya sedang menempuh pendidikan di jurusan Teknologi Informasi di Program Vokasi Universitas Brawijaya (UB). Saya memiliki minat yang besar dalam dunia teknologi, khususnya dalam pengembangan web dan berbagai aspek IT modern. Saya senang belajar hal-hal baru dan selalu berusaha mengembangkan kemampuan untuk mencapai tujuan akademis dan profesional saya.</p>
    
    <!-- Add an image for visual appeal with standard size -->
    <img 
      src="@/assets/css/ranggaganteng.jpg" 
      alt="My Image" 
      class="mx-auto rounded-full shadow-lg mb-6 w-32 h-32 object-cover transition duration-300 transform hover:scale-110" 
    />
  </div>
</section>
<!-- Education & Skills Section -->
<section id="education-skills" class="py-16 bg-[#fafafa] text-gray-800">
  <div class="container mx-auto">
    <h3 class="text-4xl font-bold mb-6 text-center">Education & Skills</h3>
    
    <!-- Use a two-column grid for Education and Skills -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      
      <!-- Education Section -->
      <div class="flex flex-col">
        <h4 class="text-3xl font-semibold mb-4">Education</h4>
        <div v-for="education in educations" :key="education.school" class="bg-white p-8 rounded-lg shadow-lg transform hover:scale-105 transition duration-300 flex-grow mb-6">
          <h4 class="text-2xl font-semibold">{{ education.degree }}</h4>
          <p class="text-teal-500">{{ education.school }} | {{ education.graduationYear }}</p>
          <p class="mt-4">{{ education.description }}</p>
        </div>
      </div>

      <!-- Skills Section -->
      <div class="flex flex-col">
        <h4 class="text-3xl font-semibold mb-4">Basic Skills</h4>
        <div class="bg-white p-8 rounded-lg shadow-lg transform hover:scale-105 transition duration-300 flex-grow mb-6">
          <ul class="list-disc pl-5 mt-4 space-y-2">
            <li><i class="fab fa-html5 text-orange-600"></i> HTML & CSS</li>
            <li><i class="fab fa-js-square text-yellow-500"></i> JavaScript</li>
            <li><i class="fab fa-python text-blue-500"></i> Python</li>
            <li><i class="fas fa-database text-green-500"></i> SQL</li>
            <li><i class="fab fa-node text-green-600"></i> Node.js</li>
            <li><i class="fab fa-git text-orange-600"></i> Version Control (Git)</li>
            <li><i class="fas fa-mobile-alt text-teal-500"></i> Responsive Web Design</li>
            <li><i class="fas fa-lightbulb text-yellow-300"></i> Problem Solving</li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- Hobbies Section -->
<section id="hobbies" class="py-16 bg-gray-100 text-gray-800 relative overflow-hidden">
  <div class="absolute inset-0 bg-[#84cc16] opacity-30"></div> <!-- Light green overlay -->
  <div class="container mx-auto text-center relative z-10">
    <h3 class="text-4xl font-bold mb-6">Hobbies</h3>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
      <div class="bg-white text-black p-6 rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
        <i class="fas fa-swimmer fa-3x mb-4"></i> <!-- Ikon Renang -->
        <h4 class="text-xl font-semibold">Renang</h4>
      </div>
      <div class="bg-white text-black p-6 rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
        <i class="fas fa-paint-brush fa-3x mb-4"></i> <!-- Ikon Menggambar -->
        <h4 class="text-xl font-semibold">Menggambar</h4>
      </div>
      <div class="bg-white text-black p-6 rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
        <i class="fas fa-microphone-alt fa-3x mb-4"></i> <!-- Ikon Menyanyi -->
        <h4 class="text-xl font-semibold">Menyanyi</h4>
      </div>
      <div class="bg-white text-black p-6 rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
        <i class="fas fa-video fa-3x mb-4"></i> <!-- Ikon Editing Video -->
        <h4 class="text-xl font-semibold">Editing Video</h4>
      </div>
    </div>
  </div>
</section>

<!-- contact Me -->
<section 
  id="contact" 
  class="py-16 text-white relative overflow-hidden"
  :style="{ backgroundImage: `url(${contactBackground})` }"
>
  <div class="absolute inset-0 bg-black opacity-50"></div> <!-- Dark overlay for better visibility -->
  <div class="container mx-auto relative z-10 flex justify-between">
    <!-- Left side for contact details -->
    <div class="w-1/2">
      <h3 class="text-4xl font-bold mb-6 text-center">Contact Me</h3>
      <p class="text-lg mb-6 text-center">
        Feel free to contact me for work opportunities or collaborations. I am always open to discussing new projects, creative ideas, or opportunities to be part of your vision.
      </p>
      
      <div class="mt-6 space-y-2">
        <div class="flex items-center justify-start">
          <i class="fas fa-envelope text-2xl mr-2"></i>
          <a href="mailto:gilangyanuarirangga@gmail.com" class="text-yellow-400">gilangyanuarirangga@gmail.com</a>
        </div>
        <div class="flex items-center justify-start">
          <i class="fab fa-whatsapp text-2xl mr-2"></i>
          <a href="https://wa.me/6287789413234" class="text-yellow-400">087889413234</a>
        </div>
        <div class="flex items-center justify-start">
          <i class="fas fa-phone text-2xl mr-2"></i>
          <span class="text-yellow-400">+62-8788-9413-234</span>
        </div>
      </div>

      <div class="mt-4 space-y-2">
        <div class="flex items-center justify-start">
          <i class="fab fa-instagram text-2xl mr-2"></i>
          <a href="https://instagram.com/ranggagilang05" class="text-yellow-400">@ranggagilang05</a>
        </div>
        <div class="flex items-center justify-start">
          <i class="fab fa-facebook text-2xl mr-2"></i>
          <a href="https://facebook.com/ranggagilang" class="text-yellow-400">Rangga Gilang</a>
        </div>
        <div class="flex items-center justify-start">
          <i class="fab fa-github text-2xl mr-2"></i>
          <a href="https://github.com/Rggagilang01" class="text-yellow-400">Github</a>
        </div>
        <div class="flex items-center justify-start">
          <i class="fab fa-linkedin text-2xl"></i>
          <a href="https://www.linkedin.com/in/tubagus-rangga-gilang-yanuari-113aab288?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" class="inline-block mx-2 text-yellow-400">LinkedIn</a>
        </div>
      </div>
    </div>

    <!-- Right side for life motto as a card -->
    <div class="w-1/2 flex justify-center items-center flex-col">
      <div class="bg-white p-6 rounded-lg shadow-lg max-w-md w-full text-left">
        <p class="text-lg text-black">
          "In every challenge lies an opportunity for growth. Believe in your potential and never underestimate the power of perseverance. Keep striving for excellence, and remember that every step you take brings you closer to your dreams."
        </p>
      </div>

      <!-- Copyright Information -->
      <div class="mt-4 text-center">
        <p class="text-white">&copy; 2024 TB Rangga Gilang Yanuari. All rights reserved.</p>
      </div>
    </div>
  </div>
</section>
  </div>
</template>

<script>
export default {
  name: 'CVPage',
  data() {
    return {
      scrollY: 0,
      heroBackground: 'https://images.unsplash.com/photo-1639162147585-60019ada4361?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D', // Ganti ini dengan URL gambar hero
      contactBackground: 'https://i.pinimg.com/564x/31/bc/3a/31bc3ae4dafb837467671f581b9ea82a.jpg', // Ganti ini dengan URL gambar untuk contact section
      educations: [
        { degree: 'SD', school: 'SDN 1 Tirtayasa', graduationYear: '2017', description: 'Belajar dasar-dasar akademik dan moral di sekolah ini.' },
        { degree: 'SMP', school: 'SMPN 1 Tirtayasa', graduationYear: '2020', description: 'Mengikuti ekstrakurikuler sains dan seni.' },
        { degree: 'SMA', school: 'SMAN 2 Tirtayasa', graduationYear: '2023', description: 'Belajar ilmu-ilmu pengetahuan alam dan sosial.' },
        { degree: 'D3 Teknologi Informasi', school: 'Universitas Brawijaya', graduationYear: '-', description: '-' }
      ],
      experiences: [
        {
          title: "Senior Designer",
          company: "XYZ Company",
          years: "2020 - Present",
          description: "Led the design team in creating branding and marketing materials for large clients. Worked on web design projects and delivered high-quality UI/UX solutions."
        },
        {
          title: "Freelance Web Developer",
          company: "",
          years: "2018 - 2020",
          description: "Developed custom websites for a variety of clients, focusing on creating responsive, SEO-friendly designs with clean code using modern web development technologies."
        }
      ]
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY;
    },
    scrollToSection(sectionId) {
      document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
    }
  }
}
</script>

<style scoped>
/* Custom Styles */
.hero {
  background-size: cover;
  background-position: center;
}

.about-title {
  font-family: 'Poppins', sans-serif; /* Use a modern, clean font */
  letter-spacing: 1px; /* Slight letter spacing for better readability */
}

.about-description {
  font-family: 'Lora', serif; /* A stylish serif font for contrast */
  line-height: 1.6; /* Improved readability */
}

html {
  scroll-behavior: smooth;
}

section {
  background-size: cover;
  background-position: center;
}
</style>
