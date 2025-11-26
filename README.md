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
