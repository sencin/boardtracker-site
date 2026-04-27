<script setup lang="ts">
const features = [
  { title: "Tenants", desc: "Manage tenant records easily" },
  { title: "Rooms", desc: "Track occupancy & availability" },
  { title: "Assignments", desc: "Auto rent computation" },
  { title: "Payments", desc: "Monitor rent payments" },
  { title: "Expenses", desc: "Track bills & utilities" },
  { title: "Inventory", desc: "Manage room items" },
];
</script>

<template>
  <div class="bg-white dark:bg-gray-950 text-gray-900 dark:text-gray-100 transition-colors">

    <!-- NAVBAR -->
    <nav class="sticky top-0 z-50 backdrop-blur bg-white/70 dark:bg-gray-900/70 border-b border-gray-200 dark:border-gray-800">
      <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
        <h1 class="font-bold text-lg">BoardTracker</h1>

        <a href="/downloads/boardtracker.apk"
           class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition">
          Download
        </a>
      </div>
    </nav>

    <!-- HERO -->
    <section class="relative overflow-hidden">
      <!-- gradient background -->
      <div class="absolute inset-0 bg-gradient-to-br from-blue-600 to-blue-800 opacity-90"></div>

      <!-- glow -->
      <div class="absolute -top-40 -left-40 w-[400px] h-[400px] bg-blue-400 rounded-full blur-3xl opacity-30"></div>

      <div class="relative max-w-6xl mx-auto px-6 py-24 grid md:grid-cols-2 gap-12 items-center text-white">

        <!-- TEXT -->
        <div>
          <h1 class="text-4xl md:text-5xl font-bold leading-tight">
            Smart Boarding House
            <br />
            <span class="text-blue-200">Management System</span>
          </h1>

          <p class="mt-5 text-blue-100">
            Simplify tenant tracking, room assignments, inventory, and payments — all in one powerful app.
          </p>

          <div class="mt-8 flex items-center gap-4 flex-wrap">
            <a href="/downloads/boardtracker.apk"
               class="bg-white text-blue-700 px-6 py-3 rounded-xl font-semibold shadow hover:bg-gray-100 transition">
              Download APK
            </a>

            <span class="text-sm text-blue-200">
              Free • Offline-first • Fast
            </span>
          </div>
        </div>

        <!-- PHONE MOCKUP -->
        <div class="flex justify-center">
          <div class="bg-black rounded-[2.5rem] p-2 shadow-2xl">
            <img src="/screens/dashboard.png"
                 class="w-72 rounded-[2rem]" />
          </div>
        </div>

      </div>
    </section>

    <!-- FEATURES -->
    <section class="max-w-6xl mx-auto px-6 py-20">
      <h2 class="text-3xl font-semibold text-center mb-12">
        Everything You Need
      </h2>

      <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-6">
        <div v-for="f in features"
             :key="f.title"
             class="p-6 rounded-xl bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-800 shadow-sm hover:shadow-lg transition">

          <h3 class="font-semibold text-lg">{{ f.title }}</h3>
          <p class="text-gray-500 dark:text-gray-400 mt-2 text-sm">
            {{ f.desc }}
          </p>
        </div>
      </div>
    </section>

    <!-- SHOWCASE -->
    <section class="bg-gray-50 dark:bg-gray-900 py-20">
      <h2 class="text-3xl font-semibold text-center mb-12">
        App Preview
      </h2>

      <div class="flex justify-center">
      <div class="flex gap-6 overflow-x-auto px-6 pb-4 no-scrollbar snap-x snap-mandatory">
        <img src="/screens/dashboard.png" class="w-64 rounded-xl shadow-lg snap-center" />
        <img src="/screens/tenants.png" class="w-64 rounded-xl shadow-lg snap-center" />
        <img src="/screens/rooms.png" class="w-64 rounded-xl shadow-lg snap-center" />
        <img src="/screens/assignments.png" class="w-64 rounded-xl shadow-lg snap-center" />
      </div>
    </div>
    </section>

    <!-- CTA -->
    <section class="py-24 text-center bg-gradient-to-r from-blue-600 to-blue-800 text-white">
      <h2 class="text-3xl md:text-4xl font-bold">
        Start Managing Smarter Today
      </h2>

      <p class="mt-4 text-blue-100">
        Download BoardTracker and simplify your operations.
      </p>

      <a href="/downloads/boardtracker.apk"
         class="mt-8 inline-block bg-white text-blue-700 px-8 py-3 rounded-xl font-semibold hover:bg-gray-100 transition shadow">
        Download Now
      </a>
    </section>

  </div>
</template>