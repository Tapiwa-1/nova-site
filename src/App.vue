<template>
  <header class="bg-white shadow">
    <!-- Top Header Section -->
    <div class="bg-gray-800 text-white">
      <div class="container mx-auto px-4 py-2">
        <div class="flex flex-col lg:flex-row items-center justify-between text-center lg:text-left space-y-2 lg:space-y-0">
          <!-- Address -->
          <div class="flex items-center space-x-2">
            <i class="fas fa-map-marker-alt"></i>
            <p class="font-medium">Mabelreign, Harare, Zimbabwe</p>
          </div>
          <!-- Social Media Links -->
          <div class="flex items-center space-x-4">
            <span class="font-medium">Follow Us On:</span>
            <a href="" target="_blank" class="hover:text-blue-500">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="" target="_blank" class="hover:text-blue-400">
              <i class="fab fa-twitter"></i>
            </a>
          </div>
        </div>
      </div>
    </div>

    <!-- Middle Header Section -->
    <div class="container mx-auto px-4 py-4">
      <div class="flex flex-col lg:flex-row items-center justify-between">
        <!-- Logo -->
        <div class="mb-4 lg:mb-0">
          <a class=" text-lg font-extrabold" href="index.html">
            NOVA
          </a>
        </div>
        <!-- Contact Info -->
        <div class="space-y-4 flex flex-col lg:flex-row items-center lg:space-x-8">
          <!-- Phone Info -->
          <div class="flex items-center space-x-2">
            <i class="fas fa-phone-alt text-primary"></i>
            <div>
              <span class="block font-medium">Call Anytime 24/7</span>
              <a href="#" class="text-blue-600 hover:underline">0777 000 000 | 0777 0000 0000</a>
            </div>
          </div>
          <!-- Email Info -->
          <div class="flex items-center space-x-2">
            <i class="fas fa-envelope text-primary"></i>
            <div>
              <span class="block font-medium">Let's talk business</span>
              <a href="mailto:admin@example.com" class="text-blue-600 hover:underline">admin@example.com</a>
            </div>
          </div>
          <!-- Address Info -->
          <div class="flex items-center space-x-2 hidden xl:flex">
            <i class="fas fa-map-marker-alt text-primary"></i>
            <div>
              <span class="block font-medium">Office Address</span>
              <div class="text-blue-600">Harare, Zimbabwe</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Header Section -->
    <div class="bg-white shadow-md sticky top-0 z-10">
      <div class="container mx-auto px-4 py-3">
        <div class="flex items-center justify-between">
          <!-- Navigation Links -->
          <nav class="hidden lg:flex space-x-8">
            <a href="index.html" class="text-gray-700 hover:text-blue-600">Home</a>
            <a href="about.html" class="text-gray-700 hover:text-blue-600">About Us</a>
            <a href="service.html" class="text-gray-700 hover:text-blue-600">Services</a>
            <a href="contact.html" class="text-gray-700 hover:text-blue-600">Contact</a>
          </nav>

          <!-- Mobile Menu Button -->
          <button class="lg:hidden text-gray-700" @click="toggleMobileMenu">
            <i class="fas fa-bars text-2xl"></i>
          </button>

          <!-- Search Form -->
          <form action="#" class="hidden lg:flex items-center space-x-2">
            <input type="text" placeholder="Search here..." class="border border-gray-300 px-2 py-1 rounded">
            <button type="submit" class="text-gray-700 hover:text-blue-600">
              <i class="far fa-search"></i>
            </button>
          </form>
        </div>

        <!-- Mobile Navigation Menu -->
        <nav v-if="mobileMenuOpen" class="lg:hidden mt-3 space-y-2">
          <a href="index.html" class="block text-gray-700 hover:text-blue-600">Home</a>
          <a href="about.html" class="block text-gray-700 hover:text-blue-600">About Us</a>
          <a href="service.html" class="block text-gray-700 hover:text-blue-600">Services</a>
          <a href="contact.html" class="block text-gray-700 hover:text-blue-600">Contact</a>
        </nav>
      </div>
    </div>
  </header>
  <section class="relative bg-cover bg-center h-screen" :style="{ backgroundImage: `url('${backgroundImage}')` }">
    <div class="absolute inset-0 bg-black opacity-50"></div>
    <div class="relative z-10 flex items-center justify-center h-full text-center text-white">
      <div>
        <h1 class="text-4xl md:text-6xl font-bold mb-4">Your Amazing Headline</h1>
        <p class="text-lg md:text-2xl mb-8">This is a subheadline or description that gives more information about your headline.</p>
        <div>
          <a href="#cta1" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-6 rounded-lg mr-4">Call to Action 1</a>
          <a href="#cta2" class="bg-transparent border-2 border-white hover:bg-white hover:text-black text-white font-bold py-2 px-6 rounded-lg">Call to Action 2</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const mobileMenuOpen = ref(false);

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};
</script>

<style scoped>
/* Add any custom styles here */
</style>
