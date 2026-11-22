<template>
  <div>
    <h1 class="admin-page-title">Relief Campaigns</h1>
    <p class="admin-page-intro">
      Private records and working documents for NeSFM relief campaigns. These links are shown only
      inside the authenticated admin dashboard.
    </p>

    <section class="record-card">
      <div class="record-icon">
        <font-awesome-icon :icon="['fas', 'bullhorn']" />
      </div>
      <div class="record-copy">
        <span class="record-status">Completed</span>
        <h2>Nepal Flood Relief Campaign 2026</h2>
        <p>Donation and financial campaign records</p>
      </div>
      <a
        href="https://docs.google.com/spreadsheets/d/1PSYeq6WedTgd_zMmUK6y4kEAUMB-6TFV/preview"
        target="_blank"
        rel="noopener"
        class="record-link"
      >
        View spreadsheet
        <font-awesome-icon :icon="['fas', 'arrow-up-right-from-square']" />
      </a>
    </section>
  </div>
</template>

<script setup lang="ts">
definePageMeta({layout: 'admin', middleware: 'auth'})
useHead({title: 'Relief Campaign Records — NeSFM Admin'})
</script>

<style scoped>
.admin-page-title {
  margin: 0 0 0.5rem;
  color: #1e293b;
  font-size: 1.5rem;
}

.admin-page-intro {
  max-width: 48rem;
  margin: 0 0 1.5rem;
  color: #64748b;
  line-height: 1.6;
}

.record-card {
  display: grid;
  grid-template-columns: auto minmax(0, 1fr) auto;
  align-items: center;
  gap: 1rem;
  max-width: 52rem;
  padding: 1.25rem;
  border-radius: 0.75rem;
  background: #fff;
  box-shadow: 0 1px 4px rgba(15, 23, 42, 0.08);
}

.record-icon {
  display: grid;
  place-items: center;
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  background: #eef2ff;
  color: #1c3382;
  font-size: 1.2rem;
}

.record-status {
  display: inline-flex;
  padding: 0.15rem 0.5rem;
  border-radius: 999px;
  background: #dcfce7;
  color: #166534;
  font-size: 0.7rem;
  font-weight: 800;
  text-transform: uppercase;
}

.record-copy h2 {
  margin: 0.35rem 0 0;
  color: #1e293b;
  font-size: 1.05rem;
}

.record-copy p {
  margin: 0.25rem 0 0;
  color: #64748b;
  font-size: 0.85rem;
}

.record-link {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.6rem 0.9rem;
  border-radius: 0.5rem;
  background: #1c3382;
  color: #fff;
  font-size: 0.85rem;
  font-weight: 700;
  text-decoration: none;
}

.record-link:hover {
  background: #a31432;
}

@media (max-width: 42rem) {
  .record-card {
    grid-template-columns: auto minmax(0, 1fr);
  }

  .record-link {
    grid-column: 1 / -1;
    justify-content: center;
  }
}
</style>
