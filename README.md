# Easy-Shop-B
<!DOCTYPE html>
<html lang="bn" data-theme="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>আমার আধুনিক পোর্টফোলিও</title>
  <style>
    :root {
      --bg:#f0f4f9;
      --card:#ffffff;
      --text:#1f2d3a;
      --muted:#6e7a8c;
      --accent:#6366f1;
      --radius:14px;
      --shadow:0 25px 50px -12px rgba(0,0,0,0.25);
      --transition:.35s cubic-bezier(.4,.2,.2,1);
    }
    [data-theme="dark"] {
      --bg:#0f172a;
      --card:#1f293b;
      --text:#e2e8f0;
      --muted:#94a3b8;
      --accent:#7c3aed;
    }
    * { box-sizing:border-box; }
    body {
      margin:0;
      font-family: system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Ubuntu,sans-serif;
      background: var(--bg);
      color: var(--text);
      scroll-behavior: smooth;
      line-height:1.55;
    }
    header {
      position: sticky;
      top:0;
      z-index: 10;
      background: var(--card);
      padding: 12px 24px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap:10px;
      box-shadow: 0 10px 30px -10px rgba(0,0,0,.08);
    }
    .brand {
      font-weight: 700;
      font-size: 1.25rem;
      display:flex;
      align-items:center;
      gap:8px;
    }
    nav {
      display:flex;
      gap:18px;
      flex-wrap: wrap;
      align-items:center;
    }
    nav a {
      position: relative;
      text-decoration:none;
      color: var(--text);
      font-weight:500;
      padding:4px 0;
    }
    nav a::after {
      content:"";
      position:absolute;
      left:0;
      bottom:-2px;
      width:0;
      height:2px;
      background: var(--accent);
      border-radius:2px;
      transition: width var(--transition);
    }
    nav a:hover::after { width:100%; }

    .theme-toggle {
      background: none;
      border: 2px solid var(--accent);
      padding:6px 12px;
      border-radius:999px;
      cursor:pointer;
      font-weight:600;
      display:inline-flex;
      align-items:center;
      gap:6px;
      transition: var(--transition);
    }
    .theme-toggle:hover { background: rgba(99,102,241,.08); }

    main {
      max-width: 1100px;
      margin: auto;
      padding: 40px 20px 80px;
      display: grid;
      gap:60px;
    }

    .hero {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
      gap:40px;
      align-items:center;
    }
    .intro {
      position: relative;
    }
    .intro h1 {
      font-size: 2.4rem;
      margin:0 0 12px;
    }
    .intro p {
      margin: 0 0 20px;
      color: var(--muted);
    }
    .cta {
      display:flex;
      gap:12px;
      flex-wrap: wrap;
    }
    .btn {
      padding: 12px 24px;
      border-radius: 8px;
      font-weight:600;
      border: none;
      cursor:pointer;
      transition: var(--transition);
      display:inline-flex;
      align-items:center;
      gap:6px;
      text-decoration:none;
    }
    .btn-primary {
      background: var(--accent);
      color:#fff;
    }
    .btn-outline {
      background: transparent;
      color: var(--accent);
      border:2px solid var(--accent);
    }
    .btn-primary:hover { filter: brightness(1.1); }
    .btn-outline:hover { background: rgba(124,58,237,.08); }

    .profile-img {
      width: 100%;
      max-width: 360px;
      aspect-ratio: 1;
      border-radius: 20px;
      overflow:hidden;
      position: relative;
      margin:auto;
      box-shadow: var(--shadow);
      transition: transform var(--transition);
    }
    .profile-img img {
      width:100%;
      height:100%;
      object-fit:cover;
      display:block;
    }
    .profile-img:hover { transform: translateY(-4px); }

    section {
      position: relative;
    }
    .section-title {
      display:flex;
      align-items:center;
      gap:12px;
      margin-bottom:18px;
    }
    .section-title h2 {
      margin:0;
      font-size:1.85rem;
      position: relative;
    }
    .underline {
      flex:1;
      height:3px;
      background: var(--accent);
      border-radius:2px;
      margin-left:6px;
    }

    .cards {
      display:grid;
      grid-template-columns: repeat(auto-fit,minmax(260px,1fr));
      gap:30px;
    }
    .card {
      background: var(--card);
      border-radius: var(--radius);
      padding: 22px 18px;
      position: relative;
      overflow:hidden;
      box-shadow: var(--shadow);
      transition: var(--transition);
    }
    .card:hover { transform: translateY(-6px); }
    .card img {
      width:100%;
      border-radius:10px;
      object-fit:cover;
      margin-bottom:12px;
      display:block;
    }
    .card h3 {
      margin:8px 0 6px;
      font-size:1.2rem;
    }
    .card p {
      margin:0 0 12px;
      color: var(--muted);
      font-size:0.95rem;
    }
    .tags {
      display:flex;
      gap:8px;
      flex-wrap: wrap;
      margin-bottom:10px;
    }
    .tag {
      background: rgba(99,102,241,.1);
      padding:5px 12px;
      border-radius:999px;
      font-size:0.65rem;
      font-weight:600;
      letter-spacing:0.5px;
    }
    .links {
      display:flex;
      gap:12px;
      flex-wrap: wrap;
    }
    .socials {
      display:flex;
      gap:14px;
      margin-top:6px;
    }
    .socials a {
      display:inline-flex;
      align-items:center;
      justify-content:center;
      width:36px;
      height:36px;
      border-radius:50%;
      background: rgba(0,0,0,0.05);
      text-decoration:none;
      transition: var(--transition);
    }
    .socials a svg {
      width:18px;
      height:18px;
      display:block;
      stroke: currentColor;
      stroke-width:2;
      fill:none;
    }
    .socials a:hover { transform: scale(1.08); }

    #contact .grid {
      display: grid;
      gap:30px;
      grid-template-columns: repeat(auto-fit,minmax(260px,1fr));
    }
    .contact-card {
      background: var(--card);
      padding:20px 18px;
      border-radius:12px;
      box-shadow: var(--shadow);
    }
    .contact-item {
      display:flex;
      align-items:center;
      gap:14px;
      margin-bottom:14px;
    }
    .contact-item svg {
      width:22px;
      height:22px;
      flex-shrink:0;
    }
    .footer {
      text-align:center;
      padding:30px 18px;
      font-size:0.85rem;
      color: var(--muted);
    }

    /* small accent animation */
    .fade-up {
      opacity:0;
      transform: translateY(12px);
      animation: fadeUp .8s forwards;
    }
    @keyframes fadeUp {
      to { opacity:1; transform: translateY(0); }
    }

    @media (max-width: 900px){
      .hero { gap:24px; }
      .intro h1 { font-size:2rem; }
    }
  </style>
</head>
<body>

  <header>
    <div class="brand">
      <div style="font-size:1.4rem;">🌟</div>
      <div>আপনার নামে</div>
    </div>

    <nav aria-label="Primary">
      <a href="#about">আমার সম্পর্কে</a>
      <a href="#projects">প্রোজেক্ট</a>
      <a href="#contact">যোগাযোগ</a>
    </nav>

    <div style="display:flex; gap:12px; align-items:center;">
      <button class="theme-toggle" id="themeToggle" aria-label="থিম টগল">
        🌙 <span style="margin-left:4px;">থিম</span>
      </button>
      <a href="#projects" class="btn btn-primary">প্রোজেক্ট দেখুন</a>
    </div>
  </header>

  <main>
    <!-- Hero -->
    <section class="hero" id="about">
      <div class="intro fade-up" style="animation-delay:.1s;">
        <div class="section-title">
          <h2>হ্যালো, আমি <span style="color: var(--accent);">Saif Mahmud</span></h2>
          <div class="underline"></div>
        </div>
        <p>আমি একজন ওয়েব ডেভেলপার। আকর্ষণীয়, রেস্পন্সিভ এবং গতিশীল ওয়েব প্রোজেক্ট বানাতে ভালোবাসি। HTML, CSS, JavaScript দিয়ে সুন্দর ইউআই তৈরিতে পারদর্শী।</p>
        <div class="cta">
          <a href="#contact" class="btn btn-outline">যোগাযোগ করুণ</a>
          <a href="#projects" class="btn btn-primary">আমার কাজ</a>
        </div>
        <div class="socials" style="margin-top:14px;">
          <a href="#" aria-label="GitHub">
            <svg viewBox="0 0 24 24" aria-hidden="true">
              <path d="M12 .5a12 12 0 0 0-3.79 23.4c.6.11.82-.26.82-.58 0-.29-.01-1.05-.01-2.05-3.34.73-4.04-1.61-4.04-1.61-.55-1.4-1.34-1.77-1.34-1.77-1.1-.75.08-.74.08-.74 1.22.09 1.86 1.26 1.86 1.26 1.08 1.85 2.83 1.32 3.52 1.01.11-.78.42-1.32.76-1.62-2.66-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.13-.3-.54-1.52.12-3.17 0 0 1.01-.32 3.3 1.23a11.49 11.49 0 0 1 3-.4c1.02.01 2.05.14 3 .4 2.28-1.54 3.29-1.23 3.29-1.23.67 1.65.26 2.87.13 3.17.77.84 1.24 1.91 1.24 3.22 0 4.61-2.81 5.62-5.49 5.92.43.37.81 1.1.81 2.22 0 1.6-.01 2.88-.01 3.27 0 .32.22.7.83.58A12 12 0 0 0 12 .5"></path>
            </svg>
          </a>
          <a href="#" aria-label="LinkedIn">
            <svg viewBox="0 0 24 24" aria-hidden="true">
              <path d="M4.98 3.5a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5zm.02 7h4.5v10h-4.5v-10zm7.5 0h4.32v1.4h.06c.6-1.13 2.06-2.32 4.24-2.32 4.54 0 5.38 2.99 5.38 6.88v7.04h-4.5v-6.24c0-1.49-.03-3.4-2.07-3.4-2.08 0-2.4 1.62-2.4 3.29v6.35h-4.5v-10z"></path>
            </svg>
          </a>
          <a href="#" aria-label="Twitter">
            <svg viewBox="0 0 24 24" aria-hidden="true">
              <path d="M23.44 4.83c-.8.35-1.66.58-2.56.69a4.48 4.48 0 0 0 1.96-2.48 8.9 8.9 0 0 1-2.83 1.08 4.46 4.46 0 0 0-7.6 4.06A12.65 12.65 0 0 1 3.1 3.15a4.46 4.46 0 0 0 1.38 5.95 4.4 4.4 0 0 1-2.02-.56v.06a4.46 4.46 0 0 0 3.58 4.37 4.5 4.5 0 0 1-2.01.08 4.46 4.46 0 0 0 4.16 3.1A8.94 8.94 0 0 1 2 19.54a12.58 12.58 0 0 0 6.84 2.01c8.21 0 12.7-6.8 12.7-12.7 0-.19-.01-.38-.02-.57a9.07 9.07 0 0 0 2.24-2.31z"></path>
            </svg>
          </a>
        </div>
      </div>
      <div class="profile-img fade-up" style="animation-delay:.3s;">
        <img src="https://tinyurl.com/y263sjh4?text=আপনার+ছবি" alt="Profile photo" loading="lazy"/>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <div class="section-title">
        <h2>প্রোজেক্ট গুলো</h2>
        <div class="underline"></div>
      </div>
      <div class="cards">
        <!-- Project 1 -->
        <div class="card fade-up" style="animation-delay:.1s;">
          <img src="https://tinyurl.com/4zwkn433?text=প্রোজেক্ট+১" alt="Project 1 screenshot">
          <div class="tags">
            <div class="tag">HTML</div>
            <div class="tag">CSS</div>
            <div class="tag">Responsive</div>
          </div>
          <h3>প্রোজেক্ট ১</h3>
          <p>একটি রেস্পন্সিভ ল্যান্ডিং পেজ ডিজাইন যা মোবাইল ও ডেস্কটপ উভয়ে সুন্দর।</p>
          <div class="links">
            <a href="#" class="btn btn-outline" style="font-size:.8rem;">লাইভ দেখুন</a>
            <a href="#" class="btn btn-primary" style="font-size:.8rem;">সোর্স কোড</a>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="card fade-up" style="animation-delay:.2s;">
          <img src="https://tinyurl.com/2s3j9f65?text=প্রোজেক্ট+২" alt="Project 2 screenshot">
          <div class="tags">
            <div class="tag">JavaScript</div>
            <div class="tag">Interaction</div>
          </div>
          <h3>প্রোজেক্ট ২</h3>
          <p>ইন্টারঅ্যাকটিভ ওয়েব অ্যাপ যা ইউজার ইনপুট অনুযায়ী কন্টেন্ট রেন্ডার করে।</p>
          <div class="links">
            <a href="#" class="btn btn-outline" style="font-size:.8rem;">লাইভ দেখুন</a>
            <a href="#" class="btn btn-primary" style="font-size:.8rem;">সোর্স কোড</a>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="card fade-up" style="animation-delay:.3s;">
          <img src="https://tinyurl.com/4zwkn433?text=প্রোজেক্ট+৩" alt="Project 3 screenshot">
          <div class="tags">
            <div class="tag">Portfolio</div>
            <div class="tag">Design</div>
          </div>
          <h3>প্রোজেক্ট ৩</h3>
          <p>ব্যক্তিগত পোর্টফোলিও সাইট যেখানে প্রোজেক্ট, স্কিল ও যোগাযোগ দেখানো হয়।</p>
          <div class="links">
            <a href="#" class="btn btn-outline" style="font-size:.8rem;">লাইভ দেখুন</a>
            <a href="#" class="btn btn-primary" style="font-size:.8rem;">সোর্স কোড</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="section-title">
        <h2>যোগাযোগ</h2>
        <div class="underline"></div>
      </div>
      <div class="grid">
        <div class="contact-card fade-up" style="animation-delay:.1s;">
          <div class="contact-item">
            <svg viewBox="0 0 24 24" aria-hidden="true" fill="none" stroke="currentColor">
              <path d="M2 8.5A6.5 6.5 0 0 1 8.5 2h7A6.5 6.5 0 0 1 22 8.5v7a6.5 6.5 0 0 1-6.5 6.5h-7A6.5 6.5 0 0 1 2 15.5v-7z"></path>
              <path d="M2 8l10 6 10-6"></path>
            </svg>
            <div>
              <div style="font-weight:600;">ইমেইল</div>
              <div style="font-size:.9rem; color: var(--muted);">saifmahmud766@gmail.com</div>
            </div>
          </div>
          <div class="contact-item">
            <svg viewBox="0 0 24 24" aria-hidden="true" fill="none" stroke="currentColor">
              <path d="M3 7a4 4 0 0 1 4-4h2.6a1 1 0 0 1 .9.55l1.5 3.3a1 1 0 0 0 .9.55h3.1a4 4 0 0 1 4 4v5a4 4 0 0 1-4 4h-2.6a1 1 0 0 1-.9-.55l-1.5-3.3a1 1 0 0 0-.9-.55H7a4 4 0 0 1-4-4V7z"></path>
            </svg>
            <div>
              <div style="font-weight:600;">ফোন</div>
              <div style="font-size:.9rem; color: var(--muted);">+৮৮ ০১৭৮-৭১৮২৮৩৩</div>
            </div>
          </div>
          <div class="contact-item">
            <svg viewBox="0 0 24 24" aria-hidden="true" fill="none" stroke="currentColor">
              <path d="M12 2a10 10 0 1 0 0 20 10 10 0 0 0 0-20zm1 14.5h-2v-2h2v2zm0-4h-2V7h2v5.5z"></path>
            </svg>
            <div>
              <div style="font-weight:600;">ঠিকানা</div>
              <div style="font-size:.9rem; color: var(--muted);">ঢাকা, বাংলাদেশ</div>
            </div>
          </div>
        </div>
        <div class="contact-card fade-up" style="animation-delay:.2s;">
          <p>আপনি চাইলে এখানে ফর্মও যোগ করতে পারেন: যেমন নাম, মেইল, বার্তা পাঠানোর ইনপুট।</p>
          <p>অথবা নিচের সোশ্যাল লিঙ্ক দিয়ে আমাকে ফলো করুন:</p>
          <div class="socials">
            <a href="#" aria-label="GitHub"><svg viewBox="0 0 24 24"><path d="M12 .5a12 12 0 0 0-3.79 23.4c.6.11.82-.26.82-.58 0-.29-.01-1.05-.01-2.05-3.34.73-4.04-1.61-4.04-1.61-.55-1.4-1.34-1.77-1.34-1.77-1.1-.75.08-.74.08-.74 1.22.09 1.86 1.26 1.86 1.26 1.08 1.85 2.83 1.32 3.52 1.01.11-.78.42-1.32.76-1.62-2.66-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.13-.3-.54-1.52.12-3.17 0 0 1.01-.32 3.3 1.23a11.49 11.49 0 0 1 3-.4c1.02.01 2.05.14 3 .4 2.28-1.54 3.29-1.23 3.29-1.23.67 1.65.26 2.87.13 3.17.77.84 1.24 1.91 1.24 3.22 0 4.61-2.81 5.62-5.49 5.92.43.37.81 1.1.81 2.22 0 1.6-.01 2.88-.01 3.27 0 .32.22.7.83.58A12 12 0 0 0 12 .5"></path></svg></a>
            <a href="#" aria-label="LinkedIn"><svg viewBox="0 0 24 24"><path d="M4.98 3.5a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5zm.02 7h4.5v10h-4.5v-10zm7.5 0h4.32v1.4h.06c.6-1.13 2.06-2.32 4.24-2.32 4.54 0 5.38 2.99 5.38 6.88v7.04h-4.5v-6.24c0-1.49-.03-3.4-2.07-3.4-2.08 0-2.4 1.62-2.4 3.29v6.35h-4.5v-10z"></path></svg></a>
            <a href="#" aria-label="Twitter"><svg viewBox="0 0 24 24"><path d="M23.44 4.83c-.8.35-1.66.58-2.56.69a4.48 4.48 0 0 0 1.96-2.48 8.9 8.9 0 0 1-2.83 1.08 4.46 4.46 0 0 0-7.6 4.06A12.65 12.65 0 0 1 3.1 3.15a4.46 4.46 0 0 0 1.38 5.95 4.4 4.4 0 0 1-2.02-.56v.06a4.46 4.46 0 0 0 3.58 4.37 4.5 4.5 0 0 1-2.01.08 4.46 4.46 0 0 0 4.16 3.1A8.94 8.94 0 0 1 2 19.54a12.58 12.58 0 0 0 6.84 2.01c8.21 0 12.7-6.8 12.7-12.7 0-.19-.01-.38-.02-.57a9.07 9.07 0 0 0 2.24-2.31z"></path></svg></a>
          </div>
        </div>
      </div>
    </section>

    <div class="footer">
      © ২০২৫ সাইফ মাহমুদ. সব অধিকার সংরক্ষিত।
    </div>
  </main>

  <script>
    // থিম টগল
    const toggle = document.getElementById("themeToggle");
    const root = document.documentElement;
    function setTheme(theme) {
      root.setAttribute("data-theme", theme);
      localStorage.setItem("theme", theme);
      toggle.textContent = theme === "light" ? "🌙 থিম" : "☀️ থিম";
    }
    // লোড সময় পূর্ববর্তী থিম
    const stored = localStorage.getItem("theme");
    if (stored) setTheme(stored);
    else setTheme("light");

    toggle.addEventListener("click", () => {
      const current = root.getAttribute("data-theme");
      setTheme(current === "light" ? "dark" : "light");
    });

    // ফেড-আপ অ্যানিমেশন ট্রিগার (simple)
    document.addEventListener("DOMContentLoaded", () => {
      const els = document.querySelectorAll(".fade-up");
      els.forEach((el, i) => {
        el.style.animationDelay = (i * 0.1 + 0.1) + "s";
      });
    });
  </script>
</body>
</html>
