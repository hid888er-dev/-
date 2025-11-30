<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Мой сайт — Название компании</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --accent:#7c3aed; --muted:#94a3b8; --glass: rgba(255,255,255,0.04);
      --radius:14px; --shadow: 0 6px 24px rgba(2,6,23,0.6);
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:linear-gradient(180deg,var(--bg) 0%, #071028 100%);color:#e6eef8}
    a{color:inherit;text-decoration:none}
    .container{max-width:1100px;margin:0 auto;padding:28px}

    /* Header */
    header{display:flex;align-items:center;justify-content:space-between;padding:10px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:46px;height:46px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#4f46e5);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav{display:flex;gap:16px;align-items:center}
    .btn{background:var(--accent);padding:10px 14px;border-radius:10px;color:white;font-weight:600}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center;margin-top:28px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:28px;border-radius:var(--radius);box-shadow:var(--shadow)}
    h1{font-size:34px;margin:0 0 12px}
    p.lead{color:var(--muted);margin:0 0 18px}

    /* Features */
    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:18px}
    .feature{padding:14px;border-radius:12px;background:var(--glass);border:1px solid rgba(255,255,255,0.03)}

    /* Portfolio */
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:18px}
    .proj{height:130px;border-radius:12px;overflow:hidden;background-size:cover;background-position:center}

    /* Contact */
    form{display:grid;gap:10px}
    input,textarea{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:12px;border-radius:10px;color:inherit}
    textarea{min-height:120px}

    footer{margin-top:28px;color:var(--muted);font-size:14px}

    /* Responsive */
    @media(max-width:980px){
      .hero{grid-template-columns:1fr}
      .grid{grid-template-columns:repeat(2,1fr)}
      .features{grid-template-columns:repeat(2,1fr)}
    }
    @media(max-width:560px){
      .grid{grid-template-columns:1fr}
      nav{display:none}
      header{gap:12px}
      h1{font-size:28px}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">N</div>
        <div>
          <div style="font-weight:700">Название компании</div>
          <div style="font-size:13px;color:var(--muted)">Короткое описание — слоган</div>
        </div>
      </div>
      <nav>
        <a href="#about">О нас</a>
        <a href="#services">Услуги</a>
        <a href="#work">Портфолио</a>
        <a href="#contact" class="btn">Связаться</a>
      </nav>
    </header>

    <section class="hero">
      <div class="card">
        <h1>Создаю сайты, которые продают</h1>
        <p class="lead">Качественный дизайн, быстрая верстка и SEO‑оптимизация. Я помогу вам выйти в интернет с современным, адаптивным сайтом.</p>
        <div class="features">
          <div class="feature">
            <strong>Адаптивный</strong>
            <div style="font-size:13px;color:var(--muted)">Работает на мобильных и десктопах</div>
          </div>
          <div class="feature">
            <strong>Быстро</strong>
            <div style="font-size:13px;color:var(--muted)">Оптимизированные изображения и код</div>
          </div>
          <div class="feature">
            <strong>SEO</strong>
            <div style="font-size:13px;color:var(--muted)">Лучшие практики для видимости в поиске</div>
          </div>
        </div>

        <div style="margin-top:18px;display:flex;gap:10px">
          <a class="btn" href="#contact">Заказать сайт</a>
          <a href="#work" style="align-self:center;color:var(--muted)">Посмотреть работы</a>
        </div>
      </div>

      <aside>
        <div class="card" style="display:flex;flex-direction:column;gap:12px">
          <div style="font-weight:700">Быстрая контактная форма</div>
          <!-- Для реальной отправки замените action на ваш endpoint (Formspree, Netlify Forms или сервер) -->
          <form action="https://formspree.io/f/your-form-id" method="POST">
            <input type="text" name="name" placeholder="Ваше имя" required>
            <input type="email" name="email" placeholder="Email" required>
            <input type="text" name="subject" placeholder="Тема">
            <textarea name="message" placeholder="Сообщение" required></textarea>
            <button type="submit" class="btn">Отправить</button>
          </form>
        </div>
      </aside>
    </section>

    <section id="about" style="margin-top:28px">
      <div class="card">
        <h2>О компании</h2>
        <p style="color:var(--muted)">Короткий абзац о вас или вашей компании. Расскажите кем вы являетесь, какие задачи решаете и почему клиенты выбирают вас. Замените этот текст на реальный контент.</p>
      </div>
    </section>

    <section id="services" style="margin-top:18px">
      <div class="card">
        <h2>Услуги</h2>
        <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:12px">
          <div class="feature"><strong>Дизайн</strong><div style="font-size:13px;color:var(--muted)">UI/UX дизайн интерфейсов</div></div>
          <div class="feature"><strong>Вёрстка</strong><div style="font-size:13px;color:var(--muted)">HTML/CSS/JS, адаптивность</div></div>
          <div class="feature"><strong>Поддержка</strong><div style="font-size:13px;color:var(--muted)">Техподдержка и обновления</div></div>
        </div>
      </div>
    </section>

    <section id="work" style="margin-top:18px">
      <div class="card">
        <h2>Портфолио</h2>
        <div class="grid">
          <div class="proj" style="background-image:url('https://images.unsplash.com/photo-1506765515384-028b60a970df?q=80&w=800&auto=format&fit=crop&s=placeholder')"></div>
          <div class="proj" style="background-image:url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=800&auto=format&fit=crop&s=placeholder')"></div>
          <div class="proj" style="background-image:url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=800&auto=format&fit=crop&s=placeholder')"></div>
        </div>
        <div style="margin-top:12px;color:var(--muted);font-size:14px">Замените изображения на скриншоты ваших проектов.</div>
      </div>
    </section>

    <section id="contact" style="margin-top:18px">
      <div class="card">
        <h2>Контакты</h2>
        <p style="color:var(--muted)">Email: <a href="mailto:hello@site.ru">hello@site.ru</a> · Телефон: +7 (900) 000‑00‑00</p>
        <div style="display:flex;gap:12px;flex-wrap:wrap;margin-top:12px">
          <div style="padding:12px;border-radius:10px;background:var(--glass);min-width:220px">Адрес офиса<br><span style="color:var(--muted);font-size:13px">Город, Улица, дом</span></div>
          <div style="padding:12px;border-radius:10px;background:var(--glass);min-width:220px">График работы<br><span style="color:var(--muted);font-size:13px">Пн–Пт 09:00–18:00</span></div>
        </div>
      </div>
    </section>

    <footer>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
        <div>© <span id="year"></span> Название компании</div>
        <div style="color:var(--muted)">Сделано с заботой — ваш сайт</div>
      </div>
    </footer>
  </div>

  <script>
    document.getElementById('year').innerText = new Date().getFullYear();
  </script>

  <!--
    Инструкция по использованию:
    1) Сохраните этот файл как index.html
    2) Замените текст и изображения на свои. Изображения можно положить в папку /assets и поменять пути.
    3) Для формы: используйте Formspree, Netlify Forms или настройте сервер. В action укажите реальный endpoint.
    4) Для деплоя: GitHub Pages, Netlify или Vercel — просто загрузите репозиторий.

    Если хотите, могу:
    - Перевести в многостраничный сайт или React/Vue проект
    - Подключить CMS (Contentful, Sanity, Netlify CMS)
    - Подготовить пакет для загрузки (zip) или настроить деплой
  -->
</body>
</html>
![Screenshot_٢٠٢٥١١٣٠_٠٠١٣٣٨_One UI Home](https://github.com/user-attachments/assets/582084de-ccea-4a7d-883a-95306b498f55)
 -
Ресторан 
