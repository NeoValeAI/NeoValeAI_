<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>AI Hustle — Turn ideas into millions</title>
  <meta name="description" content="For young people who hate school but love AI — learn, get inspired, and build profitable AI projects.">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="brand">AI Hustle</div>
    <nav>
      <button id="langBtn">NL</button>
    </nav>
  </header>

  <main class="container">
    <section id="hero" class="hero">
      <h1 data-i18n="hero_title">Make millions with AI — even if you hate school</h1>
      <p data-i18n="hero_sub">Practical steps, project blueprints, and an AI idea generator to kickstart your hustle.</p>
      <div class="cta-row">
        <button id="startBtn" class="btn" data-i18n="get_started">Get started</button>
        <button id="ideaBtn" class="btn alt" data-i18n="generate_idea">Generate AI Idea</button>
      </div>
    </section>

    <section id="features" class="cards">
      <article class="card">
        <h3 data-i18n="feature_1_title">Mini-courses</h3>
        <p data-i18n="feature_1_desc">Short, project-based lessons: build an AI bot, start a gig, ship an MVP.</p>
      </article>
      <article class="card">
        <h3 data-i18n="feature_2_title">Idea Generator</h3>
        <p data-i18n="feature_2_desc">An AI-powered generator that gives 10 low-cost, high-margin project ideas.</p>
      </article>
      <article class="card">
        <h3 data-i18n="feature_3_title">Community</h3>
        <p data-i18n="feature_3_desc">Connect with other doers, mentors, and collaborators.</p>
      </article>
    </section>

    <section id="generator" class="panel hidden">
      <h2 data-i18n="gen_title">AI Idea Generator</h2>
      <p data-i18n="gen_sub">Click to get ideas you can start this week.</p>
      <div id="ideasList" class="ideas"></div>
      <div class="note" data-i18n="gen_note">Tip: combine ideas and iterate fast.</div>
      <button id="closeGen" class="btn" data-i18n="close">Close</button>
    </section>

    <section id="resources" class="panel small">
      <h2 data-i18n="res_title">Resources</h2>
      <ul>
        <li data-i18n="res_1">Step-by-step project guides</li>
        <li data-i18n="res_2">Budget templates</li>
        <li data-i18n="res_3">Pitch & freelance scripts</li>
      </ul>
    </section>

    <footer class="site-footer">
      <small>© <span id="year"></span> AI Hustle — Built for young makers.</small>
    </footer>
  </main>

  <script src="translations.js"></script>
  <script src="script.js"></script>
</body>
</html>
:root{
  --bg:#0f1724; --card:#0b1220; --accent:#6ee7b7; --muted:#9ca3af; --glass: rgba(255,255,255,0.03);
}
*{box-sizing:border-box}
body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; background:linear-gradient(180deg,#071023 0%, #071126 100%); color:#e6eef6; -webkit-font-smoothing:antialiased}
.container{max-width:980px;margin:32px auto;padding:16px}
.site-header{display:flex;justify-content:space-between;align-items:center;padding:12px 16px;background:transparent}
.brand{font-weight:800;font-size:20px;letter-spacing:0.6px}
nav button{background:var(--glass);border:1px solid rgba(255,255,255,0.06);color:var(--muted);padding:8px 12px;border-radius:8px;cursor:pointer}
.hero{padding:28px;margin:16px 0;background:linear-gradient(90deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));border-radius:12px}
.hero h1{margin:0 0 8px;font-size:28px}
.hero p{margin:0 0 16px;color:var(--muted)}
.btn{background:var(--accent);border:none;padding:10px 14px;border-radius:10px;color:#032;cursor:pointer;font-weight:700}
.btn.alt{background:transparent;border:1px solid rgba(255,255,255,0.08);color:var(--muted)}

.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px;margin:18px 0}
.card{background:var(--card);padding:16px;border-radius:10px;box-shadow:0 4px 18px rgba(2,6,23,0.6)}

.panel{background:var(--card);padding:16px;border-radius:10px;margin:12px 0}
.small{padding:12px}
.hidden{display:none}
.ideas{display:flex;flex-direction:column;gap:8px;margin:12px 0}
.idea-pill{background:var(--glass);padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.03)}

.note{color:var(--muted);font-size:13px;margin-top:8px}
.site-footer{text-align:center;margin:22px 0;color:var(--muted)}

@media (max-width:560px){
  .hero h1{font-size:20px}
}
const TRANSLATIONS = {
  "en": {
    "hero_title":"Make millions with AI — even if you hate school",
    "hero_sub":"Practical steps, project blueprints, and an AI idea generator to kickstart your hustle.",
    "get_started":"Get started",
    "generate_idea":"Generate AI Idea",
    "feature_1_title":"Mini-courses",
    "feature_1_desc":"Short, project-based lessons: build an AI bot, start a gig, ship an MVP.",
    "feature_2_title":"Idea Generator",
    "feature_2_desc":"An AI-powered generator that gives 10 low-cost, high-margin project ideas.",
    "feature_3_title":"Community",
    "feature_3_desc":"Connect with other doers, mentors, and collaborators.",
    "gen_title":"AI Idea Generator",
    "gen_sub":"Click to get ideas you can start this week.",
    "gen_note":"Tip: combine ideas and iterate fast.",
    "close":"Close",
    "res_title":"Resources",
    "res_1":"Step-by-step project guides",
    "res_2":"Budget templates",
    "res_3":"Pitch & freelance scripts"
  },
  "nl": {
    "hero_title":"Verdien miljoenen met AI — ook als je een hekel hebt aan school",
    "hero_sub":"Praktische stappen, projecthandleidingen en een AI-idee-generator om je hustle te starten.",
    "get_started":"Begin nu",
    "generate_idea":"Genereer idee",
    "feature_1_title":"Mini-cursussen",
    "feature_1_desc":"Korte, projectgerichte lessen: bouw een AI-bot, begin een gig, lever een MVP.",
    "feature_2_title":"Idee-generator",
    "feature_2_desc":"Een AI-gestuurde generator die 10 goedkope, hoge-winsten projectideeën geeft.",
    "feature_3_title":"Community",
    "feature_3_desc":"Verbind met andere makers, mentoren en samenwerkers.",
    "gen_title":"AI Idee-generator",
    "gen_sub":"Klik om ideeën te krijgen die je deze week kunt starten.",
    "gen_note":"Tip: combineer ideeën en werk snel iteratief.",
    "close":"Sluiten",
    "res_title":"Hulpbronnen",
    "res_1":"Stapsgewijze projectgidsen",
    "res_2":"Budget-sjablonen",
    "res_3":"Pitch- & freelance-scripts"
  }
};
/* Lightweight client: translation, language toggle, idea generator.
   To use OpenAI in production, add a serverless function that holds the API key.
   See comments below for an example server endpoint. */

const defaultLang = localStorage.getItem('lang') || 'en';
let LANG = defaultLang;

function t(key){ return TRANSLATIONS[LANG][key] || TRANSLATIONS['en'][key] || key; }

function applyTranslations(){
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    el.textContent = t(key);
  });
}

document.addEventListener('DOMContentLoaded', ()=>{
  applyTranslations();
  document.getElementById('year').textContent = new Date().getFullYear();
  document.getElementById('langBtn').addEventListener('click', ()=>{
    LANG = LANG === 'en' ? 'nl' : 'en';
    localStorage.setItem('lang', LANG);
    document.getElementById('langBtn').textContent = LANG === 'en' ? 'NL' : 'EN';
    applyTranslations();
  });
  document.getElementById('ideaBtn').addEventListener('click', openGenerator);
  document.getElementById('closeGen').addEventListener('click', ()=>{
    document.getElementById('generator').classList.add('hidden');
  });
});

function openGenerator(){
  const panel = document.getElementById('generator');
  panel.classList.remove('hidden');
  generateIdeas();
}

const SEED_IDEAS = [
  "Micro-SaaS: An AI tool that automates Instagram captions for niche stores, charge €29/month.",
  "Niche tutoring bot: Offer automated homework help for one subject and sell subscriptions.",
  "AI art prints: Generate themed art + print-on-demand; market on Etsy.",
  "Local business lead generator: Use AI to create outreach emails and charge per lead.",
  "Resume & cover letter agency: AI-generated tailored applications for job seekers.",
  "Voice clone gigs: Create custom voice messages for streamers and podcasters.",
  "Chat-based premium course: Combine a mini-course with a paid private chatbot tutor.",
  "Data-labeling microservice: Coordinate micro-tasks and sell cleaned datasets to researchers.",
  "AI-driven dropshipping descriptions: Automate product pages and sell the service.",
  "Micro-consulting: Build 5 templates (e.g., cold email + funnel) and sell as a package."
];

function generateIdeas(){
  const list = document.getElementById('ideasList');
  list.innerHTML = '';
  // Show 6 random ideas from seed
  const shuffled = SEED_IDEAS.sort(()=>0.5-Math.random()).slice(0,6);
  shuffled.forEach(text => {
    const el = document.createElement('div');
    el.className = 'idea-pill';
    el.textContent = text;
    list.appendChild(el);
  });
}

/* --- Example serverless function (Node) to call OpenAI safely ---
   (DO NOT put API keys in the browser)
   Deploy as Netlify Function / Vercel Serverless / AWS Lambda.

exports.handler = async (event) => {
  const body = JSON.parse(event.body || '{}');
  // validate input, rate limit, auth checks here
  const resp = await fetch('https://api.openai.com/v1/chat/completions',{
    method:'POST', headers:{
      'Content-Type':'application/json',
      'Authorization':'Bearer ' + process.env.OPENAI_API_KEY
    },
    body: JSON.stringify({
      model:'gpt-4o-mini',
      messages:[{role:'user', content: 'Generate 10 low-cost AI side hustle ideas for teens'}],
      max_tokens:600
    })
  });
  const data = await resp.json();
  return { statusCode:200, body: JSON.stringify(data) };
};
*/
AI Hustle — static starter website

How to use:
1. Put files in a folder and open index.html to preview.
2. To enable a real AI generator, create a serverless endpoint that calls the OpenAI API (server-side).
3. Deploy the folder on Netlify/Vercel/GitHub Pages.

Scaling ideas:
- Auth & saved profiles (Supabase / Clerk)
- Paid courses & Stripe checkout
- Community hub + mentorship marketplace
- Analytics (Plausible or GA)
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Néo Vale — CV & AI Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="brand">Néo Vale</div>
    <nav>
      <button id="langBtn">NL</button>
    </nav>
  </header>

  <main class="container">
    <section id="hero" class="hero">
      <h1 data-i18n="hero_title">Néo Vale</h1>
      <p data-i18n="hero_sub">Young entrepreneur passionate about AI and helping youth achieve success.</p>
    </section>

    <section id="objective" class="panel">
      <h2 data-i18n="objective_title">Objective</h2>
      <p data-i18n="objective_text">To inspire and guide young people in leveraging AI and entrepreneurship to build successful projects and unlock their potential.</p>
    </section>

    <section id="skills" class="panel">
      <h2 data-i18n="skills_title">Interests & Skills</h2>
      <ul>
        <li>Entrepreneurship</li>
        <li>AI & Technology</li>
        <li>Youth Mentorship</li>
        <li>Creativity & Problem-Solving</li>
        <li>Community Building</li>
      </ul>
    </section>

    <section id="achievements" class="panel">
      <h2 data-i18n="achievements_title">Achievements / Pride</h2>
      <p data-i18n="achievements_text">Proud of contributing to the growth and development of young people, helping them navigate opportunities and think independently about their future.</p>
    </section>

    <section id="ai_ideas" class="panel">
      <h2 data-i18n="ai_title">AI Side Hustle Ideas</h2>
      <p data-i18n="ai_sub">Click the button below to get 6 AI project ideas you can start this week!</p>
      <button id="ideaBtn" class="btn" data-i18n="ai_button">Generate Ideas</button>
      <div id="ideasList" class="ideas"></div>
    </section>

    <section id="location" class="panel">
      <h2 data-i18n="location_title">Location</h2>
      <p>Belgium</p>
    </section>

    <section id="quote" class="panel">
      <h2 data-i18n="quote_title">Motivation Quote</h2>
      <p>"If you don’t try, you’ll never know."</p>
    </section>

    <footer class="site-footer">
      <small>© <span id="year"></span> Néo Vale</small>
    </footer>
  </main>

  <script src="translations.js"></script>
  <script src="script.js"></script>
</body>
</html>
body { font-family: Arial, sans-serif; background: #f4f4f9; color: #333; margin: 0; padding: 0; }
.container { max-width: 800px; margin: 20px auto; padding: 15px; }
.site-header { background: #0b1220; color: #fff; padding: 15px; display: flex; justify-content: space-between; align-items: center; }
.brand { font-size: 22px; font-weight: bold; }
.panel { background: #fff; padding: 15px; margin: 15px 0; border-radius: 8px; box-shadow: 0 2px 6px rgba(0,0,0,0.1); }
h1,h2 { margin: 0 0 10px 0; }
ul { padding-left: 20px; }
.site-footer { text-align: center; margin: 20px 0; color: #555; }
button { padding: 6px 12px; border-radius: 6px; border: none; cursor: pointer; background: #6ee7b7; color: #032; font-weight: bold; }
.ideas { display: flex; flex-direction: column; gap: 8px; margin-top: 12px; }
.idea-pill { background: #e6f7f1; padding: 8px 12px; border-radius: 6px; border: 1px solid #b3e6d8; }
const TRANSLATIONS = {
  "en": {
    "hero_title": "Néo Vale",
    "hero_sub": "Young entrepreneur passionate about AI and helping youth achieve success.",
    "objective_title": "Objective",
    "objective_text": "To inspire and guide young people in leveraging AI and entrepreneurship to build successful projects and unlock their potential.",
    "skills_title": "Interests & Skills",
    "achievements_title": "Achievements / Pride",
    "achievements_text": "Proud of contributing to the growth and development of young people, helping them navigate opportunities and think independently about their future.",
    "ai_title": "AI Side Hustle Ideas",
    "ai_sub": "Click the button below to get 6 AI project ideas you can start this week!",
    "ai_button": "Generate Ideas",
    "location_title": "Location",
    "quote_title": "Motivation Quote"
  },
  "nl": {
    "hero_title": "Néo Vale",
    "hero_sub": "Jonge ondernemer gepassioneerd over AI en het helpen van jongeren om succes te behalen.",
    "objective_title": "Doel",
    "objective_text": "Jongeren inspireren en begeleiden om AI en ondernemerschap te gebruiken voor succesvolle projecten en hun potentieel te ontgrendelen.",
    "skills_title": "Interesses & Vaardigheden",
    "achievements_title": "Prestaties / Trots",
    "achievements_text": "Trots op het bijdragen aan de groei en ontwikkeling van jongeren, hen helpen kansen te zien en zelfstandig na te denken over hun toekomst.",
    "ai_title": "AI Side Hustle Ideeën",
    "ai_sub": "Klik op de knop hieronder om 6 AI-projectideeën te krijgen die je deze week kunt starten!",
    "ai_button": "Genereer Ideeën",
    "location_title": "Locatie",
    "quote_title": "Motiverend citaat"
  }
};
const defaultLang = localStorage.getItem('lang') || 'en';
let LANG = defaultLang;

const SEED_IDEAS = [
  "Micro-SaaS: AI tool that automates Instagram captions for niche stores, charge €29/month.",
  "AI tutoring bot: Offer automated homework help for one subject and sell subscriptions.",
  "AI art prints: Generate themed art + print-on-demand; sell on Etsy.",
  "Local business lead generator: Use AI to create outreach emails and charge per lead.",
  "Resume & cover letter service: AI-generated tailored applications for job seekers.",
  "Voice clone gigs: Create custom voice messages for streamers and podcasters.",
  "Chat-based premium course: Mini-course + paid private chatbot tutor.",
  "Data-labeling microservice: Coordinate micro-tasks and sell cleaned datasets to researchers.",
  "AI-driven dropshipping descriptions: Automate product pages and sell the service.",
  "Micro-consulting templates: Build 5 templates (e.g., cold email + funnel) and sell."
];

function t(key){ return TRANSLATIONS[LANG][key] || TRANSLATIONS['en'][key] || key; }

function applyTranslations(){
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    el.textContent = t(key);
  });
}

function generateIdeas(){
  const list = document.getElementById('ideasList');
  list.innerHTML = '';
  const shuffled = SEED_IDEAS.sort(()=>0.5-Math.random()).slice(0,6);
  shuffled.forEach(text => {
    const el = document.createElement('div');
    el.className = 'idea-pill';
    el.textContent = text;
    list.appendChild(el);
  });
}

document.addEventListener('DOMContentLoaded', ()=>{
  applyTranslations();
  document.getElementById('year').textContent = new Date().getFullYear();
  document.getElementById('langBtn').addEventListener('click', ()=>{
    LANG = LANG === 'en' ? 'nl' : 'en';
    localStorage.setItem('lang', LANG);
    document.getElementById('langBtn').textContent = LANG === 'en' ? 'NL' : 'EN';
    applyTranslations();
  });
  document.getElementById('ideaBtn').addEventListener('click', generateIdeas);
});
const defaultLang = localStorage.getItem('lang') || 'en';
let LANG = defaultLang;

function t(key){ return TRANSLATIONS[LANG][key] || TRANSLATIONS['en'][key] || key; }

function applyTranslations(){
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    el.textContent = t(key);
  });
}

// Voeg hier je OpenAI API key toe
const OPENAI_API_KEY = "YOUR_OPENAI_API_KEY"; // <- zet hier je eigen sleutel

async function generateIdeasAI(){
  const list = document.getElementById('ideasList');
  list.innerHTML = "Generating ideas...";

  try {
    const response = await fetch("https://api.openai.com/v1/chat/completions", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": `Bearer ${OPENAI_API_KEY}`
      },
      body: JSON.stringify({
        model: "gpt-4",
        messages: [
          {
            role: "system",
            content: "You are a helpful assistant that suggests innovative AI-based business ideas for young entrepreneurs."
          },
          {
            role: "user",
            content: "Give me 6 short, practical AI business ideas a young person can start this week."
          }
        ],
        max_tokens: 300
      })
    });

    const data = await response.json();
    const text = data.choices[0].message.content;
    const ideas = text.split(/\n|\d+\./).filter(i => i.trim() !== "");

    list.innerHTML = "";
    ideas.forEach(idea => {
      const el = document.createElement('div');
      el.className = 'idea-pill';
      el.textContent = idea.trim();
      list.appendChild(el);
    });
  } catch(err){
    list.innerHTML = "Error generating ideas. Make sure your API key is correct.";
    console.error(err);
  }
}

document.addEventListener('DOMContentLoaded', ()=>{
  applyTranslations();
  document.getElementById('year').textContent = new Date().getFullYear();
  document.getElementById('langBtn').addEventListener('click', ()=>{
    LANG = LANG === 'en' ? 'nl' : 'en';
    localStorage.setItem('lang', LANG);
    document.getElementById('langBtn').textContent = LANG === 'en' ? 'NL' : 'EN';
    applyTranslations();
  });
  document.getElementById('ideaBtn').addEventListener('click', generateIdeasAI);
});
sk-7Hj2bK9XqU2a...etc...
const OPENAI_API_KEY = "JOUW_API_KEY_HIER";
const OPENAI_API_KEY = "sk-7Hj2bK9XqU2aAbCdEfGhI...";
const OPENAI_API_KEY = "sk-...je code hier...";
sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx
sk-Lk3Gm...AbCdEf1234
const OPENAI_API_KEY = "JOUW_API_KEY_HIER";
const OPENAI_API_KEY = "sk-Lk3Gm...AbCdEf1234";
const OPENAI_API_KEY = "sk-...de sleutel die je net hebt gekregen...";
sk-Fa4H8zjDkX8R7vA9bK1HfJt...
const OPENAI_API_KEY = "sk-JOUWCODEHIER";
const OPENAI_API_KEY = "sk-Fa4H8zjDkX8R7vA9bK1HfJt12345";
const OPENAI_API_KEY = "sk-...JE_EIGEN_KEY_HIER...";
const OPENAI_API_KEY = "sk-...JE_EIGEN_KEY_HIER...";
<section id="blog" class="panel">
  <h2>Waarom jongeren nu met AI moeten starten</h2>
  
  <!-- Motivatie-afbeelding -->
  <img src="motivatie.jpg" alt="Motivatie AI" style="width:100%; max-width:600px; display:block; margin:10px auto; border-radius:8px;">

  <p>Hey, ik ben Néo Vale! Ik weet dat school voor veel jongeren voelt als een verplichting waar je geen passie in kan leggen. Maar wist je dat je je vrije tijd, creativiteit en AI kan gebruiken om iets groots te bouwen? Vandaag wil ik je laten zien waarom nu het moment is om te starten met AI en ondernemerschap.</p>
  
  <ul>
    <li><strong>AI is jouw persoonlijke superkracht:</strong> Met AI-tools kan je sneller leren, nieuwe ideeën bedenken en zelfs producten of diensten maken zonder miljoenen te investeren.</li>
    <li><strong>Begin klein, denk groot:</strong> Je hoeft niet direct een miljard te verdienen. Begin met een klein project, test iets uit, leer en groei.</li>
    <li><strong>Focus op jezelf en anderen:</strong> Gebruik AI om problemen van jezelf of anderen op te lossen. Dat is wat echt waardevol is.</li>
    <li><strong>Durf te proberen:</strong> Het ergste dat kan gebeuren? Je leert iets nieuws. Het beste dat kan gebeuren? Je bouwt een toekomst die jij zelf kiest.</li>
  </ul>

  <p>Jong zijn betekent dat je nog alles kan proberen en leren. Gebruik die tijd verstandig. Experimenteer met AI, deel je ideeën, en bouw iets waar je trots op kan zijn. Start vandaag, zelfs met één klein project.</p>

  <!-- Call-to-action knop -->
  <div style="text-align:center; margin-top:15px;">
    <button id="blogIdeaBtn" class="btn">Klik hier voor 6 AI-ideeën!</button>
  </div>
</section>

<script>
  // Zorg dat de knop werkt als de bestaande AI generator knop
  document.getElementById('blogIdeaBtn').addEventListener('click', ()=>{
    const ideaBtn = document.getElementById('ideaBtn');
    if(ideaBtn){
      ideaBtn.click(); // Simuleer klikken op de bestaande "Generate Ideas" knop
      window.scrollTo({ top: document.getElementById('ai_ideas').offsetTop, behavior: 'smooth' });
    }
  });
</script>
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>NeoValeAI</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f4f4f9; color: #333; margin:0; padding:0; }
    .container { max-width: 800px; margin:20px auto; padding:15px; }
    .site-header { background:#0b1220; color:#fff; padding:15px; display:flex; justify-content:space-between; align-items:center; }
    .brand { font-size:22px; font-weight:bold; }
    .panel { background:#fff; padding:15px; margin:15px 0; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.1); }
    h1,h2 { margin:0 0 10px 0; }
    ul { padding-left:20px; }
    .site-footer { text-align:center; margin:20px 0; color:#555; }
    button { padding:6px 12px; border-radius:6px; border:none; cursor:pointer; background:#6ee7b7; color:#032; font-weight:bold; }
    .ideas { display:flex; flex-direction:column; gap:8px; margin-top:12px; }
    .idea-pill { background:#e6f7f1; padding:8px 12px; border-radius:6px; border:1px solid #b3e6d8; }
    img { width:100%; max-width:600px; display:block; margin:10px auto; border-radius:8px; }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="brand">NeoValeAI</div>
    <nav>
      <button id="langBtn">NL</button>
    </nav>
  </header>

  <main class="container">
    <!-- Hero / Intro -->
    <section id="hero" class="panel">
      <h1>Néo Vale</h1>
      <p>Young entrepreneur passionate about AI and helping youth achieve success.</p>
    </section>

    <!-- Objective -->
    <section id="objective" class="panel">
      <h2>Objective</h2>
      <p>To inspire and guide young people in leveraging AI and entrepreneurship to build successful projects and unlock their potential.</p>
    </section>

    <!-- Skills -->
    <section id="skills" class="panel">
      <h2>Interests & Skills</h2>
      <ul>
        <li>Entrepreneurship</li>
        <li>AI & Technology</li>
        <li>Youth Mentorship</li>
        <li>Creativity & Problem-Solving</li>
        <li>Community Building</li>
      </ul>
    </section>

    <!-- Achievements -->
    <section id="achievements" class="panel">
      <h2>Achievements / Pride</h2>
      <p>Proud of contributing to the growth and development of young people, helping them navigate opportunities and think independently about their future.</p>
    </section>

    <!-- Blogpost -->
    <section id="blog" class="panel">
      <h2>Waarom jongeren nu met AI moeten starten</h2>
      <img src="motivatie.jpg" alt="Motivatie AI">
      <p>Hey, ik ben Néo Vale! School voelt soms als verplichting, maar je kan je vrije tijd, creativiteit en AI gebruiken om iets groots te bouwen.</p>
      <ul>
        <li><strong>AI is jouw persoonlijke superkracht:</strong> Tools helpen sneller leren, ideeën bedenken en projecten maken zonder miljoenen te investeren.</li>
        <li><strong>Begin klein, denk groot:</strong> Start klein, leer, groei, en bouw iets groots.</li>
        <li><strong>Focus op jezelf en anderen:</strong> Los problemen op met AI en creëer waarde.</li>
        <li><strong>Durf te proberen:</strong> Falen is leren, succes is bouwen aan je toekomst.</li>
      </ul>
      <p>Start vandaag, experimenteer en bouw iets waar je trots op bent.</p>
      <div style="text-align:center; margin-top:15px;">
        <button id="blogIdeaBtn">Klik hier voor 6 AI-ideeën!</button>
      </div>
    </section>

    <!-- AI Ideas -->
    <section id="ai_ideas" class="panel">
      <h2>AI Side Hustle Ideas</h2>
      <p>Click the button below to get 6 AI project ideas you can start this week!</p>
      <button id="ideaBtn" class="btn">Generate Ideas</button>
      <div id="ideasList" class="ideas"></div>
    </section>

    <!-- Location -->
    <section id="location" class="panel">
      <h2>Location</h2>
      <p>Belgium</p>
    </section>

    <!-- Footer -->
    <footer class="site-footer">
      <small>© <span id="year"></span> NeoValeAI</small>
    </footer>
  </main>

  <script>
    // OpenAI API key (vul hier je eigen key in)
    const OPENAI_API_KEY = "sk-JOUW_KEY_HIER";

    const SEED_IDEAS = [
      "Micro-SaaS: AI tool that automates Instagram captions for niche stores, charge €29/month.",
      "AI tutoring bot: Offer automated homework help for one subject and sell subscriptions.",
      "AI art prints: Generate themed art + print-on-demand; sell on Etsy.",
      "Local business lead generator: Use AI to create outreach emails and charge per lead.",
      "Resume & cover letter service: AI-generated tailored applications for job seekers.",
      "Voice clone gigs: Create custom voice messages for streamers and podcasters.",
      "Chat-based premium course: Mini-course + paid private chatbot tutor.",
      "Data-labeling microservice: Coordinate micro-tasks and sell cleaned datasets to researchers.",
      "AI-driven dropshipping descriptions: Automate product pages and sell the service.",
      "Micro-consulting templates: Build 5 templates (e.g., cold email + funnel) and sell."
    ];

    function generateIdeas(){
      const list = document.getElementById('ideasList');
      list.innerHTML = '';
      const shuffled = SEED_IDEAS.sort(()=>0.5-Math.random()).slice(0,6);
      shuffled.forEach(text => {
        const el = document.createElement('div');
        el.className = 'idea-pill';
        el.textContent = text;
        list.appendChild(el);
      });
    }

    document.addEventListener('DOMContentLoaded', ()=>{
      document.getElementById('year').textContent = new Date().getFullYear();

      document.getElementById('ideaBtn').addEventListener('click', generateIdeas);
      document.getElementById('blogIdeaBtn').addEventListener('click', ()=>{
        generateIdeas();
        window.scrollTo({ top: document.getElementById('ai_ideas').offsetTop, behavior: 'smooth' });
      });
    });
  </script>
</body>
</html>
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>NeoValeAI</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="brand">NeoValeAI</div>
    <nav>
      <button id="langBtn">NL</button>
    </nav>
  </header>

  <main class="container">
    <!-- Hero / Intro -->
    <section id="hero" class="panel">
      <h1 data-i18n="hero_title">Néo Vale</h1>
      <p data-i18n="hero_sub">Young entrepreneur passionate about AI and helping youth achieve success.</p>
    </section>

    <!-- Objective -->
    <section id="objective" class="panel">
      <h2 data-i18n="objective_title">Objective</h2>
      <p data-i18n="objective_text">To inspire and guide young people in leveraging AI and entrepreneurship to build successful projects and unlock their potential.</p>
    </section>

    <!-- Skills -->
    <section id="skills" class="panel">
      <h2 data-i18n="skills_title">Interests & Skills</h2>
      <ul>
        <li>Entrepreneurship</li>
        <li>AI & Technology</li>
        <li>Youth Mentorship</li>
        <li>Creativity & Problem-Solving</li>
        <li>Community Building</li>
      </ul>
    </section>

    <!-- Achievements -->
    <section id="achievements" class="panel">
      <h2 data-i18n="achievements_title">Achievements / Pride</h2>
      <p data-i18n="achievements_text">Proud of contributing to the growth and development of young people, helping them navigate opportunities and think independently about their future.</p>
    </section>

    <!-- Blogpost -->
    <section id="blog" class="panel">
      <h2 data-i18n="blog_title">Waarom jongeren nu met AI moeten starten</h2>
      <img src="motivatie.jpg" alt="Motivatie AI">
      <p data-i18n="blog_intro">Hey, ik ben Néo Vale! School voelt soms als verplichting, maar je kan je vrije tijd, creativiteit en AI gebruiken om iets groots te bouwen.</p>
      <ul>
        <li data-i18n="blog_point1"><strong>AI is jouw persoonlijke superkracht:</strong> Tools helpen sneller leren, ideeën bedenken en projecten maken zonder miljoenen te investeren.</li>
        <li data-i18n="blog_point2"><strong>Begin klein, denk groot:</strong> Start klein, leer, groei, en bouw iets groots.</li>
        <li data-i18n="blog_point3"><strong>Focus op jezelf en anderen:</strong> Los problemen op met AI en creëer waarde.</li>
        <li data-i18n="blog_point4"><strong>Durf te proberen:</strong> Falen is leren, succes is bouwen aan je toekomst.</li>
      </ul>
      <p data-i18n="blog_end">Start vandaag, experimenteer en bouw iets waar je trots op bent.</p>
      <div style="text-align:center; margin-top:15px;">
        <button id="blogIdeaBtn" class="btn" data-i18n="blog_button">Klik hier voor 6 AI-ideeën!</button>
      </div>
    </section>

    <!-- AI Ideas -->
    <section id="ai_ideas" class="panel">
      <h2 data-i18n="ai_title">AI Side Hustle Ideas</h2>
      <p data-i18n="ai_sub">Click the button below to get 6 AI project ideas you can start this week!</p>
      <button id="ideaBtn" class="btn" data-i18n="ai_button">Generate Ideas</button>
      <div id="ideasList" class="ideas"></div>
    </section>

    <!-- Location -->
    <section id="location" class="panel">
      <h2 data-i18n="location_title">Location</h2>
      <p>Belgium</p>
    </section>

    <!-- Footer -->
    <footer class="site-footer">
      <small>© <span id="year"></span> NeoValeAI</small>
    </footer>
  </main>

  <script src="translations.js"></script>
  <script src="script.js"></script>
</body>
</html>
body { font-family: Arial, sans-serif; background: #f4f4f9; color: #333; margin:0; padding:0; }
.container { max-width:800px; margin:20px auto; padding:15px; }
.site-header { background:#0b1220; color:#fff; padding:15px; display:flex; justify-content:space-between; align-items:center; }
.brand { font-size:22px; font-weight:bold; }
.panel { background:#fff; padding:15px; margin:15px 0; border-radius:8px; box-shadow:0 2px 6px rgba(
body {
  font-family: Arial, sans-serif;
  margin:0;
  padding:0;
  color:#fff;
  background: linear-gradient(135deg, #0b1220, #1f1f3b, #3a3a6f);
  background-size: 400% 400%;
  animation: gradientMove 15s ease infinite;
}

@keyframes gradientMove {
  0% {background-position:0% 50%;}
  50% {background-position:100% 50%;}
  100% {background-position:0% 50%;}
}
body::after {
  content: '';
  position: fixed;
  top:0; left:0; right:0; bottom:0;
  background-image: radial-gradient(circle at 20% 20%, rgba(255,255,255,0.05) 1px, transparent 1px),
                    radial-gradient(circle at 80% 80%, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 50px 50px;
  pointer-events:none;
  z-index:0;
}
<!-- CV / Portfolio Section -->
<section id="cv" class="panel">
  <h2>Curriculum Vitae</h2>

  <p><strong>Naam:</strong> Néo Vale</p>
  <p><strong>Locatie:</strong> België</p>
  <p><strong>Doel:</strong> Jongeren inspireren en begeleiden naar succes met AI en ondernemerschap.</p>

  <h3>Profiel</h3>
  <p>Jong, ambitieus en gepassioneerd over AI en technologie. Mijn missie is om jongeren te helpen hun potentieel te ontdekken en praktische projecten te starten die echt impact hebben.</p>

  <h3>Vaardigheden</h3>
  <ul>
    <li>AI & Technologie</li>
    <li>Ondernemerschap</li>
    <li>Creatief probleemoplossend denken</li>
    <li>Mentorschap voor jongeren</li>
    <li>Communicatie & community building</li>
  </ul>

  <h3>Ervaring / Projecten</h3>
  <ul>
    <li><strong>AI Idea Generator Website:</strong> Ontwikkeld een interactieve website voor jongeren om AI-ondernemersideeën te ontdekken.</li>
    <li><strong>Mentorship & Community Building:</strong> Helpen van jonge mensen bij het starten van kleine AI-projecten en leren over zelfstandigheid.</li>
    <li><strong>Experimenten met Micro-SaaS en AI tools:</strong> Testen van AI-applicaties voor creatieve en praktische doeleinden.</li>
  </ul>

  <h3>Opleiding</h3>
  <ul>
    <li>School: (focus op zelf-leren en praktische projecten)</li>
    <li>Extra: Online AI-cursussen, tutorials en experimentele projecten</li>
  </ul>

  <h3>Trots / Prestaties</h3>
  <ul>
    <li>Helpen
<meta name="description" content="NeoValeAI helpt jongeren om hun passie te ontdekken, AI te gebruiken en eigen projecten te starten die leiden tot succes en vrijheid.">
# 🌐 NeoValeAI

**NeoValeAI** is een inspirerend project van Néo Vale, gemaakt om jongeren te helpen hun passie te vinden, AI te gebruiken en hun eigen toekomst te bouwen met technologie en ondernemerschap.

## 🚀 Features
- Interactieve AI Idea Generator  
- Motivatieblog voor jongeren  
- Meertalige website (Nederlands & Engels)  
- Simpel design, gemaakt om te leren en te inspireren  

## 🧠 Doel
Het doel van dit project is om jongeren te tonen dat ze geen diploma of geld nodig hebben om iets groots te beginnen.  
Met creativiteit, internet en AI kan je vandaag al aan je toekomst werken.

## ⚙️ Installatie
1. Download of clone dit project.  
2. Open `index.html` in je browser.  
3. (Optioneel) Voeg je eigen OpenAI API Key toe in `script.js` om AI-functies te activeren.

## 💬 Contact
👤 **Néo Vale**  
📍 België  
🌍 Website: [https://neovaleai.github.io](https://neovaleai.github.io) *(als je hem online zet)*  

---

✨ *Made with passion and AI — for the next generation.*
https://jouwgebruikersnaam.github.io/NeoValeAI
NeoValeAI
