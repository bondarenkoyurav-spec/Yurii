[index.html](https://github.com/user-attachments/files/23833030/index.html)
<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Invest&Help — інвестиційно-соціальний краудфандинг</title>
<meta name="description" content="Платформа інвестиційно-соціального краудфандингу для малого і середнього бізнесу та волонтерських проектів.">

<style>
:root{
  --bg:#0f1724; 
  --card:#071028; 
  --accent:#22c1c3; 
  --accent-2:#6ee7b7; 
  --muted:#9fb0c8; 
  --radius:14px; 
  --maxw:1200px; 
  --ff: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
}

*{box-sizing:border-box}
html,body{height:100%;margin:0;font-family:var(--ff);background:var(--bg);color:#eaf6f5}
a{color:var(--accent-2);text-decoration:none}
.wrap{max-width:var(--maxw);margin:0 auto;padding:28px}

/* Header */
header{position:sticky;top:14px;z-index:60}
.nav{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:12px;background:var(--bg);border-radius:12px;}
.brand{display:flex;align-items:center;gap:12px;font-family:'Segoe UI', sans-serif;}
.logo{
  width:72px;height:42px;border-radius:10px;display:flex;justify-content:center;align-items:center;
  font-weight:700;font-size:18px;color:#ffffff;background:var(--bg);position:relative;z-index:1;
}
.logo::after{
  content:"";
  position:absolute;
  top:-4px; left:-4px; right:-4px; bottom:-4px;
  border-radius:14px;
  background: linear-gradient(135deg, #8a4cff,#00e676,#4fc3f7,#006c9c);
  z-index:-1;
  filter:blur(12px);
  animation: glowLogo 2s ease-in-out infinite alternate;
}
@keyframes glowLogo {0%{opacity:0.5;}50%{opacity:1;}100%{opacity:0.5;}}

nav ul{display:flex;gap:12px;list-style:none;margin:0;padding:0}
nav li{padding:8px 12px;border-radius:8px}
nav a{font-weight:600;color:var(--muted)}
.cta{padding:8px 14px;background:linear-gradient(90deg,var(--accent),var(--accent-2));border-radius:10px;color:#042024;font-weight:800}

.hero {
  display: grid;
  grid-template-columns: 1fr 150px; /* ліва - текст, права - показники */
  gap: 24px;
  align-items:center;
  padding:40px 0;
}
.contact-card {
  width:350px;      /* однакова ширина */
  min-height:100px; /* однакова висота */
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
}

/* HERO */
.hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;padding:40px 0}
.hero h1{font-size:40px;margin:0 0 12px;line-height:1.02}
.hero p{color:var(--muted);margin:0 0 20px}
.hero .actions{display:flex;gap:12px}
.btn{padding:10px 14px;border-radius:10px;font-weight:700;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit;cursor:pointer;transition:0.3s}
.btn:hover{transform:scale(1.05)}
.btn.primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));border:0;color:#042024}
.card{background:var(--card);padding:18px;border-radius:16px;transition:transform 0.3s, box-shadow 0.3s}
.card:hover{transform:translateY(-5px) scale(1.02);box-shadow:0 15px 40px rgba(0,0,0,0.6)}

/* Project grid */
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:18px}
.project{border-radius:12px;overflow:hidden;background:var(--card);box-shadow:0 8px 30px rgba(2,6,23,0.6);display:flex;flex-direction:column;cursor:pointer}
.project .body{padding:12px;display:flex;flex-direction:column;gap:8px}
.project h3{margin:0;font-size:16px}
.project p{margin:0;color:var(--muted);font-size:14px}
.progress{height:10px;background:rgba(255,255,255,0.03);border-radius:999px;overflow:hidden;margin:4px 0}
.progress > i{display:block;height:100%;background:linear-gradient(90deg,var(--accent),var(--accent-2))}
.meta{display:flex;justify-content:space-between;font-size:13px;color:var(--muted);margin-top:6px}

/* Form */
.form input,.form textarea,.form select{width:100%;padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit;margin-bottom:10px}

/* Footer */
footer{padding:28px 0;color:var(--muted);text-align:center}

/* Responsive */
@media (max-width:980px){.hero{grid-template-columns:1fr}.grid{grid-template-columns:repeat(2,1fr)}nav ul{display:none}}
@media (max-width:640px){.grid{grid-template-columns:1fr}}
</style>
</head>
<body>
<div class="wrap">
  <!-- HEADER -->
  <header>
    <div class="nav">
      <div class="brand">
        <div class="logo">CoRise</div>
      </div>
      <nav>
        <ul>
          <li><a href="#top">Головна</a></li>
          <li><a href="#projects">Проєкти</a></li>
          <li><a href="#how">Як це працює</a></li>
          <li><a href="#contact">Контакти</a></li>
        </ul>
      </nav>
      <div style="display:flex;gap:10px;align-items:center">
        <a class="cta" href="#create">Запустити проєкт</a>
        <a class="btn" href="#login">Увійти</a>
      </div>
    </div>
  </header>

 <!-- HERO -->
<section class="hero">
  <!-- Ліва колонка: текст -->
  <div>
    <h1 style="font-size:36px">Інвестиційно‑соціальний краудфандинг<br><span style="color:var(--accent-2);font-size:32px">для малого, середнього бізнесу та волонтерських ініціатив</span></h1>
    <p style="margin-bottom:20px;color:var(--muted)">Платформа допомагає з'єднати відповідальних інвесторів, бізнес та волонтерські проєкти — прозоро, безпечно та з фокусом на соціальний ефект.</p>
    <div class="actions">
      <a class="btn primary" href="#projects">Переглянути проєкти</a>
      <a class="btn" href="#how">Як це працює</a>
      <a class="btn" href="#create">Запустити проєкт</a>
    </div>
  </div>

  <!-- Права колонка: показники -->
  <div style="display:flex;flex-direction:column;gap:12px;align-items:flex-end">
    <div class="card" style="width:350px;text-align:center;padding:10px;">
      <div style="font-size:22px;font-weight:700;color:var(--accent)">250+</div>
      <div style="color:var(--muted);font-size:12px">Успішних проєктів</div>
    </div>
    <div class="card" style="width:350px;text-align:center;padding:10px;">
      <div style="font-size:22px;font-weight:700;color:var(--accent)">1200+</div>
      <div style="color:var(--muted);font-size:12px">Задоволених інвесторів</div>
    </div>
    <div class="card" style="width:350px;text-align:center;padding:10px;">
      <div style="font-size:22px;font-weight:700;color:var(--accent)">15 млн+</div>
      <div style="color:var(--muted);font-size:12px">Залучених USD</div>
    </div>
    <div class="card" style="width:350px;text-align:center;padding:10px;">
      <div style="font-size:22px;font-weight:700;color:var(--accent)">100%</div>
      <div style="color:var(--muted);font-size:12px">Прозорість та безпека</div>
    </div>
  </div>
</section>

 <h2>Візія</h2>
<p style="margin-bottom:20px;color:var(--muted)">Ми створюємо платформу, яка стане місцем об’єднання людей навколо реалізації ідей, що змінюють громади, бізнес і суспільство. Це простір, де підприємці, волонтери та небайдужі громадяни можуть разом перетворювати плани на реальні проєкти. Платформа забезпечить прозорий, безпечний і зручний процес збору коштів, сприяючи довірі між авторами ініціатив і тими, хто їх підтримує. Нашою метою є формування культури взаємопідтримки та спільного розвитку — коли кожен внесок, навіть найменший, стає частиною великої зміни. Ми прагнемо, щоб ця платформа стала каталізатором для появи нових можливостей для розвитку малих та середніх бізнесів та суспільних ініціатив.</p>
<br></br>

  <!-- PROJECTS -->
  <section id="projects">
    <h2>Останні проєкти</h2>
    <div id="grid" class="grid"></div>
  </section>
<br></br>
  <!-- HOW IT WORKS -->
  <section id="how">
    <h2>Як це працює</h2>
    <div style="display:flex;gap:12px;flex-wrap:wrap">
      <div class="card"><div style="font-weight:800">1. Реєструйтесь</div><div style="color:var(--muted)">Створіть акаунт і налаштуйте профіль.</div></div>
      <div class="card"><div style="font-weight:800">2. Подайте проєкт</div><div style="color:var(--muted)">Опишіть ціль, категорію та бюджет.</div></div>
      <div class="card"><div style="font-weight:800">3. Залучайте інвестиції</div><div style="color:var(--muted)">Інвестори обирають проєкти і підтримують їх фінансово.</div></div>
    </div>
  </section>
<br></br>
  <!-- CREATE PROJECT -->
  <section id="create">
    <h2>Запустити проєкт</h2>
    <div class="card form">
      <input id="p_title" placeholder="Назва проєкту">
      <select id="p_category">
        <option value="business">Бізнес</option>
        <option value="social">Соціальний</option>
        <option value="volunteer">Волонтерський</option>
      </select>
      <input id="p_goal" type="number" placeholder="Цільова сума (USD)">
      <textarea id="p_desc" rows="5" placeholder="Короткий опис проєкту"></textarea>
      <button class="btn primary" onclick="createProject()">Опублікувати проєкт (демо)</button>
      <div style="color:var(--muted);font-size:13px;margin-top:8px">Демо зберігається лише у поточній сесії.</div>
    </div>
  </section>
<br></br>
 <!-- CONTACT -->
<section id="contact">
  <h2>Контакти</h2>
  <div style="display:flex;gap:12px;flex-wrap:wrap;justify-content:center;text-align:center">
    <div class="card contact-card">
      <div style="font-weight:700;margin-bottom:4px">Підтримка</div>
      support@CoRise.example
    </div>
    <div class="card contact-card">
      <div style="font-weight:700;margin-bottom:4px">Офіс</div>
      Київ, Україна
    </div>
    <div class="card contact-card">
      <div style="font-weight:700;margin-bottom:4px">Телефон</div>
      +380 44 123 45 67
    </div>
  </div>
<footer>© <span id="y">2025</span> CoRise · Платформа демо</footer>

</section>

<script>
const projects = [
  {id:1,title:"Кав'ярня на колесах",category:"business",goal:5000,raised:3200,desc:"Мобільна кав'ярня для підтримки локальних фермерів."},
  {id:2,title:"Бібліотека для дітей",category:"social",goal:2000,raised:1800,desc:"Створення дитячої бібліотеки у селі."},
  {id:3,title:"Волонтерська допомога ЗСУ",category:"volunteer",goal:10000,raised:7500,desc:"Закупівля спорядження та медикаментів для бійців."},
  {id:4,title:"Еко-магазин",category:"business",goal:8000,raised:4100,desc:"Продаж екологічних товарів та локальної продукції."},
  {id:5,title:"Соціальний центр для літніх",category:"social",goal:3000,raised:1200,desc:"Простір для спілкування та допомоги літнім людям."},
  {id:6,title:"Допомога тваринам",category:"volunteer",goal:4000,raised:2500,desc:"Придбання корму та медичного забезпечення для притулків."}
];
const grid=document.getElementById("grid");
function renderProjects(list){
  grid.innerHTML='';
  list.forEach(p=>{
    const card=document.createElement("div");
    card.className="project card";
    card.innerHTML=`<div class="body">
      <h3>${p.title}</h3>
      <p>${p.desc}</p>
      <div class="progress"><i style="width:${Math.min(100,p.raised/p.goal*100)}%"></i></div>
      <div class="meta"><span>$${p.raised} / $${p.goal}</span><span>${p.category}</span></div>
      <button class="btn primary" onclick="donate(${p.id})">Донатити</button>
    </div>`;
    grid.appendChild(card);
  });
}
renderProjects(projects);
function createProject(){
  const title=document.getElementById("p_title").value;
  const category=document.getElementById("p_category").value;
  const goal=parseFloat(document.getElementById("p_goal").value)||0;
  const desc=document.getElementById("p_desc").value;
  if(!title||!desc||goal<=0){alert("Будь ласка, заповніть усі поля коректно."); return;}
  const newProj={id:projects.length+1,title,category,goal,raised:0,desc};
  projects.push(newProj);
  renderProjects(projects);
  alert("Проєкт додано (демо).");
  document.getElementById("p_title").value="";
  document.getElementById("p_goal").value="";
  document.getElementById("p_desc").value="";
}
function donate(id){
  const amount = prompt("Введіть суму донату USD:");
  if(amount && !isNaN(amount)){
    const project = projects.find(p=>p.id===id);
    project.raised += Number(amount);
    renderProjects(projects);
    alert(`Дякуємо за вашу підтримку $${amount}!`);
  }
}
document.getElementById("y").textContent=new Date().getFullYear();
</script>
</body>
</html>   
