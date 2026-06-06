# nqd35932052.github.io
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio Kỹ Thuật Số | Nguyễn Quốc Dũng</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Mulish:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #F7F4EF;
    --ink: #1A1714;
    --sage: #4A7C5F;
    --sage-light: #E8F0EB;
    --gold: #C9A84C;
    --gold-light: #F5EDD6;
    --warm-gray: #8C8480;
    --border: #DDD8D2;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Mulish', sans-serif;
    background: var(--cream);
    color: var(--ink);
    line-height: 1.7;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(247,244,239,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 48px;
    display: flex; align-items: center; justify-content: space-between;
    height: 64px;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.25rem; font-weight: 700;
    color: var(--ink); text-decoration: none;
    letter-spacing: 0.03em;
  }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    font-size: 0.82rem; font-weight: 600; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--warm-gray);
    text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sage); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    padding-top: 64px;
  }
  .hero-left {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 60px 80px 80px;
  }
  .hero-tag {
    display: inline-flex; align-items: center; gap: 10px;
    font-size: 0.75rem; font-weight: 700; letter-spacing: 0.14em;
    text-transform: uppercase; color: var(--sage);
    margin-bottom: 28px;
  }
  .hero-tag::before {
    content: ''; width: 32px; height: 2px; background: var(--sage);
  }
  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 5vw, 4.5rem);
    font-weight: 900; line-height: 1.05;
    color: var(--ink); margin-bottom: 8px;
  }
  .hero-name span { color: var(--sage); }
  .hero-course {
    font-size: 0.9rem; color: var(--warm-gray);
    font-weight: 400; margin-bottom: 28px; font-style: italic;
  }
  .hero-desc {
    font-size: 1.05rem; color: #4A4540; max-width: 460px;
    margin-bottom: 44px; line-height: 1.8;
  }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--sage); color: var(--white);
    padding: 14px 32px; border-radius: 4px;
    font-size: 0.82rem; font-weight: 700; letter-spacing: 0.08em;
    text-transform: uppercase; text-decoration: none;
    transition: background 0.2s, transform 0.2s;
  }
  .btn-primary:hover { background: #3a6349; transform: translateY(-2px); }
  .btn-outline {
    border: 2px solid var(--ink); color: var(--ink);
    padding: 12px 30px; border-radius: 4px;
    font-size: 0.82rem; font-weight: 700; letter-spacing: 0.08em;
    text-transform: uppercase; text-decoration: none;
    transition: all 0.2s;
  }
  .btn-outline:hover { background: var(--ink); color: var(--cream); transform: translateY(-2px); }

  .hero-right {
    background: var(--sage);
    display: flex; flex-direction: column; justify-content: center; align-items: center;
    padding: 80px 60px;
    position: relative; overflow: hidden;
  }
  .hero-right::before {
    content: '';
    position: absolute; top: -60px; right: -60px;
    width: 300px; height: 300px;
    border: 60px solid rgba(255,255,255,0.08);
    border-radius: 50%;
  }
  .hero-right::after {
    content: '';
    position: absolute; bottom: -80px; left: -40px;
    width: 220px; height: 220px;
    background: rgba(255,255,255,0.05);
    border-radius: 50%;
  }
  .avatar-ring {
    width: 180px; height: 180px;
    border-radius: 50%;
    border: 4px solid rgba(255,255,255,0.4);
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 32px; position: relative; z-index: 1;
    background: rgba(255,255,255,0.12);
  }
  .avatar-initials {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem; font-weight: 900;
    color: white; letter-spacing: -0.02em;
  }
  .hero-stats {
    display: grid; grid-template-columns: 1fr 1fr; gap: 20px;
    width: 100%; max-width: 320px; position: relative; z-index: 1;
  }
  .stat-card {
    background: rgba(255,255,255,0.15);
    border-radius: 8px; padding: 20px;
    backdrop-filter: blur(8px);
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 900; color: white; line-height: 1;
  }
  .stat-label {
    font-size: 0.75rem; color: rgba(255,255,255,0.75);
    font-weight: 600; letter-spacing: 0.06em;
    text-transform: uppercase; margin-top: 6px;
  }

  /* ── SECTIONS ── */
  section { padding: 100px 80px; }
  .section-header { margin-bottom: 60px; }
  .section-tag {
    font-size: 0.72rem; font-weight: 700; letter-spacing: 0.16em;
    text-transform: uppercase; color: var(--sage);
    display: inline-flex; align-items: center; gap: 10px;
    margin-bottom: 14px;
  }
  .section-tag::before { content: ''; width: 24px; height: 2px; background: var(--sage); }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    font-weight: 700; color: var(--ink); line-height: 1.15;
  }
  .section-sub {
    font-size: 1rem; color: var(--warm-gray);
    margin-top: 12px; max-width: 560px;
  }

  /* ── ABOUT ── */
  #about { background: var(--white); }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: start; }
  .about-info { display: flex; flex-direction: column; gap: 20px; }
  .info-card {
    border-left: 3px solid var(--sage); padding-left: 20px;
  }
  .info-label {
    font-size: 0.72rem; font-weight: 700; letter-spacing: 0.12em;
    text-transform: uppercase; color: var(--warm-gray); margin-bottom: 4px;
  }
  .info-value { font-size: 1rem; font-weight: 600; color: var(--ink); }
  .about-goals h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; font-weight: 700; margin-bottom: 16px;
  }
  .goal-item {
    display: flex; gap: 14px; margin-bottom: 16px;
    padding: 18px; border-radius: 8px;
    background: var(--sage-light); border: 1px solid rgba(74,124,95,0.15);
  }
  .goal-icon {
    width: 36px; height: 36px; flex-shrink: 0;
    background: var(--sage); border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem;
  }
  .goal-text { font-size: 0.9rem; color: #3A4A40; line-height: 1.6; }
  .goal-text strong { color: var(--ink); }

  /* ── PROJECTS ── */
  #projects { background: var(--cream); }
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 28px; }
  .project-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 12px; overflow: hidden;
    transition: box-shadow 0.3s, transform 0.3s;
    cursor: pointer;
  }
  .project-card:hover {
    box-shadow: 0 20px 60px rgba(26,23,20,0.1);
    transform: translateY(-4px);
  }
  .project-header {
    padding: 28px 28px 0;
    display: flex; align-items: flex-start; justify-content: space-between;
  }
  .project-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.5rem; font-weight: 900;
    color: var(--sage); opacity: 0.25; line-height: 1;
  }
  .project-badge {
    font-size: 0.7rem; font-weight: 700; letter-spacing: 0.1em;
    text-transform: uppercase; padding: 4px 12px;
    border-radius: 20px;
  }
  .badge-green { background: var(--sage-light); color: var(--sage); }
  .badge-gold { background: var(--gold-light); color: #7A5C20; }
  .project-body { padding: 16px 28px 28px; }
  .project-lesson {
    font-size: 0.72rem; font-weight: 700; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--warm-gray); margin-bottom: 8px;
  }
  .project-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 700; margin-bottom: 12px; color: var(--ink);
  }
  .project-desc { font-size: 0.88rem; color: #5A534E; line-height: 1.7; margin-bottom: 20px; }
  .project-footer {
    display: flex; align-items: center; justify-content: space-between;
    padding-top: 18px; border-top: 1px solid var(--border);
  }
  .project-tags { display: flex; gap: 8px; flex-wrap: wrap; }
  .tag {
    font-size: 0.7rem; font-weight: 600;
    background: var(--cream); color: var(--warm-gray);
    padding: 4px 10px; border-radius: 4px;
    border: 1px solid var(--border);
  }
  .project-link {
    font-size: 0.78rem; font-weight: 700; color: var(--sage);
    text-decoration: none; letter-spacing: 0.05em;
    display: flex; align-items: center; gap: 6px;
  }
  .project-link:hover { color: #3a6349; }

  /* ── CONCLUSION ── */
  #conclusion {
    background: var(--ink);
    color: var(--cream);
  }
  #conclusion .section-tag { color: var(--gold); }
  #conclusion .section-tag::before { background: var(--gold); }
  #conclusion .section-title { color: var(--cream); }
  #conclusion .section-sub { color: rgba(247,244,239,0.65); }
  .conclusion-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
  .reflection-block {
    background: rgba(247,244,239,0.06);
    border: 1px solid rgba(247,244,239,0.12);
    border-radius: 12px; padding: 32px;
  }
  .reflection-block h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-weight: 700;
    color: var(--gold); margin-bottom: 16px;
    display: flex; align-items: center; gap: 10px;
  }
  .reflection-block p {
    font-size: 0.92rem; color: rgba(247,244,239,0.8);
    line-height: 1.8;
  }
  .skills-list { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 16px; }
  .skill-chip {
    font-size: 0.75rem; font-weight: 600;
    padding: 6px 14px; border-radius: 20px;
    background: rgba(74,124,95,0.3);
    border: 1px solid rgba(74,124,95,0.5);
    color: #9ECFB0;
  }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    border-top: 1px solid rgba(247,244,239,0.1);
    padding: 40px 80px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .footer-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-weight: 700; color: var(--cream);
  }
  .footer-note {
    font-size: 0.8rem; color: rgba(247,244,239,0.45);
    font-style: italic;
  }
  .footer-links { display: flex; gap: 24px; }
  .footer-links a {
    font-size: 0.78rem; font-weight: 600; letter-spacing: 0.08em;
    text-transform: uppercase; color: rgba(247,244,239,0.5);
    text-decoration: none; transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--gold); }

  /* ── DIVIDER ── */
  .divider {
    width: 100%; height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 0;
  }

  /* ── SCROLL ANIMATION ── */
  .fade-up {
    opacity: 0; transform: translateY(30px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    nav { padding: 0 24px; }
    .hero { grid-template-columns: 1fr; }
    .hero-left { padding: 60px 32px; }
    .hero-right { padding: 60px 32px; min-height: 50vh; }
    section { padding: 70px 32px; }
    .about-grid, .projects-grid, .conclusion-grid { grid-template-columns: 1fr; gap: 28px; }
    footer { flex-direction: column; gap: 20px; text-align: center; padding: 40px 32px; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Portfolio.NQD</a>
  <ul class="nav-links">
    <li><a href="#about">Giới thiệu</a></li>
    <li><a href="#projects">Dự án</a></li>
    <li><a href="#conclusion">Tổng kết</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-left">
    <div class="hero-tag">Portfolio Kỹ Thuật Số</div>
    <h1 class="hero-name">Nguyễn<br><span>Quốc Dũng</span></h1>
    <p class="hero-course">Nhập môn Công nghệ số &amp; Ứng dụng Trí tuệ nhân tạo</p>
    <p class="hero-desc">
      Tổng hợp hành trình học tập và phát triển kỹ năng số của tôi — từ quản lý tệp tin, tìm kiếm học thuật, đến ứng dụng AI sáng tạo trong cuộc sống và học tập.
    </p>
    <div class="hero-btns">
      <a href="#projects" class="btn-primary">Xem Dự án</a>
      <a href="#about" class="btn-outline">Về tôi</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="avatar-ring">
      <span class="avatar-initials">NQD</span>
    </div>
    <div class="hero-stats">
      <div class="stat-card">
        <div class="stat-num">6</div>
        <div class="stat-label">Bài tập hoàn thành</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">3</div>
        <div class="stat-label">Trang Portfolio</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">6+</div>
        <div class="stat-label">Kỹ năng mới</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">AI</div>
        <div class="stat-label">Ứng dụng thực tế</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-header fade-up">
    <div class="section-tag">Trang Giới Thiệu</div>
    <h2 class="section-title">Về bản thân tôi</h2>
    <p class="section-sub">Chia sẻ mục tiêu học tập và định hướng phát triển cá nhân trong môi trường số.</p>
  </div>
  <div class="about-grid">
    <div class="about-info fade-up">
      <div class="info-card">
        <div class="info-label">Họ và tên</div>
        <div class="info-value">Nguyễn Quốc Dũng</div>
      </div>
      <div class="info-card">
        <div class="info-label">Ngành học</div>
        <div class="info-value">Công nghệ vật liệu và vi điện tử</div>
      </div>
      <div class="info-card">
        <div class="info-label">Trường</div>
        <div class="info-value">Đại học Công Nghệ - ĐHQGHN</div>
      </div>
      <div class="info-card">
        <div class="info-label">Mã số sinh viên</div>
        <div class="info-value">25023953</div>
      </div>
      <div class="info-card">
        <div class="info-label">Mục tiêu Portfolio</div>
        <div class="info-value">"Thể hiện các kỹ năng số đã học và lưu trữ sản phẩm cá nhân để dễ dàng truy cập và chia sẻ"</div>
      </div>
    </div>
    <div class="about-goals fade-up">
      <h3>Mục tiêu học tập</h3>
      <div class="goal-item">
        <div class="goal-icon">💻</div>
        <div class="goal-text"><strong>Làm chủ công nghệ số</strong> — Hiểu và sử dụng thành thạo các công cụ kỹ thuật số phục vụ học tập và làm việc hiệu quả.</div>
      </div>
      <div class="goal-item">
        <div class="goal-icon">🤖</div>
        <div class="goal-text"><strong>Ứng dụng AI có trách nhiệm</strong> — Khai thác sức mạnh của trí tuệ nhân tạo một cách đúng đắn, sáng tạo và có đạo đức.</div>
      </div>
      <div class="goal-item">
        <div class="goal-icon">🌐</div>
        <div class="goal-text"><strong>Hợp tác trong môi trường số</strong> — Phát triển kỹ năng làm việc nhóm, giao tiếp và chia sẻ trong không gian trực tuyến.</div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-header fade-up">
    <div class="section-tag">Trang Dự Án</div>
    <h2 class="section-title">Các bài tập hoàn thành</h2>
    <p class="section-sub">Tập hợp và trình bày kết quả từ Bài 1 đến Bài 6 — hành trình học tập qua từng chủ đề.</p>
  </div>
  <div class="projects-grid">

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">01</div>
        <span class="project-badge badge-green">Bài 1 – Mục 1.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 1</div>
        <div class="project-title">Máy tính và các thiết bị ngoại vi</div>
        <div class="project-desc">Trình bày cấu trúc thư mục tối ưu và quy tắc đặt tên tệp đã thiết lập. Bao gồm ảnh chụp minh hoạ cách tổ chức tệp tin hiệu quả và khoa học.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Tệp tin</span>
            <span class="tag">Thư mục</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">02</div>
        <span class="project-badge badge-gold">Bài 2 – Mục 2.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 2</div>
        <div class="project-title">Khai thác dữ liệu và thông tin</div>
        <div class="project-desc">Trình bày kết quả tìm kiếm học thuật bằng các toán tử nâng cao và bảng đánh giá nguồn tin đã thực hiện. So sánh độ tin cậy của các nguồn khác nhau.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Tìm kiếm</span>
            <span class="tag">Học thuật</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">03</div>
        <span class="project-badge badge-green">Bài 3 – Mục 3.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 3</div>
        <div class="project-title">Tổng quan về Trí tuệ nhân tạo</div>
        <div class="project-desc">Trình bày sự so sánh giữa Prompt ban đầu và Prompt cải tiến cùng kết quả đầu ra từ AI. Minh chứng rõ hiệu quả của kỹ thuật viết Prompt.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Prompt</span>
            <span class="tag">AI</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">04</div>
        <span class="project-badge badge-gold">Bài 4 – Mục 4.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 4</div>
        <div class="project-title">Giao tiếp và hợp tác trong môi trường số</div>
        <div class="project-desc">Trình bày minh chứng về việc sử dụng công cụ quản lý dự án nhóm và cách thức phối hợp trực tuyến. Bao gồm ảnh chụp màn hình và nhật ký hoạt động nhóm.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Nhóm</span>
            <span class="tag">Trực tuyến</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">05</div>
        <span class="project-badge badge-green">Bài 5 – Mục 5.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 5</div>
        <div class="project-title">Sáng tạo nội dung số</div>
        <div class="project-desc">Trình bày sản phẩm nội dung số hoàn thiện — hình ảnh, video hoặc bài viết — được hỗ trợ bởi các công cụ AI sáng tạo. Thể hiện quy trình sản xuất nội dung.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Nội dung</span>
            <span class="tag">AI tạo sinh</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

    <div class="project-card fade-up">
      <div class="project-header">
        <div class="project-num">06</div>
        <span class="project-badge badge-gold">Bài 6 – Mục 6.4</span>
      </div>
      <div class="project-body">
        <div class="project-lesson">Bài tập 6</div>
        <div class="project-title">An toàn và liêm chính học thuật trong môi trường số</div>
        <div class="project-desc">Trình bày bộ nguyên tắc cá nhân về sử dụng AI có trách nhiệm dựa trên các nghiên cứu đã thực hiện. Phân tích các tình huống thực tế và cách xử lý.</div>
        <div class="project-footer">
          <div class="project-tags">
            <span class="tag">Đạo đức</span>
            <span class="tag">An toàn</span>
          </div>
          <a href="#" class="project-link">Xem chi tiết →</a>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- CONCLUSION -->
<section id="conclusion">
  <div class="section-header fade-up">
    <div class="section-tag">Trang Tổng Kết</div>
    <h2 class="section-title">Nhìn lại hành trình</h2>
    <p class="section-sub">Chia sẻ trải nghiệm, kiến thức và cảm nhận cá nhân sau khi hoàn thành dự án Portfolio này.</p>
  </div>
  <div class="conclusion-grid">
    <div class="reflection-block fade-up">
      <h3>💡 Những điều tôi học được</h3>
      <p>Qua 6 bài tập trong học kỳ này, tôi đã tích lũy được những kỹ năng số thiết thực — từ tổ chức tệp tin khoa học, tìm kiếm học thuật hiệu quả, đến khai thác AI có chọn lọc và có trách nhiệm. Mỗi bài tập là một bước tiến trong hành trình trở thành công dân số.</p>
      <div class="skills-list">
        <span class="skill-chip">Quản lý tệp tin</span>
        <span class="skill-chip">Tìm kiếm học thuật</span>
        <span class="skill-chip">Kỹ thuật Prompt</span>
        <span class="skill-chip">Làm việc nhóm số</span>
        <span class="skill-chip">AI sáng tạo</span>
        <span class="skill-chip">Đạo đức AI</span>
      </div>
    </div>
    <div class="reflection-block fade-up">
      <h3>🌱 Điểm tâm đắc nhất</h3>
      <p>Điều tôi tâm đắc nhất là nhận ra rằng AI không phải là "phép màu" hay công cụ thay thế tư duy, mà là cộng sự đắc lực khi người dùng biết đặt câu hỏi đúng và tư duy phản biện. Kỹ năng viết Prompt hiệu quả thực sự là kỹ năng của thế kỷ 21.</p>
    </div>
    <div class="reflection-block fade-up">
      <h3>⚡ Thách thức đã vượt qua</h3>
      <p>Thách thức lớn nhất là cân bằng giữa việc sử dụng AI hỗ trợ và đảm bảo tính liêm chính học thuật. Xây dựng Portfolio cũng đòi hỏi tư duy thiết kế và kỹ năng tổ chức nội dung mà tôi chưa từng thực hành trước đây.</p>
    </div>
    <div class="reflection-block fade-up">
      <h3>🚀 Định hướng phát triển</h3>
      <p>Tôi dự định tiếp tục phát triển Portfolio này như một "hồ sơ số" của bản thân — bổ sung thêm các dự án mới, hoàn thiện kỹ năng lập trình và ứng dụng AI vào lĩnh vực chuyên ngành của mình trong các học kỳ tới.</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Portfolio.NQD</div>
  <div class="footer-note">Dự án cá nhân — Nhập môn Công nghệ số &amp; Ứng dụng Trí tuệ nhân tạo</div>
  <div class="footer-links">
    <a href="#home">Đầu trang</a>
    <a href="#projects">Dự án</a>
    <a href="#conclusion">Tổng kết</a>
  </div>
</footer>

<script>
  // Scroll animation
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // Smooth scroll for nav links
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const target = document.querySelector(a.getAttribute('href'));
      if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
  });
</script>
</body>
</html>
