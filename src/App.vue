<template>
  <div class="app-shell min-vh-100 d-flex flex-column">
    <header class="app-header">
      <div class="container header-content">
        <router-link to="/" class="brand-lockup" aria-label="Pedabayalu Polling home">
          <span class="brand-mark">
            <i class="bi bi-person-vcard-fill"></i>
          </span>
          <span class="brand-copy">
            <strong>Pedabayalu Polling</strong>
            <small>Personnel directory</small>
          </span>
        </router-link>

        <span class="event-badge">
          <span class="event-indicator"></span>
          MPTC &amp; ZPTC 2026
        </span>
      </div>
    </header>

    <main class="flex-grow-1">
      <router-view />
    </main>

    <footer class="app-footer">
      <div class="container d-flex flex-wrap justify-content-between gap-2">
        <span>Pedabayalu polling personnel directory</span>
        <span>Official duty information</span>
      </div>
    </footer>
  </div>
</template>

<style>
:root {
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  color: #17243b;
  background: #f4f7fb;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
}

body {
  margin: 0;
  background: #f4f7fb;
}

.app-shell {
  background:
    radial-gradient(ellipse at 8% 0%, rgba(216, 231, 255, 0.62), transparent 34rem),
    #f4f7fb;
}

.app-header {
  position: relative;
  z-index: 10;
  background: rgba(255, 255, 255, 0.9);
  border-bottom: 1px solid #e8edf5;
  backdrop-filter: blur(16px);
}

.header-content {
  min-height: 76px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.brand-lockup {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  color: #17243b;
  text-decoration: none;
}

.brand-mark {
  width: 42px;
  height: 42px;
  display: grid;
  place-items: center;
  border-radius: 14px;
  color: #fff;
  background: linear-gradient(145deg, #3478f6, #2053c8);
  box-shadow: 0 7px 16px rgba(37, 99, 235, 0.22);
  font-size: 1.15rem;
}

.brand-copy {
  display: grid;
  gap: 0.1rem;
}

.brand-copy strong {
  font-size: 0.95rem;
  letter-spacing: -0.02em;
}

.brand-copy small {
  color: #758198;
  font-size: 0.72rem;
  font-weight: 500;
}

.event-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.55rem 0.85rem;
  border: 1px solid #e4eaf3;
  border-radius: 999px;
  color: #42516a;
  background: #fff;
  font-size: 0.76rem;
  font-weight: 700;
  white-space: nowrap;
}

.event-indicator {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #29a879;
  box-shadow: 0 0 0 3px #e1f6ed;
}

.app-footer {
  padding: 1.1rem 0;
  border-top: 1px solid #e8edf5;
  color: #8590a3;
  font-size: 0.75rem;
}

@media (max-width: 420px) {
  .header-content {
    min-height: 68px;
  }

  .brand-mark {
    width: 38px;
    height: 38px;
  }

  .event-badge {
    padding: 0.5rem 0.65rem;
    font-size: 0.68rem;
  }
}
</style>
