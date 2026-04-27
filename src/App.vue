<script setup lang="ts">
</script>

<template>
  <div class="app">
    <!-- NAVBAR -->
    <nav class="navbar">
      <h2>BoardTracker</h2>
      <a href="/downloads/boardtracker.apk" class="btn small">Download</a>
    </nav>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-text">
        <h1>Manage Your Boarding House Smarter</h1>
        <p>
          Track tenants, rooms, payments, and inventory — all in one app.
        </p>

        <a href="/downloads/boardtracker.apk" class="btn">
          Download APK
        </a>

        <span class="sub">Free • Offline-first</span>
      </div>

      <div class="hero-image">
        <img src="/screens/dashboard.png" />
      </div>
    </section>

    <!-- FEATURES -->
    <section class="features">
      <h2>Everything You Need</h2>

      <div class="grid">
        <div class="card" v-for="f in features" :key="f.title">
          <h3>{{ f.title }}</h3>
          <p>{{ f.desc }}</p>
        </div>
      </div>
    </section>

    <!-- SHOWCASE -->
    <section class="showcase">
      <h2>App Screens</h2>

      <div class="screens">
        <img src="/screens/dashboard.png" />
        <img src="/screens/tenants.png" />
        <img src="/screens/rooms.png" />
        <img src="/screens/assignments.png" />
      </div>
    </section>

    <!-- CTA -->
    <section class="cta">
      <h2>Start Managing Better Today</h2>
      <a href="/downloads/boardtracker.apk" class="btn">
        Download Now
      </a>
    </section>

  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      features: [
        { title: "Tenants", desc: "Manage tenant info easily" },
        { title: "Rooms", desc: "Track occupancy and capacity" },
        { title: "Assignments", desc: "Auto compute rent" },
        { title: "Payments", desc: "Track rent payments" },
        { title: "Expenses", desc: "Monitor bills" },
        { title: "Inventory", desc: "Manage room items" },
      ],
    };
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

.app {
  text-align: center;
}

/* NAVBAR */
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background: white;
}

/* HERO */
.hero {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  padding: 80px 20px;
  background: linear-gradient(135deg, #2563eb, #1e40af);
  color: white;
}

.hero-text {
  max-width: 400px;
}

.hero h1 {
  font-size: 36px;
  font-weight: bold;
}

.hero p {
  margin: 20px 0;
}

.hero-image img {
  width: 260px;
  border-radius: 20px;
  margin-left: 30px;
}

/* BUTTON */
.btn {
  display: inline-block;
  margin-top: 15px;
  padding: 10px 20px;
  background: white;
  color: #2563eb;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
}

.small {
  padding: 6px 12px;
}

/* FEATURES */
.features {
  padding: 60px 20px;
}

.grid {
  margin-top: 20px;
  display: grid;
  gap: 15px;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}

.card {
  padding: 20px;
  background: #f3f4f6;
  border-radius: 10px;
}

/* SHOWCASE */
.showcase {
  padding: 60px 20px;
}

.screens {
  display: flex;
  gap: 15px;
  overflow-x: auto;
}

.screens img {
  width: 220px;
  border-radius: 12px;
}

/* CTA */
.cta {
  padding: 60px;
  background: #2563eb;
  color: white;
}

/* FOOTER */
footer {
  padding: 20px;
  background: #111827;
  color: white;
}
</style>