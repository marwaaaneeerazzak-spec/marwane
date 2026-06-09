<!DOCTYPE html>
<html lang="ar-MA" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نشاطو - Nchato | نتحركو مع الفاميلة</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --ocean: #1B4F72;
    --ocean-light: #2E86C1;
    --orange: #E67E22;
    --orange-light: #F39C12;
    --white: #FAFAFA;
    --gray-light: #ECF0F1;
    --gray-mid: #BDC3C7;
    --text-dark: #1a1a2e;
    --text-mid: #555;
    --green: #27AE60;
    --radius: 16px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Nunito', 'Segoe UI', Tahoma, sans-serif;
    background: var(--white);
    color: var(--text-dark);
    direction: rtl;
  }

  /* NAV */
  nav {
    background: var(--ocean);
    padding: 0 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 64px;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 12px rgba(0,0,0,0.15);
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    color: white;
    text-decoration: none;
  }

  .logo-icon {
    width: 38px;
    height: 38px;
    background: var(--orange);
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
  }

  .logo-text {
    font-size: 22px;
    font-weight: 900;
    letter-spacing: -0.5px;
  }

  .logo-text span { color: var(--orange-light); }

  .nav-links {
    display: flex;
    gap: 8px;
    list-style: none;
  }

  .nav-links a {
    color: rgba(255,255,255,0.85);
    text-decoration: none;
    font-size: 14px;
    font-weight: 600;
    padding: 8px 14px;
    border-radius: 8px;
    transition: all 0.2s;
  }

  .nav-links a:hover, .nav-links a.active {
    background: rgba(255,255,255,0.15);
    color: white;
  }

  .nav-points {
    background: var(--orange);
    color: white;
    font-weight: 900;
    font-size: 14px;
    padding: 8px 16px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    gap: 6px;
    cursor: pointer;
    transition: transform 0.2s;
  }

  .nav-points:hover { transform: scale(1.05); }

  /* HERO */
  .hero {
    background: linear-gradient(135deg, var(--ocean) 0%, var(--ocean-light) 60%, #1abc9c 100%);
    padding: 64px 24px 80px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    width: 400px;
    height: 400px;
    background: rgba(255,255,255,0.04);
    border-radius: 50%;
    top: -100px;
    left: -100px;
  }

  .hero::after {
    content: '';
    position: absolute;
    width: 300px;
    height: 300px;
    background: rgba(230,126,34,0.12);
    border-radius: 50%;
    bottom: -80px;
    right: -60px;
  }

  .hero-badge {
    display: inline-block;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    color: white;
    font-size: 13px;
    font-weight: 700;
    padding: 6px 16px;
    border-radius: 20px;
    margin-bottom: 20px;
    letter-spacing: 0.5px;
  }

  .hero h1 {
    color: white;
    font-size: clamp(32px, 6vw, 56px);
    font-weight: 900;
    line-height: 1.15;
    margin-bottom: 16px;
  }

  .hero h1 span { color: var(--orange-light); }

  .hero p {
    color: rgba(255,255,255,0.85);
    font-size: clamp(15px, 2.5vw, 18px);
    max-width: 560px;
    margin: 0 auto 32px;
    line-height: 1.7;
  }

  .hero-btns {
    display: flex;
    gap: 12px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn-primary {
    background: var(--orange);
    color: white;
    border: none;
    padding: 14px 32px;
    border-radius: 12px;
    font-size: 16px;
    font-weight: 800;
    cursor: pointer;
    transition: all 0.2s;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }

  .btn-primary:hover {
    background: var(--orange-light);
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(230,126,34,0.4);
  }

  .btn-secondary {
    background: rgba(255,255,255,0.15);
    color: white;
    border: 2px solid rgba(255,255,255,0.4);
    padding: 14px 32px;
    border-radius: 12px;
    font-size: 16px;
    font-weight: 700;
    cursor: pointer;
    transition: all 0.2s;
    text-decoration: none;
  }

  .btn-secondary:hover {
    background: rgba(255,255,255,0.25);
    transform: translateY(-2px);
  }

  .hero-stats {
    display: flex;
    gap: 40px;
    justify-content: center;
    margin-top: 48px;
    flex-wrap: wrap;
  }

  .hero-stat {
    color: white;
    text-align: center;
  }

  .hero-stat .num {
    font-size: 28px;
    font-weight: 900;
    color: var(--orange-light);
    display: block;
  }

  .hero-stat .label {
    font-size: 13px;
    opacity: 0.8;
    font-weight: 600;
  }

  /* SECTION STYLES */
  section {
    padding: 56px 24px;
    max-width: 1100px;
    margin: 0 auto;
  }

  .section-header {
    text-align: center;
    margin-bottom: 40px;
  }

  .section-eyebrow {
    font-size: 12px;
    font-weight: 800;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--orange);
    margin-bottom: 10px;
  }

  .section-title {
    font-size: clamp(24px, 4vw, 36px);
    font-weight: 900;
    color: var(--ocean);
    line-height: 1.2;
  }

  .section-sub {
    font-size: 15px;
    color: var(--text-mid);
    margin-top: 10px;
    line-height: 1.7;
  }

  /* ACTIVITIES */
  .activities-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
  }

  .activity-card {
    background: white;
    border-radius: var(--radius);
    overflow: hidden;
    box-shadow: 0 2px 16px rgba(0,0,0,0.08);
    transition: all 0.3s;
    cursor: pointer;
    border: 2px solid transparent;
  }

  .activity-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 32px rgba(0,0,0,0.12);
    border-color: var(--orange-light);
  }

  .card-banner {
    height: 160px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 64px;
    position: relative;
  }

  .card-banner.bhar { background: linear-gradient(135deg, #1B4F72, #2E86C1); }
  .card-banner.jri { background: linear-gradient(135deg, #27AE60, #2ecc71); }
  .card-banner.march { background: linear-gradient(135deg, #8E44AD, #9b59b6); }
  .card-banner.velo { background: linear-gradient(135deg, #E67E22, #F39C12); }
  .card-banner.yoga { background: linear-gradient(135deg, #C0392B, #e74c3c); }
  .card-banner.tennis { background: linear-gradient(135deg, #16A085, #1abc9c); }

  .card-diff {
    position: absolute;
    top: 12px;
    left: 12px;
    padding: 4px 10px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: 800;
    color: white;
  }

  .diff-easy { background: var(--green); }
  .diff-med { background: var(--orange); }
  .diff-hard { background: #e74c3c; }

  .card-pts {
    position: absolute;
    top: 12px;
    right: 12px;
    background: rgba(0,0,0,0.4);
    color: white;
    font-size: 12px;
    font-weight: 800;
    padding: 4px 10px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    gap: 4px;
  }

  .card-body {
    padding: 20px;
  }

  .card-title {
    font-size: 19px;
    font-weight: 900;
    color: var(--ocean);
    margin-bottom: 6px;
  }

  .card-desc {
    font-size: 14px;
    color: var(--text-mid);
    line-height: 1.6;
    margin-bottom: 16px;
  }

  .card-meta {
    display: flex;
    gap: 12px;
    margin-bottom: 16px;
    flex-wrap: wrap;
  }

  .meta-tag {
    background: var(--gray-light);
    color: var(--text-mid);
    font-size: 12px;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    gap: 4px;
  }

  .card-progress {
    margin-bottom: 14px;
  }

  .progress-label {
    display: flex;
    justify-content: space-between;
    font-size: 12px;
    font-weight: 700;
    margin-bottom: 6px;
    color: var(--text-mid);
  }

  .progress-bar {
    height: 8px;
    background: var(--gray-light);
    border-radius: 4px;
    overflow: hidden;
  }

  .progress-fill {
    height: 100%;
    border-radius: 4px;
    background: linear-gradient(90deg, var(--ocean-light), var(--orange));
    transition: width 1s ease;
  }

  .card-btn {
    width: 100%;
    background: var(--ocean);
    color: white;
    border: none;
    padding: 12px;
    border-radius: 10px;
    font-size: 15px;
    font-weight: 800;
    cursor: pointer;
    transition: all 0.2s;
    font-family: inherit;
  }

  .card-btn:hover {
    background: var(--ocean-light);
    transform: scale(1.02);
  }

  /* LEADERBOARD */
  .leaderboard-section {
    background: var(--gray-light);
    border-radius: 24px;
    padding: 40px 32px;
    margin: 0 24px;
  }

  .leaderboard-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  @media (max-width: 640px) {
    .leaderboard-grid { grid-template-columns: 1fr; }
  }

  .lb-card {
    background: white;
    border-radius: var(--radius);
    overflow: hidden;
    box-shadow: 0 2px 12px rgba(0,0,0,0.07);
  }

  .lb-header {
    padding: 16px 20px;
    font-size: 16px;
    font-weight: 900;
    color: white;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .lb-header.men { background: linear-gradient(135deg, var(--ocean), var(--ocean-light)); }
  .lb-header.women { background: linear-gradient(135deg, #C0392B, #e74c3c); }

  .lb-list {
    padding: 12px 0;
  }

  .lb-item {
    display: flex;
    align-items: center;
    padding: 10px 20px;
    gap: 12px;
    transition: background 0.2s;
  }

  .lb-item:hover { background: var(--gray-light); }

  .lb-rank {
    width: 28px;
    height: 28px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    font-weight: 900;
    flex-shrink: 0;
  }

  .rank-1 { background: #FFD700; color: #333; }
  .rank-2 { background: #C0C0C0; color: #333; }
  .rank-3 { background: #CD7F32; color: white; }
  .rank-other { background: var(--gray-light); color: var(--text-mid); }

  .lb-avatar {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    flex-shrink: 0;
  }

  .lb-name {
    flex: 1;
    font-size: 14px;
    font-weight: 700;
    color: var(--text-dark);
  }

  .lb-pts {
    font-size: 14px;
    font-weight: 900;
    color: var(--orange);
  }

  /* CHALLENGES */
  .challenges-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 16px;
  }

  .challenge-card {
    background: white;
    border-radius: var(--radius);
    padding: 24px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.07);
    border-right: 4px solid var(--orange);
    transition: all 0.2s;
  }

  .challenge-card:hover {
    transform: translateX(-4px);
    box-shadow: 0 8px 24px rgba(0,0,0,0.1);
  }

  .challenge-icon {
    font-size: 36px;
    margin-bottom: 12px;
  }

  .challenge-title {
    font-size: 17px;
    font-weight: 900;
    color: var(--ocean);
    margin-bottom: 8px;
  }

  .challenge-desc {
    font-size: 13px;
    color: var(--text-mid);
    line-height: 1.6;
    margin-bottom: 16px;
  }

  .challenge-reward {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .reward-pts {
    background: var(--orange);
    color: white;
    font-size: 13px;
    font-weight: 900;
    padding: 5px 12px;
    border-radius: 20px;
  }

  .challenge-timer {
    font-size: 12px;
    color: var(--text-mid);
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 4px;
  }

  /* BADGES */
  .badges-grid {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .badge-item {
    text-align: center;
    width: 100px;
  }

  .badge-icon {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    margin: 0 auto 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    transition: transform 0.2s;
  }

  .badge-icon:hover { transform: scale(1.1) rotate(5deg); }

  .badge-item.locked .badge-icon { filter: grayscale(1); opacity: 0.4; }

  .badge-name {
    font-size: 12px;
    font-weight: 700;
    color: var(--text-mid);
  }

  /* PROFILE WIDGET */
  .profile-widget {
    background: linear-gradient(135deg, var(--ocean), var(--ocean-light));
    border-radius: 20px;
    padding: 32px;
    color: white;
    display: flex;
    align-items: center;
    gap: 24px;
    margin: 0 24px 40px;
    flex-wrap: wrap;
  }

  .profile-avatar {
    width: 80px;
    height: 80px;
    background: rgba(255,255,255,0.2);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 40px;
    flex-shrink: 0;
  }

  .profile-info { flex: 1; }

  .profile-name {
    font-size: 22px;
    font-weight: 900;
    margin-bottom: 4px;
  }

  .profile-level {
    font-size: 13px;
    opacity: 0.8;
    margin-bottom: 12px;
  }

  .level-bar {
    height: 10px;
    background: rgba(255,255,255,0.2);
    border-radius: 5px;
    overflow: hidden;
    max-width: 280px;
  }

  .level-fill {
    height: 100%;
    background: var(--orange);
    border-radius: 5px;
    width: 68%;
  }

  .profile-stats {
    display: flex;
    gap: 24px;
    flex-wrap: wrap;
  }

  .p-stat {
    text-align: center;
  }

  .p-stat .num {
    font-size: 26px;
    font-weight: 900;
    color: var(--orange-light);
    display: block;
  }

  .p-stat .label {
    font-size: 12px;
    opacity: 0.8;
  }

  /* FOOTER */
  footer {
    background: var(--ocean);
    color: rgba(255,255,255,0.7);
    text-align: center;
    padding: 32px 24px;
    font-size: 14px;
  }

  footer strong {
    color: var(--orange-light);
    font-weight: 900;
  }

  /* MODAL */
  .modal-overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.6);
    z-index: 200;
    align-items: center;
    justify-content: center;
    padding: 20px;
  }

  .modal-overlay.open { display: flex; }

  .modal {
    background: white;
    border-radius: 20px;
    padding: 32px;
    max-width: 480px;
    width: 100%;
    position: relative;
    animation: slideUp 0.3s ease;
  }

  @keyframes slideUp {
    from { transform: translateY(30px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
  }

  .modal-close {
    position: absolute;
    top: 16px;
    left: 16px;
    background: var(--gray-light);
    border: none;
    width: 32px;
    height: 32px;
    border-radius: 50%;
    font-size: 16px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .modal-title {
    font-size: 24px;
    font-weight: 900;
    color: var(--ocean);
    margin-bottom: 8px;
  }

  .modal-body {
    font-size: 15px;
    color: var(--text-mid);
    line-height: 1.7;
    margin-bottom: 24px;
  }

  .modal-pts-badge {
    background: linear-gradient(135deg, var(--orange), var(--orange-light));
    color: white;
    border-radius: 12px;
    padding: 16px 24px;
    text-align: center;
    margin-bottom: 20px;
    font-size: 28px;
    font-weight: 900;
  }

  .modal-pts-badge small {
    display: block;
    font-size: 13px;
    opacity: 0.85;
    font-weight: 600;
  }

  /* TOAST */
  .toast {
    position: fixed;
    bottom: 24px;
    left: 50%;
    transform: translateX(-50%) translateY(80px);
    background: var(--green);
    color: white;
    padding: 14px 24px;
    border-radius: 12px;
    font-weight: 800;
    font-size: 15px;
    z-index: 300;
    transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
    white-space: nowrap;
  }

  .toast.show { transform: translateX(-50%) translateY(0); }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    nav .nav-links { display: none; }
    .leaderboard-section { margin: 0 12px; }
    .profile-widget { margin: 0 12px 32px; }
    section { padding: 40px 16px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="logo">
    <div class="logo-icon">🏃</div>
    <span class="logo-text">نشا<span>طو</span></span>
  </a>
  <ul class="nav-links">
    <li><a href="#activites" class="active">الأنشطة</a></li>
    <li><a href="#challenges">التحديات</a></li>
    <li><a href="#leaderboard">الترتيب</a></li>
    <li><a href="#badges">الشارات</a></li>
  </ul>
  <div class="nav-points" onclick="showToast('⭐ عندك 1,240 نقطة!')">
    ⭐ <span id="total-pts">1,240</span> نقطة
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-badge">💪 للراجل والعيلة — ابدا دابا!</div>
  <h1>تحرك مع <span>الفاميلة</span><br>واكسب نقاط!</h1>
  <p>سواسلك تطبيق فيه كل أنشطة البحر والجري والمارش — بالدارجة، لأننا ماشيين مع بعضياتنا 🤝</p>
  <div class="hero-btns">
    <a href="#activites" class="btn-primary">🚀 ابدا الآن</a>
    <a href="#leaderboard" class="btn-secondary">🏆 شوف الترتيب</a>
  </div>
  <div class="hero-stats">
    <div class="hero-stat">
      <span class="num">3,400+</span>
      <span class="label">ناس فالحي</span>
    </div>
    <div class="hero-stat">
      <span class="num">6</span>
      <span class="label">نوع نشاط</span>
    </div>
    <div class="hero-stat">
      <span class="num">50K+</span>
      <span class="label">كيلو متحاربين</span>
    </div>
    <div class="hero-stat">
      <span class="num">1M+</span>
      <span class="label">نقطة موزعة</span>
    </div>
  </div>
</div>

<!-- PROFILE WIDGET -->
<div style="padding: 40px 24px 0; max-width: 1100px; margin: 0 auto;">
  <div class="profile-widget">
    <div class="profile-avatar">👨</div>
    <div class="profile-info">
      <div class="profile-name">أحمد العمراني</div>
      <div class="profile-level">المستوى 7 — رياضي محترف ⬆️ 340 نقطة للمستوى 8</div>
      <div class="level-bar"><div class="level-fill"></div></div>
    </div>
    <div class="profile-stats">
      <div class="p-stat">
        <span class="num">1,240</span>
        <span class="label">نقطة هاد الأسبوع</span>
      </div>
      <div class="p-stat">
        <span class="num">23</span>
        <span class="label">نشاط كمل</span>
      </div>
      <div class="p-stat">
        <span class="num">8</span>
        <span class="label">شارة كسب</span>
      </div>
    </div>
  </div>
</div>

<!-- ACTIVITIES -->
<section id="activites">
  <div class="section-header">
    <div class="section-eyebrow">🏅 الأنشطة</div>
    <div class="section-title">اختار نشاطك وابدا تجمع نقاط</div>
    <div class="section-sub">كل نشاط بنقاط مختلفة — كلما زدت كلما كسبتي أكتر!</div>
  </div>

  <div class="activities-grid">

    <!-- BHAR -->
    <div class="activity-card" onclick="openModal('bhar')">
      <div class="card-banner bhar">
        🏊‍♂️
        <div class="card-diff diff-med">متوسط</div>
        <div class="card-pts">⭐ 150 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">السباحة فالبحر 🌊</div>
        <div class="card-desc">سبح 30 دقيقة فالبحر مع الاهتمام بالسلامة. مزيان للقلب والعضلات.</div>
        <div class="card-meta">
          <span class="meta-tag">⏱ 30 دقيقة</span>
          <span class="meta-tag">👨‍👩‍👧 للفاميلة</span>
          <span class="meta-tag">🌅 صباح-مساء</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>3/5 جلسات</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:60%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

    <!-- JRI -->
    <div class="activity-card" onclick="openModal('jri')">
      <div class="card-banner jri">
        🏃‍♂️
        <div class="card-diff diff-easy">سهل</div>
        <div class="card-pts">⭐ 100 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">الجري الصباحي 🌄</div>
        <div class="card-desc">قبل الفطور — جر 3 كيلو. كل خطوة كتحسب وكتعطيك نقاط!</div>
        <div class="card-meta">
          <span class="meta-tag">📍 3 كيلو</span>
          <span class="meta-tag">🕕 صباح</span>
          <span class="meta-tag">👟 وحدك أو جماعة</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>4/7 أيام</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:57%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

    <!-- MARCH -->
    <div class="activity-card" onclick="openModal('march')">
      <div class="card-banner march">
        🚶‍♂️
        <div class="card-diff diff-easy">سهل</div>
        <div class="card-pts">⭐ 80 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">المارش العائلي 👨‍👩‍👧‍👦</div>
        <div class="card-desc">مشي مع العيال 5 كيلو — حتى الجنان أو كورنيش. راحة للجميع!</div>
        <div class="card-meta">
          <span class="meta-tag">📍 5 كيلو</span>
          <span class="meta-tag">👨‍👩‍👧‍👦 مع العيلة</span>
          <span class="meta-tag">🌳 طبيعة</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>2/4 مرات</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:50%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

    <!-- VELO -->
    <div class="activity-card" onclick="openModal('velo')">
      <div class="card-banner velo">
        🚴‍♂️
        <div class="card-diff diff-med">متوسط</div>
        <div class="card-pts">⭐ 120 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">الدراجة مع الدراري 🚴</div>
        <div class="card-desc">جولة بالفيلو مع الأولاد — 10 كيلو مغامرة وضحك وصحة!</div>
        <div class="card-meta">
          <span class="meta-tag">📍 10 كيلو</span>
          <span class="meta-tag">👦👧 + الدراري</span>
          <span class="meta-tag">🎒 نزهة</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>1/3 جلسات</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:33%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

    <!-- YOGA -->
    <div class="activity-card" onclick="openModal('yoga')">
      <div class="card-banner yoga">
        🧘‍♂️
        <div class="card-diff diff-easy">سهل</div>
        <div class="card-pts">⭐ 90 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">اليوغا والاسترخاء 🌸</div>
        <div class="card-desc">20 دقيقة صباح أو مساء — للمرأة والراجل. ذهن وجسم مرتاحين.</div>
        <div class="card-meta">
          <span class="meta-tag">⏱ 20 دقيقة</span>
          <span class="meta-tag">🏠 فالدار</span>
          <span class="meta-tag">🌙 صباح/مساء</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>5/7 أيام</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:71%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

    <!-- TENNIS -->
    <div class="activity-card" onclick="openModal('tennis')">
      <div class="card-banner tennis">
        🎾
        <div class="card-diff diff-hard">صعيب</div>
        <div class="card-pts">⭐ 200 نقطة</div>
      </div>
      <div class="card-body">
        <div class="card-title">التنس العائلي 🎾</div>
        <div class="card-desc">ماتش مع المرأة أو الكبار — ساعة من الضحك والتنافس الحلو!</div>
        <div class="card-meta">
          <span class="meta-tag">⏱ 1 ساعة</span>
          <span class="meta-tag">🎾 ملعب</span>
          <span class="meta-tag">👫 ثنائي</span>
        </div>
        <div class="card-progress">
          <div class="progress-label">
            <span>تقدمك هاد الأسبوع</span>
            <span>0/2 ماتشات</span>
          </div>
          <div class="progress-bar"><div class="progress-fill" style="width:0%"></div></div>
        </div>
        <button class="card-btn">✅ سجل نشاطك</button>
      </div>
    </div>

  </div>
</section>

<!-- CHALLENGES -->
<section id="challenges">
  <div class="section-header">
    <div class="section-eyebrow">🔥 التحديات</div>
    <div class="section-title">تحديات هاد الأسبوع</div>
    <div class="section-sub">كمّل التحدي واكسب نقاط إضافية — التحديات كتتجدد كل أسبوع!</div>
  </div>
  <div class="challenges-grid">
    <div class="challenge-card">
      <div class="challenge-icon">🌊</div>
      <div class="challenge-title">أسبوع البحر</div>
      <div class="challenge-desc">سبح 5 مرات هاد الأسبوع. ولا مشكلة إلا البحر والشمس!</div>
      <div class="challenge-reward">
        <span class="reward-pts">⭐ +500 نقطة</span>
        <span class="challenge-timer">⏳ 3 أيام باقيين</span>
      </div>
    </div>
    <div class="challenge-card">
      <div class="challenge-icon">👨‍👩‍👧‍👦</div>
      <div class="challenge-title">الفاميلة كاملة تمشي</div>
      <div class="challenge-desc">مشي مع الزوجة والدراري مرتين هاد الأسبوع — بلا عذر!</div>
      <div class="challenge-reward">
        <span class="reward-pts">⭐ +300 نقطة</span>
        <span class="challenge-timer">⏳ 5 أيام باقيين</span>
      </div>
    </div>
    <div class="challenge-card">
      <div class="challenge-icon">🌅</div>
      <div class="challenge-title">الجري قبل الفطور</div>
      <div class="challenge-desc">جر 3 كيلو 7 أيام فالصباح — كتحس بفرق كبير!</div>
      <div class="challenge-reward">
        <span class="reward-pts">⭐ +700 نقطة</span>
        <span class="challenge-timer">⏳ أسبوع كامل</span>
      </div>
    </div>
    <div class="challenge-card">
      <div class="challenge-icon">🚴‍♂️</div>
      <div class="challenge-title">الفيلو يوم السبت</div>
      <div class="challenge-desc">جولة الفيلو العائلية كل سبت — وين بغيتي فالمدينة!</div>
      <div class="challenge-reward">
        <span class="reward-pts">⭐ +250 نقطة</span>
        <span class="challenge-timer">⏳ يوم واحد</span>
      </div>
    </div>
  </div>
</section>

<!-- LEADERBOARD -->
<div style="max-width: 1100px; margin: 0 auto; padding: 0 24px 40px;">
  <div class="leaderboard-section" id="leaderboard">
    <div class="section-header" style="margin-bottom: 28px;">
      <div class="section-eyebrow">🏆 الترتيب</div>
      <div class="section-title">ترتيب هاد الأسبوع</div>
      <div class="section-sub">شوف فين واقف — الأول كياخد جائزة مفاجأة! 🎁</div>
    </div>
    <div class="leaderboard-grid">
      <!-- MEN -->
      <div class="lb-card">
        <div class="lb-header men">🏃‍♂️ الرجال</div>
        <div class="lb-list">
          <div class="lb-item">
            <div class="lb-rank rank-1">🥇</div>
            <div class="lb-avatar" style="background:#FFF9C4">👨</div>
            <div class="lb-name">كريم البقالي</div>
            <div class="lb-pts">2,840 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-2">🥈</div>
            <div class="lb-avatar" style="background:#F3E5F5">👨‍🦱</div>
            <div class="lb-name">يوسف الكسار</div>
            <div class="lb-pts">2,510 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-3">🥉</div>
            <div class="lb-avatar" style="background:#E8F5E9">👦</div>
            <div class="lb-name">محمد المنصوري</div>
            <div class="lb-pts">2,200 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-other">4</div>
            <div class="lb-avatar" style="background:#E3F2FD">👨‍🦳</div>
            <div class="lb-name">أحمد العمراني (أنت)</div>
            <div class="lb-pts">1,240 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-other">5</div>
            <div class="lb-avatar" style="background:#FBE9E7">🧔</div>
            <div class="lb-name">إلياس الزياني</div>
            <div class="lb-pts">980 ⭐</div>
          </div>
        </div>
      </div>
      <!-- WOMEN -->
      <div class="lb-card">
        <div class="lb-header women">🏃‍♀️ النساء</div>
        <div class="lb-list">
          <div class="lb-item">
            <div class="lb-rank rank-1">🥇</div>
            <div class="lb-avatar" style="background:#FCE4EC">👩</div>
            <div class="lb-name">سناء الراضي</div>
            <div class="lb-pts">3,120 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-2">🥈</div>
            <div class="lb-avatar" style="background:#E8EAF6">👩‍🦱</div>
            <div class="lb-name">أمينة بنحمو</div>
            <div class="lb-pts">2,760 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-3">🥉</div>
            <div class="lb-avatar" style="background:#E0F7FA">👩‍🦰</div>
            <div class="lb-name">فاطمة الزهري</div>
            <div class="lb-pts">2,400 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-other">4</div>
            <div class="lb-avatar" style="background:#F3E5F5">👱‍♀️</div>
            <div class="lb-name">نجاة المسعودي</div>
            <div class="lb-pts">1,890 ⭐</div>
          </div>
          <div class="lb-item">
            <div class="lb-rank rank-other">5</div>
            <div class="lb-avatar" style="background:#FFF8E1">👩‍🦳</div>
            <div class="lb-name">لطيفة بلخير</div>
            <div class="lb-pts">1,560 ⭐</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- BADGES -->
<section id="badges">
  <div class="section-header">
    <div class="section-eyebrow">🎖 الشارات</div>
    <div class="section-title">شاراتك — كسبتي هادي!</div>
    <div class="section-sub">كل إنجاز عندو شارة خاصة. كلما تحركتي كلما ملّيتي الكولاج!</div>
  </div>
  <div class="badges-grid">
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#1B4F72,#2E86C1)">🏊‍♂️</div>
      <div class="badge-name">سباح البحر</div>
    </div>
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#27AE60,#2ecc71)">🌅</div>
      <div class="badge-name">الباكرجي</div>
    </div>
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#E67E22,#F39C12)">🔥</div>
      <div class="badge-name">7 أيام موالية</div>
    </div>
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#8E44AD,#9b59b6)">👨‍👩‍👧‍👦</div>
      <div class="badge-name">بطل الفاميلة</div>
    </div>
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#FFD700,#FFA500)">⭐</div>
      <div class="badge-name">1000 نقطة</div>
    </div>
    <div class="badge-item">
      <div class="badge-icon" style="background: linear-gradient(135deg,#C0392B,#e74c3c)">🎾</div>
      <div class="badge-name">تنسوي</div>
    </div>
    <div class="badge-item locked">
      <div class="badge-icon" style="background: linear-gradient(135deg,#16A085,#1abc9c)">🚴‍♂️</div>
      <div class="badge-name">فارس الدرب</div>
    </div>
    <div class="badge-item locked">
      <div class="badge-icon" style="background: linear-gradient(135deg,#2C3E50,#34495e)">🏆</div>
      <div class="badge-name">الأول شهرياً</div>
    </div>
    <div class="badge-item locked">
      <div class="badge-icon" style="background: linear-gradient(135deg,#7F8C8D,#95a5a6)">💎</div>
      <div class="badge-name">ماسي</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div style="font-size: 28px; margin-bottom: 10px;">🏃‍♂️ نشاطو</div>
  <p>صنع بـ ❤️ للعائلة المغربية — <strong>نتحركو مع بعضياتنا!</strong></p>
  <p style="margin-top: 8px; font-size: 12px; opacity: 0.5;">© 2025 نشاطو — حقوق محفوظة</p>
</footer>

<!-- MODAL -->
<div class="modal-overlay" id="modal" onclick="closeModalOut(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div id="modal-content"></div>
  </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
  const activities = {
    bhar: {
      emoji: '🏊‍♂️', title: 'السباحة فالبحر', pts: 150,
      desc: 'السباحة فالبحر هي من أحسن الرياضات للجسم كامل. تقوي القلب والرئتين والعضلات. سبح 30 دقيقة الصباح أو المساء مع الاهتمام بسلامة الدراري دايما.',
      tips: ['🌊 ابدا بالمياه الهادئة', '☀️ تجنب الشمس بين 12 و3', '🧴 دير الكريم قبل الخروج', '👀 ما تخليش الدراري بوحدهم']
    },
    jri: {
      emoji: '🏃‍♂️', title: 'الجري الصباحي', pts: 100,
      desc: 'الجري قبل الفطور كيحرق الدهون أكتر. 3 كيلومترات فالأحياء أو الغابة — ابدا بالمشي سريع وكل أسبوع زيد شوية.',
      tips: ['⏰ قوم باكر واجري', '💧 اشرب ماء قبل وبعد', '👟 حذاء مريح ضروري', '📱 تتبع الكيلومترات']
    },
    march: {
      emoji: '🚶‍♂️', title: 'المارش العائلي', pts: 80,
      desc: 'مشي 5 كيلو مع الزوجة والدراري يوم العطلة — للكورنيش أو الجنان. مزيان للصحة ولقوت مع بعضياتنا.',
      tips: ['🎒 خذ بيك ماء وفاكهة', '📍 اختار طريق زين', '🎮 خلي الدراري يلعبو فالطبيعة', '📸 خذ تصاور مع بعضياتنا']
    },
    velo: {
      emoji: '🚴‍♂️', title: 'الدراجة مع الدراري', pts: 120,
      desc: 'جولة 10 كيلو بالفيلو يوم السبت — أو في أي وقت! مناسبة للدراري اللي من 6 سنين فما فوق.',
      tips: ['⛑️ خوذة للجميع', '🛠️ تحقق من التيرات', '🛣️ اختار الطريق الهادئة', '🎉 كل ما بلغتو نقطة احتفلو']
    },
    yoga: {
      emoji: '🧘‍♂️', title: 'اليوغا والاسترخاء', pts: 90,
      desc: '20 دقيقة فالدار — على الحصيرة فالصالون أو الحديقة. للمرأة والراجل سواسية. كتخفف الضغط وكتحسن النوم.',
      tips: ['🌅 الصباح أحسن وقت', '📵 بعيد على الهاتف', '🎵 موسيقى هادئة', '👶 الدراري الكبار يقدرو يشاركو']
    },
    tennis: {
      emoji: '🎾', title: 'التنس العائلي', pts: 200,
      desc: 'ماتش ساعة مع الزوجة أو صاحبك — رياضة كاملة، ضحك كثير، وتنافس حلو. كتبنيو العلاقات وكتجمع النقاط!',
      tips: ['🎾 الملاعب البلدية برخص', '👟 حذاء تنس ضروري', '☀️ الصباح أو المساء أحسن', '🥤 خذ ماء كافي معك']
    }
  };

  let currentPts = 1240;

  function openModal(key) {
    const act = activities[key];
    document.getElementById('modal-content').innerHTML = `
      <div style="font-size:56px; text-align:center; margin-bottom:16px">${act.emoji}</div>
      <div class="modal-title">${act.title}</div>
      <div class="modal-pts-badge">
        +${act.pts} نقطة
        <small>كتكسبهم فور ما تسجل</small>
      </div>
      <div class="modal-body">${act.desc}</div>
      <div style="margin-bottom:20px">
        <div style="font-weight:800; color:var(--ocean); margin-bottom:10px">💡 نصائح مهمة:</div>
        ${act.tips.map(t => `<div style="padding:6px 0; font-size:14px; color:var(--text-mid)">${t}</div>`).join('')}
      </div>
      <button class="btn-primary" style="width:100%; justify-content:center" onclick="recordActivity(${act.pts}, '${act.title}')">
        ✅ سجل النشاط الآن (+${act.pts} ⭐)
      </button>
    `;
    document.getElementById('modal').classList.add('open');
  }

  function closeModal() {
    document.getElementById('modal').classList.remove('open');
  }

  function closeModalOut(e) {
    if (e.target === document.getElementById('modal')) closeModal();
  }

  function recordActivity(pts, name) {
    closeModal();
    currentPts += pts;
    document.getElementById('total-pts').textContent = currentPts.toLocaleString('ar-MA');
    showToast(`🎉 برافو! كسبتي +${pts} نقطة للـ"${name}"!`);
  }

  function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 3500);
  }

  // Animate progress bars on scroll
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) e.target.style.width = e.target.getAttribute('data-width') || e.target.style.width;
    });
  });
</script>
</body>
</html>
