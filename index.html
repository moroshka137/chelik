<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#4a6cf7">
<title>StudyNotes — умные конспекты</title>

<script src="https://cdn.jsdelivr.net/npm/tesseract.js@5/dist/tesseract.min.js"></script>

<style>
  :root{
    --bg:#f4f6fb; --card:#fff; --accent:#4a6cf7; --accent2:#eef1ff;
    --text:#1e2233; --muted:#7a819c; --border:#e3e7f2;
    --danger:#e94f5a; --ok:#2eb872; --star:#f5a623;
    --shadow:0 4px 20px rgba(30,34,51,.08);
  }
  *{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
  html,body{height:100%}
  body{
    font-family:'Segoe UI',system-ui,sans-serif;
    background:var(--bg); color:var(--text);
    display:flex; min-height:100dvh; overflow:hidden;
  }

  /* ============ MASCOT ============ */
  .mascot{
    width:160px; height:auto; display:block;
    margin:0 auto 12px;
    animation:float 3s ease-in-out infinite;
    filter:drop-shadow(0 8px 18px rgba(30,34,51,.14));
  }
  .brand-mascot{
    width:36px; height:36px; flex-shrink:0;
    filter:drop-shadow(0 2px 4px rgba(30,34,51,.12));
  }
  .empty-mascot{
    width:150px; height:auto; display:block;
    margin:0 auto 12px;
    animation:float 3s ease-in-out infinite;
  }
  @keyframes float{
    0%,100%{transform:translateY(0) rotate(-1deg)}
    50%   {transform:translateY(-8px) rotate(1deg)}
  }

  /* ================= LAYOUT ================= */
  .app{display:none; width:100%; height:100dvh}
  .app.on{display:flex}

  aside{
    width:290px; flex-shrink:0; background:var(--card);
    border-right:1px solid var(--border);
    padding:18px; overflow-y:auto;
    display:flex; flex-direction:column; gap:6px;
    transition:transform .25s;
  }
  .brand{
    display:flex; align-items:center; gap:10px;
    font-size:19px; font-weight:700; color:var(--accent);
    margin-bottom:14px;
  }
  aside h2{
    font-size:11px; text-transform:uppercase; letter-spacing:.8px;
    color:var(--muted); margin:12px 0 6px;
  }
  .item{
    padding:8px 12px; border-radius:8px; cursor:pointer;
    font-size:14px; display:flex; justify-content:space-between;
    align-items:center; transition:.15s;
  }
  .item:hover{background:var(--accent2)}
  .item.active{background:var(--accent); color:#fff}
  .item .star{color:var(--star); font-size:13px}
  .item.active .star{color:#fff}

  .userbox{
    margin-top:auto; padding-top:14px; border-top:1px solid var(--border);
    display:flex; align-items:center; gap:10px; font-size:13px;
  }
  .avatar{
    width:34px; height:34px; border-radius:50%;
    background:var(--accent); color:#fff;
    display:grid; place-items:center; font-weight:700;
  }
  .link{color:var(--accent); cursor:pointer; font-size:13px}

  main{flex:1; overflow-y:auto; padding:24px; position:relative}
  header{
    display:flex; justify-content:space-between; align-items:flex-start;
    gap:14px; margin-bottom:20px; flex-wrap:wrap;
  }
  header h1{font-size:22px}
  .path{font-size:12px; color:var(--muted); margin-top:4px}

  .toolbar{display:flex; gap:8px; flex-wrap:wrap; align-items:center}
  .search{
    padding:9px 14px; border:1px solid var(--border);
    border-radius:8px; font-size:14px; background:#fff; min-width:180px;
  }

  .btn{
    background:var(--accent); color:#fff; border:none;
    padding:10px 16px; border-radius:8px; cursor:pointer;
    font-size:14px; font-weight:600; transition:.15s;
    display:inline-flex; align-items:center; gap:6px;
  }
  .btn:hover{opacity:.9}
  .btn.ghost{background:var(--accent2); color:var(--accent)}
  .btn.sm{padding:6px 12px; font-size:12px}
  .btn.icon{padding:8px; background:transparent; color:var(--muted)}
  .btn.icon:hover{background:var(--accent2); color:var(--accent)}
  .btn.icon.on{color:var(--star)}

  .note{
    background:var(--card); border:1px solid var(--border);
    border-radius:14px; padding:18px; margin-bottom:14px;
    box-shadow:var(--shadow); position:relative;
  }
  .note h3{font-size:16px; margin-bottom:6px; padding-right:60px}
  .note .meta{font-size:12px; color:var(--muted); margin-bottom:10px}
  .note p{font-size:14px; line-height:1.65; white-space:pre-wrap; margin-bottom:10px}
  .note img{display:block; max-width:100%; border-radius:10px;
            border:1px solid var(--border); margin-top:8px}
  .note .acts{
    position:absolute; top:14px; right:14px; display:flex; gap:2px;
  }
  .tags{display:flex; gap:6px; flex-wrap:wrap; margin-top:10px}
  .tag{
    background:var(--accent2); color:var(--accent);
    padding:3px 10px; border-radius:99px; font-size:11px; font-weight:600;
  }

  .empty{text-align:center; padding:50px 20px; color:var(--muted); font-size:14px}

  /* ============ GRAPH ============ */
  .graph-wrap{
    background:#14162a; border-radius:14px; overflow:hidden;
    height:calc(100dvh - 130px); position:relative;
    box-shadow:var(--shadow);
  }
  #graph{display:block; width:100%; height:100%; cursor:grab}
  #graph:active{cursor:grabbing}
  .graph-hint{
    position:absolute; bottom:14px; left:14px;
    color:#8b91b4; font-size:11px; pointer-events:none;
    background:rgba(0,0,0,.4); padding:6px 12px; border-radius:99px;
  }

  /* ============ AUTH ============ */
  .auth{
    display:none; width:100%; height:100dvh;
    align-items:center; justify-content:center;
    padding:20px; background:
      radial-gradient(circle at 20% 20%, #e8edff, transparent 50%),
      radial-gradient(circle at 80% 80%, #ffeef0, transparent 50%),
      var(--bg);
  }
  .auth.on{display:flex}
  .auth-card{
    background:var(--card); border-radius:20px; padding:30px;
    width:420px; max-width:100%; box-shadow:0 20px 60px rgba(30,34,51,.15);
    text-align:center;
  }
  .auth-card h1{font-size:22px; margin-bottom:6px}
  .auth-card .sub{color:var(--muted); font-size:13px; margin-bottom:20px}
  .auth-card .field{text-align:left; margin-bottom:12px}
  .auth-card label{display:block; font-size:12px; color:var(--muted); margin-bottom:5px}
  .switch{margin-top:16px; font-size:13px; color:var(--muted)}
  .switch b{color:var(--accent); cursor:pointer}
  .err{color:var(--danger); font-size:13px; min-height:18px; margin-top:8px}

  /* ============ MODAL ============ */
  .modal-bg{
    position:fixed; inset:0; background:rgba(20,25,50,.55);
    display:none; align-items:center; justify-content:center;
    z-index:50; padding:16px; backdrop-filter:blur(3px);
  }
  .modal-bg.open{display:flex}
  .modal{
    background:var(--card); width:800px; max-width:100%;
    max-height:92dvh; overflow-y:auto; border-radius:16px;
    padding:22px;
  }
  .modal h2{margin-bottom:14px; font-size:18px}

  .tabs{display:flex; gap:6px; margin-bottom:14px; flex-wrap:wrap}
  .tab{
    padding:9px 14px; border-radius:8px; background:var(--accent2);
    color:var(--accent); cursor:pointer; font-size:13px; font-weight:600;
    transition:.15s; user-select:none;
  }
  .tab.active{background:var(--accent); color:#fff}

  .field{margin-bottom:12px}
  .field label{display:block; font-size:12px; color:var(--muted); margin-bottom:4px}
  input,textarea,select{
    width:100%; padding:10px; border:1px solid var(--border);
    border-radius:8px; font-family:inherit; font-size:14px;
    background:#fafbff; outline:none;
  }
  input:focus,textarea:focus,select:focus{border-color:var(--accent)}
  textarea{resize:vertical; min-height:130px}
  .row{display:flex; gap:10px; flex-wrap:wrap}
  .row .field{flex:1; min-width:140px}
  .modal-actions{display:flex; gap:10px; justify-content:flex-end; margin-top:16px; flex-wrap:wrap}

  .pane{background:#fafbff; border:1px solid var(--border);
        border-radius:10px; padding:14px; margin-bottom:12px}
  .file-drop{
    border:2px dashed var(--border); border-radius:10px;
    padding:24px; text-align:center; color:var(--muted);
    cursor:pointer; font-size:14px; transition:.15s;
  }
  .file-drop:hover{border-color:var(--accent); color:var(--accent)}
  .preview{max-width:100%; border-radius:8px; margin-top:12px; display:none}
  .progress{height:8px; background:var(--accent2); border-radius:99px;
            overflow:hidden; margin-top:10px; display:none}
  .progress > div{height:100%; width:0; background:var(--accent); transition:width .2s}

  .rec-btn{
    display:inline-flex; align-items:center; gap:10px;
    padding:12px 22px; border-radius:99px; border:none;
    background:var(--accent); color:#fff; cursor:pointer;
    font-size:14px; font-weight:600;
  }
  .rec-btn.recording{background:var(--danger); animation:pulse 1.2s infinite}
  @keyframes pulse{
    0%{box-shadow:0 0 0 0 rgba(233,79,90,.55)}
    70%{box-shadow:0 0 0 14px rgba(233,79,90,0)}
    100%{box-shadow:0 0 0 0 rgba(233,79,90,0)}
  }
  .interim{font-size:13px; color:var(--muted); font-style:italic;
           margin-top:10px; min-height:18px}

  .canvas-tools{display:flex; gap:10px; align-items:center;
                flex-wrap:wrap; margin-bottom:10px}
  .swatch{width:26px;height:26px;border-radius:50%;
          border:2px solid transparent; cursor:pointer; transition:.15s}
  .swatch.active{border-color:var(--text); transform:scale(1.15)}
  #canvasWrap{overflow:auto; border:1px solid var(--border);
              border-radius:10px; background:#fff}
  #board{display:block; cursor:crosshair; touch-action:none; width:100%; height:auto}
  .tool-btn{padding:6px 12px; border-radius:8px; border:1px solid var(--border);
            background:#fff; cursor:pointer; font-size:13px; font-weight:600}
  .tool-btn.active{background:var(--accent); color:#fff; border-color:var(--accent)}

  .tags-input{display:flex; gap:6px; flex-wrap:wrap; align-items:center;
              padding:6px; border:1px solid var(--border); border-radius:8px;
              background:#fafbff; min-height:42px}
  .tags-input input{border:none; background:transparent; flex:1; min-width:120px; padding:4px}
  .tags-input input:focus{outline:none}
  .tag-pill{
    background:var(--accent2); color:var(--accent);
    padding:4px 8px 4px 10px; border-radius:99px; font-size:12px;
    font-weight:600; display:inline-flex; gap:6px; align-items:center;
  }
  .tag-pill b{cursor:pointer; opacity:.6}
  .tag-pill b:hover{opacity:1}

  /* ============ MOBILE ============ */
  .burger{
    display:none; position:fixed; top:12px; left:12px; z-index:40;
    background:var(--accent); color:#fff; border:none;
    width:42px; height:42px; border-radius:12px; cursor:pointer;
    font-size:20px; box-shadow:var(--shadow);
  }
  .overlay{display:none; position:fixed; inset:0; background:rgba(0,0,0,.4); z-index:29}
  .overlay.on{display:block}

  @media (max-width:860px){
    aside{
      position:fixed; left:0; top:0; bottom:0; z-index:30;
      transform:translateX(-100%); width:270px;
      box-shadow:4px 0 30px rgba(0,0,0,.15);
    }
    aside.open{transform:translateX(0)}
    .burger{display:block}
    main{padding:16px; padding-top:66px}
    header h1{font-size:19px}
    .graph-wrap{height:calc(100dvh - 170px)}
    .modal{padding:16px}
    .modal-actions .btn{flex:1}
    .note{padding:14px}
    .note h3{padding-right:80px}
    .mascot{width:130px}
    .empty-mascot{width:120px}
  }
</style>
</head>
<body>

<!-- ==================================================
     🐭 МАСКОТ (SVG) — мультяшная крыса
     ================================================== -->
<svg width="0" height="0" style="position:absolute" aria-hidden="true">
  <symbol id="mouse" viewBox="0 0 240 240">

    <!-- ================= ХВОСТ ================= -->
    <path d="M164 196
             Q218 208 226 162
             Q232 122 210 116
             Q196 113 193 126
             Q190 138 202 141
             Q216 145 213 165
             Q209 188 166 184 Z"
          fill="#f4b6b6" stroke="#2b2430" stroke-width="4.5"
          stroke-linejoin="round"/>
    <path d="M218 130 L207 141 M222 148 L209 154 M221 168 L208 172"
          stroke="#2b2430" stroke-width="3" stroke-linecap="round" fill="none"/>

    <!-- ================= УШИ ================= -->
    <circle cx="66" cy="62" r="40"
            fill="#8a8580" stroke="#2b2430" stroke-width="4.5"/>
    <ellipse cx="70" cy="66" rx="21" ry="24" fill="#f7bdbd"/>
    <circle cx="176" cy="58" r="40"
            fill="#8a8580" stroke="#2b2430" stroke-width="4.5"/>
    <ellipse cx="180" cy="62" rx="21" ry="24" fill="#f7bdbd"/>

    <!-- ================= ТЕЛО ================= -->
    <path d="M120 46
             Q56 56 48 152
             Q46 218 120 222
             Q194 218 192 152
             Q184 56 120 46 Z"
          fill="#8a8580" stroke="#2b2430" stroke-width="4.5"
          stroke-linejoin="round"/>

    <!-- светлый живот -->
    <ellipse cx="120" cy="168" rx="54" ry="48" fill="#a8a39d" opacity=".45"/>

    <!-- блик на макушке -->
    <ellipse cx="98" cy="72" rx="20" ry="10"
             fill="#ffffff" opacity=".28" transform="rotate(-15 98 72)"/>

    <!-- ================= ГЛАЗА ================= -->
    <circle cx="92" cy="116" r="23"
            fill="#ffffff" stroke="#2b2430" stroke-width="4.5"/>
    <circle cx="148" cy="116" r="23"
            fill="#ffffff" stroke="#2b2430" stroke-width="4.5"/>
    <circle cx="99" cy="120" r="13" fill="#2b2430"/>
    <circle cx="155" cy="120" r="13" fill="#2b2430"/>
    <circle cx="103" cy="114" r="4.5" fill="#ffffff"/>
    <circle cx="159" cy="114" r="4.5" fill="#ffffff"/>

    <!-- румянец -->
    <circle cx="60" cy="148" r="11" fill="#f7bdbd" opacity=".55"/>
    <circle cx="180" cy="148" r="11" fill="#f7bdbd" opacity=".55"/>

    <!-- ================= НОС И РОТ ================= -->
    <ellipse cx="120" cy="156" rx="14" ry="11"
             fill="#f7bdbd" stroke="#2b2430" stroke-width="4.5"/>
    <path d="M120 167 Q120 180 106 182
             M120 167 Q120 180 134 182"
          stroke="#2b2430" stroke-width="3.5" fill="none"
          stroke-linecap="round"/>

    <!-- ================= УСИКИ ================= -->
    <path d="M64 150 L24 140
             M64 160 L20 160
             M66 170 L26 180"
          stroke="#2b2430" stroke-width="2.5" stroke-linecap="round"/>
    <path d="M176 150 L216 140
             M176 160 L220 160
             M174 170 L214 180"
          stroke="#2b2430" stroke-width="2.5" stroke-linecap="round"/>

    <!-- ================= ЛАПКИ ================= -->
    <ellipse cx="78" cy="220" rx="20" ry="11"
             fill="#f7bdbd" stroke="#2b2430" stroke-width="4.5"/>
    <ellipse cx="162" cy="220" rx="20" ry="11"
             fill="#f7bdbd" stroke="#2b2430" stroke-width="4.5"/>
    <path d="M70 220 L70 228 M78 220 L78 228 M86 220 L86 228
             M154 220 L154 228 M162 220 L162 228 M170 220 L170 228"
          stroke="#2b2430" stroke-width="2" stroke-linecap="round" opacity=".7"/>
  </symbol>
</svg>

<!-- ================= AUTH SCREEN ================= -->
<div class="auth on" id="authScreen">
  <div class="auth-card">
    <svg class="mascot" viewBox="0 0 240 240"><use href="#mouse"/></svg>
    <h1>StudyNotes</h1>
    <div class="sub">Умные конспекты для школы</div>

    <div id="loginForm">
      <div class="field"><label>Логин</label><input id="lLogin" autocomplete="username"></div>
      <div class="field"><label>Пароль</label><input id="lPass" type="password" autocomplete="current-password"></div>
      <div class="err" id="lErr"></div>
      <button class="btn" style="width:100%;margin-top:8px" id="loginBtn">Войти</button>
      <div class="switch">Нет аккаунта? <b id="toReg">Зарегистрироваться</b></div>
    </div>

    <div id="regForm" style="display:none">
      <div class="field"><label>Логин</label><input id="rLogin" autocomplete="username"></div>
      <div class="field"><label>Пароль (от 4 символов)</label><input id="rPass" type="password" autocomplete="new-password"></div>
      <div class="field"><label>Повторите пароль</label><input id="rPass2" type="password" autocomplete="new-password"></div>
      <div class="err" id="rErr"></div>
      <button class="btn" style="width:100%;margin-top:14px" id="regBtn">Создать аккаунт</button>
      <div class="switch">Уже есть аккаунт? <b id="toLogin">Войти</b></div>
    </div>

    <div style="font-size:11px;color:#b0b5cc;margin-top:18px;line-height:1.5">
      🔒 Данные хранятся локально в вашем браузере.<br>
      Пароль хешируется через SHA-256.
    </div>
  </div>
</div>

<!-- ================= APP ================= -->
<button class="burger" id="burger">☰</button>
<div class="overlay" id="overlay"></div>

<div class="app" id="app">
  <aside id="sidebar">
    <div class="brand">
      <svg class="brand-mascot" viewBox="0 0 240 240"><use href="#mouse"/></svg>
      StudyNotes
    </div>

    <h2>Разделы</h2>
    <div class="item active" id="navNotes">📘 Мои конспекты</div>
    <div class="item" id="navFav">⭐ Избранное</div>
    <div class="item" id="navGraph">🕸 Граф связей</div>

    <h2>Классы</h2>
    <div id="classes"></div>
    <h2>Предметы</h2>
    <div id="subjects"></div>
    <h2>Темы</h2>
    <div id="topics"></div>

    <div class="userbox">
      <div class="avatar" id="avatar">?</div>
      <div style="flex:1">
        <div id="userName" style="font-weight:600">—</div>
        <div class="link" id="logoutBtn">Выйти</div>
      </div>
    </div>
  </aside>

  <main>
    <header>
      <div>
        <h1 id="pageTitle">Мои конспекты</h1>
        <div class="path" id="pagePath">—</div>
      </div>
      <div class="toolbar">
        <input class="search" id="searchInput" placeholder="🔍 Поиск по тексту и тегам">
        <button class="btn" id="addBtn">+ Конспект</button>
      </div>
    </header>

    <div id="content"></div>
  </main>
</div>

<!-- ================= MODAL ================= -->
<div class="modal-bg" id="modalBg">
  <div class="modal">
    <h2>Новый конспект</h2>

    <div class="row">
      <div class="field"><label>Класс</label><select id="selClass"></select></div>
      <div class="field"><label>Предмет</label>
        <input id="inpSubject" list="subjectList" placeholder="Алгебра">
        <datalist id="subjectList"></datalist>
      </div>
    </div>
    <div class="row">
      <div class="field"><label>Тема</label><input id="inpTopic" placeholder="Квадратные уравнения"></div>
      <div class="field"><label>Название параграфа</label><input id="inpTitle" placeholder="Параграф 12"></div>
    </div>

    <div class="field">
      <label>Теги (Enter, чтобы добавить)</label>
      <div class="tags-input" id="tagsBox">
        <input id="tagInput" placeholder="алгебра, формулы, экзамен...">
      </div>
    </div>

    <div class="tabs">
      <div class="tab active" data-tab="text">✍️ Ввод</div>
      <div class="tab" data-tab="file">📄 Файл</div>
      <div class="tab" data-tab="photo">📷 Фото → текст</div>
      <div class="tab" data-tab="audio">🎙️ Аудио → текст</div>
      <div class="tab" data-tab="draw">🎨 Рисунок</div>
    </div>

    <div class="pane" id="pane-text">
      <div style="font-size:13px;color:var(--muted)">Введите текст ниже ↓</div>
    </div>

    <div class="pane" id="pane-file" style="display:none">
      <div class="file-drop" id="fileDrop">
        Нажмите или перетащите .txt / .md файл
        <input type="file" id="fileInput" accept=".txt,.md,text/plain" hidden>
      </div>
    </div>

    <div class="pane" id="pane-photo" style="display:none">
      <div class="file-drop" id="photoDrop">
        📷 Нажмите или перетащите фото конспекта (JPG/PNG)
        <input type="file" id="photoInput" accept="image/*" hidden>
      </div>
      <img id="photoPreview" class="preview" alt="превью">
      <div class="progress" id="ocrProgress"><div></div></div>
      <div id="ocrStatus" style="font-size:12px;color:var(--muted);margin-top:8px"></div>
      <button class="btn" id="ocrBtn" disabled style="margin-top:10px">🧠 Распознать текст</button>
    </div>

    <div class="pane" id="pane-audio" style="display:none">
      <button class="rec-btn" id="recBtn">🎙️ Начать запись</button>
      <div class="interim" id="interim"></div>
      <div style="font-size:12px;color:var(--muted);margin-top:8px">
        Chrome / Edge. Говорите чётко — текст появится в поле ниже.
      </div>
    </div>

    <div class="pane" id="pane-draw" style="display:none">
      <div class="canvas-tools">
        <div class="swatch active" style="background:#1e2233" data-color="#1e2233"></div>
        <div class="swatch" style="background:#e94f5a" data-color="#e94f5a"></div>
        <div class="swatch" style="background:#4a6cf7" data-color="#4a6cf7"></div>
        <div class="swatch" style="background:#2eb872" data-color="#2eb872"></div>
        <div class="swatch" style="background:#f5a623" data-color="#f5a623"></div>
        <div class="swatch" style="background:#9b51e0" data-color="#9b51e0"></div>
        <input type="range" id="brushSize" min="1" max="30" value="3" style="width:100px">
        <button class="tool-btn" id="eraserBtn">🧽 Ластик</button>
        <button class="tool-btn" id="undoBtn">↶</button>
        <button class="tool-btn" id="clearBtn">🗑</button>
        <button class="tool-btn" id="dlCanvasBtn">⬇ Скачать PNG</button>
      </div>
      <div id="canvasWrap"><canvas id="board" width="820" height="460"></canvas></div>
    </div>

    <div class="field">
      <label>Текст конспекта</label>
      <textarea id="inpText" placeholder="Текст конспекта..."></textarea>
    </div>

    <div class="modal-actions">
      <button class="btn ghost" id="cancelBtn">Отмена</button>
      <button class="btn" id="saveBtn">Сохранить</button>
    </div>
  </div>
</div>

<script>
/* ============================================================
   0. УТИЛИТЫ
   ============================================================ */
const $  = id => document.getElementById(id);
const esc = s => (s||'').replace(/[&<>"']/g, c =>
  ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));

async function sha256(str){
  const buf = new TextEncoder().encode(str);
  const hash = await crypto.subtle.digest('SHA-256', buf);
  return [...new Uint8Array(hash)].map(b => b.toString(16).padStart(2,'0')).join('');
}

/* ============================================================
   1. АВТОРИЗАЦИЯ
   ============================================================ */
const USERS_KEY = 'sn_users';
const SESSION_KEY = 'sn_session';
let CURRENT_USER = null;

const loadUsers = () => JSON.parse(localStorage.getItem(USERS_KEY) || '{}');
const saveUsers = u => localStorage.setItem(USERS_KEY, JSON.stringify(u));
function dbKey(){ return 'sn_db_' + CURRENT_USER; }

async function doRegister(){
  const login = $('rLogin').value.trim().toLowerCase();
  const p1 = $('rPass').value, p2 = $('rPass2').value;
  const err = $('rErr');
  err.textContent = '';

  if(login.length < 3)              return err.textContent = 'Логин минимум 3 символа';
  if(!/^[a-z0-9_]+$/.test(login))   return err.textContent = 'Логин: a-z, 0-9, _';
  if(p1.length < 4)                 return err.textContent = 'Пароль минимум 4 символа';
  if(p1 !== p2)                     return err.textContent = 'Пароли не совпадают';

  const users = loadUsers();
  if(users[login]) return err.textContent = 'Такой логин уже занят';

  users[login] = { hash: await sha256(p1), created: Date.now() };
  saveUsers(users);
  localStorage.setItem(SESSION_KEY, login);
  startSession(login);
}

async function doLogin(){
  const login = $('lLogin').value.trim().toLowerCase();
  const pass  = $('lPass').value;
  const err = $('lErr');
  err.textContent = '';

  const users = loadUsers();
  if(!users[login]) return err.textContent = 'Пользователь не найден';
  const hash = await sha256(pass);
  if(hash !== users[login].hash) return err.textContent = 'Неверный пароль';

  localStorage.setItem(SESSION_KEY, login);
  startSession(login);
}

function startSession(login){
  CURRENT_USER = login;
  $('authScreen').classList.remove('on');
  $('app').classList.add('on');
  $('userName').textContent = login;
  $('avatar').textContent = login[0].toUpperCase();

  DB = JSON.parse(localStorage.getItem(dbKey()) || '{}');
  cur = { cls:null, subj:null, topic:null, view:'notes', favOnly:false, query:'' };
  renderAll();
}

function logout(){
  localStorage.removeItem(SESSION_KEY);
  CURRENT_USER = null;
  location.reload();
}

$('toReg').onclick    = () => { $('loginForm').style.display='none'; $('regForm').style.display=''; };
$('toLogin').onclick  = () => { $('regForm').style.display='none'; $('loginForm').style.display=''; };
$('loginBtn').onclick = doLogin;
$('regBtn').onclick   = doRegister;
$('logoutBtn').onclick = logout;
[$('lPass'),$('rPass2')].forEach(i => i.addEventListener('keydown', e => {
  if(e.key === 'Enter') i.id === 'lPass' ? doLogin() : doRegister();
}));

/* ============================================================
   2. ХРАНИЛИЩЕ
   ============================================================ */
let DB = {};
const saveDB = () => localStorage.setItem(dbKey(), JSON.stringify(DB));

const CLASSES = ['5','6','7','8','9','10','11'];
const DEFAULT_SUBJECTS = ['Алгебра','Геометрия','Русский язык','Литература',
  'История','Физика','Химия','Биология','География','Английский язык'];

let cur = { cls:null, subj:null, topic:null, view:'notes', favOnly:false, query:'' };

/* ============================================================
   3. САЙДБАР
   ============================================================ */
function renderClasses(){
  const el = $('classes');
  el.innerHTML = CLASSES.map(c =>
    `<div class="item ${cur.cls===c?'active':''}" data-cls="${c}">${c} класс</div>`).join('');
  el.querySelectorAll('.item').forEach(i =>
    i.onclick = () => { cur={...cur,cls:i.dataset.cls,subj:null,topic:null,view:'notes',favOnly:false}; closeSidebar(); renderAll(); });
}
function renderSubjects(){
  const el = $('subjects');
  if(!cur.cls){ el.innerHTML = '<div style="font-size:12px;color:#aaa;padding:4px 12px">— сначала класс</div>'; return; }
  const subs = [...new Set([...Object.keys(DB[cur.cls]||{}), ...DEFAULT_SUBJECTS])];
  el.innerHTML = subs.map(s =>
    `<div class="item ${cur.subj===s?'active':''}" data-s="${s}">${s}</div>`).join('');
  el.querySelectorAll('.item').forEach(i =>
    i.onclick = () => { cur={...cur,subj:i.dataset.s,topic:null,view:'notes'}; closeSidebar(); renderAll(); });
}
function renderTopics(){
  const el = $('topics');
  if(!cur.cls || !cur.subj){ el.innerHTML = '<div style="font-size:12px;color:#aaa;padding:4px 12px">— сначала предмет</div>'; return; }
  const topics = Object.keys((DB[cur.cls]||{})[cur.subj]||{});
  if(!topics.length){ el.innerHTML = '<div style="font-size:12px;color:#aaa;padding:4px 12px">пусто</div>'; return; }
  el.innerHTML = topics.map(t =>
    `<div class="item ${cur.topic===t?'active':''}" data-t="${t}">${t}</div>`).join('');
  el.querySelectorAll('.item').forEach(i =>
    i.onclick = () => { cur={...cur,topic:i.dataset.t,view:'notes'}; closeSidebar(); renderAll(); });
}

/* ============================================================
   4. СБОР КОНСПЕКТОВ
   ============================================================ */
function collectNotes(filter){
  const out = [];
  for(const cls of Object.keys(DB)){
    for(const subj of Object.keys(DB[cls])){
      for(const topic of Object.keys(DB[cls][subj])){
        DB[cls][subj][topic].forEach(n => {
          const item = {cls,subj,topic,...n};
          if(filter(item)) out.push(item);
        });
      }
    }
  }
  return out.sort((a,b) => new Date(b.date) - new Date(a.date));
}

function matchQuery(n, q){
  if(!q) return true;
  q = q.toLowerCase();
  return (n.title||'').toLowerCase().includes(q)
      || (n.text ||'').toLowerCase().includes(q)
      || (n.tags ||[]).some(t => t.toLowerCase().includes(q))
      || n.topic.toLowerCase().includes(q)
      || n.subj.toLowerCase().includes(q);
}

/* ============================================================
   5. КОНТЕНТ
   ============================================================ */
function renderContent(){
  const content = $('content');
  const title = $('pageTitle');
  const path  = $('pagePath');

  if(cur.view === 'graph'){
    title.textContent = '🕸 Граф связей';
    path.textContent = 'Кликните по узлу, чтобы перейти к конспекту';
    content.innerHTML = `
      <div class="graph-wrap">
        <canvas id="graph"></canvas>
        <div class="graph-hint">🖱 тянуть — перемещать · колесо — зум · клик по узлу — открыть</div>
      </div>`;
    initGraph();
    return;
  }

  if(cur.view === 'favorites' || cur.favOnly){
    title.textContent = '⭐ Избранное';
    path.textContent = 'Ваши лучшие конспекты';
    const list = collectNotes(n => n.fav);
    content.innerHTML = list.length
      ? list.map(renderNoteCard).join('')
      : emptyHTML('Пока ничего в избранном', 'Жмите ⭐ на карточке конспекта');
    bindNoteActions();
    return;
  }

  if(cur.cls && cur.subj && cur.topic){
    title.textContent = cur.topic;
    path.textContent = `${cur.cls} класс · ${cur.subj}`;
    let notes = (DB[cur.cls]?.[cur.subj]?.[cur.topic] || []);
    if(cur.query) notes = notes.filter(n =>
      matchQuery({...n, topic:cur.topic, subj:cur.subj}, cur.query));
    content.innerHTML = notes.length
      ? notes.map(n => renderNoteCard({cls:cur.cls,subj:cur.subj,topic:cur.topic,...n})).join('')
      : emptyHTML('Здесь пока пусто', 'Нажмите «+ Конспект», чтобы добавить');
    bindNoteActions();
    return;
  }

  if(cur.query){
    title.textContent = `🔍 «${cur.query}»`;
    const list = collectNotes(n => matchQuery(n, cur.query));
    path.textContent = `Найдено: ${list.length}`;
    content.innerHTML = list.length
      ? list.map(renderNoteCard).join('')
      : emptyHTML('Ничего не найдено', 'Попробуйте другой запрос');
    bindNoteActions();
    return;
  }

  title.textContent = 'Мои конспекты';
  path.textContent = 'Выберите класс, предмет или тему слева';

  const all = collectNotes(() => true);
  if(!all.length){
    content.innerHTML = emptyHTML('Ещё нет конспектов',
      'Нажмите «+ Конспект» или откройте граф связей');
  } else {
    content.innerHTML = `
      <div style="font-size:13px;color:var(--muted);margin-bottom:12px">
        Всего: <b>${all.length}</b> · Обновите фильтр слева или ищите через поиск
      </div>
      ${all.slice(0,30).map(renderNoteCard).join('')}`;
  }
  bindNoteActions();
}

function emptyHTML(title, sub){
  return `<div class="empty">
    <svg class="empty-mascot" viewBox="0 0 240 240"><use href="#mouse"/></svg>
    <div style="font-weight:600;color:var(--text);margin-bottom:6px">${title}</div>
    <div>${sub}</div>
  </div>`;
}

function renderNoteCard(n){
  return `
  <div class="note" data-id="${n.id}" data-cls="${n.cls}" data-subj="${esc(n.subj)}" data-topic="${esc(n.topic)}">
    <div class="acts">
      <button class="btn icon fav ${n.fav?'on':''}" title="В избранное">${n.fav?'⭐':'☆'}</button>
      <button class="btn icon del" title="Удалить">🗑</button>
    </div>
    <h3>${esc(n.title)}</h3>
    <div class="meta">${new Date(n.date).toLocaleString('ru-RU')} · ${esc(n.cls)} кл · ${esc(n.subj)} · ${esc(n.topic)}</div>
    ${n.text ? `<p>${esc(n.text)}</p>` : ''}
    ${n.image ? `<img src="${n.image}" alt="рисунок">` : ''}
    ${n.image ? `<button class="btn ghost sm dl-img" style="margin-top:8px">⬇ Скачать рисунок</button>` : ''}
    ${(n.tags?.length) ? `<div class="tags">${n.tags.map(t => `<span class="tag">#${esc(t)}</span>`).join('')}</div>` : ''}
  </div>`;
}

function bindNoteActions(){
  document.querySelectorAll('.note').forEach(card => {
    const id = +card.dataset.id;
    const {cls,subj,topic} = card.dataset;
    const note = DB[cls]?.[subj]?.[topic]?.find(x => x.id === id);
    if(!note) return;

    card.querySelector('.fav')?.addEventListener('click', e => {
      e.stopPropagation();
      note.fav = !note.fav;
      saveDB(); renderContent();
    });

    card.querySelector('.del')?.addEventListener('click', e => {
      e.stopPropagation();
      if(!confirm('Удалить конспект?')) return;
      DB[cls][subj][topic] = DB[cls][subj][topic].filter(x => x.id !== id);
      if(!DB[cls][subj][topic].length) delete DB[cls][subj][topic];
      if(!Object.keys(DB[cls][subj] || {}).length) delete DB[cls][subj];
      saveDB(); renderAll();
    });

    card.querySelector('.dl-img')?.addEventListener('click', () => {
      const a = document.createElement('a');
      a.href = note.image;
      a.download = `${note.title.replace(/\s+/g,'_')}_${id}.png`;
      a.click();
    });
  });
}

function renderAll(){
  renderClasses(); renderSubjects(); renderTopics(); renderContent();
  $('navNotes').classList.toggle('active', cur.view === 'notes' && !cur.favOnly);
  $('navFav').classList.toggle('active',   cur.view === 'favorites' || cur.favOnly);
  $('navGraph').classList.toggle('active', cur.view === 'graph');
}

/* ============================================================
   6. ГРАФ
   ============================================================ */
let graphState = null;

function initGraph(){
  const canvas = $('graph');
  if(!canvas) return;

  const wrap = canvas.parentElement;
  const dpr = devicePixelRatio || 1;
  canvas.width  = wrap.clientWidth  * dpr;
  canvas.height = wrap.clientHeight * dpr;
  const ctx = canvas.getContext('2d');
  ctx.scale(dpr, dpr);

  const nodes = [], byId = {}, links = [];
  const add = (id, label, type, meta = {}) => {
    if(byId[id]) return byId[id];
    const n = { id, label, type, ...meta,
      x: Math.random()*wrap.clientWidth, y: Math.random()*wrap.clientHeight,
      vx:0, vy:0, r: type==='note'?5 : type==='topic'?9 : type==='subject'?13 : 18 };
    nodes.push(n); byId[id] = n; return n;
  };
  const link = (a,b) => links.push({a: byId[a], b: byId[b]});

  for(const cls of Object.keys(DB)){
    add('c:'+cls, cls+' класс', 'class');
    for(const subj of Object.keys(DB[cls])){
      add('s:'+cls+':'+subj, subj, 'subject', {cls, subj});
      link('c:'+cls, 's:'+cls+':'+subj);
      for(const topic of Object.keys(DB[cls][subj])){
        add('t:'+cls+':'+subj+':'+topic, topic, 'topic', {cls, subj, topic});
        link('s:'+cls+':'+subj, 't:'+cls+':'+subj+':'+topic);
        for(const n of DB[cls][subj][topic]){
          add('n:'+n.id, n.title, 'note', {cls, subj, topic, id:n.id});
          link('t:'+cls+':'+subj+':'+topic, 'n:'+n.id);
          (n.tags||[]).forEach(tag => {
            add('tag:'+tag, '#'+tag, 'tag');
            link('n:'+n.id, 'tag:'+tag);
          });
        }
      }
    }
  }

  const W = wrap.clientWidth, H = wrap.clientHeight;
  let scale = 1, offsetX = 0, offsetY = 0;

  function tick(){
    for(let i=0;i<nodes.length;i++){
      for(let j=i+1;j<nodes.length;j++){
        const a=nodes[i], b=nodes[j];
        let dx=b.x-a.x, dy=b.y-a.y;
        let d2 = dx*dx+dy*dy || 1;
        if(d2 > 40000) continue;
        const d = Math.sqrt(d2);
        const f = 400 / d2;
        const fx = dx/d*f, fy = dy/d*f;
        a.vx -= fx; a.vy -= fy;
        b.vx += fx; b.vy += fy;
      }
    }
    for(const l of links){
      const dx = l.b.x-l.a.x, dy = l.b.y-l.a.y;
      const d = Math.hypot(dx,dy) || 1;
      const f = (d - 90) * 0.008;
      const fx = dx/d*f, fy = dy/d*f;
      l.a.vx += fx; l.a.vy += fy;
      l.b.vx -= fx; l.b.vy -= fy;
    }
    for(const n of nodes){
      n.vx += (W/2 - n.x) * 0.0008;
      n.vy += (H/2 - n.y) * 0.0008;
      n.vx *= 0.86; n.vy *= 0.86;
      n.x += n.vx; n.y += n.vy;
    }
  }

  function draw(){
    ctx.clearRect(0,0,W,H);
    ctx.save();
    ctx.translate(offsetX, offsetY);
    ctx.scale(scale, scale);

    ctx.strokeStyle = 'rgba(140,150,200,.22)';
    ctx.lineWidth = 1;
    for(const l of links){
      ctx.beginPath();
      ctx.moveTo(l.a.x, l.a.y);
      ctx.lineTo(l.b.x, l.b.y);
      ctx.stroke();
    }

    const colors = {
      class:'#ffffff', subject:'#a8b4ff', topic:'#8ea2ff',
      note:'#cfd5f5', tag:'#ffc48a'
    };
    for(const n of nodes){
      const isHover = graphState.hover === n;
      ctx.beginPath();
      ctx.arc(n.x, n.y, n.r + (isHover?3:0), 0, Math.PI*2);
      ctx.fillStyle = colors[n.type] || '#ccc';
      ctx.fill();
      if(isHover){ ctx.strokeStyle = '#4a6cf7'; ctx.lineWidth = 2; ctx.stroke(); }
    }

    ctx.font = '12px system-ui,sans-serif';
    ctx.fillStyle = 'rgba(220,225,255,.75)';
    for(const n of nodes){
      if(n.r < 9 && scale < 1.4 && graphState.hover !== n) continue;
      ctx.fillText(n.label, n.x + n.r + 5, n.y + 4);
    }
    ctx.restore();
  }

  function loop(){ tick(); draw(); requestAnimationFrame(loop); }

  let dragging = null, panning = false, lastX=0, lastY=0;
  let downX=0, downY=0;

  function toWorld(e){
    const r = canvas.getBoundingClientRect();
    return {
      x: (e.clientX - r.left - offsetX) / scale,
      y: (e.clientY - r.top  - offsetY) / scale
    };
  }
  function pick(p){
    for(let i=nodes.length-1;i>=0;i--){
      const n = nodes[i];
      if(Math.hypot(n.x-p.x, n.y-p.y) < n.r + 6) return n;
    }
    return null;
  }

  canvas.addEventListener('mousedown', e => {
    downX = e.clientX; downY = e.clientY;
    const p = toWorld(e);
    const n = pick(p);
    if(n){ dragging = n; n.fixed = true; }
    else { panning = true; lastX = e.clientX; lastY = e.clientY; }
  });
  canvas.addEventListener('mousemove', e => {
    const p = toWorld(e);
    const hit = pick(p);
    graphState.hover = hit;
    canvas.style.cursor = hit ? 'pointer' : (panning ? 'grabbing' : 'grab');
    if(dragging){ dragging.x = p.x; dragging.y = p.y; dragging.vx = dragging.vy = 0; }
    else if(panning){
      offsetX += e.clientX - lastX; offsetY += e.clientY - lastY;
      lastX = e.clientX; lastY = e.clientY;
    }
  });
  window.addEventListener('mouseup', e => {
    if(dragging && Math.hypot(e.clientX-downX, e.clientY-downY) < 4){
      openNode(dragging);
    }
    dragging = null; panning = false;
  });

  canvas.addEventListener('wheel', e => {
    e.preventDefault();
    const factor = e.deltaY < 0 ? 1.12 : 0.89;
    scale = Math.max(0.35, Math.min(3, scale * factor));
  }, {passive:false});

  let pinch = null;
  canvas.addEventListener('touchstart', e => {
    if(e.touches.length === 2){
      const [a,b] = e.touches;
      pinch = { d: Math.hypot(a.clientX-b.clientX, a.clientY-b.clientY), s: scale };
    } else if(e.touches.length === 1){
      const t = e.touches[0];
      const p = toWorld(t);
      const n = pick(p);
      if(n) dragging = n; else { panning = true; lastX = t.clientX; lastY = t.clientY; }
    }
  }, {passive:true});
  canvas.addEventListener('touchmove', e => {
    if(e.touches.length === 2 && pinch){
      const [a,b] = e.touches;
      const d = Math.hypot(a.clientX-b.clientX, a.clientY-b.clientY);
      scale = Math.max(0.35, Math.min(3, pinch.s * d / pinch.d));
    } else if(e.touches.length === 1){
      const t = e.touches[0];
      if(dragging){ const p = toWorld(t); dragging.x = p.x; dragging.y = p.y; }
      else if(panning){
        offsetX += t.clientX - lastX; offsetY += t.clientY - lastY;
        lastX = t.clientX; lastY = t.clientY;
      }
    }
  }, {passive:true});
  canvas.addEventListener('touchend', () => { dragging=null; panning=false; pinch=null; });

  graphState = { hover:null };
  loop();
}

function openNode(n){
  if(n.type === 'note' || n.type === 'topic'){
    cur = {...cur, cls:n.cls, subj:n.subj, topic:n.topic, view:'notes', favOnly:false};
  } else if(n.type === 'subject'){
    cur = {...cur, cls:n.cls, subj:n.subj, topic:null, view:'notes', favOnly:false};
  } else if(n.type === 'class'){
    cur = {...cur, cls:n.id.slice(2), subj:null, topic:null, view:'notes', favOnly:false};
  } else {
    cur = {...cur, query:n.label.replace(/^#/,''), view:'notes', favOnly:false};
    $('searchInput').value = cur.query;
  }
  renderAll();
}

/* ============================================================
   7. МОБИЛЬНОЕ МЕНЮ
   ============================================================ */
const sidebar = $('sidebar'), overlay = $('overlay');
$('burger').onclick  = () => { sidebar.classList.add('open'); overlay.classList.add('on'); };
overlay.onclick      = closeSidebar;
function closeSidebar(){ sidebar.classList.remove('open'); overlay.classList.remove('on'); }

/* ============================================================
   8. НАВИГАЦИЯ
   ============================================================ */
$('navNotes').onclick = () => { cur = {...cur, view:'notes', favOnly:false}; closeSidebar(); renderAll(); };
$('navFav').onclick   = () => { cur = {...cur, view:'favorites', favOnly:true}; closeSidebar(); renderAll(); };
$('navGraph').onclick = () => { cur = {...cur, view:'graph'}; closeSidebar(); renderAll(); };
$('searchInput').oninput = e => {
  cur.query = e.target.value.trim(); cur.view='notes'; renderContent();
};

/* ============================================================
   9. РИСОВАНИЕ
   ============================================================ */
class Board {
  constructor(canvas){
    this.c = canvas; this.ctx = canvas.getContext('2d');
    this.color = '#1e2233'; this.size = 3; this.eraser = false;
    this.drawing = false; this.history = []; this.hasContent = false;
    this.reset(); this.bind();
  }
  reset(){
    const {ctx,c} = this;
    ctx.fillStyle = '#fff'; ctx.fillRect(0,0,c.width,c.height);
    ctx.lineCap = 'round'; ctx.lineJoin = 'round';
    this.history = [c.toDataURL()]; this.hasContent = false;
  }
  snapshot(){
    this.history.push(this.c.toDataURL());
    if(this.history.length > 30) this.history.shift();
  }
  undo(){
    if(this.history.length <= 1) return;
    this.history.pop();
    const img = new Image();
    img.onload = () => {
      const {ctx,c} = this;
      ctx.fillStyle = '#fff'; ctx.fillRect(0,0,c.width,c.height);
      ctx.drawImage(img,0,0);
    };
    img.src = this.history[this.history.length-1];
  }
  pos(e){
    const r = this.c.getBoundingClientRect();
    const p = e.touches ? e.touches[0] : e;
    return {
      x: (p.clientX - r.left) * (this.c.width  / r.width),
      y: (p.clientY - r.top ) * (this.c.height / r.height)
    };
  }
  start(e){ e.preventDefault(); this.drawing = true;
    const p = this.pos(e); this.ctx.beginPath(); this.ctx.moveTo(p.x, p.y); }
  move(e){
    if(!this.drawing) return;
    e.preventDefault();
    const p = this.pos(e);
    this.ctx.strokeStyle = this.eraser ? '#fff' : this.color;
    this.ctx.lineWidth = this.eraser ? this.size*4 : this.size;
    this.ctx.lineTo(p.x, p.y); this.ctx.stroke();
    this.hasContent = true;
  }
  end(){ if(!this.drawing) return; this.drawing = false; this.snapshot(); }
  bind(){
    const c = this.c;
    c.addEventListener('mousedown', e => this.start(e));
    c.addEventListener('mousemove', e => this.move(e));
    window.addEventListener('mouseup', () => this.end());
    c.addEventListener('mouseleave', () => this.end());
    c.addEventListener('touchstart', e => this.start(e), {passive:false});
    c.addEventListener('touchmove',  e => this.move(e),  {passive:false});
    c.addEventListener('touchend',   () => this.end());
  }
  toDataURL(){ return this.hasContent ? this.c.toDataURL('image/png') : null; }
}

const board = new Board($('board'));

document.querySelectorAll('.swatch').forEach(sw => sw.onclick = () => {
  document.querySelectorAll('.swatch').forEach(x => x.classList.remove('active'));
  sw.classList.add('active');
  board.color = sw.dataset.color; board.eraser = false;
  $('eraserBtn').classList.remove('active');
});
$('brushSize').oninput = e => board.size = +e.target.value;
$('eraserBtn').onclick = e => {
  board.eraser = !board.eraser;
  e.target.classList.toggle('active', board.eraser);
};
$('undoBtn').onclick  = () => board.undo();
$('clearBtn').onclick = () => board.reset();
$('dlCanvasBtn').onclick = () => {
  if(!board.hasContent) return alert('Нарисуйте что-нибудь сначала');
  const a = document.createElement('a');
  a.href = board.c.toDataURL('image/png');
  a.download = 'рисунок_' + Date.now() + '.png';
  a.click();
};

/* ============================================================
   10. ТЕГИ
   ============================================================ */
let pendingTags = [];
function renderTags(){
  const box = $('tagsBox');
  box.querySelectorAll('.tag-pill').forEach(x => x.remove());
  pendingTags.forEach(t => {
    const pill = document.createElement('span');
    pill.className = 'tag-pill';
    pill.innerHTML = '#' + esc(t) + ' <b>✕</b>';
    pill.querySelector('b').onclick = () => {
      pendingTags = pendingTags.filter(x => x !== t); renderTags();
    };
    box.insertBefore(pill, $('tagInput'));
  });
}
$('tagInput').addEventListener('keydown', e => {
  if(e.key === 'Enter' || e.key === ','){
    e.preventDefault();
    const v = e.target.value.trim().replace(/^#/,'').toLowerCase();
    if(v && !pendingTags.includes(v) && pendingTags.length < 10){
      pendingTags.push(v); renderTags();
    }
    e.target.value = '';
  }
  if(e.key === 'Backspace' && !e.target.value && pendingTags.length){
    pendingTags.pop(); renderTags();
  }
});

/* ============================================================
   11. МОДАЛКА
   ============================================================ */
const modal = $('modalBg');

function switchTab(name){
  document.querySelectorAll('.tab').forEach(t =>
    t.classList.toggle('active', t.dataset.tab === name));
  ['text','file','photo','audio','draw'].forEach(k => {
    $('pane-' + k).style.display = (k === name) ? '' : 'none';
  });
}
document.querySelectorAll('.tab').forEach(t => t.onclick = () => switchTab(t.dataset.tab));

function openModal(){
  const selClass = $('selClass');
  selClass.innerHTML = CLASSES.map(c => `<option>${c}</option>`).join('');
  if(cur.cls) selClass.value = cur.cls;

  const subs = [...new Set([...DEFAULT_SUBJECTS, ...Object.keys(DB[cur.cls] || {})])];
  $('subjectList').innerHTML = subs.map(s => `<option value="${s}">`).join('');
  $('inpSubject').value = cur.subj || '';
  $('inpTopic').value   = cur.topic || '';
  $('inpTitle').value   = '';
  $('inpText').value    = '';
  $('interim').textContent = '';
  $('ocrStatus').textContent = '';
  $('photoPreview').style.display = 'none';
  $('photoPreview').src = '';
  $('ocrBtn').disabled = true;
  $('ocrProgress').style.display = 'none';
  $('fileDrop').innerHTML = 'Нажмите или перетащите .txt / .md файл<input type="file" id="fileInput" accept=".txt,.md,text/plain" hidden>';
  const fi = $('fileInput');
  fi.onchange = e => e.target.files[0] && readTextFile(e.target.files[0]);
  $('fileDrop').onclick = () => fi.click();

  pendingTags = []; renderTags();
  board.reset();
  switchTab('text');
  modal.classList.add('open');
}
function closeModal(){ modal.classList.remove('open'); stopRecognition(); }
$('addBtn').onclick    = openModal;
$('cancelBtn').onclick = closeModal;
modal.onclick = e => { if(e.target === modal) closeModal(); };

/* ============================================================
   12. ФАЙЛ
   ============================================================ */
const fileDrop = $('fileDrop');
fileDrop.ondragover  = e => { e.preventDefault(); fileDrop.style.borderColor = '#4a6cf7'; };
fileDrop.ondragleave = () => fileDrop.style.borderColor = '';
fileDrop.ondrop = e => {
  e.preventDefault(); fileDrop.style.borderColor = '';
  if(e.dataTransfer.files[0]) readTextFile(e.dataTransfer.files[0]);
};
function readTextFile(file){
  const r = new FileReader();
  r.onload = () => {
    $('inpText').value = r.result;
    fileDrop.innerHTML = `✅ Загружен: <b>${esc(file.name)}</b>`;
  };
  r.readAsText(file, 'UTF-8');
}

/* ============================================================
   13. ФОТО → ТЕКСТ
   ============================================================ */
const photoInput = $('photoInput'), photoDrop = $('photoDrop');
let photoFile = null;

photoDrop.onclick = () => photoInput.click();
photoDrop.ondragover  = e => { e.preventDefault(); photoDrop.style.borderColor='#4a6cf7'; };
photoDrop.ondragleave = () => photoDrop.style.borderColor='';
photoDrop.ondrop = e => {
  e.preventDefault(); photoDrop.style.borderColor='';
  if(e.dataTransfer.files[0]) loadPhoto(e.dataTransfer.files[0]);
};
photoInput.onchange = e => e.target.files[0] && loadPhoto(e.target.files[0]);

function loadPhoto(file){
  photoFile = file;
  const prev = $('photoPreview');
  prev.src = URL.createObjectURL(file);
  prev.style.display = 'block';
  $('ocrBtn').disabled = false;
  $('ocrStatus').textContent = `Файл: ${file.name} (${(file.size/1024).toFixed(0)} КБ)`;
}

$('ocrBtn').onclick = async () => {
  if(!photoFile) return;
  const btn = $('ocrBtn'), bar = $('ocrProgress'),
        barInner = bar.firstElementChild, status = $('ocrStatus');
  btn.disabled = true; bar.style.display = 'block'; barInner.style.width='0%';
  status.textContent = 'Загрузка нейросети…';
  try {
    const worker = await Tesseract.createWorker(['rus','eng'], 1, {
      logger: m => {
        if(m.status === 'recognizing text'){
          barInner.style.width = Math.round(m.progress*100) + '%';
          status.textContent = `Распознавание… ${Math.round(m.progress*100)}%`;
        } else status.textContent = m.status + '…';
      }
    });
    const {data:{text}} = await worker.recognize(photoFile);
    await worker.terminate();
    const clean = text.replace(/\n{3,}/g,'\n\n').trim();
    if(clean){
      const ta = $('inpText');
      ta.value = (ta.value ? ta.value + '\n\n' : '') + clean;
      status.textContent = `✅ Распознано символов: ${clean.length}`;
    } else status.textContent = '⚠️ Текст не найден';
    barInner.style.width = '100%';
  } catch(err){ status.textContent = '❌ Ошибка: ' + err.message; }
  finally { btn.disabled = false; }
};

/* ============================================================
   14. АУДИО → ТЕКСТ
   ============================================================ */
const SR = window.SpeechRecognition || window.webkitSpeechRecognition;
let recognition = null, recording = false;
const recBtn = $('recBtn'), interimBox = $('interim');

function stopRecognition(){
  if(recognition && recording){
    recording = false;
    try { recognition.stop(); } catch(_){}
    recBtn.classList.remove('recording');
    recBtn.textContent = '🎙️ Начать запись';
    interimBox.textContent = '';
  }
}
recBtn.onclick = () => {
  if(!SR) return alert('Ваш браузер не поддерживает распознавание речи.\nИспользуйте Chrome или Edge.');
  if(recording){ stopRecognition(); return; }

  recognition = new SR();
  recognition.lang = 'ru-RU';
  recognition.continuous = true;
  recognition.interimResults = true;

  recognition.onresult = e => {
    let fin = '', int = '';
    for(let i=e.resultIndex; i<e.results.length; i++){
      const t = e.results[i][0].transcript;
      if(e.results[i].isFinal) fin += t + ' ';
      else int += t;
    }
    if(fin){
      const ta = $('inpText');
      ta.value += (ta.value && !ta.value.endsWith('\n') ? '\n' : '') + fin.trim();
    }
    interimBox.textContent = int;
  };
  recognition.onerror = e => { interimBox.textContent = 'Ошибка: ' + e.error; stopRecognition(); };
  recognition.onend   = () => { if(recording){ try{ recognition.start(); }catch(_){} } };

  recognition.start();
  recording = true;
  recBtn.classList.add('recording');
  recBtn.textContent = '⏹ Остановить запись';
};

/* ============================================================
   15. СОХРАНЕНИЕ
   ============================================================ */
$('saveBtn').onclick = () => {
  const cls   = $('selClass').value;
  const subj  = $('inpSubject').value.trim();
  const topic = $('inpTopic').value.trim();
  const title = $('inpTitle').value.trim() || 'Без названия';
  const text  = $('inpText').value.trim();
  const image = board.toDataURL();

  const rest = $('tagInput').value.trim().replace(/^#/,'').toLowerCase();
  if(rest && !pendingTags.includes(rest)) pendingTags.push(rest);

  if(!subj || !topic) return alert('Заполните предмет и тему');
  if(!text && !image) return alert('Конспект пуст: нет ни текста, ни рисунка');

  DB[cls] ??= {};
  DB[cls][subj] ??= {};
  DB[cls][subj][topic] ??= [];
  DB[cls][subj][topic].push({
    id: Date.now(), title, text, image,
    tags: [...pendingTags],
    fav: false,
    date: new Date().toISOString()
  });

  saveDB();
  cur = {...cur, cls, subj, topic, view:'notes', favOnly:false};
  stopRecognition();
  closeModal();
  renderAll();
};

/* ============================================================
   16. СТАРТ
   ============================================================ */
(function boot(){
  const session = localStorage.getItem(SESSION_KEY);
  if(session && loadUsers()[session]) startSession(session);
})();

window.addEventListener('resize', () => {
  if(cur.view === 'graph' && graphState) initGraph();
});
</script>
</body>
</html>
