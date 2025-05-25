<template>
  <div class="min-h-screen bg-gradient-to-b from-green-50 to-green-100">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white bg-opacity-90 shadow-md z-50">
      <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
        <div class="flex items-center space-x-2">
          <img src="./assets/logo.png" alt="CoolStreet Logo" class="h-10 w-10 object-contain">
          <span class="font-bold text-xl text-green-700">CoolStreet</span>
        </div>
        
        <!-- Mobile menu button -->
        <button @click="mobileMenuOpen = !mobileMenuOpen" class="md:hidden focus:outline-none">
          <svg class="w-6 h-6 text-green-700" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
        
        <!-- Desktop navigation -->
        <div class="hidden md:flex space-x-8">
          <a href="#about" class="text-gray-600 hover:text-green-600 transition-colors">About</a>
          <a href="#benefits" class="text-gray-600 hover:text-green-600 transition-colors">Benefits</a>
          <a href="#how-it-works" class="text-gray-600 hover:text-green-600 transition-colors">How It Works</a>
          <a href="#waitlist" class="text-gray-600 hover:text-green-600 transition-colors">Join Waitlist</a>
        </div>
      </div>
      
      <!-- Mobile navigation -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-white px-4 py-2 shadow-inner">
        <div class="flex flex-col space-y-3">
          <a @click="mobileMenuOpen = false" href="#about" class="text-gray-600 py-1">About</a>
          <a @click="mobileMenuOpen = false" href="#benefits" class="text-gray-600 py-1">Benefits</a>
          <a @click="mobileMenuOpen = false" href="#how-it-works" class="text-gray-600 py-1">How It Works</a>
          <a @click="mobileMenuOpen = false" href="#waitlist" class="text-gray-600 py-1">Join Waitlist</a>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative pt-24 pb-12 md:pt-32 md:pb-16 px-4">
      <div class="max-w-6xl mx-auto">
        <div class="flex flex-col md:flex-row items-center">
          <div class="w-full md:w-1/2 mb-8 md:mb-0">
            <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-green-800 mb-4">
              Combat Urban Heat Islands with <span class="text-green-600">Natural Shade</span>
            </h1>
            <p class="text-lg text-gray-600 mb-8">
              CoolStreet designs modular green structures that bring nature back to urban spaces,
              providing shade and cooling during heatwaves.
            </p>
            <a href="#waitlist" class="inline-block bg-green-600 hover:bg-green-700 text-white font-medium py-3 px-8 rounded-full shadow-lg transition-all transform hover:scale-105">
              Join the Waitlist
            </a>
          </div>
          <div class="w-full md:w-1/2">
            <img src="./assets/hero-image.png" alt="CoolStreet green structure" class="rounded-xl shadow-xl mx-auto w-full max-w-md">
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-12 md:py-16 px-4 bg-white">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-bold text-center text-green-800 mb-10">About CoolStreet</h2>
        <div class="flex flex-col md:flex-row gap-8 items-center">
          <div class="w-full md:w-1/2">
            <img src="./assets/about-image.png" alt="CoolStreet concept" class="rounded-xl shadow-lg w-full">
          </div>
          <div class="w-full md:w-1/2">
            <p class="text-gray-700 mb-4">
              CoolStreet is developing innovative metallic structures covered with plants that can be easily 
              installed at the beginning of summer and removed at the end.
            </p>
            <p class="text-gray-700 mb-4">
              Our mission is to help cities combat rising temperatures during increasingly 
              severe heatwaves by introducing modular green spaces that provide shade and natural cooling.
            </p>
            <p class="text-gray-700">
              Currently in the design and conception phase, our product is backed by EPFL and Innovation Park, 
              with several municipalities already on our waiting list.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Benefits Section -->
    <section id="benefits" class="py-12 md:py-16 px-4 bg-green-50">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-bold text-center text-green-800 mb-10">Benefits</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-shadow">
            <div class="text-green-600 text-4xl mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z" />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-green-800 mb-2">Reduce Temperature</h3>
            <p class="text-gray-600">Lower ambient temperatures in urban areas by introducing vegetation that provides natural cooling.</p>
          </div>
          
          <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-shadow">
            <div class="text-green-600 text-4xl mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z" />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-green-800 mb-2">Seasonal Flexibility</h3>
            <p class="text-gray-600">Install when needed during summer months and remove during colder seasons for maximum flexibility.</p>
          </div>
          
          <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-shadow">
            <div class="text-green-600 text-4xl mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
              </svg>
            </div>
            <h3 class="text-xl font-semibold text-green-800 mb-2">Beautify Urban Spaces</h3>
            <p class="text-gray-600">Transform concrete city environments into green oases that enhance quality of life.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- How It Works -->
    <section id="how-it-works" class="py-12 md:py-16 px-4 bg-white">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-bold text-center text-green-800 mb-10">How It Works</h2>
        <div class="flex flex-col space-y-8">
          <div class="flex flex-col md:flex-row items-center gap-6">
            <div class="w-full md:w-1/3 flex justify-center">
              <div class="bg-green-100 rounded-full h-20 w-20 flex items-center justify-center text-2xl font-bold text-green-800">1</div>
            </div>
            <div class="w-full md:w-2/3">
              <h3 class="text-xl font-semibold text-green-700 mb-2">Design & Planning</h3>
              <p class="text-gray-600">Our team works with your city to identify heat-vulnerable areas and design customized green structures.</p>
            </div>
          </div>
          
          <div class="flex flex-col md:flex-row items-center gap-6">
            <div class="w-full md:w-1/3 flex justify-center">
              <div class="bg-green-100 rounded-full h-20 w-20 flex items-center justify-center text-2xl font-bold text-green-800">2</div>
            </div>
            <div class="w-full md:w-2/3">
              <h3 class="text-xl font-semibold text-green-700 mb-2">Installation</h3>
              <p class="text-gray-600">At the start of summer, our team installs the modular metallic structures and establishes the vegetation.</p>
            </div>
          </div>
          
          <div class="flex flex-col md:flex-row items-center gap-6">
            <div class="w-full md:w-1/3 flex justify-center">
              <div class="bg-green-100 rounded-full h-20 w-20 flex items-center justify-center text-2xl font-bold text-green-800">3</div>
            </div>
            <div class="w-full md:w-2/3">
              <h3 class="text-xl font-semibold text-green-700 mb-2">Maintenance</h3>
              <p class="text-gray-600">We maintain the plants and structures throughout the season to ensure optimal performance and appearance.</p>
            </div>
          </div>
          
          <div class="flex flex-col md:flex-row items-center gap-6">
            <div class="w-full md:w-1/3 flex justify-center">
              <div class="bg-green-100 rounded-full h-20 w-20 flex items-center justify-center text-2xl font-bold text-green-800">4</div>
            </div>
            <div class="w-full md:w-2/3">
              <h3 class="text-xl font-semibold text-green-700 mb-2">Removal & Storage</h3>
              <p class="text-gray-600">At the end of summer, we carefully dismantle the structures and store them until the next season.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Partners Section -->
    <section class="py-12 md:py-16 px-4 bg-green-50">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-bold text-center text-green-800 mb-4">Backed By</h2>
        <p class="text-center text-gray-600 mb-10">CoolStreet is supported by leading institutions</p>
        
        <div class="flex flex-wrap justify-center items-center gap-8 md:gap-16">
          <div class="w-32 md:w-40">
            <img src="./assets/epfl-logo.png" alt="EPFL" class="w-full grayscale hover:grayscale-0 transition-all">
          </div>
          <div class="w-32 md:w-40">
            <img src="./assets/innovation-park-logo.png" alt="Innovation Park" class="w-full grayscale hover:grayscale-0 transition-all">
          </div>
        </div>
      </div>
    </section>

    <!-- Waitlist Section -->
    <section id="waitlist" class="py-12 md:py-16 px-4 bg-green-700 text-white">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-bold text-center mb-4">Join the Waitlist</h2>
        <p class="text-center mb-10 max-w-2xl mx-auto">
          CoolStreet is currently in the design and conception phase. Join our waitlist to be among the first to 
          bring green cooling solutions to your city.
        </p>
        
        <form @submit.prevent="submitForm" class="max-w-md mx-auto bg-white rounded-lg p-6 shadow-xl">
          <div class="mb-4">
            <label for="name" class="block text-gray-700 text-sm font-medium mb-1">Name</label>
            <input type="text" id="name" v-model="form.name" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-green-500 text-gray-700" required>
          </div>
          
          <div class="mb-4">
            <label for="email" class="block text-gray-700 text-sm font-medium mb-1">Email</label>
            <input type="email" id="email" v-model="form.email" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-green-500 text-gray-700" required>
          </div>
          
          <div class="mb-4">
            <label for="organization" class="block text-gray-700 text-sm font-medium mb-1">Organization/City</label>
            <input type="text" id="organization" v-model="form.organization" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-green-500 text-gray-700">
          </div>
          
          <div class="mb-6">
            <label for="message" class="block text-gray-700 text-sm font-medium mb-1">Message (Optional)</label>
            <textarea id="message" v-model="form.message" rows="3" class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-green-500 text-gray-700"></textarea>
          </div>
          
          <button type="submit" class="w-full bg-green-600 hover:bg-green-800 text-white font-medium py-2 px-4 rounded-md transition-colors">
            Join Waitlist
          </button>
        </form>
        
        <div class="mt-10 text-center">
          <p>Already <span class="font-bold">3 cities</span> on our waitlist!</p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-green-900 text-white py-8 px-4">
      <div class="max-w-6xl mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="flex items-center space-x-2 mb-4 md:mb-0">
            <img src="./assets/logo-white.png" alt="CoolStreet Logo" class="h-8 w-8">
            <span class="font-bold text-xl">CoolStreet</span>
          </div>
          
          <div class="mb-4 md:mb-0">
            <div class="flex space-x-4">
              <a href="#" class="text-green-200 hover:text-white">
                <span class="sr-only">Facebook</span>
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" />
                </svg>
              </a>
              <a href="#" class="text-green-200 hover:text-white">
                <span class="sr-only">Twitter</span>
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" />
                </svg>
              </a>
              <a href="#" class="text-green-200 hover:text-white">
                <span class="sr-only">LinkedIn</span>
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                </svg>
              </a>
            </div>
          </div>
          
          <div class="text-sm text-green-200">
            © 2025 CoolStreet. All rights reserved.
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import "@/assets/main.css"
export default {
  name: 'App',
  data() {
    return {
      mobileMenuOpen: false,
      form: {
        name: '',
        email: '',
        organization: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Here you would typically send the form data to your backend
      alert('Thank you for joining our waitlist! We will contact you soon.');
      // Reset form
      this.form = {
        name: '',
        email: '',
        organization: '',
        message: ''
      };
    }
  }
}
</script>

<style>
@import 'https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css';

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>