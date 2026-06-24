<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Кабинет — мебель для офиса</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --walnut:#2E2118;
    --beige:#EDE3D0;
    --paper:#FAF6EE;
    --charcoal:#2B2620;
    --sage:#76876B;
    --brass:#B08C56;
    --line: rgba(43,38,32,0.16);
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--charcoal);
    font-family:'Inter', sans-serif;
    -webkit-font-smoothing:antialiased;
  }

  .wrap{max-width:1120px;margin:0 auto;padding:0 32px;}

  a{color:inherit;}

  /* ---------- Header ---------- */
  header{
    position:sticky;top:0;z-index:50;
    background:rgba(250,246,238,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  .nav{
    display:flex;align-items:center;justify-content:space-between;
    padding:20px 32px;
  }
  .logo{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:22px;
    letter-spacing:0.01em;
  }
  .logo span{color:var(--sage);}
  .nav-links{display:flex;gap:32px;font-size:14px;}
  .nav-links a{text-decoration:none;color:var(--charcoal);opacity:0.75;transition:opacity .2s;}
  .nav-links a:hover{opacity:1;}
  .nav-cta{
    font-size:13px;
    border:1px solid var(--charcoal);
    padding:9px 18px;
    border-radius:999px;
    text-decoration:none;
    transition:background .2s,color .2s;
  }
  .nav-cta:hover{background:var(--charcoal);color:var(--paper);}

  /* ---------- Hero ---------- */
  .hero{
    padding:96px 0 64px;
    display:grid;
    grid-template-columns:1.1fr 0.9fr;
    gap:48px;
    align-items:center;
  }
  .eyebrow{
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--sage);
    margin:0 0 18px;
  }
  h1{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:clamp(38px,5vw,60px);
    line-height:1.05;
    margin:0 0 24px;
    letter-spacing:-0.01em;
  }
  h1 em{
    font-style:italic;
    color:var(--sage);
  }
  .hero p{
    font-size:17px;
    line-height:1.6;
    color:rgba(43,38,32,0.78);
    max-width:480px;
    margin:0 0 32px;
  }
  .hero-actions{display:flex;gap:14px;flex-wrap:wrap;}
  .btn{
    font-size:14px;font-weight:500;
    padding:13px 24px;
    border-radius:8px;
    text-decoration:none;
    display:inline-flex;align-items:center;gap:8px;
    transition:transform .15s, box-shadow .15s;
  }
  .btn-primary{background:var(--charcoal);color:var(--paper);}
  .btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 18px rgba(43,38,32,0.22);}
  .btn-ghost{border:1px solid var(--line);color:var(--charcoal);}
  .btn-ghost:hover{border-color:var(--charcoal);}

  .hero-art{display:flex;justify-content:center;}
  .hero-art svg{width:100%;max-width:380px;}

  /* ---------- Strip ---------- */
  .strip{
    border-top:1px solid var(--line);
    border-bottom:1px solid var(--line);
    background:var(--beige);
  }
  .strip .wrap{
    display:flex;
    justify-content:space-between;
    padding:18px 32px;
    font-family:'JetBrains Mono', monospace;
    font-size:12px;
    letter-spacing:0.04em;
    color:rgba(43,38,32,0.65);
    flex-wrap:wrap;
    gap:8px 24px;
  }

  /* ---------- Features ---------- */
  .features{padding:88px 0;}
  .section-head{margin-bottom:48px;max-width:560px;}
  .section-head .eyebrow{margin-bottom:14px;}
  .section-head h2{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:clamp(28px,3.4vw,38px);
    margin:0;
    line-height:1.15;
  }
  .feature-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .feature{
    background:var(--paper);
    padding:32px 28px;
  }
  .feature .mark{
    width:34px;height:34px;
    margin-bottom:20px;
  }
  .feature h3{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:19px;
    margin:0 0 10px;
  }
  .feature p{
    font-size:14.5px;
    line-height:1.6;
    color:rgba(43,38,32,0.72);
    margin:0;
  }

  /* ---------- Download / hangtags ---------- */
  .download{
    padding:96px 0 110px;
    background:var(--walnut);
    color:var(--paper);
  }
  .download .section-head h2{color:var(--paper);}
  .download .section-head p{
    color:rgba(250,246,238,0.65);
    font-size:15.5px;
    margin-top:14px;
    max-width:520px;
    line-height:1.6;
  }
  .tags{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:28px;
  }
  .tag{
    position:relative;
    background:var(--paper);
    color:var(--charcoal);
    border-radius:4px;
    padding:30px 28px 28px;
    border:1px solid rgba(43,38,32,0.08);
  }
  .tag::before{
    content:"";
    position:absolute;
    top:22px;left:22px;
    width:14px;height:14px;
    border-radius:50%;
    background:var(--walnut);
    box-shadow:inset 0 0 0 3px var(--paper);
  }
  .tag.disabled{
    opacity:0.55;
  }
  .tag-top{
    display:flex;justify-content:space-between;align-items:flex-start;
    margin-left:34px;
    margin-bottom:22px;
  }
  .tag-platform{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:24px;
  }
  .tag-badge{
    font-family:'JetBrains Mono', monospace;
    font-size:11px;
    letter-spacing:0.06em;
    text-transform:uppercase;
    padding:5px 10px;
    border-radius:999px;
    background:var(--beige);
    color:var(--walnut);
    white-space:nowrap;
  }
  .tag-badge.soon{background:rgba(43,38,32,0.08);color:rgba(43,38,32,0.55);}
  .specs{
    margin-left:34px;
    border-top:1px dashed var(--line);
    border-bottom:1px dashed var(--line);
    padding:14px 0;
    margin-bottom:22px;
  }
  .spec-row{
    display:flex;justify-content:space-between;
    font-family:'JetBrains Mono', monospace;
    font-size:12.5px;
    padding:4px 0;
    color:rgba(43,38,32,0.7);
  }
  .spec-row b{color:var(--charcoal);font-weight:500;}
  .tag-cta{
    margin-left:34px;
    display:flex;
  }
  .tag-cta .btn-primary{width:100%;justify-content:center;background:var(--walnut);}
  .tag-cta .btn-primary:hover{box-shadow:0 8px 18px rgba(0,0,0,0.25);}
  .tag-cta .btn-disabled{
    width:100%;justify-content:center;
    background:rgba(43,38,32,0.08);
    color:rgba(43,38,32,0.45);
    cursor:not-allowed;
  }
  .tag-note{
    margin-left:34px;
    margin-top:12px;
    font-size:12.5px;
    color:rgba(43,38,32,0.55);
    line-height:1.5;
  }

  /* ---------- Footer ---------- */
  footer{
    padding:36px 0;
    background:var(--beige);
  }
  .footer-row{
    display:flex;justify-content:space-between;align-items:center;
    flex-wrap:wrap;gap:12px;
    font-size:13px;
    color:rgba(43,38,32,0.6);
  }

  @media (max-width:860px){
    .hero{grid-template-columns:1fr;padding-top:64px;}
    .hero-art{order:-1;}
    .feature-grid{grid-template-columns:1fr;}
    .tags{grid-template-columns:1fr;}
    .nav-links{display:none;}
  }

  :focus-visible{outline:2px solid var(--sage);outline-offset:2px;}
  @media (prefers-reduced-motion:reduce){*{transition:none!important;}}
</style>
</head>
<body>

<header>
  <div class="nav wrap" style="padding:20px 0;">
    <div class="logo">Каби<span>нет</span></div>
    <nav class="nav-links">
      <a href="#features">Приложение</a>
      <a href="#download">Скачать</a>
      <a href="#footer">Контакты</a>
    </nav>
    <a class="nav-cta" href="#download">Скачать приложение</a>
  </div>
</header>

<section class="hero">
  <div class="wrap" style="display:contents;">
    <div>
      <p class="eyebrow">Магазин офисной мебели</p>
      <h1>Мебель для&nbsp;кабинета —<br>теперь и в&nbsp;<em>приложении</em></h1>
      <p>Каталог столов, кресел и систем хранения, расчёт стоимости и оформление заказа — всё то же, что в шоуруме, но на вашем телефоне или компьютере.</p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="#download">Скачать приложение</a>
        <a class="btn btn-ghost" href="#features">Что внутри</a>
      </div>
    </div>
    <div class="hero-art">
      <svg viewBox="0 0 360 320" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="40" y="170" width="220" height="10" rx="2" fill="#2E2118"/>
        <rect x="55" y="180" width="10" height="70" fill="#2E2118"/>
        <rect x="235" y="180" width="10" height="70" fill="#2E2118"/>
        <rect x="60" y="120" width="150" height="50" rx="3" fill="#B08C56"/>
        <rect x="60" y="120" width="150" height="50" rx="3" stroke="#2E2118" stroke-width="2"/>
        <line x1="135" y1="120" x2="135" y2="170" stroke="#2E2118" stroke-width="1.5"/>
        <circle cx="280" cy="150" r="36" fill="#76876B"/>
        <rect x="262" y="186" width="36" height="46" rx="4" fill="#76876B"/>
        <rect x="270" y="232" width="6" height="36" fill="#2E2118"/>
        <rect x="284" y="232" width="6" height="36" fill="#2E2118"/>
        <path d="M252 150 Q280 110 308 150" stroke="#2E2118" stroke-width="2" fill="none"/>
        <rect x="30" y="270" width="300" height="3" fill="#2B2620" opacity="0.15"/>
      </svg>
    </div>
  </div>
</section>

<div class="strip">
  <div class="wrap">
    <span>android · apk</span>
    <span>windows · exe</span>
    <span>каталог обновляется еженедельно</span>
  </div>
</div>

<section class="features" id="features">
  <div class="wrap">
    <div class="section-head">
      <p class="eyebrow">Приложение</p>
      <h2>Один каталог. Любой экран.</h2>
    </div>
    <div class="feature-grid">
      <div class="feature">
        <svg class="mark" viewBox="0 0 34 34"><rect x="3" y="3" width="28" height="28" rx="4" fill="none" stroke="#76876B" stroke-width="2"/><line x1="3" y1="13" x2="31" y2="13" stroke="#76876B" stroke-width="2"/></svg>
        <h3>Каталог мебели</h3>
        <p>Столы, кресла, шкафы и стеллажи с фото, размерами и материалами — фильтруйте по типу помещения и бюджету.</p>
      </div>
      <div class="feature">
        <svg class="mark" viewBox="0 0 34 34"><circle cx="17" cy="17" r="14" fill="none" stroke="#76876B" stroke-width="2"/><path d="M17 9v8l6 4" stroke="#76876B" stroke-width="2" fill="none"/></svg>
        <h3>Расчёт и заказ</h3>
        <p>Соберите комплект мебели для кабинета, увидьте итоговую сумму и сроки поставки — без звонков в шоурум.</p>
      </div>
      <div class="feature">
        <svg class="mark" viewBox="0 0 34 34"><path d="M5 25l8-14 6 9 4-6 6 11" stroke="#76876B" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round"/></svg>
        <h3>Статус доставки</h3>
        <p>Следите за сборкой и доставкой заказа в реальном времени, прямо из приложения.</p>
      </div>
    </div>
  </div>
</section>

<section class="download" id="download">
  <div class="wrap">
    <div class="section-head">
      <p class="eyebrow">Скачать</p>
      <h2>Выберите версию приложения</h2>
      <p>Установочные файлы для Android и Windows. Размер и версия указаны на ярлыке каждого файла.</p>
    </div>

    <div class="tags">
      <div class="tag">
        <div class="tag-top">
          <div class="tag-platform">Android</div>
          <div class="tag-badge">apk</div>
        </div>
        <div class="specs">
          <div class="spec-row"><span>Версия</span><b>1.0 (debug)</b></div>
          <div class="spec-row"><span>Размер файла</span><b>5,7 МБ</b></div>
          <div class="spec-row"><span>Требования</span><b>Android 8.0+</b></div>
        </div>
        <div class="tag-cta">
          <a class="btn btn-primary" href="https://disk.yandex.ru/d/D86RqiIX6Iqrow" target="_blank" rel="noopener noreferrer">Скачать APK</a>
        </div>
        <div class="tag-note">Файл из неизвестного источника — перед установкой разрешите загрузку из «сторонних источников» в настройках телефона.</div>
      </div>

      <div class="tag">
        <div class="tag-top">
          <div class="tag-platform">Windows</div>
          <div class="tag-badge">exe</div>
        </div>
        <div class="specs">
          <div class="spec-row"><span>Версия</span><b>1.0</b></div>
          <div class="spec-row"><span>Размер файла</span><b>—</b></div>
          <div class="spec-row"><span>Требования</span><b>Windows 10+</b></div>
        </div>
        <div class="tag-cta">
          <a class="btn btn-primary" href="https://disk.yandex.ru/d/zehl0wnasdEW1A" target="_blank" rel="noopener noreferrer">Скачать EXE</a>
        </div>
        <div class="tag-note">Версия для Windows. Запустите установочный файл после скачивания.</div>
      </div>
    </div>
  </div>
</section>

<footer id="footer">
  <div class="wrap footer-row">
    <span>© 2026 Кабинет — магазин офисной мебели</span>
    <span>Москва · ул. Складская, 14</span>
  </div>
</footer>

</body>
</html>
