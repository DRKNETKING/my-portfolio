<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Portofolio — abdulhabib</title>
  <meta name="description" content="Portofolio projek — abdulhabib H. Lihat projek, gambar, dan kontak." />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <link rel="manifest" href="/manifest.json" />
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa4b2; --accent:#06b6d4; --accent-2:#7c3aed; --glass: rgba(255,255,255,0.04);
      --max-w:1100px; --glass-2: rgba(6,182,212,0.10);
      --radius:12px;
    }
    [data-theme='light']{ --bg:#f6f8fb; --card:#ffffff; --muted:#475569; --accent:#0b7285; --accent-2:#6b21a8; color: #0b1220 }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;padding:0; font-family:Inter,system-ui,Segoe UI,Roboto,"Helvetica Neue",Arial; background:linear-gradient(180deg,var(--bg) 0%, #0a1320 60%); color:var(--muted); -webkit-font-smoothing:antialiased;
      display:flex; justify-content:center; padding:36px 18px;
    }
    .container{width:100%; max-width:var(--max-w);}
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:22px}
    .brand{display:flex;align-items:center;gap:14px}
    .logo{width:54px;height:54px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;font-weight:700;color:#021024}
    .hero{padding:20px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:var(--radius);box-shadow:0 8px 30px rgba(2,6,23,0.6);display:flex;gap:20px;align-items:center}
    .hero-left{flex:1}
    h1{margin:0;font-size:28px;line-height:1.05;color:var(--muted)}
    h1 span{color:var(--accent)}
    p.lead{color:var(--muted);margin-top:10px;margin-bottom:12px}
    .cta{display:inline-flex;gap:10px}
    .btn{padding:10px 14px;border-radius:10px;border:0;font-weight:600;cursor:pointer}
    .btn-primary{background:var(--accent);color:#021024}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}
    .hero-right{width:220px}
    .avatar{width:220px;height:220px;border-radius:16px;overflow:hidden;box-shadow:0 10px 40px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}

    /* projects */
    section.projects{margin-top:18px}
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .card{background:var(--card);padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,0.03);overflow:hidden;display:flex;flex-direction:column;gap:10px;transition:transform .28s ease, box-shadow .28s ease}
    .card:hover{transform:translateY(-8px) scale(1.01);box-shadow:0 18px 40px rgba(0,0,0,0.45);}
    .card .thumb{position:relative;border-radius:10px;overflow:hidden}
    .card .thumb::after{content:"";position:absolute;inset:0;border-radius:10px;pointer-events:none;box-shadow:0 0 32px rgba(6,182,212,0);transition:box-shadow .3s ease}
    .card:hover .thumb::after{box-shadow:0 0 30px rgba(6,182,212,0.18), inset 0 0 24px rgba(124,58,237,0.06)}
    .card img{width:100%;height:160px;object-fit:cover;border-radius:8px;display:block;transition:transform .5s ease}
    .card:hover img{transform:scale(1.06)}
    .card .meta{display:flex;justify-content:space-between;align-items:center}
    .tags{display:flex;gap:8px;flex-wrap:wrap}
    .tag{font-size:12px;padding:6px 8px;border-radius:999px;background:var(--glass);color:var(--muted)}
    .card h3{margin:6px 0 0 0;font-size:16px;color:var(--muted)}
    .card p{margin:6px 0;color:var(--muted);font-size:14px}
    .links{display:flex;gap:8px;flex-wrap:wrap}
    a.link{font-size:13px;padding:8px 10px;border-radius:8px;background:rgba(255,255,255,0.03);color:var(--muted);text-decoration:none}

    /* detail page area (client-side routing) */
    .detail{display:none;padding:16px;background:var(--card);border-radius:12px;margin-top:18px}
    .detail.open{display:block}
    .detail .top{display:flex;gap:16px;align-items:flex-start;flex-wrap:wrap}
    .detail img{width:48%;border-radius:10px}

    /* modal */
    .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:linear-gradient(180deg, rgba(2,6,23,0.7), rgba(2,6,23,0.9));z-index:60}
    .modal.open{display:flex}
    .modal-card{max-width:900px;width:94%;background:#071229;padding:14px;border-radius:12px}
    .modal-card img{width:100%;height:auto;border-radius:8px}
    .modal-close{position:absolute;top:18px;right:18px;padding:8px;border-radius:8px;background:rgba(255,255,255,0.02);border:0;color:var(--muted);cursor:pointer}

    /* contact form */
    form.contact{display:grid;grid-template-columns:1fr 320px;gap:12px;align-items:start}
    form input, form textarea{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);background:transparent;color:var(--muted)}
    form button{padding:10px 14px;border-radius:10px;border:0;background:var(--accent);color:#021024;font-weight:700}

    /* misc */
    footer{margin-top:20px;color:var(--muted);font-size:13px;text-align:center}
    .controls{display:flex;gap:8px;align-items:center}
    .theme-toggle{padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;cursor:pointer}

    /* responsive */
    @media (max-width:980px){.grid{grid-template-columns:repeat(2,1fr)}.hero{flex-direction:column;align-items:flex-start}.hero-right{width:100%}.avatar{width:100%;height:160px}form.contact{grid-template-columns:1fr}}
    @media (max-width:600px){.grid{grid-template-columns:1fr}.container{padding:0 8px}h1{font-size:20px}.detail img{width:100%;margin-bottom:12px}}
  </style>
</head>
<body>
  <div class="container" id="app">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">AH</div>
        <div>
          <div style="font-weight:700;color:var(--muted)">abdulhabib H</div>
          <div style="font-size:13px;color:var(--muted)">Frontend Developer • UI/UX • Pembuat solusi ringan</div>
        </div>
      </div>
      <nav class="controls" aria-label="Main">
        <a class="btn btn-ghost" href="#projects">Projek</a>
        <a class="btn btn-ghost" href="#contact">Kontak</a>
        <button id="themeBtn" class="theme-toggle" aria-pressed="false" title="Toggle theme">🌗</button>
      </nav>
    </header>

    <div class="hero" role="banner">
      <div class="hero-left">
        <h1>Halo — Saya <span>abdulhabib H</span></h1>
        <div style="font-size:15px;font-weight:600;color:var(--muted);margin-top:6px">Membangun tampilan web modern, cepat, dan responsif.</div>
        <p class="lead">Berikut kumpulan projek pilihan saya. Klik "Lihat" untuk memperbesar gambar, "Detail" untuk membuka halaman projek, atau gunakan link GitHub untuk melihat kode.</p>

        <div class="cta">
          <a class="btn btn-primary" href="#contact">Hubungi Saya</a>
          <a class="btn btn-ghost" href="/resume.pdf" target="_blank" rel="noopener">Unduh CV</a>
        </div>
      </div>

      <div class="hero-right" aria-hidden="true">
        <div class="avatar">
          <img src="https://picsum.photos/seed/avatar/800/800" alt="Avatar abdulhabib" style="width:100%;height:100%;object-fit:cover" loading="lazy" />
        </div>
      </div>
    </div>

    <section id="projects" class="projects" aria-labelledby="projects-heading">
      <h2 id="projects-heading" style="margin:16px 0 10px 0;color:var(--muted)">Projek Pilihan</h2>
      <div class="grid" id="projectsGrid">

        <!-- 1. Sistem Akademik Modern -->
        <article class="card" data-slug="sistem-akademik" data-title="Sistem Akademik Modern" data-desc="Dashboard akademik dengan presensi realtime, laporan, dan export PDF." data-img="https://picsum.photos/seed/techportal/1200/800">
          <div class="thumb">
            <img
              src="https://picsum.photos/seed/techportal/800/600"
              srcset="https://picsum.photos/seed/techportal/400/300 400w, https://picsum.photos/seed/techportal/800/600 800w, https://picsum.photos/seed/techportal/1200/800 1200w"
              sizes="(max-width:600px) 100vw, 33vw"
              alt="Tampilan dashboard Sistem Akademik"
              loading="lazy">
          </div>
          <div class="meta">
            <div>
              <h3>Sistem Akademik Modern</h3>
              <p>Dashboard untuk mengelola akademik, presensi, dan laporan realtime.</p>
            </div>
            <div class="tags"><span class="tag">PHP</span><span class="tag">MySQL</span></div>
          </div>
          <div class="links">
            <a class="link" href="https://github.com/username/project1" target="_blank" rel="noopener">GitHub</a>
            <a class="link" href="#/project/sistem-akademik" data-action="detail">Detail</a>
            <a class="link" href="#" data-action="preview">Lihat</a>
          </div>
        </article>

        <!-- 2. Smart Notes App -->
        <article class="card" data-slug="smart-notes" data-title="Smart Notes App" data-desc="Aplikasi PWA untuk pencatatan produktivitas dengan sync dan offline mode." data-img="https://picsum.photos/seed/technotes/1200/800">
          <div class="thumb">
            <img
              src="https://picsum.photos/seed/technotes/800/600"
              srcset="https://picsum.photos/seed/technotes/400/300 400w, https://picsum.photos/seed/technotes/800/600 800w, https://picsum.photos/seed/technotes/1200/800 1200w"
              sizes="(max-width:600px) 100vw, 33vw"
              alt="Tampilan Smart Notes App"
              loading="lazy">
          </div>
          <div class="meta">
            <div>
              <h3>Smart Notes App</h3>
              <p>PWA pencatatan produktivitas harian dengan sinkronisasi dan offline.</p>
            </div>
            <div class="tags"><span class="tag">PWA</span><span class="tag">LocalStorage</span></div>
          </div>
          <div class="links">
            <a class="link" href="https://github.com/username/project2" target="_blank" rel="noopener">GitHub</a>
            <a class="link" href="#/project/smart-notes" data-action="detail">Detail</a>
            <a class="link" href="#" data-action="preview">Lihat</a>
          </div>
        </article>

        <!-- 3. E-Commerce Lite -->
        <article class="card" data-slug="ecommerce-lite" data-title="E-Commerce Lite" data-desc="Mini marketplace: katalog, keranjang, dan checkout sederhana — optimasi performance." data-img="https://picsum.photos/seed/techecom/1200/800">
          <div class="thumb">
            <img
              src="https://picsum.photos/seed/techecom/800/600"
              srcset="https://picsum.photos/seed/techecom/400/300 400w, https://picsum.photos/seed/techecom/800/600 800w, https://picsum.photos/seed/techecom/1200/800 1200w"
              sizes="(max-width:600px) 100vw, 33vw"
              alt="Tampilan E-Commerce Lite"
              loading="lazy">
          </div>
          <div class="meta">
            <div>
              <h3>E-Commerce Lite</h3>
              <p>Mini marketplace dengan UI cepat dan modern.</p>
            </div>
            <div class="tags"><span class="tag">JS</span><span class="tag">Stripe</span></div>
          </div>
          <div class="links">
            <a class="link" href="https://github.com/username/project3" target="_blank" rel="noopener">GitHub</a>
            <a class="link" href="#/project/ecommerce-lite" data-action="detail">Detail</a>
            <a class="link" href="#" data-action="preview">Lihat</a>
          </div>
        </article>

      </div>
    </section>

    <!-- Detail Page -->
    <div class="detail" id="detailPage">
      <div class="top">
        <img id="detailImg" src="" alt="Project Image" loading="lazy">
        <div>
          <h2 id="detailTitle"></h2>
          <p id="detailDesc"></p>
          <a class="btn btn-primary" id="detailLink" href="#" target="_blank" rel="noopener">Kunjungi Projek</a>
        </div>
      </div>
    </div>

    <!-- Modal for Image Preview -->
    <div class="modal" id="imageModal">
      <div class="modal-card">
        <button class="modal-close" id="modalClose">&times;</button>
        <img id="modalImg" src="" alt="Preview Image">
      </div>
    </div>

    <section id="contact" aria-labelledby="contact-heading">
      <h2 id="contact-heading" style="margin:16px 0 10px 0;color:var(--muted)">Kontak</h2>
      <form class="contact" action="#" method="post">
        <div>
          <input type="text" name="name" placeholder="Nama Anda" required>
          <input type="email" name="email" placeholder="Email Anda" required>
          <textarea name="message" placeholder="Pesan Anda" rows="5" required></textarea>
        </div>
        <button type="submit">Kirim Pesan</button>
      </form>
    </section>

    <footer>
      <p>&copy; 2023 abdulhabib H. Dibuat dengan ❤️ menggunakan HTML, CSS, dan JavaScript.</p>
    </footer>
  </div>

  <script>
    // Theme Toggle
    const themeBtn = document.getElementById('themeBtn');
    const body = document.body;
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme) {
      body.setAttribute('data-theme', savedTheme);
      themeBtn.textContent = savedTheme === 'light' ? '🌞' : '🌗';
    }
    themeBtn.addEventListener('click', () => {
      const currentTheme = body.getAttribute('data-theme');
      const newTheme = currentTheme === 'light' ? 'dark' : 'light';
      body.setAttribute('data-theme', newTheme);
      localStorage.setItem('theme', newTheme);
      themeBtn.textContent = newTheme === 'light' ? '🌞' : '🌗';
    });

    // Project Detail and Modal Handling
    const detailPage = document.getElementById('detailPage');
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImg');
    const modalClose = document.getElementById('modalClose');
    const detailImg = document.getElementById('detailImg');
    const detailTitle = document.getElementById('detailTitle');
    const detailDesc = document.getElementById('detailDesc');
    const detailLink = document.getElementById('detailLink');

    document.addEventListener('click', (e) => {
      if (e.target.matches('[data-action="detail"]')) {
        e.preventDefault();
        const card = e.target.closest('.
