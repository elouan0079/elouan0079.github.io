<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fiches de révision — Rimbaud · Cahiers de Douai</title>
<style>
:root {
  --cream: #faf8f3;
  --paper: #ffffff;
  --ink: #1a1814;
  --ink-muted: #6b6760;
  --ink-faint: #9c9890;
  --border: #e8e4db;
  --border-strong: #d0ccc0;
  --purple-bg: #eeedfe; --purple: #534ab7; --purple-dark: #3c3489;
  --teal-bg: #e1f5ee; --teal: #0f6e56;
  --coral-bg: #faece7; --coral: #993c1d; --coral-mid: #d85a30;
  --blue-bg: #e6f1fb; --blue: #185fa5; --blue-mid: #378add;
  --amber-bg: #faeeda; --amber: #854f0b;
  --green-bg: #eaf3de; --green: #3b6d11;
  --red-bg: #fcebeb; --red: #a32d2d;
  --radius: 10px; --radius-sm: 6px;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { font-family: 'Georgia', 'Times New Roman', serif; background: var(--cream); color: var(--ink); line-height: 1.6; }

/* NAV */
nav {
  position: sticky; top: 48px; z-index: 99;
  background: rgba(250,248,243,0.97);
  backdrop-filter: blur(6px);
  border-bottom: 1px solid var(--border);
  padding: 0 1rem;
  overflow-x: auto;
  white-space: nowrap;
}
.nav-inner { display: inline-flex; gap: 0; min-width: 100%; }
nav a {
  display: inline-block;
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 12px; font-weight: 600;
  color: var(--ink-muted); text-decoration: none;
  padding: 0.65rem 1rem;
  border-bottom: 2px solid transparent;
  transition: color 0.15s, border-color 0.15s;
  letter-spacing: 0.02em;
}
nav a:hover { color: var(--ink); border-bottom-color: var(--border-strong); }
nav a.active { color: var(--purple); border-bottom-color: var(--purple); }

/* TAB BAR */
#tab-bar {
  position: sticky; top: 0; z-index: 100;
  background: var(--ink);
  overflow-x: auto;
  white-space: nowrap;
  border-bottom: none;
}
.tab-inner { display: inline-flex; min-width: 100%; }
.tab-btn {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 12px; font-weight: 600;
  color: rgba(255,255,255,0.55);
  background: none; border: none; cursor: pointer;
  padding: 0.8rem 1.1rem;
  border-bottom: 2px solid transparent;
  transition: color 0.15s, border-color 0.15s;
  letter-spacing: 0.02em;
  white-space: nowrap;
}
.tab-btn:hover { color: rgba(255,255,255,0.85); }
.tab-btn.active { color: #fff; border-bottom-color: #fff; }

/* TAB PANELS */
.tab-panel { display: none; }
.tab-panel.active { display: block; }

/* INNER TABS (sous-onglets dans Autres textes) */
.inner-tab-bar {
  background: var(--cream);
  border-bottom: 1px solid var(--border-strong);
  padding: 0 1rem;
  overflow-x: auto;
  white-space: nowrap;
  position: sticky;
  top: 48px;
  z-index: 98;
}
.inner-tab-inner { display: inline-flex; min-width: 100%; }
.inner-tab-btn {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 13px; font-weight: 600;
  color: var(--ink-muted);
  background: none; border: none; cursor: pointer;
  padding: 0.75rem 1.1rem;
  border-bottom: 2px solid transparent;
  transition: color 0.15s, border-color 0.15s;
  letter-spacing: 0.02em;
}
.inner-tab-btn:hover { color: var(--ink); }
.inner-tab-btn.active { color: var(--ink); border-bottom-color: var(--ink); }
.inner-panel { display: none; }
.inner-panel.active { display: block; }
.coming-soon {
  text-align: center;
  padding: 5rem 2rem;
  font-family: 'Helvetica Neue', Arial, sans-serif;
}
.coming-soon .cs-icon { font-size: 2.5rem; margin-bottom: 1rem; }
.coming-soon h2 { font-size: 1.3rem; font-weight: 600; color: var(--ink); margin-bottom: 0.5rem; font-style: normal; }
.coming-soon p { font-size: 13px; color: var(--ink-muted); }

/* LAYOUT */
.container { max-width: 860px; margin: 0 auto; padding: 2rem 1rem 3rem; }

/* PAGE HEADER */
.page-header { text-align: center; margin-bottom: 2.5rem; padding-bottom: 1.5rem; border-bottom: 1px solid var(--border-strong); }
.page-header .surtitre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 11px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 8px; }
.page-header h1 { font-size: clamp(1.5rem, 4vw, 2.2rem); font-weight: normal; font-style: italic; color: var(--ink); margin-bottom: 6px; }
.page-header .sub { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; color: var(--ink-muted); }

/* SECTION BLOCKS */
.bloc { margin-bottom: 2.5rem; }
.bloc-titre {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 10px; font-weight: 700; letter-spacing: 0.12em;
  text-transform: uppercase; color: var(--ink-faint);
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--border);
}

/* CARDS */
.card { background: var(--paper); border: 1px solid var(--border); border-radius: var(--radius); overflow: hidden; margin-bottom: 1.5rem; }
.card-header { padding: 1.25rem 1.5rem; border-bottom: 1px solid var(--border); }
.card-section { padding: 1.25rem 1.5rem; border-bottom: 1px solid var(--border); }
.card-section:last-child { border-bottom: none; }
.section-label { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 12px; }

/* FICHE HEADER */
.fiche-numero { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 5px; }
.fiche-titre { font-size: clamp(1.2rem, 3.5vw, 1.6rem); font-style: italic; font-weight: normal; color: var(--ink); margin-bottom: 3px; }
.fiche-sous { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; color: var(--ink-muted); margin-bottom: 10px; }

/* TAGS */
.tags { display: flex; flex-wrap: wrap; gap: 6px; }
.tag { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 11px; font-weight: 600; padding: 3px 10px; border-radius: 20px; }
.tag-purple { background: var(--purple-bg); color: var(--purple-dark); }
.tag-teal   { background: var(--teal-bg);   color: var(--teal); }
.tag-coral  { background: var(--coral-bg);  color: var(--coral); }
.tag-blue   { background: var(--blue-bg);   color: var(--blue); }
.tag-amber  { background: var(--amber-bg);  color: var(--amber); }
.tag-green  { background: var(--green-bg);  color: var(--green); }

/* POEME */
.poeme { border-left: 3px solid var(--purple); padding: 1rem 1.2rem; background: var(--cream); border-radius: 0 var(--radius-sm) var(--radius-sm) 0; font-size: clamp(13px, 2.5vw, 15px); line-height: 2; }
.poeme.bleu { border-left-color: var(--blue-mid); }
.poeme .strophe { margin-bottom: 1rem; }
.poeme .strophe:last-child { margin-bottom: 0; }

/* PLAN GRID */
.plan-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; }
.plan-card { background: var(--cream); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 0.85rem 1rem; }
.plan-num { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 4px; }
.plan-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; font-weight: 600; color: var(--ink); margin-bottom: 5px; }
.plan-sous { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; color: var(--ink-muted); line-height: 1.5; }

/* POINTS */
.points { display: flex; flex-direction: column; gap: 10px; }
.point { display: flex; gap: 10px; align-items: flex-start; }
.point-dot { width: 7px; height: 7px; border-radius: 50%; flex-shrink: 0; margin-top: 7px; }
.dot-purple { background: var(--purple); }
.dot-teal   { background: var(--teal); }
.dot-coral  { background: var(--coral); }
.dot-amber  { background: var(--amber); }
.dot-blue   { background: var(--blue); }
.dot-green  { background: var(--green); }
.point-text { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; color: var(--ink); line-height: 1.65; }
.point-text strong { font-weight: 700; }

/* FIGURES */
.figures-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(165px, 1fr)); gap: 8px; }
.figure-card { background: var(--cream); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 0.7rem 0.9rem; }
.figure-nom { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; font-weight: 700; color: var(--ink); margin-bottom: 3px; }
.figure-ex { font-size: 12px; color: var(--ink-muted); line-height: 1.5; font-style: italic; }

/* QUESTIONS */
.questions { display: flex; flex-direction: column; gap: 8px; }
.question { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; color: var(--ink); background: var(--cream); border-left: 3px solid var(--teal); border-radius: 0 var(--radius-sm) var(--radius-sm) 0; padding: 0.65rem 1rem; line-height: 1.5; }
.question.bleu { border-left-color: var(--blue); }

/* CHUTE BOX */
.chute-box { background: var(--cream); border: 1px solid var(--coral-mid); border-radius: var(--radius-sm); padding: 0.9rem 1.1rem; font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; line-height: 1.7; color: var(--ink); }
.chute-citation { font-family: 'Georgia', serif; font-style: italic; font-size: 14px; color: var(--ink); margin-bottom: 8px; display: block; }

/* INFO BOX */
.info-box { background: var(--blue-bg); border-left: 3px solid var(--blue-mid); border-radius: 0 var(--radius-sm) var(--radius-sm) 0; padding: 0.85rem 1rem; font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; line-height: 1.65; color: var(--ink); margin-top: 10px; }
.info-box strong { font-weight: 700; }

/* FRISE CHRONOLOGIQUE */
.frise { position: relative; padding-left: 2rem; }
.frise::before { content: ''; position: absolute; left: 7px; top: 6px; bottom: 6px; width: 2px; background: var(--border-strong); border-radius: 2px; }
.frise-item { position: relative; margin-bottom: 1.25rem; }
.frise-item:last-child { margin-bottom: 0; }
.frise-dot { position: absolute; left: -2rem; top: 4px; width: 14px; height: 14px; border-radius: 50%; background: var(--paper); border: 2px solid var(--border-strong); display: flex; align-items: center; justify-content: center; }
.frise-dot.key { border-color: var(--purple); background: var(--purple-bg); }
.frise-dot.war { border-color: var(--coral); background: var(--coral-bg); }
.frise-dot.pub { border-color: var(--teal); background: var(--teal-bg); }
.frise-dot.life { border-color: var(--amber); background: var(--amber-bg); }
.frise-date { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 11px; font-weight: 700; color: var(--ink-faint); margin-bottom: 2px; letter-spacing: 0.04em; }
.frise-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; font-weight: 600; color: var(--ink); margin-bottom: 2px; }
.frise-desc { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; color: var(--ink-muted); line-height: 1.5; }

/* LÉGENDE FRISE */
.frise-legende { display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 1.25rem; }
.legende-item { display: flex; align-items: center; gap: 6px; font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 11px; color: var(--ink-muted); }
.legende-dot { width: 10px; height: 10px; border-radius: 50%; border: 2px solid; }
.legende-dot.key { border-color: var(--purple); background: var(--purple-bg); }
.legende-dot.war { border-color: var(--coral); background: var(--coral-bg); }
.legende-dot.pub { border-color: var(--teal); background: var(--teal-bg); }
.legende-dot.life { border-color: var(--amber); background: var(--amber-bg); }

/* SYMBOLISME */
.symb-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; }
.symb-card { background: var(--cream); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 0.85rem 1rem; }
.symb-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; font-weight: 700; color: var(--ink); margin-bottom: 6px; }
.symb-texte { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; color: var(--ink-muted); line-height: 1.6; }

/* CAHIERS */
.liasse { background: var(--cream); border: 1px solid var(--border); border-radius: var(--radius-sm); padding: 0.85rem 1rem; margin-bottom: 10px; }
.liasse-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; font-weight: 700; color: var(--ink); margin-bottom: 6px; }
.liasse-list { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; color: var(--ink-muted); line-height: 1.8; }

/* ANALYSE LINEAIRE ACCORDEON */
.mvt { border: 1px solid var(--border); border-radius: var(--radius-sm); margin-bottom: 8px; overflow: hidden; }
.mvt-header { background: var(--cream); padding: 0.75rem 1rem; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; }
.mvt-header:hover { background: var(--border); }
.mvt-num { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 0.08em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 2px; }
.mvt-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; font-weight: 600; color: var(--ink); }
.mvt-arrow { font-size: 12px; color: var(--ink-faint); transition: transform 0.2s; flex-shrink: 0; margin-left: 8px; }
.mvt-arrow.open { transform: rotate(180deg); }
.mvt-body { display: none; padding: 1rem; border-top: 1px solid var(--border); background: var(--paper); }
.mvt-body.open { display: block; }
.mvt-body .point { margin-bottom: 6px; }
.mvt-body .point:last-child { margin-bottom: 0; }

/* COMMENTAIRE SECTIONS */
.com-section { margin-bottom: 1rem; }
.com-section-titre { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 12px; font-weight: 700; color: var(--ink); margin-bottom: 6px; border-left: 3px solid var(--blue-mid); padding-left: 8px; }
.com-texte { font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 13px; color: var(--ink); line-height: 1.65; }
.com-texte em { color: var(--purple-dark); font-style: italic; }

/* CITATION */
.citation { font-style: italic; color: var(--purple-dark); }

/* FOOTER */
footer { text-align: center; font-family: 'Helvetica Neue', Arial, sans-serif; font-size: 11px; color: var(--ink-faint); padding: 1.5rem 1rem; border-top: 1px solid var(--border); margin-top: 1rem; }

/* RESPONSIVE */
@media (max-width: 480px) {
  .container { padding: 1rem 0.75rem 2rem; }
  .card-header, .card-section { padding: 1rem; }
  .plan-grid { grid-template-columns: 1fr; }
  .figures-grid { grid-template-columns: 1fr 1fr; }
  .symb-grid { grid-template-columns: 1fr; }
  .frise { padding-left: 1.75rem; }
  nav a { padding: 0.65rem 0.75rem; font-size: 11px; }
}

@media print {
  nav { display: none; }
  body { background: white; }
  .card { break-inside: avoid; }
  .card-section { break-inside: avoid; }
}
</style>
</head>
<body>

<!-- MODAL AVERTISSEMENT -->
<div id="disclaimer-overlay" style="
  position: fixed; inset: 0; z-index: 9999;
  background: rgba(26,24,20,0.55);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);
  display: flex; align-items: center; justify-content: center;
  padding: 1.25rem;
">
  <div style="
    background: #ffffff;
    border-radius: 14px;
    max-width: 480px; width: 100%;
    padding: 2rem 2rem 1.75rem;
    box-shadow: 0 20px 60px rgba(0,0,0,0.2);
    font-family: 'Helvetica Neue', Arial, sans-serif;
  ">
    <div style="display:flex; align-items:center; gap:10px; margin-bottom:1rem;">
      <div style="
        width:36px; height:36px; border-radius:50%;
        background:#faeeda; display:flex; align-items:center; justify-content:center;
        flex-shrink:0; font-size:18px;
      ">⚠️</div>
      <div style="font-size:16px; font-weight:700; color:#1a1814;">Information importante</div>
    </div>

    <p style="font-size:13.5px; color:#3a3830; line-height:1.7; margin-bottom:0.9rem;">
      Ces fiches de révision sont des <strong>outils d'aide à la préparation</strong> du bac de français, mais elles peuvent être <strong>incomplètes ou contenir des inexactitudes</strong>.
    </p>
    <p style="font-size:13.5px; color:#3a3830; line-height:1.7; margin-bottom:0.9rem;">
      Certaines analyses peuvent manquer de nuances, certains contenus peuvent ne pas être à jour ou ne pas correspondre exactement au programme de ton établissement.
    </p>
    <p style="font-size:13.5px; color:#3a3830; line-height:1.7; margin-bottom:1.5rem;">
      <strong>Ne te fie pas à ce site à 100%.</strong> Consulte toujours tes cours, ton professeur et des sources officielles pour compléter ou vérifier les informations.
    </p>

    <label style="
      display:flex; align-items:flex-start; gap:10px;
      cursor:pointer; margin-bottom:1.25rem;
      font-size:13px; color:#1a1814; line-height:1.5;
    ">
      <input type="checkbox" id="disclaimer-check" onchange="toggleDisclaimerBtn()" style="
        width:17px; height:17px; margin-top:1px; flex-shrink:0;
        accent-color:#534ab7; cursor:pointer;
      ">
      J'ai pris connaissance de cette information et je comprends que ces fiches peuvent être incomplètes.
    </label>

    <button id="disclaimer-btn" onclick="closeDisclaimer()" disabled style="
      width:100%; padding:0.75rem;
      background:#e8e4db; color:#9c9890;
      border:none; border-radius:8px;
      font-family:'Helvetica Neue',Arial,sans-serif;
      font-size:13.5px; font-weight:600;
      cursor:not-allowed;
      transition: background 0.2s, color 0.2s;
    ">Accéder aux fiches</button>
  </div>
</div>

<div id="tab-bar">
  <div class="tab-inner">
    <button class="tab-btn active" onclick="switchTab('cahiers-douai')">Cahiers de Douai</button>
    <button class="tab-btn" onclick="switchTab('parti-pris')">Le Parti pris des choses</button>
    <button class="tab-btn" onclick="switchTab('on-ne-badine')">On ne badine pas avec l'amour</button>
    <button class="tab-btn" onclick="switchTab('autres')">Autres textes</button>
  </div>
</div>



<div id="panel-cahiers-douai" class="tab-panel active">
<div class="container">

  <div class="page-header">
    <div class="surtitre">Cahiers de Douai · Bac de français</div>
    <h1>Arthur Rimbaud</h1>
    <div class="sub">Fiches de révision complètes · 4 sections · 3 poèmes</div>
  </div>


  <!-- =================== RIMBAUD AUTEUR =================== -->
  <div id="rimbaud" class="bloc">
    <div class="bloc-titre">L'auteur</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche auteur</div>
        <div class="fiche-titre">Arthur Rimbaud (1854–1891)</div>
        <div class="fiche-sous">Poète français · Enfant prodige · Révolté</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-purple">Symbolisme</span>
          <span class="tag tag-coral">Parnassianisme</span>
          <span class="tag tag-amber">Poète maudit</span>
          <span class="tag tag-teal">Cahiers de Douai</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Portrait</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text">Né le <strong>20 octobre 1854</strong> à Charleville (Ardennes), dans une famille modeste. Son père, militaire, abandonne le foyer très tôt. Sa mère, austère et rigoriste, joue un rôle déterminant dans son éducation.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-blue"></div>
            <div class="point-text">Élève brillant, il se révèle très jeune comme un prodige : il remporte des concours de latin, apprend le grec, l'allemand et commence à écrire des poèmes dès ses 15 ans.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text">Adolescent révolté, il multiplie les <strong>fugues</strong> (1870–1871) et est recueilli par son professeur <strong>Georges Izambard</strong> puis par le poète <strong>Paul Démeny</strong>. C'est à Démeny qu'il confie les <em>Cahiers de Douai</em>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-amber"></div>
            <div class="point-text">À 17 ans, il rejoint <strong>Paul Verlaine</strong> à Paris. Leur relation tumultueuse et leur errance à travers l'Europe nourrit une création poétique radicale. Verlaine finit par lui tirer dessus en 1873 à Bruxelles.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-teal"></div>
            <div class="point-text">À <strong>21 ans</strong>, il cesse d'écrire et part pour l'Abyssinie (actuelle Éthiopie) où il devient <strong>commerçant et trafiquant d'armes</strong>. Il ne publiera plus aucun poème de son vivant.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text">Mort le <strong>10 novembre 1891</strong> à Marseille, à 37 ans, d'un cancer des os. Son œuvre poétique, écrite en seulement cinq ans, influencera durablement toute la poésie moderne.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Œuvres principales</div>
        <div class="figures-grid">
          <div class="figure-card">
            <div class="figure-nom">Cahiers de Douai (1870)</div>
            <div class="figure-ex">22 poèmes écrits à 16 ans. Jamais publiés de son vivant.</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Le Bateau ivre (1871)</div>
            <div class="figure-ex">Poème d'une liberté formelle éblouissante, écrit à 17 ans.</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Une saison en enfer (1873)</div>
            <div class="figure-ex">Prose poétique autobiographique. Seule œuvre publiée de son vivant.</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Illuminations (1886)</div>
            <div class="figure-ex">Poèmes en prose révolutionnaires, publiés par Verlaine.</div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <!-- =================== FRISE CHRONOLOGIQUE =================== -->
  <div id="frise" class="bloc">
    <div class="bloc-titre">Frise chronologique</div>

    <div class="card">
      <div class="card-section">
        <div class="frise-legende">
          <div class="legende-item"><div class="legende-dot key"></div> Création poétique</div>
          <div class="legende-item"><div class="legende-dot war"></div> Événement historique</div>
          <div class="legende-item"><div class="legende-dot pub"></div> Publication</div>
          <div class="legende-item"><div class="legende-dot life"></div> Vie personnelle</div>
        </div>
        <div class="frise">

          <div class="frise-item">
            <div class="frise-dot life"></div>
            <div class="frise-date">20 octobre 1854</div>
            <div class="frise-titre">Naissance à Charleville</div>
            <div class="frise-desc">Naissance de Jean-Nicolas Arthur Rimbaud dans les Ardennes.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot key"></div>
            <div class="frise-date">1869–1870</div>
            <div class="frise-titre">Premiers poèmes</div>
            <div class="frise-desc">À 15–16 ans, Rimbaud écrit ses premiers textes et correspond avec le poète Théodore de Banville.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot life"></div>
            <div class="frise-date">Août–septembre 1870</div>
            <div class="frise-titre">Première fugue</div>
            <div class="frise-desc">Rimbaud fugue à Paris sans billet, est arrêté, emprisonné à Mazas puis libéré grâce à son professeur Izambard qui le recueille à Douai.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot war"></div>
            <div class="frise-date">Juillet 1870 – Mai 1871</div>
            <div class="frise-titre">Guerre franco-prussienne</div>
            <div class="frise-desc">La France est envahie par la Prusse. Défaite de Sedan (sept. 1870), siège de Paris, Commune de Paris (mars-mai 1871). Ces événements traumatisent le jeune Rimbaud.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot key"></div>
            <div class="frise-date">Automne 1870</div>
            <div class="frise-titre">Cahiers de Douai</div>
            <div class="frise-desc">Lors de ses séjours à Douai, Rimbaud compose 22 poèmes remis en deux liasses à Paul Démeny. Parmi eux : <em>Le Dormeur du val</em>, <em>Vénus anadyomène</em>, <em>Ma Bohême</em>.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot key"></div>
            <div class="frise-date">13 mai 1871</div>
            <div class="frise-titre">Lettre du Voyant</div>
            <div class="frise-desc">Dans sa célèbre lettre à Paul Démeny, Rimbaud expose sa théorie poétique : <em>« Je est un autre »</em> et le dérèglement raisonné de tous les sens.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot key"></div>
            <div class="frise-date">Septembre 1871</div>
            <div class="frise-titre">Le Bateau ivre</div>
            <div class="frise-desc">Rimbaud envoie ce long poème à Verlaine. Il monte à Paris et la relation avec Verlaine commence.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot life"></div>
            <div class="frise-date">1871–1873</div>
            <div class="frise-titre">Errance avec Verlaine</div>
            <div class="frise-desc">Les deux poètes vivent ensemble, voyagent en Belgique et en Angleterre. Rimbaud rédige <em>Une saison en enfer</em>. En juillet 1873, Verlaine blesse Rimbaud d'un coup de pistolet à Bruxelles.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot pub"></div>
            <div class="frise-date">1873</div>
            <div class="frise-titre">Une saison en enfer</div>
            <div class="frise-desc">Seule œuvre publiée par Rimbaud de son vivant. Il en fait imprimer quelques exemplaires puis abandonne définitivement la littérature.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot pub"></div>
            <div class="frise-date">1886</div>
            <div class="frise-titre">Illuminations publiées</div>
            <div class="frise-desc">Verlaine publie les <em>Illuminations</em> à l'insu de Rimbaud, qui est alors en Afrique. Ces poèmes en prose révolutionnaires lui valent une reconnaissance posthume immédiate.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot life"></div>
            <div class="frise-date">1880–1891</div>
            <div class="frise-titre">Silence et exil africain</div>
            <div class="frise-desc">Rimbaud vit en Abyssinie (Éthiopie, Somalie), travaille comme commerçant et trafiquant d'armes. Il correspond avec sa famille mais n'écrit plus de poésie.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot life"></div>
            <div class="frise-date">10 novembre 1891</div>
            <div class="frise-titre">Mort à Marseille</div>
            <div class="frise-desc">Rimbaud meurt à 37 ans d'un cancer des os à l'Hôpital de la Conception à Marseille, après l'amputation de sa jambe droite.</div>
          </div>

          <div class="frise-item">
            <div class="frise-dot pub"></div>
            <div class="frise-date">1895</div>
            <div class="frise-titre">Œuvres complètes</div>
            <div class="frise-desc">Sa sœur Isabelle et Verlaine publient ses œuvres complètes. La postérité reconnaîtra Rimbaud comme l'un des plus grands poètes français.</div>
          </div>

        </div>
      </div>
    </div>
  </div>


  <!-- =================== SYMBOLISME =================== -->
  <div id="symbolisme" class="bloc">
    <div class="bloc-titre">Mouvement littéraire</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Mouvement · Fin XIXe siècle</div>
        <div class="fiche-titre">Le Symbolisme</div>
        <div class="fiche-sous">et le Parnasse — deux courants qui traversent l'œuvre de Rimbaud</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-purple">1857–1900 environ</span>
          <span class="tag tag-blue">Réaction au Romantisme</span>
          <span class="tag tag-green">Suggestivité</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Le Symbolisme — définition et caractéristiques</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Définition :</strong> Mouvement poétique apparu vers 1857 (avec Baudelaire) et théorisé dans le <em>Manifeste symboliste</em> de Jean Moréas (1886). Le symbolisme refuse l'imitation directe de la réalité et préfère suggérer les choses plutôt que les nommer.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Le symbole :</strong> Chaque objet, paysage ou sensation peut renvoyer à une réalité invisible, spirituelle ou intérieure. La poésie devient un langage codé, une exploration de l'âme.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>La musique du vers :</strong> Le symbolisme accorde une importance capitale à la <strong>musicalité</strong> du langage. Verlaine écrit : <em>« De la musique avant toute chose »</em>. Le son prime parfois sur le sens.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Synesthésie :</strong> Mélange des sens (vision, ouïe, odorat…) pour créer des correspondances. Chez Baudelaire : <em>« Les parfums, les couleurs et les sons se répondent »</em>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>Refus du réalisme :</strong> Contre la description objective du monde réel. Le poète symboliste cherche à atteindre une réalité cachée, un idéal inaccessible, l'indicible.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Les grands auteurs symbolistes</div>
        <div class="symb-grid">
          <div class="symb-card">
            <div class="symb-titre">Charles Baudelaire (1821–1867)</div>
            <div class="symb-texte">Précurseur. <em>Les Fleurs du Mal</em> (1857) fondent la modernité poétique avec la théorie des correspondances.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">Paul Verlaine (1844–1896)</div>
            <div class="symb-texte">Maître de la musicalité. <em>Fêtes galantes, Romances sans paroles</em>. Compagnon de Rimbaud.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">Arthur Rimbaud (1854–1891)</div>
            <div class="symb-texte">Poète visionnaire. Théorie du dérèglement des sens. Œuvre brève mais révolutionnaire.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">Stéphane Mallarmé (1842–1898)</div>
            <div class="symb-texte">Le plus radical. Poésie hermétique, suggestive. <em>Un coup de dés</em> révolutionne la typographie.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Le Parnasse — courant parallèle</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Définition :</strong> Mouvement poétique des années 1860–1880. Le nom vient de la revue <em>Le Parnasse contemporain</em> (1866). À la différence du symbolisme, le Parnasse prône une poésie <strong>impersonnelle, froide et ciselée</strong>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>L'art pour l'art :</strong> Théophile Gautier théorise que l'art n'a pas à être utile ou moral. La beauté formelle suffit. La poésie est comparée à la sculpture : dure, précise, immuable.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Refus du lyrisme romantique :</strong> Pas de confession intime, pas de débordement sentimental. Le poète parnassien s'efface derrière son objet. Leconte de Lisle et Théophile Gautier en sont les chefs de file.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Rimbaud et le Parnasse :</strong> Dans les <em>Cahiers de Douai</em>, Rimbaud s'inscrit dans une démarche parnassienne (précision descriptive, froideur objective) tout en la dépassant par son ironie et sa violence poétique — notamment dans <em>Vénus anadyomène</em>.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Rimbaud entre les deux mouvements</div>
        <div class="symb-grid">
          <div class="symb-card">
            <div class="symb-titre">Aspect parnassien dans les Cahiers</div>
            <div class="symb-texte">Description précise et froide du corps (Vénus), objectivité apparente du tableau (Dormeur du val), refus du lyrisme sentimental direct.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">Aspect symboliste dans les Cahiers</div>
            <div class="symb-texte">La nature comme symbole (le val = tombeau), suggestion plutôt que nomination explicite (la mort jamais nommée), synesthésies (lumière qui pleut, rivière qui chante).</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">Dépassement des deux</div>
            <div class="symb-texte">Rimbaud va plus loin avec sa théorie du « Voyant » : le poète doit dérégler tous ses sens pour accéder à l'inconnu et inventer un langage universel.</div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <!-- =================== CAHIERS DE DOUAI =================== -->
  <div id="cahiers" class="bloc">
    <div class="bloc-titre">Le recueil</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Recueil · 1870 (publication posthume)</div>
        <div class="fiche-titre">Les Cahiers de Douai</div>
        <div class="fiche-sous">22 poèmes · 2 liasses · Rimbaud a 16 ans</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-purple">22 poèmes</span>
          <span class="tag tag-coral">Guerre franco-prussienne</span>
          <span class="tag tag-teal">Jamais publié de son vivant</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Contexte de composition</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Automne 1870 :</strong> Lors de ses fugues depuis Charleville, Rimbaud séjourne chez son professeur Georges Izambard à Douai, puis chez les cousines de ce dernier, les demoiselles Gindre. C'est dans ce cadre protégé qu'il compose et recopie ses poèmes.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>La guerre comme toile de fond :</strong> La guerre franco-prussienne fait rage (juillet 1870 – mai 1871). Les Ardennes sont occupées. Cette violence du monde réel imprègne les poèmes : <em>Le Dormeur du val</em>, <em>Le Mal</em>, <em>Rages de Césars</em>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Remis à Paul Démeny :</strong> En octobre 1870, Rimbaud confie ses poèmes en deux liasses au poète Paul Démeny. Il lui demandera plus tard de les brûler (lettre de 1871). Démeny ne le fera pas. Les manuscrits seront publiés bien après la mort du poète.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Structure du recueil — les deux liasses</div>
        <div class="liasse">
          <div class="liasse-titre">Première liasse (à Izambard) — 9 poèmes</div>
          <div class="liasse-list">
            Première soirée · Sensation · Ophélie · Bal des pendus · Le Châtiment de Tartuffe · Vénus anadyomène · Les Reparties de Nina · À la musique · Les Effarés
          </div>
        </div>
        <div class="liasse">
          <div class="liasse-titre">Deuxième liasse (à Démeny) — 13 poèmes</div>
          <div class="liasse-list">
            Roman · Le Mal · Rages de Césars · Rêvé pour l'hiver · Le Dormeur du val · Au Cabaret-Vert · La Maline · L'Éclatante Victoire de Sarrebruck · Le Buffet · Ma Bohême · Les Corbeaux · Les Assis · Tête de faune
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Thèmes majeurs du recueil</div>
        <div class="symb-grid">
          <div class="symb-card">
            <div class="symb-titre">La révolte et la fuite</div>
            <div class="symb-texte">Rimbaud exprime sa soif de liberté, son rejet de la société bourgeoise et de sa mère. <em>Ma Bohême</em>, <em>Sensation</em> : l'errance comme idéal.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">La dénonciation de la guerre</div>
            <div class="symb-texte"><em>Le Dormeur du val</em>, <em>Le Mal</em> : la guerre franco-prussienne est dénoncée avec force et originalité, sans discours moralisateur direct.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">La nature et l'évasion</div>
            <div class="symb-texte">La nature est omniprésente : refuge, idéal, espace de liberté. Elle incarne l'opposé du monde social oppressant.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">La critique du lyrisme</div>
            <div class="symb-texte"><em>Vénus anadyomène</em>, <em>À la musique</em> : parodie des conventions poétiques, du blason, de la poésie romantique et du lyrisme traditionnel.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">L'amour et le désir</div>
            <div class="symb-texte"><em>Roman</em>, <em>Première soirée</em> : représentations sensuelles et parfois provocatrices de la femme et du désir adolescent.</div>
          </div>
          <div class="symb-card">
            <div class="symb-titre">La misère sociale</div>
            <div class="symb-texte"><em>Les Effarés</em>, <em>Les Assis</em> : regards sur les marginaux, les pauvres, les exclus. Compassion et ironie mêlées.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Caractéristiques formelles</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Formes classiques maîtrisées :</strong> Rimbaud utilise majoritairement le sonnet (14 vers) et les alexandrins (12 syllabes), formes héritées de la tradition poétique française — mais il les subvertit.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>Rejets et contre-rejets :</strong> Enjambements fréquents qui perturbent le rythme classique, créent des effets de surprise et de tension. Rimbaud joue avec la versification pour mimer son sujet.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Construction en trompe-l'œil :</strong> Plusieurs poèmes fonctionnent sur le principe de la chute révélatrice (notamment <em>Le Dormeur du val</em>), obligeant le lecteur à une relecture du texte.</div>
          </div>
        </div>
      </div>
    </div>
  </div>


  <!-- =================== FICHE 1 : VÉNUS =================== -->
  <div id="venus" class="bloc">
    <div class="bloc-titre">Fiche poème 1</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche 1 · 27 juillet 1870</div>
        <div class="fiche-titre">Vénus anadyomène</div>
        <div class="fiche-sous">Sonnet · 2 quatrains + 2 tercets · Alexandrins</div>
        <div class="tags">
          <span class="tag tag-purple">Anti-portrait parodique</span>
          <span class="tag tag-teal">Esthétique parnassienne</span>
          <span class="tag tag-coral">Destruction du lyrisme</span>
          <span class="tag tag-amber">Art de la provocation</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Texte du poème</div>
        <div class="poeme">
          <div class="strophe">
            Comme d'un cercueil vert en fer blanc, une tête<br>
            De femme à cheveux bruns fortement pommadés<br>
            D'une vieille baignoire émerge, lente et bête,<br>
            Avec des déficits assez mal ravaudés ;
          </div>
          <div class="strophe">
            Puis le col gras et gris, les larges omoplates<br>
            Qui saillent ; le dos court qui rentre et qui ressort ;<br>
            Puis les rondeurs des reins semblent prendre l'essor ;<br>
            La graisse sous la peau paraît en feuilles plates ;
          </div>
          <div class="strophe">
            L'échine est un peu rouge, et le tout sent un goût<br>
            Horrible étrangement ; on remarque surtout<br>
            Des singularités qu'il faut voir à la loupe…
          </div>
          <div class="strophe">
            Les reins portent deux mots gravés : Clara Venus ;<br>
            – Et tout ce corps remue et tend sa large croupe<br>
            Belle hideusement d'un ulcère à l'anus.
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Introduction et problématique</div>
        <div class="info-box">
          Dans ce sonnet des <em>Cahiers de Douai</em> (1870), Rimbaud revisite le thème de Vénus — déesse de l'amour inspiratrice des poètes (Louise Labé, Ronsard, Baudelaire) et des peintres (Botticelli, Alexandre Cabanel en 1863) — pour se positionner de façon critique face au <strong>lyrisme traditionnel</strong>. Le titre « anadyomène » signifie « qui sort des eaux » : c'est Vénus émergeant de la mer, thème noble que Rimbaud va systématiquement détruire.
          <br><br>
          <strong>Problématique :</strong> Comment Rimbaud réalise-t-il un anti-portrait parodique de Vénus pour faire émerger un art poétique nouveau — l'art parnassien ?
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Plan du commentaire composé</div>
        <div class="plan-grid">
          <div class="plan-card">
            <div class="plan-num">Partie I</div>
            <div class="plan-titre">L'anti-portrait parodique de Vénus</div>
            <div class="plan-sous">A. Un contre-blason · B. La dépréciation de Vénus · C. Parodie des tableaux de la naissance de Vénus</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Partie II</div>
            <div class="plan-titre">Une poésie nouvelle</div>
            <div class="plan-sous">A. La destruction du lyrisme traditionnel · B. Un art de la provocation · C. Un art poétique parnassien</div>
          </div>
        </div>
      </div>

      <!-- PARTIE I accordeon -->
      <div class="card-section">
        <div class="section-label">Partie I — L'anti-portrait parodique de Vénus</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">I.A</div>
              <div class="mvt-titre">Un contre-blason</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text">Le <strong>blason</strong> est un court poème évoquant des parties du corps féminin pour en faire l'éloge, de haut en bas. Rimbaud en reprend la structure : <strong>champ lexical du corps</strong> de haut en bas (femme, cheveux, col, omoplates, reins, échine, croupe, anus).</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text">Mais il prend le <strong>contre-pied</strong> de la tradition en évitant les parties qui valorisent la féminité, pour choisir au contraire des parties sans charge poétique (omoplates) ou franchement <strong>vulgaires</strong> (anus). Rappelle le « Blason du laid tétin » de Clément <strong>Marot</strong> (1534).</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text">Loin du blason qui <strong>divinise</strong> la femme, Rimbaud met en valeur la <strong>laideur</strong> et dévalorise la figure féminine.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">I.B</div>
              <div class="mvt-titre">La dépréciation de Vénus</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Rimes subversives :</strong> <span class="citation">« tête »</span> rime avec <span class="citation">« bête »</span> ; surtout, <span class="citation">« Venus »</span> rime avec <span class="citation">« anus »</span> → désacralisation ironique de la déesse. Les rimes elles-mêmes deviennent un instrument de parodie.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Animalisation :</strong> <span class="citation">« lente et bête »</span>, <span class="citation">« col gras et gris »</span>, <span class="citation">« large croupe »</span>, <span class="citation">« tout ce corps remue »</span>. Possible souvenir de <strong>Baudelaire</strong> dans <em>Le Serpent qui danse</em> — mais à l'inverse : là où Baudelaire suggérait la sensualité et l'idéal, Rimbaud met en valeur la <strong>maladresse</strong> du mouvement.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Rejets et contre-rejets</strong> qui miment la disharmonie du corps : rejet de <span class="citation">« Horrible »</span> (v.9-10) ; contre-rejet de <span class="citation">« une tête / De femme »</span> (v.1-2). L'<strong>hyperbole</strong> <span class="citation">« tout ce corps »</span> et le verbe <span class="citation">« remue »</span> accentuent l'animalité. Le <strong>parallélisme</strong> <span class="citation">« qui rentre et qui ressort »</span> rend le mouvement mécanique.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">I.C</div>
              <div class="mvt-titre">Parodie des tableaux de la naissance de Vénus</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text">Parodie de la <em>Naissance de Vénus</em> de <strong>Botticelli</strong> (1485) et du tableau à succès d'<strong>Alexandre Cabanel</strong> (exposé en 1863, 8 ans avant le poème). Le <strong>champ lexical des couleurs</strong> (vert, blanc, bruns, gris, rouge) rapproche le poème d'un tableau.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text">Le <strong>vert et le blanc</strong> de <span class="citation">« un cercueil vert en fer blanc »</span> rappellent la vague et l'écume des tableaux. Mais le <strong>rouge</strong> de <span class="citation">« l'échine est un peu rouge »</span> détruit toute sensualité. La « <strong>vieille baignoire</strong> » remplace ironiquement le coquillage de Botticelli.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text">La <strong>blondeur</strong> traditionnelle de Vénus est remplacée par des cheveux bruns <span class="citation">« fortement pommadés »</span> — terme qui évoque l'artifice du maquillage théâtral, comme une Vénus de <strong>Commedia dell'Arte</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Parodie de synesthésie baudelairienne :</strong> champ lexical de la vue (remarque, voir, loupe), allitération en [g] (col <em>g</em>ras et <em>g</em>ris), champ lexical de l'odorat (sent, goût, horrible) — mais les sens convergent uniquement vers la <strong>laideur et l'horreur</strong>, à l'inverse des Correspondances de Baudelaire.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- PARTIE II accordeon -->
      <div class="card-section">
        <div class="section-label">Partie II — Une poésie nouvelle</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">II.A</div>
              <div class="mvt-titre">La destruction du lyrisme traditionnel</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Référence à Ronsard détruite :</strong> L'ouverture par <span class="citation">« Comme… »</span> rappelle <em>« Comme un chevreuil »</em> de Ronsard. Les mots <strong>chevreuil</strong> et <strong>cercueil</strong> sont proches phoniquement — Rimbaud se plaît à pervertir les mots du lyrisme de la Pléiade.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Référence à Louise Labé :</strong> Les mots gravés <span class="citation">« Clara Venus »</span> (v.12) sont en latin et rappellent le sonnet V de Louise Labé : <em>« Clere Venus qui erres par les cieux »</em>. Ces références à la Pléiade montrent une désinvolture <strong>moqueuse</strong> envers le lyrisme traditionnel.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Connecteurs a-poétiques :</strong> <span class="citation">« Puis »</span> (répété aux v.5 et 7), <span class="citation">« avec »</span>, <span class="citation">« surtout »</span> cassent le rythme lyrique. La répétition de <em>Puis</em> suggère un poème dont le lyrisme s'épuise et se répète mécaniquement.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Allitérations en [r] et [s]</strong> qui font entendre le caractère itératif d'une poésie à bout de souffle : <em>« Puis les <strong>r</strong>ondeurs des <strong>r</strong>eins semblent p<strong>r</strong>end<strong>r</strong>e l'esso<strong>r</strong> / La g<strong>r</strong>aisse sous la peau pa<strong>r</strong>aît en feuilles plates »</em>.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">II.B</div>
              <div class="mvt-titre">Un art de la provocation</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text">Pour Rimbaud, la beauté naît du <strong>choc, de la surprise et de l'inattendu</strong>. Cette Vénus n'est pas rejetée — elle est le support d'une <strong>beauté oxymorique</strong>. Deux oxymores la caractérisent : <span class="citation">« Horrible étrangement »</span> et <span class="citation">« Belle hideusement »</span>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Versification subvertie :</strong> Le sonnet n'obéit plus aux règles classiques. 1er quatrain : rimes croisées (ABAB) ; 2e quatrain : rimes embrassées (ACCA) ; tercets : système rimique indépendant (DDEFEF). La structure elle-même est <strong>irrégulière et provocatrice</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Alexandrin brisé :</strong> Le rythme des hémistiches est délibérément rompu : <em>« Puis/ le col /gras et gris,// les larges/ omoplates »</em> (1/2/3//3/3) ou <em>« Les reins por/tent deux mots gravés:/ Clara /Venus »</em> (3/5/2/2). L'alexandrin est une arme de plus contre le classicisme.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">II.C</div>
              <div class="mvt-titre">Un art poétique parnassien</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>La poésie comme sujet :</strong> Champ lexical de l'écriture et de la précision : <span class="citation">« feuilles plates »</span>, <span class="citation">« singularités »</span>, <span class="citation">« loupe »</span>, <span class="citation">« mots gravés »</span>. La loupe assimile le travail poétique à la <strong>sculpture ou à l'orfèvrerie</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Effacement du « je » lyrique :</strong> Remplacé par le pronom impersonnel <span class="citation">« on »</span> (<em>« on remarque surtout… »</em>, v.10). Le poète parnassien ne laisse pas transparaître ses sentiments — il s'efface derrière une <strong>objectivité froide</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Profusion descriptive :</strong> Multiplication des adjectifs et expansions du nom (<span class="citation">« cheveux bruns fortement pommadés »</span>, <span class="citation">« vieille baignoire »</span>) pour décrire la réalité le plus <strong>précisément</strong> possible, comme un peintre ou un naturaliste.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Conclusion :</strong> Influencé par la revue <em>Le Parnasse contemporain</em>, Rimbaud s'en distanciera progressivement. L'art pour l'art ne le satisfera pas longtemps ; sa soif de liberté langagière trouvera son expression dans des poèmes comme <em>Voyelles</em> ou <em>Le Bateau ivre</em>.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Figures de style à retenir</div>
        <div class="figures-grid">
          <div class="figure-card">
            <div class="figure-nom">Oxymore (×2)</div>
            <div class="figure-ex">« Horrible étrangement » · « Belle hideusement »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Rejet / contre-rejet</div>
            <div class="figure-ex">« goût / Horrible » · « une tête / De femme »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Hyperbole</div>
            <div class="figure-ex">« tout ce corps remue » → animalité totale</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Parallélisme</div>
            <div class="figure-ex">« qui rentre et qui ressort » → mouvement mécanique</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Allitération en [r]</div>
            <div class="figure-ex">« rondeurs des reins… prendre l'essor » → épuisement du lyrisme</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Allitération en [g]</div>
            <div class="figure-ex">« col gras et gris » → laideur sonore</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Rime parodique</div>
            <div class="figure-ex">Venus / anus · tête / bête</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Champ lex. écriture</div>
            <div class="figure-ex">feuilles plates, loupe, singularités, mots gravés</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Champ lex. corps</div>
            <div class="figure-ex">Tête → col → omoplates → dos → reins → échine → croupe → anus</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Intertextualité</div>
            <div class="figure-ex">Ronsard, Louise Labé, Marot, Baudelaire, Botticelli, Cabanel</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question">Quelle image Rimbaud donne-t-il de Vénus dans ce poème ?</div>
          <div class="question">En quoi « Vénus anadyomène » est-il une critique du lyrisme traditionnel ?</div>
          <div class="question">En quoi peut-on dire que ce poème est parodique ?</div>
          <div class="question">Comment définir l'esthétique parnassienne à partir de ce poème ?</div>
          <div class="question">Quel rapport ce poème entretient-il avec les tableaux de la naissance de Vénus ?</div>
        </div>
      </div>
    </div>
  </div>


  <!-- =================== FICHE 2 : DORMEUR =================== -->
  <div id="dormeur" class="bloc">
    <div class="bloc-titre">Fiche poème 2</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche 2 · Octobre 1870</div>
        <div class="fiche-titre">Le Dormeur du val</div>
        <div class="fiche-sous">Sonnet · 2 quatrains + 2 tercets · Alexandrins à rimes croisées</div>
        <div class="tags">
          <span class="tag tag-blue">Dénonciation de la guerre</span>
          <span class="tag tag-teal">Tableau bucolique trompeur</span>
          <span class="tag tag-amber">Chute tragique</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Texte du poème</div>
        <div class="poeme bleu">
          <div class="strophe">
            C'est un trou de verdure où chante une rivière,<br>
            Accrochant follement aux herbes des haillons<br>
            D'argent ; où le soleil, de la montagne fière,<br>
            Luit : c'est un petit val qui mousse de rayons.
          </div>
          <div class="strophe">
            Un soldat jeune, bouche ouverte, tête nue,<br>
            Et la nuque baignant dans le frais cresson bleu,<br>
            Dort ; il est étendu dans l'herbe, sous la nue,<br>
            Pâle dans son lit vert où la lumière pleut.
          </div>
          <div class="strophe">
            Les pieds dans les glaïeuls, il dort. Souriant comme<br>
            Sourirait un enfant malade, il fait un somme :<br>
            Nature, berce-le chaudement : il a froid.
          </div>
          <div class="strophe">
            Les parfums ne font pas frissonner sa narine ;<br>
            Il dort dans le soleil, la main sur sa poitrine,<br>
            Tranquille. Il a deux trous rouges au côté droit.
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Introduction et problématique</div>
        <div class="info-box">
          Rimbaud a 16 ans lorsqu'il écrit ce poème en pleine <strong>guerre franco-prussienne</strong>. Marqué par les horreurs qu'il voit, il compose ce sonnet qui donne à voir la mort d'un soldat à travers une stratégie de dissimulation habile : le poème entier fonctionne comme un <strong>trompe-l'œil</strong>, maintenant l'illusion du sommeil jusqu'au dernier vers.
          <br><br>
          <strong>Problématique :</strong> En quoi ce poème dénonce-t-il, de façon originale, les atrocités de la guerre ?
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Analyse linéaire — mouvements du texte (cliquer pour développer)</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">1er quatrain · Vers 1–4</div>
              <div class="mvt-titre">Un tableau bucolique empli de quiétude</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Nature omniprésente :</strong> Champ lexical de la nature (verdure, rivière, herbes, soleil, montagne) et de la couleur verte. Le lieu est présenté comme un havre de paix.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Lumière et éclat :</strong> Le soleil « luit », des « haillons d'argent » (rejets au début du vers pour mettre en évidence la lumière). La scène est inondée de rayons.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Nature vivante et personnifiée :</strong> La rivière « chante », « accroche follement ». Le verbe chanter et l'adverbe « follement » créent une touche festive. Assonances en nasales : chante, accrochant, follement.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Harmonie des éléments :</strong> Eau (rivière), terre (herbes), feu (soleil). Le tableau n'est pas statique : la nature est en mouvement (participe présent « accrochant », verbe « mousse »).</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">2e quatrain · Vers 5–8</div>
              <div class="mvt-titre">Un soldat paisiblement endormi</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Irruption du personnage :</strong> L'article indéfini « un soldat » (et non « le ») lui confère une portée universelle. Ce pourrait être n'importe quel soldat, n'importe quelle guerre.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Description d'un enfant endormi :</strong> Rythme ternaire harmonieux (« bouche ouverte, / tête nue »), « bouche ouverte » évoque un enfant. Le rejet de « Dort » en début de vers met en évidence le sommeil apparent.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Communion avec la nature :</strong> Le soldat est dans « son lit vert où la lumière pleut » — la nature devient un berceau protecteur. Synesthésie : la lumière « pleut » (vue + toucher).</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Indices à relire :</strong> « Pâle » — la pâleur du soldat peut indiquer l'anémie due à une blessure. Mais le lecteur, encore dans l'illusion du sommeil, ne le remarque pas.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">1er tercet · Vers 9–11</div>
              <div class="mvt-titre">L'émergence d'ambiguïtés</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Comparaison troublante :</strong> <span class="citation">« Souriant comme sourirait un enfant malade »</span> — le conditionnel introduit une incertitude. La mention de la « maladie » ternit le tableau serein. Le rejet crée une discordance subtile.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Pieds dans les glaïeuls :</strong> Les glaïeuls sont des fleurs associées aux enterrements. Le lecteur attentif peut y voir un indice funèbre. La mort commence à se glisser dans les détails.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Antithèse chaud/froid :</strong> <span class="citation">« berce-le chaudement : il a froid »</span> — quatre coupes dans ce vers créent une sensation de cassure. L'antithèse préfigure la mort. La Nature est apostrophée comme une mère protectrice.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">2e tercet · Vers 12–14</div>
              <div class="mvt-titre">La chute tragique</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Négation totale :</strong> <span class="citation">« Les parfums ne font pas frissonner sa narine »</span> — négation de la vie. Assonances en fricatives et sifflantes (parfums, font, frissonner, narine) qui heurtent l'oreille comme une mise en garde.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Fausse quiétude maintenue :</strong> « Il dort », « Tranquille », « la main sur sa poitrine » — Rimbaud continue d'entretenir l'illusion jusqu'au bout. Le rejet de « Tranquille » souligne une immobilité anormale dans cette nature vivante.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-red" style="background: var(--red)"></div>
                <div class="point-text"><strong>La chute :</strong> <span class="citation">« Il a deux trous rouges au côté droit. »</span> La mort n'est pas nommée. Elle est montrée de façon picturale, par un zoom sur la blessure. L'euphémisme « deux trous rouges » désigne les impacts de balles. La proposition courte et le point final créent un effet de choc maximal.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Commentaire littéraire — plan pour l'écrit</div>
        <div class="plan-grid">
          <div class="plan-card">
            <div class="plan-num">Partie I</div>
            <div class="plan-titre">Un décor apaisant et charmeur</div>
            <div class="plan-sous">A. Un cadre lumineux · B. Une nature vivante · C. Un environnement protecteur</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Partie II</div>
            <div class="plan-titre">Un sommeil ambigu</div>
            <div class="plan-sous">A. Un sommeil profond · B. L'ambivalence des termes · C. Une chute brutale et sans appel</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Partie III</div>
            <div class="plan-titre">L'efficacité de la dénonciation</div>
            <div class="plan-sous">A. Progression dramatique · B. Des contrastes frappants · C. Une lecture rétrospective obligatoire</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">La chute — à retenir absolument</div>
        <div class="chute-box">
          <span class="chute-citation">« Tranquille. Il a deux trous rouges au côté droit. »</span>
          La mort n'est pas nommée : elle est montrée de façon picturale, par un effet de zoom sur la blessure. L'euphémisme « deux trous rouges » désigne pudiquement les impacts de balles. La proposition courte et brutale après le point fort produit un choc maximal. Le rouge contraste violemment avec le vert dominant. « Deux trous rouges » fait écho à « trou de verdure » (v.1) → le lecteur doit relire tout le poème.
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">La mort dissimulée — indices à repérer dès la première lecture</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.1 — « trou de verdure »</strong> : le mot « trou » préfigure les « deux trous rouges » du v.14. En relisant, le décor idyllique révèle une nature funèbre.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.8 — « Pâle »</strong> : la pâleur du soldat est un indice de sa blessure et de la perte de sang, non d'un simple teint clair.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.9 — « Les pieds dans les glaïeuls »</strong> : les glaïeuls sont des fleurs de deuil. Position qui rappelle celle d'un mort dans son cercueil.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.10 — « enfant malade »</strong> : le conditionnel et la maladie introduisent une incertitude sur l'état réel du soldat.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.11 — « il a froid »</strong> : la froideur est un signe classique de la mort, ici camouflé par l'antithèse avec « chaudement ».</div>
          </div>
          <div class="point">
            <div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>v.12 — narine qui ne frémit pas</strong> : signe clinique de décès. Seul un mort ne réagit pas aux odeurs environnantes.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Figures de style à retenir</div>
        <div class="figures-grid">
          <div class="figure-card">
            <div class="figure-nom">Personnification</div>
            <div class="figure-ex">« où chante une rivière » · « Nature, berce-le »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Rejet</div>
            <div class="figure-ex">« D'argent » (v.3) · « Dort » (v.7) · « Tranquille » (v.14)</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Antithèse</div>
            <div class="figure-ex">« berce-le chaudement : il a froid »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Euphémisme</div>
            <div class="figure-ex">« deux trous rouges » pour les blessures mortelles</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Comparaison</div>
            <div class="figure-ex">« Souriant comme sourirait un enfant malade »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Négation totale</div>
            <div class="figure-ex">« Les parfums ne font pas frissonner sa narine »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Synesthésie</div>
            <div class="figure-ex">« la lumière pleut » → vue + toucher</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Écho structurel</div>
            <div class="figure-ex">« trou de verdure » (v.1) ↔ « deux trous rouges » (v.14)</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Conclusion</div>
        <div class="info-box">
          Le sonnet « Le Dormeur du val » instaure des <strong>contrastes frappants</strong> : entre la nature vivante et l'immobilité du soldat, entre les couleurs (vert, bleu, rouge), entre le chaud et le froid, entre la vie et la mort. Il est construit selon une <strong>progression dramatique</strong> entièrement tournée vers la chute, obligeant à une lecture rétrospective. La <strong>dénonciation de la guerre</strong> est d'autant plus efficace qu'elle est indirecte : Rimbaud ne nomme jamais ni la guerre, ni la mort, ni même le conflit franco-prussien. La violence surgit avec d'autant plus de force dans le dernier vers.
          <br><br>
          <strong>Ouvertures possibles :</strong> « Le Mal » de Rimbaud (autre poème des Cahiers dénonçant la guerre) · « L'Évadé » de Boris Vian · « Dulce et Decorum Est » de Wilfred Owen.
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question bleu">En quoi ce poème dénonce-t-il, de façon originale, les atrocités de la guerre ?</div>
          <div class="question bleu">Comment la construction du poème est-elle entièrement tournée vers la chute ?</div>
          <div class="question bleu">Quel rôle joue la nature dans ce poème ?</div>
          <div class="question bleu">En quoi la mort est-elle suggérée avant d'être révélée ?</div>
          <div class="question bleu">Que met Rimbaud en opposition dans ce sonnet ?</div>
          <div class="question bleu">Comment la chute du sonnet invite-t-elle à une relecture du poème ?</div>
        </div>
      </div>
    </div>
  </div>

  <!-- =================== FICHE 3 : MA BOHÈME =================== -->
  <div id="boheme" class="bloc">
    <div class="bloc-titre">Fiche poème 3</div>

    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche 3 · Automne 1870 · Sous-titre : « Fantaisie »</div>
        <div class="fiche-titre">Ma Bohème</div>
        <div class="fiche-sous">Sonnet · 2 quatrains + 2 tercets · Alexandrins · Forme classique malmenée</div>
        <div class="tags">
          <span class="tag tag-green">Liberté et vagabondage</span>
          <span class="tag tag-teal">Autodérision</span>
          <span class="tag tag-purple">Parodie romantique</span>
          <span class="tag tag-amber">Art poétique</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Texte du poème</div>
        <div class="poeme" style="border-left-color: #3b6d11; text-align: center;">
          <div class="strophe">
            Je m'en allais, les poings dans mes poches crevées ;<br>
            Mon paletot aussi devenait idéal ;<br>
            J'allais sous le ciel, Muse ! et j'étais ton féal ;<br>
            Oh ! là ! là ! que d'amours splendides j'ai rêvées !
          </div>
          <div class="strophe">
            Mon unique culotte avait un large trou.<br>
            – Petit-Poucet rêveur, j'égrenais dans ma course<br>
            Des rimes. Mon auberge était à la Grande-Ourse.<br>
            – Mes étoiles au ciel avaient un doux frou-frou
          </div>
          <div class="strophe">
            Et je les écoutais, assis au bord des routes,<br>
            Ces bons soirs de septembre où je sentais des gouttes<br>
            De rosée à mon front, comme un vin de vigueur ;
          </div>
          <div class="strophe">
            Où, rimant au milieu des ombres fantastiques,<br>
            Comme des lyres, je tirais les élastiques<br>
            De mes souliers blessés, un pied près de mon cœur !
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Introduction et problématique</div>
        <div class="info-box" style="border-left-color: #3b6d11;">
          « Ma Bohème » est sans doute inspirée de la <strong>fugue d'octobre 1870</strong>. Rimbaud a 16 ans et cherche à échapper à la pesanteur familiale. Ce qu'il nomme « bohème » — vie de pauvreté mais de liberté, d'insouciance et de poésie — est une réappropriation de clichés romantiques, annoncée par le possessif <em>« ma »</em> du titre. Le sous-titre <em>« Fantaisie »</em> renforce l'idée de liberté.
          <br><br>
          Le poème est un <strong>sonnet en apparence classique</strong>, mais sa forme est constamment malmenée par des enjambements et décalages rythmiques qui miment le rythme de l'errance.
          <br><br>
          <strong>Problématique :</strong> Quelles sont les caractéristiques de la « bohème » idéale de ce tout jeune poète ?
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Plan de l'analyse linéaire</div>
        <div class="plan-grid">
          <div class="plan-card">
            <div class="plan-num">Mouvement I · v. 1–5</div>
            <div class="plan-titre">L'espiègle vagabond</div>
            <div class="plan-sous">Vagabondage sans but, posture désinvolte, pauvreté exhibée, dédicace ironique à la Muse</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Mouvement II · v. 6–11</div>
            <div class="plan-titre">Un Petit-Poucet à la belle étoile</div>
            <div class="plan-sous">Personnage de conte enfantin, étoiles et rimes, contact avec la nature nocturne</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Mouvement III · v. 12–14</div>
            <div class="plan-titre">La lyre faite de lacets : chute parodique</div>
            <div class="plan-sous">Autodérision finale, parodie des symboles lyriques, double sens du « pied » poétique</div>
          </div>
        </div>
      </div>

      <!-- ANALYSE LINEAIRE ACCORDEON -->
      <div class="card-section">
        <div class="section-label">Analyse linéaire détaillée (cliquer pour développer)</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">Vers 1–5</div>
              <div class="mvt-titre">I — L'espiègle vagabond</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-green"></div>
                <div class="point-text"><strong>« Je m'en allais » (v.1) :</strong> Déplacement sans but défini, marche libre et continue. La posture <span class="citation">« les poings dans mes poches »</span> est désinvolte. Les <span class="citation">« poches crevées »</span> illustrent la pauvreté par l'usure du vêtement. Un <strong>enjambement interne</strong> perturbe d'emblée le rythme classique de l'alexandrin.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Autodérision dès le v.2 :</strong> Le <span class="citation">« paletot »</span> (manteau) qui <span class="citation">« devenait idéal »</span> joue sur le double sens : il correspond à l'idéal de pauvreté bohème, ET il est si usé qu'il n'en reste qu'une <em>idée</em>. Le jeu sonore entre « paletot » et « aussi » (le son [o] deux fois) donne un côté <strong>cocasse</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>La Muse invoquée (v.3) :</strong> L'invocation de la Muse (divinité antique de la poésie) est brusque, inattendue, réduite à un monosyllabe à la césure, ponctué d'un point d'exclamation. C'est une manière <strong>espiègle</strong> de convoquer ce cliché poétique. Le vieux mot <span class="citation">« féal »</span> (fidèle), choisi pour rimer avec « idéal », ajoute à l'humour décalé.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Exclamation populaire (v.3–4) :</strong> <span class="citation">« Oh ! là ! là ! »</span>, tiré du langage courant, est parfaitement <strong>décalée</strong> dans l'alexandrin classique. <span class="citation">« Que d'amours splendides j'ai rêvées ! »</span> — les amours sont rêvées, non réalisées ; la rime <em>rêvées / crevées</em> (v.1 et 4) suggère ironiquement que le rêve est voué à l'échec.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Enjambement sur le 2e quatrain (v.5) :</strong> <span class="citation">« Mon unique culotte avait un large trou. »</span> Ce débordement au mépris des règles classiques donne un tour <strong>naïf et cocasse</strong>. Les mots « culotte » et « large trou » coulent le grotesque et le trivial dans l'alexandrin.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">Vers 6–11</div>
              <div class="mvt-titre">II — Un Petit-Poucet à la belle étoile</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-green"></div>
                <div class="point-text"><strong>« Petit-Poucet rêveur » (v.6) :</strong> Le tiret signale un changement d'images. Rimbaud se présente en <strong>personnage de conte</strong> — enfantin, malicieux — plutôt qu'en féal solennel de la Muse. L'adjectif « rêveur » élève ce Petit-Poucet au rang de poète.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Des rimes semées (v.6–7) :</strong> Au lieu de cailloux, Rimbaud sème des rimes : <span class="citation">« j'égrenais dans ma course / Des rimes »</span>. Le <strong>rejet</strong> de <span class="citation">« Des rimes »</span> en début de vers les met en valeur comme les cailloux jetés d'une poche.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Possession poétique (v.7–8) :</strong> Les possessifs <span class="citation">« mon auberge »</span> et <span class="citation">« mes étoiles »</span> rappellent que Rimbaud décrit des impressions <strong>personnelles</strong>. L'auberge « à la Grande-Ourse » signifie qu'il n'a pas d'auberge du tout. Le <span class="citation">« doux frou-frou »</span> des étoiles — son de froissement de soieries — est une image sonore étonnante et poétique.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Contact avec la nature (v.9–11) :</strong> La phrase se prolonge sur le 1er tercet : le poète est <span class="citation">« assis au bord des routes »</span>, en contact direct avec la nature automnale (<span class="citation">« ces bons soirs de septembre »</span>). Le rejet de <span class="citation">« De rosée »</span> met en valeur ces gouttelettes d'eau pure dont le poète est comme <strong>baptisé</strong>.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>La rosée comme vin de vigueur (v.11) :</strong> La comparaison <span class="citation">« comme un vin de vigueur »</span> exprime la force que le poète puise dans la nature, pour la <strong>marche autant que pour la poésie</strong>. Nature et création poétique sont ici indissociables.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div>
              <div class="mvt-num">Vers 12–14</div>
              <div class="mvt-titre">III — La lyre faite de lacets : chute parodique</div>
            </div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point">
                <div class="point-dot dot-green"></div>
                <div class="point-text"><strong>Atmosphère fantastique (v.12) :</strong> Le poète « rime » seul parmi les <span class="citation">« ombres fantastiques »</span> du soir. Cette posture de poète solitaire et nocturne est un <strong>cliché romantique</strong> que le dernier vers va immédiatement dégonfler.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Rime saugrenue (v.12–13) :</strong> Le lecteur a la surprise d'entendre <span class="citation">« ombres fantastiques »</span> rimer avec <span class="citation">« élastiques »</span>. L'objet — les lacets de chaussures — est <strong>trivial et inattendu</strong> en poésie.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>La lyre faite de lacets (v.13) :</strong> Les élastiques sont comparés à <span class="citation">« des lyres »</span>. La <strong>lyre</strong>, noble instrument antique et grand symbole de la poésie lyrique, est ici ridiculisée. Le verbe <span class="citation">« tirais »</span> révèle une manière peu gracieuse de jouer de la lyre — c'est l'<strong>autodérision</strong> à son comble.</div>
              </div>
              <div class="point">
                <div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Double sens du « pied » (v.14) :</strong> <span class="citation">« un pied près de mon cœur »</span> — le mot « pied » désigne à la fois le <strong>membre du corps</strong> (image finale cocasse et désinvolte) et l'<strong>unité de mesure poétique</strong> (le pied métrique). Rimbaud noue en une seule image le thème de la <strong>marche et celui de la poésie</strong>. Les souliers « blessés » font écho aux « poches crevées » (v.1) et au paletot usé (v.2).</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Points clés — à retenir absolument</div>
        <div class="points">
          <div class="point">
            <div class="point-dot dot-green"></div>
            <div class="point-text"><strong>Forme classique malmenée :</strong> Le sonnet est constamment perturbé par des enjambements entre quatrains (v.4-5) et entre quatrain et tercet (v.8-9). Ces débordements miment le rythme du <strong>vagabondage incessant</strong>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Parodie des postures romantiques :</strong> Rimbaud se moque des clichés (la Muse, la lyre, le poète solitaire nocturne) tout en les utilisant. L'<strong>autodérision</strong> est la marque de fabrique du poème.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>La bohème comme art poétique :</strong> Errance et poésie sont indissociables. Semer des rimes comme Petit-Poucet sème des cailloux, jouer de la lyre avec des lacets de chaussures — la <strong>dérive est la condition de la création</strong>.</div>
          </div>
          <div class="point">
            <div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>Humour et liberté :</strong> Contrairement à <em>Vénus anadyomène</em> (violence parodique) ou au <em>Dormeur du val</em> (gravité dissimulée), <em>Ma Bohème</em> est un poème <strong>léger, espiègle</strong>, où la pauvreté est assumée avec joie. C'est la fugue vécue comme libération.</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Figures de style à retenir</div>
        <div class="figures-grid">
          <div class="figure-card">
            <div class="figure-nom">Enjambement interne</div>
            <div class="figure-ex">« les poings / dans mes poches » → perturbe l'alexandrin dès v.1</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Double sens (polysémie)</div>
            <div class="figure-ex">« idéal » (v.2) · « pied » (v.14) → humour et art poétique</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Métaphore filée</div>
            <div class="figure-ex">Petit-Poucet → rimes = cailloux → marche = poésie</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Comparaison parodique</div>
            <div class="figure-ex">« Comme des lyres, je tirais les élastiques »</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Comparaison</div>
            <div class="figure-ex">« comme un vin de vigueur » → nature nourrissante</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Apostrophe</div>
            <div class="figure-ex">« Muse ! » (v.3) → invocation ironique à la divinité poétique</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Rime saugrenue</div>
            <div class="figure-ex">« fantastiques » / « élastiques » → autodérision maximale</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Exclamation populaire</div>
            <div class="figure-ex">« Oh ! là ! là ! » → langage courant dans l'alexandrin classique</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Rejet</div>
            <div class="figure-ex">« Des rimes » (v.7) · « De rosée » (v.11) → mise en valeur par rejet</div>
          </div>
          <div class="figure-card">
            <div class="figure-nom">Enjambement inter-strophes</div>
            <div class="figure-ex">v.4-5 (quatrains) · v.8-9 (quatrain-tercet) → miment l'errance</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Conclusion</div>
        <div class="info-box" style="border-left-color: #3b6d11;">
          « Ma Bohème » est un sonnet <strong>léger et humoristique</strong> qui évoque des éléments autobiographiques tout en parodiant les postures romantiques. La forme même du sonnet est malmenée : Rimbaud fait sans cesse déborder les strophes et les hémistiches, créant de nombreux décalages rythmiques qui miment le <strong>rythme du vagabondage incessant</strong>.
          <br><br>
          On y lit un amour fou de la <strong>liberté</strong>, des marches solitaires, un mépris des conventions sociales et du confort bourgeois. Comme dans <em>Le Bateau ivre</em>, la poésie liée à la fugue est une <strong>expérience de dérive</strong>.
          <br><br>
          <strong>Ouvertures possibles :</strong> <em>Sensation</em> de Rimbaud (autre poème de liberté et de nature) · <em>Le Bateau ivre</em> · <em>Au cabaret-vert</em> (autre fugue poétisée).
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question" style="border-left-color: #3b6d11;">Quelles sont les caractéristiques de la « bohème » idéale du jeune Rimbaud ?</div>
          <div class="question" style="border-left-color: #3b6d11;">En quoi ce poème parodie-t-il les postures romantiques ?</div>
          <div class="question" style="border-left-color: #3b6d11;">Comment la forme du sonnet est-elle subvertie pour mimer l'errance ?</div>
          <div class="question" style="border-left-color: #3b6d11;">En quoi l'image finale de la lyre faite de lacets est-elle à la fois triviale et symbolique ?</div>
          <div class="question" style="border-left-color: #3b6d11;">Quel lien Rimbaud établit-il entre marche et création poétique ?</div>
        </div>
      </div>
    </div>
  </div>

</div><!-- /container -->
</div><!-- /panel-cahiers-douai -->

<!-- =================== PANEL : PARTI PRIS =================== -->
<div id="panel-parti-pris" class="tab-panel">
<div class="container">

  <div class="page-header">
    <div class="surtitre">Le Parti pris des choses · Bac de français</div>
    <h1>Francis Ponge</h1>
    <div class="sub">Fiches de révision complètes · Auteur · Recueil · L'Huître</div>
  </div>

  <!-- AUTEUR -->
  <div id="ponge-auteur" class="bloc">
    <div class="bloc-titre">L'auteur</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche auteur</div>
        <div class="fiche-titre">Francis Ponge (1899–1988)</div>
        <div class="fiche-sous">Poète français · XXe siècle · Poésie des objets</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-teal">Parti pris des choses</span>
          <span class="tag tag-blue">Résistant</span>
          <span class="tag tag-amber">Contre le lyrisme</span>
          <span class="tag tag-purple">Poésie en prose</span>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Portrait</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text">Né le <strong>27 mars 1899</strong> à Montpellier. Ses origines bourgeoises et son intelligence brillante le destinent à de grandes études, mais son <strong>mutisme lors des oraux</strong> l'empêche de les achever — une ironie pour celui qui deviendra l'un des plus grands stylistes français.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text">Devient <strong>employé de bureau</strong> et exècre « l'engrenage broyeur » du monde du travail. Ce dégoût du monde trop humain nourrit directement sa poésie tournée vers les choses et les objets.</div>
          </div>
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Résistant</strong> engagé pendant l'Occupation. Il fréquente les groupes surréalistes mais n'adhère pas à leur conception de la poésie : là où les surréalistes cherchent à atteindre une « surréalité », Ponge cherche à restituer fidèlement les choses.</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text">Publie <em>Le Parti pris des choses</em> en <strong>1942</strong>, en pleine Occupation. Le recueil passe d'abord inaperçu avant d'être reconnu comme une œuvre majeure du XXe siècle. Jean-Paul Sartre sera l'un de ses premiers défenseurs enthousiastes.</div>
          </div>
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text">Mort le <strong>6 août 1988</strong> à Le Bar-sur-Loup (Alpes-Maritimes), à 89 ans. Son œuvre est aujourd'hui reconnue comme fondatrice d'une poésie matérialiste et anti-lyrique qui a profondément influencé la littérature contemporaine.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Œuvres principales</div>
        <div class="figures-grid">
          <div class="figure-card"><div class="figure-nom">Le Parti pris des choses (1942)</div><div class="figure-ex">32 poèmes en prose sur des objets, animaux et éléments du quotidien.</div></div>
          <div class="figure-card"><div class="figure-nom">La Rage de l'expression (1952)</div><div class="figure-ex">Suite du projet poétique, avec des pièces plus longues et des réflexions sur l'écriture.</div></div>
          <div class="figure-card"><div class="figure-nom">Le Grand Recueil (1961)</div><div class="figure-ex">Rassemble une grande partie de son œuvre en trois volumes.</div></div>
          <div class="figure-card"><div class="figure-nom">La Fabrique du Pré (1971)</div><div class="figure-ex">Texte génétique montrant tous les états d'un poème depuis l'ébauche.</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- FRISE -->
  <div id="ponge-frise" class="bloc">
    <div class="bloc-titre">Frise chronologique</div>
    <div class="card">
      <div class="card-section">
        <div class="frise-legende">
          <div class="legende-item"><div class="legende-dot key"></div> Création littéraire</div>
          <div class="legende-item"><div class="legende-dot war"></div> Événement historique</div>
          <div class="legende-item"><div class="legende-dot pub"></div> Publication</div>
          <div class="legende-item"><div class="legende-dot life"></div> Vie personnelle</div>
        </div>
        <div class="frise">
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">27 mars 1899</div>
            <div class="frise-titre">Naissance à Montpellier</div>
            <div class="frise-desc">Naissance de Francis Jean Gaston Alfred Ponge dans une famille de la bourgeoisie protestante.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">1916–1918</div>
            <div class="frise-titre">Échec aux oraux de l'ENS</div>
            <div class="frise-desc">Ses blocages à l'oral l'empêchent d'intégrer l'École Normale Supérieure — une ironie pour ce futur maître du langage écrit.</div>
          </div>
          <div class="frise-item"><div class="frise-dot war"></div>
            <div class="frise-date">1914–1918</div>
            <div class="frise-titre">Première Guerre mondiale</div>
            <div class="frise-desc">La violence du monde humain commence à nourrir chez Ponge un profond rejet de l'anthropocentrisme.</div>
          </div>
          <div class="frise-item"><div class="frise-dot key"></div>
            <div class="frise-date">Années 1920–1930</div>
            <div class="frise-titre">Rédaction des premiers poèmes-objets</div>
            <div class="frise-desc">Employé de bureau, Ponge compose dans l'entre-deux-guerres les poèmes qui formeront le <em>Parti pris des choses</em>. Il fréquente les surréalistes sans adhérer à leur esthétique.</div>
          </div>
          <div class="frise-item"><div class="frise-dot war"></div>
            <div class="frise-date">1939–1945</div>
            <div class="frise-titre">Seconde Guerre mondiale — Résistance</div>
            <div class="frise-desc">Ponge s'engage dans la Résistance. Le contexte de violence et d'occupation renforce son rejet d'un monde trop humain et démesurément violent.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1942</div>
            <div class="frise-titre">Publication du Parti pris des choses</div>
            <div class="frise-desc">Publié chez Gallimard pendant l'Occupation. Le recueil passe d'abord inaperçu. Jean-Paul Sartre sera l'un des premiers à en reconnaître la valeur révolutionnaire.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1952</div>
            <div class="frise-titre">La Rage de l'expression</div>
            <div class="frise-desc">Second recueil majeur, qui pousse plus loin la réflexion sur le langage et la description des choses. Ponge y montre son propre processus d'écriture.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">Années 1960–1970</div>
            <div class="frise-titre">Reconnaissance internationale</div>
            <div class="frise-desc">Ponge enseigne aux États-Unis et en Europe. Son œuvre influence profondément les mouvements du Nouveau Roman et de Tel Quel. Il est proche de Camus, Sartre, et des peintres (Braque, Fautrier).</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1971</div>
            <div class="frise-titre">La Fabrique du Pré</div>
            <div class="frise-desc">Œuvre génétique révolutionnaire : Ponge publie tous les brouillons et états successifs d'un même poème, montrant que la création poétique est un processus vivant.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">6 août 1988</div>
            <div class="frise-titre">Mort au Bar-sur-Loup</div>
            <div class="frise-desc">Ponge s'éteint à 89 ans en Provence. Son œuvre est aujourd'hui au programme du bac de français et est étudiée dans le monde entier.</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- RECUEIL -->
  <div id="ponge-recueil" class="bloc">
    <div class="bloc-titre">Le recueil</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Recueil · 1942 · Gallimard</div>
        <div class="fiche-titre">Le Parti pris des choses</div>
        <div class="fiche-sous">32 poèmes en prose · Objets, éléments, animaux, portraits</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-teal">Poésie en prose</span>
          <span class="tag tag-amber">Anti-lyrisme</span>
          <span class="tag tag-blue">Matérialisme poétique</span>
          <span class="tag tag-purple">Titre-manifeste</span>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Le titre — un manifeste</div>
        <div class="info-box">
          <strong>« Le parti pris des choses »</strong> est un titre presque polémique. Il désigne l'attitude d'un poète qui <strong>se détourne des humains</strong> pour se consacrer aux <strong>« choses »</strong>. Prendre le parti des choses, c'est choisir leur camp contre celui des hommes. C'est aussi adopter un <em>parti pris</em> — c'est-à-dire un point de vue délibérément partial — au service des objets muets que la poésie traditionnelle ignorait.
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Structure et contenu</div>
        <div class="symb-grid">
          <div class="symb-card"><div class="symb-titre">Les aliments</div><div class="symb-texte">Fruits aux saveurs intenses (Les mûres, L'orange), mollusques et fruits de mer (L'huître, La crevette, L'escargot).</div></div>
          <div class="symb-card"><div class="symb-titre">Les éléments</div><div class="symb-texte">Le recueil s'ouvre sur La pluie. Ponge est attentif à l'élément liquide : Bords de mer, De l'eau. La nature comme texte à lire.</div></div>
          <div class="symb-card"><div class="symb-titre">Les objets prosaïques</div><div class="symb-texte">Objets familiers ou dédaignés : Le cageot, La cigarette, La bougie, Le pain. Ponge les personnifie et les élève au rang poétique.</div></div>
          <div class="symb-card"><div class="symb-titre">Les portraits satiriques</div><div class="symb-texte">R.C. Seine n° (caricature des employés de bureau), Le gymnaste (portrait d'un séducteur). L'humain y est méprisable.</div></div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Thèmes majeurs</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>L'attention aiguë au détail :</strong> La démarche de Ponge tient en une <strong>attention méticuleuse à l'infinitésimal</strong>. L'écriture agit en microscope pour atteindre une « impression quasi panoramique » (Le Pain). Ces microcosmes abordés comme des macrocosmes révèlent le fonctionnement intime des choses.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Renouer le poème et le monde :</strong> Ces poèmes renouent avec la tradition antique du poème cosmique (Hésiode, Lucrèce, <em>De rerum natura</em>). En animant l'inanimé, Ponge <strong>réenchante le monde</strong>. Il va jusqu'à rêver sa fusion avec la nature : <em>« Quel bonheur, quelle joie donc d'être un escargot »</em>.</div>
          </div>
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Le rejet d'un monde trop humain :</strong> Ponge écrit dans l'entre-deux-guerres et condamne la <strong>démesure humaine</strong>. Pour lui, l'homme ne doit plus être au centre des choses. Ce rejet renvoie au climat politique violent de l'époque.</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>Le rejet du lyrisme :</strong> Ponge parodie l'automne, thème lyrique par excellence : <em>« Tout l'automne à la fin n'est plus qu'une tisane froide. »</em> Il rabaisse le poème au rang d'objet parmi les objets, <strong>inférieur à la nature</strong>.</div>
          </div>
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Réflexion sur la poésie :</strong> Derrière les descriptions d'objets se cache un <strong>art poétique</strong>. L'huître symbolise le poème hermétique qui abrite « tout un monde » accessible par l'effort. La perle finale est la métaphore de la création poétique.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Caractéristiques de l'écriture</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>Forme du dictionnaire :</strong> Chaque poème constitue la <strong>définition d'un mot</strong>. Ponge explore le signifiant (la sonorité) et le signifié (le sens) : <em>« À mi-chemin de la cage au cachot, la langue française a cageot »</em>. L'article défini (La pluie, Le pain, L'huître) et le <strong>présent de vérité générale</strong> donnent un ton encyclopédique et impersonnel.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Restauration de l'étymologie :</strong> Ponge se plaît à faire ressurgir l'étymologie oubliée des mots, provoquant une poésie inattendue. La seule polysémie d'un mot fait surgir des images surprenantes — comme le <em>« firmament »</em> de l'huître.</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>Une poésie comique :</strong> Paronomases, onomatopées (<em>« le glou-glou des gouttières »</em>), néologismes plaisants (<em>« amphibiguïté »</em>), ruptures de registre. L'humour révèle la <strong>jouissance du poète à écrire et décrire</strong>.</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- L'HUÎTRE -->
  <div id="ponge-huitre" class="bloc">
    <div class="bloc-titre">Fiche poème</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Poème en prose · Le Parti pris des choses (1942)</div>
        <div class="fiche-titre">L'Huître</div>
        <div class="fiche-sous">3 paragraphes · Forme close · Poème-définition</div>
        <div class="tags">
          <span class="tag tag-teal">Poésie nouvelle</span>
          <span class="tag tag-blue">Refus de l'homme</span>
          <span class="tag tag-purple">Métaphore poétique</span>
          <span class="tag tag-amber">Monde caché</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Texte du poème</div>
        <div class="poeme" style="border-left-color: var(--teal); text-align: left; font-family: 'Helvetica Neue', Arial, sans-serif; line-height: 1.8; font-size: 13px;">
          <div class="strophe">
            L'huître, de la grosseur d'un galet moyen, est d'une apparence plus rugueuse, d'une couleur moins unie, brillamment blanchâtre. C'est un monde opiniâtrement clos. Pourtant on peut l'ouvrir : il faut alors la tenir au creux d'un torchon, se servir d'un couteau ébréché et peu franc, s'y reprendre à plusieurs fois. Les doigts curieux s'y coupent, s'y cassent les ongles : c'est un travail grossier. Les coups qu'on lui porte marquent son enveloppe de ronds blancs, d'une sorte de halos.
          </div>
          <div class="strophe">
            À l'intérieur l'on trouve tout un monde, à boire et à manger : sous un firmament (à proprement parler) de nacre, les cieux d'en dessus s'affaissent sur les cieux d'en dessous, pour ne plus former qu'une mare, un sachet visqueux et verdâtre, qui flue et reflue à l'odeur et à la vue, frangé d'une dentelle noirâtre sur les bords.
          </div>
          <div class="strophe">
            Parfois très rare une formule perle à leur gosier de nacre, d'où l'on trouve aussitôt à s'orner.
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Introduction et problématique</div>
        <div class="info-box" style="border-left-color: var(--teal);">
          Publié en 1942 dans <em>Le Parti pris des choses</em>, « L'Huître » est un <strong>poème en prose</strong> qui rompt avec la tradition lyrique en choisissant pour sujet un objet du quotidien. Ponge en fait une <strong>description précise et distanciée</strong>, tout en cachant derrière l'huître une réflexion sur la <strong>création poétique</strong> elle-même.
          <br><br>
          <strong>Problématiques :</strong> Quelle vision du monde Ponge propose-t-il à travers l'huître ? — L'huître est-elle décrite pour elle-même ? — Quels changements poétiques ce parti pris met-il en place ?
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Plan du commentaire</div>
        <div class="plan-grid">
          <div class="plan-card"><div class="plan-num">Partie I</div><div class="plan-titre">Une poésie nouvelle</div><div class="plan-sous">A. Une forme close · B. Un sujet prosaïque · C. Un mode d'emploi</div></div>
          <div class="plan-card"><div class="plan-num">Partie II</div><div class="plan-titre">Une remise en cause du monde</div><div class="plan-sous">A. Le refus de l'homme · B. Le refus de la parole</div></div>
          <div class="plan-card"><div class="plan-num">Partie III</div><div class="plan-titre">La proposition d'un monde nouveau</div><div class="plan-sous">A. Un nouveau monde intérieur · B. Opposition des deux mondes · C. Métaphore de la création poétique</div></div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Analyse détaillée (cliquer pour développer)</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Partie I</div><div class="mvt-titre">Une poésie nouvelle</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Une forme close :</strong> Le poème forme un <strong>bloc serré sans blanc typographique</strong>, à l'image du galet de la première ligne. La disposition du texte mime visuellement l'huître, ce « monde opiniâtrement clos ». La forme est au service du fond.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Un sujet prosaïque :</strong> Les <strong>adjectifs avec le suffixe « -âtre »</strong> (<em>blanchâtre, verdâtre, noirâtre</em>) refusent toute idéalisation et connotent péjorativement l'huître. Ponge ne cherche pas la beauté mais la <strong>réalité</strong>. En faisant de l'huître un sujet poétique, il lui donne une seconde vie et l'élève au rang d'œuvre d'art.</div>
              </div>
              <div class="point"><div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Un mode d'emploi :</strong> Ponge adopte une approche <strong>descriptive et prescriptive</strong> : verbe d'état au présent de vérité générale (<em>« est d'une apparence »</em>), verbes d'action (<em>« il faut la tenir », « se servir d'un couteau »</em>). Le poème ressemble à une notice encyclopédique.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Partie II</div><div class="mvt-titre">Une remise en cause du monde</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Le refus de l'homme :</strong> L'homme est exclu du poème. Il n'apparaît que par le <strong>pronom impersonnel « il »</strong> (sujet du verbe <em>falloir</em>) et le <strong>pronom indéfini neutre « on »</strong> (3 occurrences). La <strong>métonymie</strong> « les doigts » le déshumanise. Quand il apparaît, c'est en tant qu'<strong>individu violent</strong> qui blesse l'huître — « les coups qu'on lui porte » — tandis que les halos lumineux la divinisent comme un martyr.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Allitération en [k] :</strong> <em>« les doigts <strong>c</strong>urieux s'y <strong>c</strong>oupent, s'y <strong>c</strong>assent les ongles », « les <strong>c</strong>oups <strong>qu</strong>'on lui porte »</em> — cette consonne occlusive souligne la violence de l'homme et la résistance de l'huître.</div>
              </div>
              <div class="point"><div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Le refus de la parole :</strong> Ponge représente l'huître uniquement par la description — sans lui donner la parole comme les romantiques le faisaient. Saisir l'essence des choses par l'écriture est un <strong>travail difficile et heurté</strong>, comme l'ouvrir à la main.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Partie III</div><div class="mvt-titre">La proposition d'un monde nouveau</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Un nouveau monde intérieur :</strong> L'intérieur de l'huître révèle un <strong>monde complet</strong> (mentionné deux fois : <em>« tout un monde »</em>, <em>« c'est un monde »</em>) avec ses cieux (<em>firmament</em>), son eau (<em>une mare</em>), sa terre (<em>sachet visqueux</em>). La restauration étymologique du mot <em>« firmament »</em> (voûte céleste) crée une image poétique inattendue.</div>
              </div>
              <div class="point"><div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Confrontation de deux mondes — antithèses :</strong> Le monde extérieur (dur, rugueux, opaque) s'oppose radicalement à l'intérieur (fluide, coloré, nacré). Séparés typographiquement par un retour à la ligne : aspect (<em>rugueuse / visqueux</em>), couleur (<em>blanchâtre / noirâtre</em>), forme (<em>galet / mare</em>).</div>
              </div>
              <div class="point"><div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Métaphore de la création poétique :</strong> La dernière phrase — <em>« Parfois très rare une formule perle à leur gosier de nacre »</em> — contient deux termes de parole (<em>formule, gosier</em>) et évoque la rareté et la pureté (<em>perle, nacre</em>). L'huître est une <strong>mise en abyme du poème</strong> : le travail difficile pour l'ouvrir figure l'effort du poète pour trouver la formule juste. La perle, c'est le poème réussi.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Figures de style à retenir</div>
        <div class="figures-grid">
          <div class="figure-card"><div class="figure-nom">Adjectifs en -âtre</div><div class="figure-ex">blanchâtre, verdâtre, noirâtre → refus d'idéalisation</div></div>
          <div class="figure-card"><div class="figure-nom">Allitération en [k]</div><div class="figure-ex">coupent, cassent, coups → violence de l'homme</div></div>
          <div class="figure-card"><div class="figure-nom">Métonymie</div><div class="figure-ex">« les doigts » pour désigner l'homme → déshumanisation</div></div>
          <div class="figure-card"><div class="figure-nom">Antithèse</div><div class="figure-ex">extérieur rugueux / intérieur fluide → deux mondes opposés</div></div>
          <div class="figure-card"><div class="figure-nom">Étymologie restaurée</div><div class="figure-ex">« firmament » → voûte céleste dans l'huître</div></div>
          <div class="figure-card"><div class="figure-nom">Mise en abyme</div><div class="figure-ex">L'huître = métaphore de la création poétique</div></div>
          <div class="figure-card"><div class="figure-nom">Polysémie</div><div class="figure-ex">« formule perle » → parole + bijou + rareté</div></div>
          <div class="figure-card"><div class="figure-nom">Pronom indéfini « on »</div><div class="figure-ex">3 occurrences → l'homme réduit à un agent anonyme</div></div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Conclusion</div>
        <div class="info-box" style="border-left-color: var(--teal);">
          Ponge fait de l'huître bien plus qu'une description réaliste. Il en fait une <strong>allégorie d'un monde meilleur</strong> caché à l'intérieur du monde ordinaire, et une <strong>réflexion sur la poésie</strong> elle-même : le travail difficile pour ouvrir l'huître figure l'effort du poète, et la perle figure la formule poétique rare et précieuse.
          <br><br>
          <strong>Ouvertures :</strong> Le Cageot (autre poème-définition du recueil) · Le Pain (même structure en deux temps) · Le Joujou du pauvre de Baudelaire (objet banal élevé au rang poétique).
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question" style="border-left-color: var(--teal);">Quels changements poétiques ce parti pris met-il en place ?</div>
          <div class="question" style="border-left-color: var(--teal);">Quelle vision de l'huître est dégagée par le poème ?</div>
          <div class="question" style="border-left-color: var(--teal);">À travers l'huître, quelle vision du monde propose Ponge ?</div>
          <div class="question" style="border-left-color: var(--teal);">L'huître dans ce poème est-elle décrite pour elle-même ?</div>
          <div class="question" style="border-left-color: var(--teal);">En quoi « L'Huître » peut-il se lire comme une mise en abyme de la création poétique ?</div>
        </div>
      </div>
    </div>
  </div>

</div><!-- /container -->
</div><!-- /panel-parti-pris -->

<!-- =================== PANEL : ON NE BADINE =================== -->
<div id="panel-on-ne-badine" class="tab-panel">
<div class="container">

  <div class="page-header">
    <div class="surtitre">On ne badine pas avec l'amour · Bac de français</div>
    <h1>Alfred de Musset</h1>
    <div class="sub">Fiches de révision · Auteur · Frise · Romantisme · Poètes maudits · La pièce</div>
  </div>

  <!-- AUTEUR MUSSET -->
  <div class="bloc">
    <div class="bloc-titre">L'auteur</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Fiche auteur</div>
        <div class="fiche-titre">Alfred de Musset (1810–1857)</div>
        <div class="fiche-sous">Poète, romancier, dramaturge · XIXe siècle · Romantisme · Mal du siècle</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-coral">Romantisme</span>
          <span class="tag tag-purple">Mal du siècle</span>
          <span class="tag tag-blue">Drame romantique</span>
          <span class="tag tag-amber">Poète maudit</span>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Portrait</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text">Né le <strong>11 décembre 1810</strong> à Paris dans une famille cultivée. Enfant prodige, il entre à 17 ans dans le cercle du <strong>Cénacle romantique</strong> autour de Victor Hugo. Dès ses premiers recueils, il s'impose comme l'une des voix les plus originales du romantisme.</div>
          </div>
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text">Figure emblématique du <strong>Mal du siècle</strong> — cette mélancolie et désillusion qui touche une génération dont le désir d'absolu et d'héroïsme est brisé par les échecs successifs des révolutions (1830, 1848) et l'après-gloire napoléonienne. Musset incarne ce déchirement entre l'idéal et le réel.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text">Sa relation passionnée et orageuse avec l'écrivaine <strong>George Sand</strong> (1833–1835) le marque profondément et nourrit ses œuvres les plus célèbres. Voyage à Venise, rupture douloureuse, trahison réciproque — cet amour destructeur est au cœur d'<em>On ne badine pas avec l'amour</em> et des <em>Nuits</em>.</div>
          </div>
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text">Dramaturge novateur, il crée le genre du <strong>proverbe dramatique</strong> — pièces brèves et légères illustrant un proverbe — mais aussi des drames romantiques en prose d'une grande profondeur. Ses pièces, conçues pour la lecture plutôt que la représentation (<em>Un spectacle dans un fauteuil</em>, 1832), révolutionnent la dramaturgie.</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text">Mort le <strong>2 mai 1857</strong> à Paris, à 46 ans, usé par l'alcool et les excès. Il est entré à l'<strong>Académie française</strong> en 1852. Sa vie brève et tourmentée, sa sensibilité exacerbée et son œuvre autobiographique font de lui une figure archétypale du <strong>poète maudit</strong> romantique.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Œuvres principales</div>
        <div class="figures-grid">
          <div class="figure-card"><div class="figure-nom">Les Caprices de Marianne (1833)</div><div class="figure-ex">Comédie dramatique. Premiers signes du drame romantique mussetien.</div></div>
          <div class="figure-card"><div class="figure-nom">On ne badine pas avec l'amour (1834)</div><div class="figure-ex">Proverbe dramatique en 3 actes. Drame romantique hybride. Chef-d'œuvre.</div></div>
          <div class="figure-card"><div class="figure-nom">Confessions d'un enfant du siècle (1836)</div><div class="figure-ex">Roman autobiographique. Définit le « Mal du siècle ». Inspiré de sa rupture avec George Sand.</div></div>
          <div class="figure-card"><div class="figure-nom">Les Nuits (1835–1837)</div><div class="figure-ex">Recueil poétique. Dialogue avec la Muse. Nuit de mai, de décembre, d'août, d'octobre.</div></div>
          <div class="figure-card"><div class="figure-nom">Lorenzaccio (1834)</div><div class="figure-ex">Grand drame romantique historique, considéré comme son chef-d'œuvre théâtral.</div></div>
          <div class="figure-card"><div class="figure-nom">La Nuit de mai (1835)</div><div class="figure-ex">Poème dialogué entre le poète et la Muse. Théorisation de la douleur créatrice.</div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- FRISE MUSSET -->
  <div class="bloc">
    <div class="bloc-titre">Frise chronologique</div>
    <div class="card">
      <div class="card-section">
        <div class="frise-legende">
          <div class="legende-item"><div class="legende-dot key"></div> Création littéraire</div>
          <div class="legende-item"><div class="legende-dot war"></div> Événement historique</div>
          <div class="legende-item"><div class="legende-dot pub"></div> Publication</div>
          <div class="legende-item"><div class="legende-dot life"></div> Vie personnelle</div>
        </div>
        <div class="frise">
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">11 décembre 1810</div>
            <div class="frise-titre">Naissance à Paris</div>
            <div class="frise-desc">Naissance dans une famille cultivée du faubourg Saint-Germain. Son père est fonctionnaire et homme de lettres.</div>
          </div>
          <div class="frise-item"><div class="frise-dot key"></div>
            <div class="frise-date">1827–1828</div>
            <div class="frise-titre">Entrée dans le Cénacle</div>
            <div class="frise-desc">À 17 ans, Musset intègre le cercle romantique de Victor Hugo. Il côtoie Vigny, Sainte-Beuve, Nodier. Son génie précoce est immédiatement reconnu.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1829</div>
            <div class="frise-titre">Contes d'Espagne et d'Italie</div>
            <div class="frise-desc">Premier recueil poétique. Succès immédiat. Musset montre déjà son indépendance vis-à-vis du romantisme hugolien.</div>
          </div>
          <div class="frise-item"><div class="frise-dot war"></div>
            <div class="frise-date">Juillet 1830</div>
            <div class="frise-titre">Révolution de Juillet</div>
            <div class="frise-desc">Les Trois Glorieuses renversent Charles X. La monarchie de Juillet s'installe. La génération romantique se désillusionne face aux révolutions successives.</div>
          </div>
          <div class="frise-item"><div class="frise-dot war"></div>
            <div class="frise-date">Mars 1830</div>
            <div class="frise-titre">Bataille d'Hernani</div>
            <div class="frise-desc">La pièce de Victor Hugo déclenche un affrontement violent entre classiques et romantiques. Musset est dans le camp romantique.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1833</div>
            <div class="frise-titre">Les Caprices de Marianne</div>
            <div class="frise-desc">Premier grand drame romantique de Musset. Publication dans la <em>Revue des Deux Mondes</em>.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">1833–1835</div>
            <div class="frise-titre">Liaison avec George Sand</div>
            <div class="frise-desc">Rencontre en 1833. Voyage à Venise (1834) qui tourne au désastre : Musset tombe gravement malade, Sand le soigne puis s'éprend du médecin Pietro Pagello. Rupture douloureuse en 1835.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1834</div>
            <div class="frise-titre">On ne badine pas avec l'amour · Lorenzaccio</div>
            <div class="frise-desc">Année de sa plus grande productivité. <em>On ne badine</em> est publié dans la <em>Revue des Deux Mondes</em>. <em>Lorenzaccio</em>, considéré comme son chef-d'œuvre, paraît la même année.</div>
          </div>
          <div class="frise-item"><div class="frise-dot pub"></div>
            <div class="frise-date">1835–1837</div>
            <div class="frise-titre">Les Nuits — Confessions d'un enfant du siècle</div>
            <div class="frise-desc">Après la rupture avec Sand, Musset compose ses poèmes les plus intimes. Les <em>Nuits</em> (mai, décembre, août, octobre) et le roman autobiographique <em>Confessions</em> (1836).</div>
          </div>
          <div class="frise-item"><div class="frise-dot war"></div>
            <div class="frise-date">1848</div>
            <div class="frise-titre">Révolution de 1848</div>
            <div class="frise-desc">Nouvelle désillusion pour la génération romantique. Musset, épuisé par l'alcool, ne participe plus guère à la vie littéraire.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">1852</div>
            <div class="frise-titre">Académie française</div>
            <div class="frise-desc">Élu à l'Académie française après plusieurs tentatives, il est alors au déclin physique et créatif.</div>
          </div>
          <div class="frise-item"><div class="frise-dot life"></div>
            <div class="frise-date">2 mai 1857</div>
            <div class="frise-titre">Mort à Paris</div>
            <div class="frise-desc">Musset meurt à 46 ans, usé par les excès d'alcool. La même année, Baudelaire publie <em>Les Fleurs du Mal</em> et Flaubert, <em>Madame Bovary</em> — le réalisme succède au romantisme.</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ROMANTISME -->
  <div class="bloc">
    <div class="bloc-titre">Mouvement littéraire</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Mouvement · XIXe siècle</div>
        <div class="fiche-titre">Le Romantisme</div>
        <div class="fiche-sous">1820–1850 environ · et les Poètes maudits</div>
        <div class="tags" style="margin-top:8px;">
          <span class="tag tag-coral">Subjectivité et lyrisme</span>
          <span class="tag tag-purple">Mal du siècle</span>
          <span class="tag tag-blue">Liberté artistique</span>
          <span class="tag tag-amber">Nature et mélancolie</span>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Définition et caractéristiques</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Réaction contre le classicisme :</strong> Le romantisme naît en opposition aux règles classiques (trois unités, bienséance, raison). Il revendique la <strong>liberté totale</strong> de l'artiste : mélange des genres, des styles, des tons. Victor Hugo théorise cette révolution dans la <em>Préface de Cromwell</em> (1827).</div>
          </div>
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Le moi au centre :</strong> Contrairement au classicisme qui effaçait le « je », le romantisme place la <strong>subjectivité</strong> et le <strong>lyrisme</strong> au cœur de la création. L'auteur exprime ses émotions, ses tourments, ses doutes : <em>Méditations poétiques</em> de Lamartine (1820), <em>Les Contemplations</em> de Hugo, <em>Les Nuits</em> de Musset.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Le Mal du siècle :</strong> Sentiment caractéristique de la génération née sous Napoléon. Cette jeunesse, nourrie d'idéaux héroïques, se retrouve face à un monde décevant après les échecs révolutionnaires. D'où une <strong>mélancolie existentielle</strong>, un ennui profond (<em>spleen</em>), un désir d'absolu impossible à satisfaire.</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>La nature comme miroir de l'âme :</strong> La nature romantique est <strong>anthropomorphe</strong> — elle reflète les états intérieurs du poète. Tempêtes, ruines, nuit, automne : autant de décors qui symbolisent les tourments de l'âme. Lamartine et Hugo excellent dans ces correspondances nature/sentiment.</div>
          </div>
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>L'amour absolu et impossible :</strong> L'amour romantique est toujours marqué par le <strong>manque, la séparation ou la mort</strong>. C'est un amour idéalisé que le réel détruit toujours. Chez Musset : Perdican et Camille s'aiment mais leur orgueil les empêche de le dire — jusqu'à la tragédie.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Les grands auteurs romantiques français</div>
        <div class="symb-grid">
          <div class="symb-card"><div class="symb-titre">Victor Hugo (1802–1885)</div><div class="symb-texte">Chef de file du romantisme. Préface de Cromwell (manifeste, 1827). Hernani, Notre-Dame de Paris, Les Misérables.</div></div>
          <div class="symb-card"><div class="symb-titre">Alphonse de Lamartine (1790–1869)</div><div class="symb-texte">Premier grand poète romantique. Méditations poétiques (1820). Le Lac, fondateur du lyrisme romantique.</div></div>
          <div class="symb-card"><div class="symb-titre">Alfred de Vigny (1797–1863)</div><div class="symb-texte">Romantisme stoïque et pessimiste. Chatterton (1835), Les Destinées (posthume). Le poète face à la société.</div></div>
          <div class="symb-card"><div class="symb-titre">Alfred de Musset (1810–1857)</div><div class="symb-texte">Romantisme du cœur blessé, de l'amour impossible. On ne badine pas, Les Nuits. Le plus « maudit » des romantiques.</div></div>
          <div class="symb-card"><div class="symb-titre">Théophile Gautier (1811–1872)</div><div class="symb-texte">Lien entre romantisme et parnasse. Théorise « l'art pour l'art ». Émaux et Camées (1852).</div></div>
          <div class="symb-card"><div class="symb-titre">George Sand (1804–1876)</div><div class="symb-texte">Romancière romantique et féministe. Indiana, La Mare au Diable. Compagne de Musset et Chopin.</div></div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Les Poètes maudits — un prolongement du romantisme</div>
        <div class="info-box" style="border-left-color: var(--purple);">
          L'expression <strong>« poètes maudits »</strong> est popularisée par Verlaine dans son recueil éponyme de <strong>1884</strong>. Elle désigne des poètes marqués par une vie déréglée, marginale ou tragique, incompris de leur vivant, dont l'œuvre révolutionnaire n'est reconnue que plus tard. Ces poètes représentent la radicalisation du romantisme — la souffrance n'est plus seulement thème poétique mais mode de vie.
        </div>
        <div class="points" style="margin-top:12px;">
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>Charles Baudelaire (1821–1867) :</strong> Précurseur et figure centrale. <em>Les Fleurs du Mal</em> (1857) — procès pour immoralité. Le spleen, la beauté dans le mal, la modernité urbaine. Passerelle entre romantisme et symbolisme.</div>
          </div>
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>Paul Verlaine (1844–1896) :</strong> Blessure à Bruxelles (1873), prison. <em>Romances sans paroles, Sagesse</em>. Poésie de la musicalité, de la nuance, du demi-teinte. Auteur de l'expression « poètes maudits ».</div>
          </div>
          <div class="point"><div class="point-dot dot-amber"></div>
            <div class="point-text"><strong>Arthur Rimbaud (1854–1891) :</strong> Fugues à 16 ans, abandon de la poésie à 21. <em>Cahiers de Douai, Illuminations, Une saison en enfer</em>. La révolte absolue contre tout ordre poétique et social.</div>
          </div>
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>Stéphane Mallarmé (1842–1898) :</strong> Poésie hermétique, symboliste. <em>Un coup de dés jamais n'abolira le hasard</em>. La poésie comme quête du Beau absolu et de la Pureté du langage.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Tristan Corbière (1845–1875) :</strong> Breton marginal, incompris. <em>Les Amours jaunes</em> (1873). Poésie d'une ironie cinglante et d'un désespoir masqué par l'humour noir.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Musset : entre romantisme et poètes maudits</div>
        <div class="info-box" style="border-left-color: var(--coral);">
          Musset n'est pas à proprement parler un « poète maudit » au sens de Verlaine — il était reconnu et académicien. Mais sa vie dissolue, sa <strong>dépendance à l'alcool</strong>, son amour brisé avec George Sand, sa <strong>productivité épuisée après 35 ans</strong> et sa mort prématurée en font une figure de transition entre le romantisme et la malédiction poétique. Sa <strong>souffrance amoureuse réelle</strong> transposée en littérature (<em>On ne badine</em>, <em>Les Nuits</em>, <em>Confessions</em>) annonce le lyrisme douloureux et autobiographique des poètes maudits.
        </div>
      </div>
    </div>
  </div>

  <!-- LA PIÈCE -->
  <div class="bloc">
    <div class="bloc-titre">La pièce</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Proverbe dramatique · 1834 · Revue des Deux Mondes</div>
        <div class="fiche-titre">On ne badine pas avec l'amour</div>
        <div class="fiche-sous">3 actes · Prose · Drame romantique hybride · Parcours : « Les jeux du cœur et de la parole »</div>
        <div class="tags">
          <span class="tag tag-coral">Orgueil fatal</span>
          <span class="tag tag-purple">Drame romantique</span>
          <span class="tag tag-blue">Jeux du cœur et de la parole</span>
          <span class="tag tag-teal">Critique de la religion</span>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Contexte de création</div>
        <div class="info-box" style="border-left-color: var(--coral);">
          Musset écrit la pièce en <strong>1834</strong>, en pleine relation orageuse avec George Sand — il en aurait même intégré des extraits de leur correspondance. La pièce se positionne <strong>en faveur du drame romantique</strong> contre le théâtre classique (4 ans après la bataille d'<em>Hernani</em>). Elle n'a pas été représentée du vivant de Musset — conçue pour la lecture dans son recueil <em>Un spectacle dans un fauteuil</em>.
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Résumé par actes</div>
        <div class="plan-grid">
          <div class="plan-card">
            <div class="plan-num">Acte I</div>
            <div class="plan-titre">Les retrouvailles</div>
            <div class="plan-sous">Le Baron veut marier Perdican (son fils) et Camille (sa nièce). Les deux jeunes gens s'aimaient enfants mais Camille oppose une froideur implacable. Perdican se tourne vers Rosette (sœur de lait de Camille) pour susciter la jalousie.</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Acte II</div>
            <div class="plan-titre">Les jeux de la parole</div>
            <div class="plan-sous">Camille veut entrer au couvent, préférant l'amour divin à l'amour humain inconstant. Perdican tente de l'en dissuader. Dialogue capital (scène 5) sur l'amour et l'orgueil humain.</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Acte III</div>
            <div class="plan-titre">Le dénouement tragique</div>
            <div class="plan-sous">Perdican intercepte une lettre de Camille. Il organise un piège. Double jeu de séduction/blessure. Camille et Perdican s'avouent enfin leur amour — mais Rosette, cachée, entend tout et meurt. Camille part définitivement.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Thèmes principaux</div>
        <div class="points">
          <div class="point"><div class="point-dot dot-coral"></div>
            <div class="point-text"><strong>L'amour en trois formes :</strong> amour d'enfance sincère (Perdican et Camille), amour divin de substitution (désir de Camille de devenir religieuse), libertinage stratégique et dangereux (Perdican séduisant Rosette pour blesser Camille). Le titre avertit : l'amour n'est pas un jeu.</div>
          </div>
          <div class="point"><div class="point-dot dot-purple"></div>
            <div class="point-text"><strong>L'orgueil comme moteur tragique :</strong> Perdican, vexé par le refus de Camille, met en place un stratagème fatal à Rosette. Camille, orgueilleuse, cache ses sentiments derrière la froideur. La tirade de Perdican (II, 5) — <em>« Tous les hommes sont menteurs, inconstants, faux… »</em> — place la pièce dans le sillage des moralistes du XVIIe s. (La Rochefoucauld, Pascal).</div>
          </div>
          <div class="point"><div class="point-dot dot-teal"></div>
            <div class="point-text"><strong>La parole masque du cœur :</strong> Thème central du parcours « Les jeux du cœur et de la parole ». La parole n'est pas le miroir des sentiments : Camille dit l'inverse de ce qu'elle ressent, Perdican feint l'indifférence, les affrontements verbaux camouflent des aveux d'amour. Cette duplicité rappelle le théâtre de Marivaux.</div>
          </div>
          <div class="point"><div class="point-dot dot-blue"></div>
            <div class="point-text"><strong>Critique de la religion :</strong> Les personnages religieux sont tournés en dérision — Maître Bridaine (curé amateur de bonne chère), Dame Pluche (bigote ridicule), Camille conditionnée par le couvent. Perdican accuse le couvent d'avoir <em>« empoisonné »</em> Camille. Mais le langage de Perdican lui-même utilise la rhétorique religieuse dans ses élans lyriques.</div>
          </div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Caractéristiques du drame romantique</div>
        <div class="symb-grid">
          <div class="symb-card"><div class="symb-titre">Mélange des genres</div><div class="symb-texte">Comédie (personnages secondaires burlesques) + tragédie (mort de Rosette, séparation définitive). Hugo avait théorisé ce mélange dans la Préface de Cromwell.</div></div>
          <div class="symb-card"><div class="symb-titre">Refus des 3 unités</div><div class="symb-texte">Multiplication des lieux, liberté d'action. Rupture totale avec les contraintes classiques.</div></div>
          <div class="symb-card"><div class="symb-titre">Héros romantiques</div><div class="symb-texte">Perdican et Camille : quête d'idéal et d'absolu, sensibilité exacerbée, incapacité au bonheur. Archétypes du héros romantique.</div></div>
          <div class="symb-card"><div class="symb-titre">Prose poétique</div><div class="symb-texte">La pièce est en prose mais les répliques de Perdican (II, 5 ; III, 8) atteignent une élévation lyrique rare, comparable à des poèmes en prose.</div></div>
        </div>
      </div>
      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question" style="border-left-color: var(--coral);">En quoi cette pièce constitue-t-elle un drame romantique ?</div>
          <div class="question" style="border-left-color: var(--coral);">Comment la parole est-elle un masque des sentiments dans cette pièce ?</div>
          <div class="question" style="border-left-color: var(--coral);">Quel rôle joue l'orgueil dans la tragédie de Perdican et Camille ?</div>
          <div class="question" style="border-left-color: var(--coral);">Que signifie le titre « On ne badine pas avec l'amour » ?</div>
          <div class="question" style="border-left-color: var(--coral);">En quoi le badinage amoureux est-il dangereux dans cette pièce ?</div>
        </div>
      </div>
    </div>
  </div>

  <!-- ACTE II SCÈNE 5 -->
  <div class="bloc">
    <div class="bloc-titre">Fiche texte — Analyse linéaire</div>
    <div class="card">
      <div class="card-header">
        <div class="fiche-numero">Acte II, scène 5 · Extrait · Tirade de Perdican</div>
        <div class="fiche-titre">On ne badine pas avec l'amour — Acte II, scène 5</div>
        <div class="fiche-sous">De « Vous me faites peur… » à la fin de la scène · Analyse linéaire</div>
        <div class="tags">
          <span class="tag tag-coral">Tirade emportée</span>
          <span class="tag tag-purple">Appel à l'authenticité</span>
          <span class="tag tag-blue">Critique de la religion</span>
          <span class="tag tag-amber">Éloge de l'amour imparfait</span>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Texte de l'extrait</div>
        <div class="poeme" style="border-left-color: var(--coral); text-align:left; font-family:'Helvetica Neue',Arial,sans-serif; font-size:13px; line-height:1.9;">
          <div class="strophe">
            <strong>CAMILLE.</strong> Vous me faites peur ; la colère vous prend aussi.<br><br>
            <strong>PERDICAN.</strong> Sais-tu ce que c'est que des nonnes, malheureuse fille ? Elles qui te représentent l'amour des hommes comme un mensonge, savent-elles qu'il y a pis encore, le mensonge de l'amour divin ? Savent-elles que c'est un crime qu'elles font de venir chuchoter à une vierge des paroles de femme ? Ah ! comme elles t'ont fait la leçon ! Comme j'avais prévu tout cela quand tu t'es arrêtée devant le portrait de notre vieille tante ! Tu voulais partir sans me serrer la main ; tu ne voulais revoir ni ce bois, ni cette pauvre petite fontaine, qui nous regarde tout en larmes ; tu reniais les jours de ton enfance, et le masque de plâtre que les nonnes t'ont plaqué sur les joues me refusait un baiser de frère ; mais ton cœur a battu, il a oublié sa leçon, lui qui ne sait pas lire, et tu es revenue t'asseoir sur l'herbe où nous voilà. Eh bien ! Camille, ces femmes ont bien parlé ; elles t'ont mise dans le vrai chemin ; il pourra m'en coûter le bonheur de ma vie ; mais dis-leur cela de ma part : le ciel n'est pas pour elles.<br><br>
            <strong>CAMILLE.</strong> Ni pour moi, n'est-ce pas ?<br><br>
            <strong>PERDICAN.</strong> Adieu, Camille, retourne à ton couvent, et lorsqu'on te fera de ces récits hideux qui t'ont empoisonnée, réponds ce que je vais te dire : Tous les hommes sont menteurs, inconstants, faux, bavards, hypocrites, orgueilleux et lâches, méprisables et sensuels ; toutes les femmes sont perfides, artificieuses, vaniteuses, curieuses et dépravées ; le monde n'est qu'un égoût sans fond où les phoques les plus informes rampent et se tordent sur des montagnes de fange ; mais il y a au monde une chose sainte et sublime, c'est l'union de deux de ces êtres si imparfaits et si affreux. On est souvent trompé en amour, souvent blessé et souvent malheureux ; mais on aime, et quand on est sur le bord de sa tombe, on se retourne pour regarder en arrière, et on se dit : J'ai souffert souvent, je me suis trompé quelquefois ; mais j'ai aimé. C'est moi qui ai vécu, et non pas un être factice créé par mon orgueil et mon ennui. <em>(Il sort.)</em>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Introduction et problématique</div>
        <div class="info-box" style="border-left-color: var(--coral);">
          Dans la <strong>scène 5 de l'acte II</strong>, Camille a donné rendez-vous à Perdican pour lui annoncer sa décision de rentrer au couvent. Excédé, en fin de scène, Perdican hausse le ton et tente une dernière fois de montrer à Camille l'aspect ridicule et factice de ses arguments, forgés par les nonnes qui l'ont élevée.
          <br><br>
          <strong>Problématique :</strong> Comment Perdican, dans sa colère et son dépit, tente-t-il d'appeler Camille au courage et à la sincérité face à l'amour et à la vie ?
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Plan de l'analyse linéaire</div>
        <div class="plan-grid">
          <div class="plan-card">
            <div class="plan-num">Mouvement I</div>
            <div class="plan-titre">Perdican révolté contre une Camille qu'il ne reconnaît plus</div>
            <div class="plan-sous">A. Dénonciation de l'éducation religieuse · B. L'appel au souvenir et à l'amitié</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Mouvement II</div>
            <div class="plan-titre">Un message pour les nonnes ignorantes</div>
            <div class="plan-sous">Ironie amère · Caricature outrancière · Antiphrases et gradation</div>
          </div>
          <div class="plan-card">
            <div class="plan-num">Mouvement III</div>
            <div class="plan-titre">L'appel à la sincérité et au courage face à la vie</div>
            <div class="plan-sous">Éloge de l'amour imparfait · Présent de vérité générale · Résolution finale</div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Analyse détaillée (cliquer pour développer)</div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Mouvement I — De « Vous me faites peur » à « sur l'herbe où nous voilà »</div><div class="mvt-titre">Perdican révolté contre une Camille qu'il ne reconnaît plus</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Didascalie interne :</strong> La réplique de Camille <em>« Vous me faites peur : la colère vous prend aussi »</em> sert de didascalie interne — elle indique a posteriori le ton véhément sur lequel Perdican a prononcé sa réplique précédente.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Cascade d'interrogations en anaphore :</strong> <em>« Sais-tu… ? Savent-elles… ? Savent-elles… ? »</em> — l'anaphore du verbe <em>savoir</em> en tournure interrogative s'offusque de l'<strong>ignorance des femmes</strong>. Ton agressif, apostrophe méprisante <em>« malheureuse fille »</em>.</div>
              </div>
              <div class="point"><div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Chiasme révélateur :</strong> <em>« l'amour des hommes comme un mensonge… le mensonge de l'amour divin »</em> — le chiasme (amour/mensonge/mensonge/amour) reproduit dans la syntaxe l'<strong>enfermement</strong> auquel les mensonges des nonnes condamnent les jeunes filles. Percée de l'<strong>athéisme</strong> de Perdican.</div>
              </div>
              <div class="point"><div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Gradation accusatoire :</strong> Troisième interrogation qui, avec une gradation, accuse de <strong>« crime »</strong> ces nonnes mortifères. Opposition <em>vierge</em> (jeune fille pure) / <em>femme</em> (qui souille les imaginations de ses désillusions).</div>
              </div>
              <div class="point"><div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Énumération de reproches :</strong> Cascade rythmée par des points-virgules : <em>« Tu voulais partir… tu ne voulais revoir… tu reniais… »</em>. L'imparfait montre que Perdican a saisi dès le début les intentions de fuite de Camille.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Métaphore du masque de plâtre :</strong> <em>« le masque de plâtre que les nonnes t'ont plaqué sur les joues »</em> — Perdican n'a pas la vraie Camille devant lui mais une Camille recouverte de terreurs religieuses. Le plâtre blafard cache les vraies couleurs du visage.</div>
              </div>
              <div class="point"><div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Le cœur contre la leçon :</strong> <em>« ton cœur a battu, il a oublié sa leçon, lui qui ne sait pas lire »</em> — métonymie du cœur qui symbolise la sincérité des sentiments. Les <strong>actions</strong> trahissent la vraie Camille là où les mots la masquent.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Mouvement II — De « Eh bien ! Camille » à « montagnes de fange »</div><div class="mvt-titre">Un message pour les nonnes ignorantes et malfaisantes</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Antiphones amères :</strong> <em>« Eh bien ! Camille, ces femmes ont bien parlé ; elles t'ont mise dans le vrai chemin »</em> — antiphrases ponctuées d'interjections. Le déterminant démonstratif <em>« ces femmes »</em> véhicule distance et mépris.</div>
              </div>
              <div class="point"><div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Périphrase hyperbolique :</strong> <em>« le bonheur de ma vie »</em> désigne la relation amoureuse espérée avec Camille — Perdican révèle ainsi la <strong>sincérité de ses sentiments</strong>, qu'il cachait derrière la colère.</div>
              </div>
              <div class="point"><div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Sentence :</strong> <em>« le ciel n'est pas pour elles »</em> — Perdican renverse le discours des religieuses et affirme péremptoirement que leur renoncement à l'amour les prive du bonheur véritable.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Caricature outrancière — anaphore de « tous » :</strong> <em>« Tous les hommes sont menteurs, inconstants, faux, bavards, hypocrites, orgueilleux et lâches… toutes les femmes sont perfides, artificieuses… »</em> — <strong>généralisation outrancière</strong> avec cascade d'adjectifs, voulue pour montrer l'absurdité de la vision du monde enseignée par les nonnes.</div>
              </div>
              <div class="point"><div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Métaphore de l'égout :</strong> <em>« le monde n'est qu'un égoût sans fond où les phoques les plus informes rampent et se tordent sur des montagnes de fange »</em> — négation restrictive, image volontairement repoussante. Perdican pousse le raisonnement des nonnes jusqu'à son terme absurde pour en montrer le <strong>ridicule</strong>.</div>
              </div>
            </div>
          </div>
        </div>

        <div class="mvt">
          <div class="mvt-header" onclick="toggleMvt(this)">
            <div><div class="mvt-num">Mouvement III — De « mais il y a au monde… » à la fin</div><div class="mvt-titre">L'appel à la sincérité et au courage face à la vie</div></div>
            <span class="mvt-arrow">▼</span>
          </div>
          <div class="mvt-body">
            <div class="points">
              <div class="point"><div class="point-dot dot-purple"></div>
                <div class="point-text"><strong>Retournement par « mais » :</strong> La conjonction d'opposition introduit le renversement : après le tableau écœurant du monde, Perdican affirme paradoxalement la <strong>sainteté de l'amour terrestre</strong> : <em>« il y a au monde une chose sainte et sublime, c'est l'union de deux de ces êtres si imparfaits et si affreux »</em>.</div>
              </div>
              <div class="point"><div class="point-dot dot-coral"></div>
                <div class="point-text"><strong>Vocabulaire religieux détourné :</strong> <em>« sainte et sublime »</em> — Perdican utilise paradoxalement le registre religieux pour qualifier l'<strong>amour charnel et humain</strong>, retournant ainsi les armes de l'Église contre elle-même.</div>
              </div>
              <div class="point"><div class="point-dot dot-amber"></div>
                <div class="point-text"><strong>Présent de vérité générale + pronom « on » :</strong> <em>« On est souvent trompé en amour, souvent blessé et souvent malheureux ; mais on aime »</em> — la répétition de l'adverbe <em>« souvent »</em> et le pronom universel <em>« on »</em> transforment l'expérience personnelle en <strong>vérité humaine universelle</strong>.</div>
              </div>
              <div class="point"><div class="point-dot dot-teal"></div>
                <div class="point-text"><strong>Perspective de la mort :</strong> <em>« quand on est sur le bord de sa tombe, on se retourne pour regarder en arrière »</em> — Perdican place le débat sous l'angle de la mort : seul compte ce qu'on aura vécu, non ce qu'on aura craint. L'amour, même douloureux, est la preuve qu'on a vraiment existé.</div>
              </div>
              <div class="point"><div class="point-dot dot-blue"></div>
                <div class="point-text"><strong>Opposition vivre / être factice :</strong> <em>« C'est moi qui ai vécu, et non pas un être factice créé par mon orgueil et mon ennui »</em> — dernier mot cinglant qui vise directement Camille et son refus masqué par l'orgueil. Le mot <em>factice</em> renvoie au <strong>masque de plâtre</strong> du début, bouclant la tirade.</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Figures de style à retenir</div>
        <div class="figures-grid">
          <div class="figure-card"><div class="figure-nom">Didascalie interne</div><div class="figure-ex">Réplique de Camille indique le ton de Perdican</div></div>
          <div class="figure-card"><div class="figure-nom">Anaphore</div><div class="figure-ex">« Savent-elles… ? » · « Tous les hommes… toutes les femmes »</div></div>
          <div class="figure-card"><div class="figure-nom">Chiasme</div><div class="figure-ex">amour/mensonge ↔ mensonge/amour → enfermement des nonnes</div></div>
          <div class="figure-card"><div class="figure-nom">Métaphore du masque</div><div class="figure-ex">« masque de plâtre plaqué sur les joues » → Camille masquée</div></div>
          <div class="figure-card"><div class="figure-nom">Métonymie du cœur</div><div class="figure-ex">« ton cœur a battu » → sincérité des sentiments</div></div>
          <div class="figure-card"><div class="figure-nom">Antiphrase + ironie</div><div class="figure-ex">« elles t'ont mise dans le vrai chemin » → ironie amère</div></div>
          <div class="figure-card"><div class="figure-nom">Gradation d'adjectifs</div><div class="figure-ex">« menteurs, inconstants, faux, bavards… » → caricature</div></div>
          <div class="figure-card"><div class="figure-nom">Métaphore de l'égout</div><div class="figure-ex">Le monde = égout → vision des nonnes poussée à l'absurde</div></div>
          <div class="figure-card"><div class="figure-nom">Vocabulaire religieux détourné</div><div class="figure-ex">« sainte et sublime » → pour qualifier l'amour charnel</div></div>
          <div class="figure-card"><div class="figure-nom">Présent de vérité générale</div><div class="figure-ex">« On est souvent trompé… mais on aime » → universalité</div></div>
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Conclusion</div>
        <div class="info-box" style="border-left-color: var(--coral);">
          Cette tirade constitue le <strong>cœur philosophique</strong> de la pièce. Perdican y développe une véritable <strong>apologie de l'amour imparfait</strong> contre l'idéalisme mortifère du couvent. Sa rhétorique progresse en trois temps : colère et dénonciation → caricature absurde → éloge courageux de l'amour. La <strong>chute</strong> — <em>« C'est moi qui ai vécu »</em> — est d'autant plus cruelle qu'elle désigne implicitement Camille comme un <em>être factice</em>. Mais l'ironie tragique est que Perdican lui-même, en voulant blesser Camille avec Rosette, trahit bientôt les valeurs qu'il vient de défendre.
          <br><br>
          <strong>Ouvertures :</strong> Le discours de Valère dans <em>L'Avare</em> de Molière (flatterie et sincérité) · La tirade de Cyrano de Bergerac sur le nez (diatribe retournée en éloge) · Rousseau, <em>La Nouvelle Héloïse</em> (l'amour vertueux contre la société).
        </div>
      </div>

      <div class="card-section">
        <div class="section-label">Questions possibles à l'oral</div>
        <div class="questions">
          <div class="question" style="border-left-color: var(--coral);">Comment Perdican appelle-t-il Camille au courage face à l'amour ?</div>
          <div class="question" style="border-left-color: var(--coral);">En quoi cette tirade est-elle une critique de l'éducation religieuse ?</div>
          <div class="question" style="border-left-color: var(--coral);">Quel est l'effet de la caricature outrancière dans le discours de Perdican ?</div>
          <div class="question" style="border-left-color: var(--coral);">Comment la tirade progresse-t-elle vers l'éloge de l'amour imparfait ?</div>
          <div class="question" style="border-left-color: var(--coral);">En quoi le mot final « factice » résume-t-il le reproche de Perdican à Camille ?</div>
        </div>
      </div>
    </div>
  </div>

</div><!-- /container -->
</div><!-- /panel-on-ne-badine -->

<!-- =================== PANEL : AUTRES =================== -->
<div id="panel-autres" class="tab-panel">

  <!-- SOUS-ONGLETS -->
  <div class="inner-tab-bar">
    <div class="inner-tab-inner">
      <button class="inner-tab-btn active" onclick="switchInner('lafontaine', this)">La Fontaine</button>
      <button class="inner-tab-btn" onclick="switchInner('proust', this)">Proust</button>
    </div>
  </div>

  <!-- ===== LA FONTAINE ===== -->
  <div id="inner-lafontaine" class="inner-panel active">
  <div class="container">

    <div class="page-header">
      <div class="surtitre">Fables · Bac de français</div>
      <h1>Jean de La Fontaine</h1>
      <div class="sub">Fiches de révision · Auteur · Classicisme · Le Loup et le Chien</div>
    </div>

    <!-- AUTEUR -->
    <div class="bloc">
      <div class="bloc-titre">L'auteur</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Fiche auteur</div>
          <div class="fiche-titre">Jean de La Fontaine (1621–1695)</div>
          <div class="fiche-sous">Poète français · XVIIe siècle · Fabuliste · Classicisme</div>
          <div class="tags" style="margin-top:8px;">
            <span class="tag tag-amber">Classicisme</span>
            <span class="tag tag-teal">Fables</span>
            <span class="tag tag-blue">Morale implicite</span>
            <span class="tag tag-coral">Critique sociale</span>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Portrait</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-amber"></div>
              <div class="point-text">Né le <strong>8 juillet 1621</strong> à Château-Thierry (Champagne). Fils d'un maître des eaux et forêts, il grandit entouré de la nature, qui nourrira abondamment son imaginaire poétique.</div>
            </div>
            <div class="point"><div class="point-dot dot-blue"></div>
              <div class="point-text">Protégé du surintendant <strong>Nicolas Fouquet</strong>, puis de la duchesse de Bouillon et de Madame de La Sablière. Il fréquente les salons littéraires parisiens et côtoie Molière, Racine et Boileau dans le cercle des grands auteurs classiques.</div>
            </div>
            <div class="point"><div class="point-dot dot-coral"></div>
              <div class="point-text">Auteur d'une œuvre très diverse (contes, poèmes, pièces de théâtre), il reste surtout célèbre pour ses <strong>Fables</strong> — 243 fables réparties en 12 livres publiés de 1668 à 1694 — qui lui assurent une postérité universelle.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text">Il s'inspire principalement des fabulistes grecs <strong>Ésope</strong> (VIe s. av. J.-C.) et romain <strong>Phèdre</strong> (Ier s. ap. J.-C.) dont il réinvente les apologues avec une élégance, une ironie et une profondeur psychologique entièrement nouvelles.</div>
            </div>
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text">Élu à l'<strong>Académie française</strong> en 1684. Mort le <strong>13 avril 1695</strong> à Paris. La devise qu'il s'est choisie résume son art : <em>« diversité c'est ma devise »</em>.</div>
            </div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Œuvres principales</div>
          <div class="figures-grid">
            <div class="figure-card"><div class="figure-nom">Fables I–VI (1668)</div><div class="figure-ex">Premiers livres dédiés au Dauphin. Contiennent La Cigale et la Fourmi, Le Loup et le Chien, Le Corbeau et le Renard.</div></div>
            <div class="figure-card"><div class="figure-nom">Fables VII–XI (1678–1679)</div><div class="figure-ex">Livres plus sombres et complexes. Contiennent Les Animaux malades de la peste, Le Pouvoir des fables.</div></div>
            <div class="figure-card"><div class="figure-nom">Fables XII (1694)</div><div class="figure-ex">Dernier livre, le plus philosophique et mélancolique, dédié au duc de Bourgogne.</div></div>
            <div class="figure-card"><div class="figure-nom">Contes et nouvelles (1664–1685)</div><div class="figure-ex">Œuvres plus licencieuses, inspirées de Boccace et de l'Arioste.</div></div>
          </div>
        </div>
      </div>
    </div>

    <!-- FRISE -->
    <div class="bloc">
      <div class="bloc-titre">Frise chronologique</div>
      <div class="card">
        <div class="card-section">
          <div class="frise-legende">
            <div class="legende-item"><div class="legende-dot key"></div> Création littéraire</div>
            <div class="legende-item"><div class="legende-dot war"></div> Événement historique</div>
            <div class="legende-item"><div class="legende-dot pub"></div> Publication</div>
            <div class="legende-item"><div class="legende-dot life"></div> Vie personnelle</div>
          </div>
          <div class="frise">
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">8 juillet 1621</div>
              <div class="frise-titre">Naissance à Château-Thierry</div>
              <div class="frise-desc">Naissance dans une famille de la bourgeoisie provinciale. Son père est maître des eaux et forêts.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1647</div>
              <div class="frise-titre">Mariage</div>
              <div class="frise-desc">Il épouse Marie Héricart. Le mariage sera malheureux ; ils vivront séparément dès 1658.</div>
            </div>
            <div class="frise-item"><div class="frise-dot war"></div>
              <div class="frise-date">1643–1715</div>
              <div class="frise-titre">Règne de Louis XIV</div>
              <div class="frise-desc">La Fontaine écrit sous le règne du Roi-Soleil. Ses fables critiquent subtilement la cour, la flatterie et l'absolutisme, à l'abri du masque animal.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1658–1661</div>
              <div class="frise-titre">Sous la protection de Fouquet</div>
              <div class="frise-desc">Le surintendant Fouquet devient son mécène. La Fontaine lui dédie son <em>Adonis</em>. À la chute de Fouquet (1661), il prend courageusement sa défense dans son <em>Élégie aux nymphes de Vaux</em>.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1668</div>
              <div class="frise-titre">Fables I–VI</div>
              <div class="frise-desc">Publication des six premiers livres de Fables, dédiés au jeune Dauphin. Succès immédiat. La Cigale et la Fourmi, Le Corbeau et le Renard, Le Loup et le Chien y figurent.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1672</div>
              <div class="frise-titre">Accueilli par Mme de La Sablière</div>
              <div class="frise-desc">La Fontaine vit chez Mme de La Sablière pendant vingt ans. Ce foyer lui offre stabilité et inspiration.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1678–1679</div>
              <div class="frise-titre">Fables VII–XI</div>
              <div class="frise-desc">Deuxième recueil. Ton plus grave et philosophique. Les Animaux malades de la peste, Le Pouvoir des fables.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1684</div>
              <div class="frise-titre">Académie française</div>
              <div class="frise-desc">Élu à l'Académie française après deux tentatives infructueuses (Racine lui avait été préféré).</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1694</div>
              <div class="frise-titre">Fables XII</div>
              <div class="frise-desc">Dernier livre de Fables, plus mélancolique. La Fontaine a 73 ans. Il meurt un an plus tard.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">13 avril 1695</div>
              <div class="frise-titre">Mort à Paris</div>
              <div class="frise-desc">La Fontaine meurt à Paris à 73 ans, après une conversion tardive au catholicisme. Il est enterré au cimetière des Saints-Innocents.</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- CLASSICISME -->
    <div class="bloc">
      <div class="bloc-titre">Mouvement littéraire</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Mouvement · XVIIe siècle</div>
          <div class="fiche-titre">Le Classicisme</div>
          <div class="fiche-sous">1660–1685 environ · Règne de Louis XIV</div>
          <div class="tags" style="margin-top:8px;">
            <span class="tag tag-amber">Raison et ordre</span>
            <span class="tag tag-blue">Imitation des Anciens</span>
            <span class="tag tag-teal">Plaire et instruire</span>
            <span class="tag tag-purple">Bienséance</span>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Définition et contexte</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-amber"></div>
              <div class="point-text"><strong>Contexte :</strong> Le classicisme naît sous le règne absolu de Louis XIV. La centralisation politique se traduit par une <strong>centralisation esthétique</strong> : le roi contrôle les arts, les académies régulent la langue et la littérature, et l'idéal de <strong>grandeur et d'ordre</strong> domine toute création.</div>
            </div>
            <div class="point"><div class="point-dot dot-blue"></div>
              <div class="point-text"><strong>Imitation des Anciens :</strong> Les classiques s'inspirent des auteurs grecs (Aristote, Sophocle, Homère) et latins (Virgile, Ovide, Horace). La Fontaine s'inspire d'Ésope et Phèdre ; Racine reprend les tragédies grecques ; Molière s'inspire de Plaute et Térence.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text"><strong>« Plaire et instruire » :</strong> La double finalité de l'œuvre classique, formulée par Horace (<em>aut prodesse aut delectare</em>). L'apologue (fable) est la forme idéale : il instruit par la morale tout en plaisant par le récit.</div>
            </div>
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text"><strong>La bienséance :</strong> Règle fondamentale du classicisme — ne pas choquer le public. Tout ce qui est excessif, violent ou grossier doit être atténué ou suggéré. C'est pourquoi La Fontaine critique le pouvoir par le biais d'animaux plutôt que directement.</div>
            </div>
            <div class="point"><div class="point-dot dot-coral"></div>
              <div class="point-text"><strong>Les trois unités (théâtre) :</strong> Unité de temps (24h), de lieu (un seul endroit), d'action (une seule intrigue principale). Ces règles s'appliquent à la tragédie et à la comédie classiques.</div>
            </div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Les grands auteurs classiques</div>
          <div class="symb-grid">
            <div class="symb-card"><div class="symb-titre">Jean de La Fontaine (1621–1695)</div><div class="symb-texte">Fables. Critique sociale et politique par le biais de l'apologue animal.</div></div>
            <div class="symb-card"><div class="symb-titre">Molière (1622–1673)</div><div class="symb-texte">Comédie classique. L'Avare, Le Misanthrope, Dom Juan. Critique des mœurs.</div></div>
            <div class="symb-card"><div class="symb-titre">Jean Racine (1639–1699)</div><div class="symb-texte">Tragédie classique. Phèdre, Andromaque, Britannicus. Peinture des passions.</div></div>
            <div class="symb-card"><div class="symb-titre">Nicolas Boileau (1636–1711)</div><div class="symb-texte">Théoricien du classicisme. L'Art poétique (1674) fixe les règles de la littérature classique.</div></div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">La Fontaine et le classicisme</div>
          <div class="info-box" style="border-left-color: var(--amber);">
            La Fontaine est <strong>classique par la forme</strong> (vers, rigueur, clarté, morale) mais <strong>libre par l'esprit</strong> : il mélange les genres (épique, lyrique, dramatique dans une même fable), use d'une métrique très variée (octosyllabes, décasyllabes, alexandrins dans la même fable), et critique subtilement le pouvoir de Louis XIV. Sa devise, <em>« diversité c'est ma devise »</em>, le distingue de la rigueur stricte d'un Boileau.
          </div>
        </div>
      </div>
    </div>

    <!-- LE LOUP ET LE CHIEN -->
    <div class="bloc">
      <div class="bloc-titre">Fiche poème — Fables I, 5</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Fable I, 5 · Fables Livres I–VI (1668)</div>
          <div class="fiche-titre">Le Loup et le Chien</div>
          <div class="fiche-sous">41 vers · Mètres variés · Dialogue · Apologue · Morale implicite</div>
          <div class="tags">
            <span class="tag tag-amber">Liberté vs confort</span>
            <span class="tag tag-coral">Critique de la flatterie</span>
            <span class="tag tag-blue">Apologue</span>
            <span class="tag tag-teal">Morale implicite</span>
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Texte de la fable</div>
          <div class="poeme" style="border-left-color: var(--amber); line-height: 2; font-size: 13px;">
            <div class="strophe">
              Un Loup n'avait que les os et la peau,<br>
              Tant les chiens faisaient bonne garde.<br>
              Ce Loup rencontre un Dogue aussi puissant que beau,<br>
              Gras, poli, qui s'était fourvoyé par mégarde.<br>
              L'attaquer, le mettre en quartiers,<br>
              Sire Loup l'eût fait volontiers ;<br>
              Mais il fallait livrer bataille,<br>
              Et le Mâtin était de taille<br>
              À se défendre hardiment.<br>
              Le Loup donc l'aborde humblement,<br>
              Entre en propos, et lui fait compliment<br>
              Sur son embonpoint qu'il admire.<br>
              « Il ne tiendra qu'à vous beau Sire,<br>
              D'être aussi gras que moi, lui repartit le Chien.<br>
              Quittez les bois, vous ferez bien :<br>
              Vos pareils y sont misérables,<br>
              Cancres, hères, et pauvres diables,<br>
              Dont la condition est fort misérable.<br>
              Car quoi ? rien d'assuré ; point de franche lippée ;<br>
              Tout à la pointe de l'épée.<br>
              Suivez-moi : vous aurez un bien meilleur destin. »<br>
              Le Loup reprit : « Que me faudra-t-il faire ?<br>
              — Presque rien, dit le Chien ; donner la chasse aux gens<br>
              Portants bâtons, et mendiants ;<br>
              Flatter ceux du logis, à son Maître complaire :<br>
              Moyennant quoi votre salaire<br>
              Sera force reliefs de toutes les façons :<br>
              Os de poulets, os de pigeons,<br>
              Sans parler de mainte caresse. »<br>
              Le Loup déjà se forge une félicité<br>
              Qui le fait pleurer de tendresse.<br>
              Chemin faisant, il vit le col du Chien pelé.<br>
              « Qu'est-ce là ? lui dit-il. — Rien. — Quoi ? rien ? — Peu de chose.<br>
              — Mais encor ? — Le collier dont je suis attaché<br>
              De ce que vous voyez est peut-être la cause.<br>
              — Attaché ? dit le Loup : vous ne courez donc pas<br>
              Où vous voulez ? — Pas toujours ; mais qu'importe ?<br>
              — Il importe si bien, que de tous vos repas<br>
              Je ne veux en aucune sorte,<br>
              Et ne voudrais pas même à ce prix un trésor. »<br>
              Cela dit, maître Loup s'enfuit, et court encor.
            </div>
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Introduction et problématique</div>
          <div class="info-box" style="border-left-color: var(--amber);">
            Cette fable figure dans le <strong>Livre I</strong> des <em>Fables</em> de La Fontaine, publiées en 1668. Inspirée d'Ésope, elle met en scène un loup affamé et un chien bien nourri. À travers ce dialogue vivant, La Fontaine pose la question de la <strong>liberté face au confort</strong> et critique subtilement <strong>la flatterie et la servilité</strong> à la cour de Louis XIV.
            <br><br>
            <strong>Problématique :</strong> En quoi cette fable constitue-t-elle un apologue efficace pour dénoncer la flatterie et défendre la liberté ?
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Plan du commentaire composé</div>
          <div class="plan-grid">
            <div class="plan-card"><div class="plan-num">Partie I</div><div class="plan-titre">Un récit vivant</div><div class="plan-sous">A. Caractéristiques du récit · B. Deux personnages opposés haut en couleur</div></div>
            <div class="plan-card"><div class="plan-num">Partie II</div><div class="plan-titre">La stratégie argumentative du chien</div><div class="plan-sous">A. L'argumentation du chien · B. Une argumentation convaincante</div></div>
            <div class="plan-card"><div class="plan-num">Partie III</div><div class="plan-titre">Le retournement de situation</div><div class="plan-sous">A. La chute du récit · B. Une morale implicite</div></div>
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Analyse détaillée (cliquer pour développer)</div>

          <div class="mvt">
            <div class="mvt-header" onclick="toggleMvt(this)">
              <div><div class="mvt-num">Partie I</div><div class="mvt-titre">Un récit vivant</div></div>
              <span class="mvt-arrow">▼</span>
            </div>
            <div class="mvt-body">
              <div class="points">
                <div class="point"><div class="point-dot dot-amber"></div>
                  <div class="point-text"><strong>Structure narrative complète :</strong> situation initiale (loup maigre, v.1–2) → élément perturbateur (rencontre du chien, v.2) → développement (dialogue, v.10–31) → dénouement (cou pelé révélé, v.32–40) → situation finale (fuite du loup, v.41). La fable possède toutes les caractéristiques d'un récit classique.</div>
                </div>
                <div class="point"><div class="point-dot dot-blue"></div>
                  <div class="point-text"><strong>Dynamisme formel :</strong> dialogues au style direct et indirect, <strong>métrique variée</strong> (décasyllabe, alexandrin, octosyllabe dans la même fable), rimes alternées (ABAB), suivies (AABB) et embrassées (ABBA). Cette diversité crée un rythme vivant et naturel.</div>
                </div>
                <div class="point"><div class="point-dot dot-coral"></div>
                  <div class="point-text"><strong>Opposition physique :</strong> le loup n'a <span class="citation">« que les os et la peau »</span> (locution restrictive) ; le chien est <span class="citation">« aussi puissant que beau, gras, poli »</span> (énumération et enjambement v.3–4, champ lexical de la bonne chère).</div>
                </div>
                <div class="point"><div class="point-dot dot-teal"></div>
                  <div class="point-text"><strong>Opposition psychologique :</strong> le loup est féroce mais intelligent — son premier réflexe est d'attaquer (<strong>allitération en [k]</strong> : <span class="citation">« l'attaquer, le mettre en quartiers »</span> — consonne explosive mimant la violence) mais il adopte une stratégie de flatterie. Le chien est affable et présomptueux, son adjectif <span class="citation">« poli »</span> (v.4) a un double sens : poil lisse et bien élevé.</div>
                </div>
              </div>
            </div>
          </div>

          <div class="mvt">
            <div class="mvt-header" onclick="toggleMvt(this)">
              <div><div class="mvt-num">Partie II</div><div class="mvt-titre">La stratégie argumentative du chien</div></div>
              <span class="mvt-arrow">▼</span>
            </div>
            <div class="mvt-body">
              <div class="points">
                <div class="point"><div class="point-dot dot-coral"></div>
                  <div class="point-text"><strong>Temps de parole prépondérant :</strong> le chien argumente du v.13 au v.30 — son orgueil transpiraît dans ce <strong>monologue flatteur</strong>. Il emploie l'impératif directif (<span class="citation">« quittez les bois »</span>, <span class="citation">« suivez-moi »</span>) pour guider le loup.</div>
                </div>
                <div class="point"><div class="point-dot dot-blue"></div>
                  <div class="point-text"><strong>Série d'antithèses :</strong> <span class="citation">« misérables, cancres, hères et pauvres diables »</span> s'oppose à <span class="citation">« bien meilleur destin », « os de poulets, os de pigeons », « mainte caresse »</span>. Le champ lexical de l'abondance (salaire, reliefs, os, caresses) contraste avec celui de la misère du loup.</div>
                </div>
                <div class="point"><div class="point-dot dot-amber"></div>
                  <div class="point-text"><strong>Sonorités de la flatterie :</strong> quand le loup amadoue le chien, les allitérations deviennent douces — <strong>allitérations en [m] et [l]</strong> et <strong>assonances en nasales</strong> [on/en/un] : <em>« l'aborde h<strong>um</strong>blement, entre en propos, et lui fait c<strong>om</strong>pliment, sur son <strong>em</strong>b<strong>on</strong>p<strong>oin</strong>t »</em> → le ton mielleux est mimé phonétiquement.</div>
                </div>
                <div class="point"><div class="point-dot dot-teal"></div>
                  <div class="point-text"><strong>Un loup métamorphosé :</strong> l'argumentation du chien est si efficace que le loup <span class="citation">« se forge une félicité qui le fait pleurer de tendresse »</span> (v.30–31) — de cruel, il est presque devenu doux comme un agneau. Effet comique et préparation de la chute.</div>
                </div>
              </div>
            </div>
          </div>

          <div class="mvt">
            <div class="mvt-header" onclick="toggleMvt(this)">
              <div><div class="mvt-num">Partie III</div><div class="mvt-titre">Le retournement de situation</div></div>
              <span class="mvt-arrow">▼</span>
            </div>
            <div class="mvt-body">
              <div class="points">
                <div class="point"><div class="point-dot dot-coral"></div>
                  <div class="point-text"><strong>La chute :</strong> <span class="citation">« Chemin faisant, il vit le col du Chien pelé »</span> (v.32). Le passé simple <em>« vit »</em> et le point final à la fin du vers soulignent le choc soudain. Le col pelé par le collier révèle la <strong>servitude cachée</strong> derrière le confort.</div>
                </div>
                <div class="point"><div class="point-dot dot-blue"></div>
                  <div class="point-text"><strong>Dialogue saccadé :</strong> <span class="citation">« Rien. — Quoi ? rien ? — Peu de chose. / — Mais encor ? »</span> — répliques nominales et brèves, souvent en rejet en début de vers, questions interrogatives du loup. Son discours se fait haché, comme s'il s'étranglait d'indignation.</div>
                </div>
                <div class="point"><div class="point-dot dot-teal"></div>
                  <div class="point-text"><strong>Le mot de la fin appartient au loup :</strong> <span class="citation">« de tous vos repas / Je ne veux en aucune sorte, / Et ne voudrais pas même à ce prix un trésor. »</span> — réponse cinglante. La Fontaine lui donne le dernier mot et accorde ses pensées intimes tout au long du récit : c'est sa <strong>préférence implicite</strong> pour le loup.</div>
                </div>
                <div class="point"><div class="point-dot dot-amber"></div>
                  <div class="point-text"><strong>Morale implicite :</strong> la morale n'est pas formulée explicitement — elle se déduit du récit : <em>mieux vaut être libre et affamé que riche et asservi</em>. Les animaux sont allégoriques : le chien représente les courtisans flatteurs de Louis XIV qui sacrifient leur liberté au confort, le loup représente l'indépendance d'esprit.</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Figures de style à retenir</div>
          <div class="figures-grid">
            <div class="figure-card"><div class="figure-nom">Allitération en [k]</div><div class="figure-ex">« l'attaquer, le mettre en quartiers » → violence du loup</div></div>
            <div class="figure-card"><div class="figure-nom">Allitération en [m][l] + nasales</div><div class="figure-ex">« humblement, compliment, embonpoint » → ton mielleux</div></div>
            <div class="figure-card"><div class="figure-nom">Antithèse</div><div class="figure-ex">misère du loup / abondance du chien → opposition des deux modes de vie</div></div>
            <div class="figure-card"><div class="figure-nom">Locution restrictive</div><div class="figure-ex">« ne…que les os et la peau » → maigreur extrême du loup</div></div>
            <div class="figure-card"><div class="figure-nom">Double sens</div><div class="figure-ex">« poli » → poil lisse ET bien élevé</div></div>
            <div class="figure-card"><div class="figure-nom">Morale implicite</div><div class="figure-ex">Liberté > confort — déduite du récit, non formulée</div></div>
            <div class="figure-card"><div class="figure-nom">Allégorie</div><div class="figure-ex">Chien = courtisan flatteur · Loup = esprit libre</div></div>
            <div class="figure-card"><div class="figure-nom">Métrique variée</div><div class="figure-ex">Octosyllabes, décasyllabes, alexandrins mêlés → dynamisme</div></div>
          </div>
        </div>

        <div class="card-section">
          <div class="section-label">Questions possibles à l'oral</div>
          <div class="questions">
            <div class="question" style="border-left-color: var(--amber);">En quoi cette fable constitue-t-elle un apologue ?</div>
            <div class="question" style="border-left-color: var(--amber);">Que La Fontaine critique-t-il dans cette fable ?</div>
            <div class="question" style="border-left-color: var(--amber);">Étudiez les stratégies argumentatives dans cette fable.</div>
            <div class="question" style="border-left-color: var(--amber);">Que représentent les personnages de cette fable ?</div>
            <div class="question" style="border-left-color: var(--amber);">Comment La Fontaine défend-il implicitement la liberté ?</div>
          </div>
        </div>
      </div>
    </div>

  </div><!-- /container lafontaine -->
  </div><!-- /inner-lafontaine -->

  <!-- ===== PROUST ===== -->
  <div id="inner-proust" class="inner-panel">
  <div class="container">

    <div class="page-header">
      <div class="surtitre">À la recherche du temps perdu · Bac de français</div>
      <h1>Marcel Proust</h1>
      <div class="sub">Fiches de révision · Auteur · Frise · La Recherche · Modernisme</div>
    </div>

    <!-- AUTEUR PROUST -->
    <div class="bloc">
      <div class="bloc-titre">L'auteur</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Fiche auteur</div>
          <div class="fiche-titre">Marcel Proust (1871–1922)</div>
          <div class="fiche-sous">Romancier français · XXe siècle · Modernisme · Mémoire involontaire</div>
          <div class="tags" style="margin-top:8px;">
            <span class="tag tag-purple">Modernisme</span>
            <span class="tag tag-blue">Mémoire involontaire</span>
            <span class="tag tag-teal">Roman-fleuve</span>
            <span class="tag tag-amber">Belle Époque</span>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Portrait</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text">Né le <strong>10 juillet 1871</strong> à Auteuil (Paris). Son père est un célèbre médecin hygiéniste, sa mère est issue d'une riche famille juive. Cette double appartenance sociale et religieuse nourrit sa sensibilité aux questions d'identité, de milieu et d'exclusion sociale.</div>
            </div>
            <div class="point"><div class="point-dot dot-coral"></div>
              <div class="point-text">Enfant <strong>asthmatique et hypersensible</strong>, il développe très tôt une relation fusionnelle avec sa mère et un rapport douloureux au temps et à la séparation. La maladie l'oblige à vivre, dans les dernières années de sa vie, dans une <strong>chambre entièrement calfeutrée au liège</strong> pour se protéger du bruit et des odeurs déclenchant ses crises.</div>
            </div>
            <div class="point"><div class="point-dot dot-blue"></div>
              <div class="point-text">Jeune homme mondain, il fréquente assidûment les <strong>salons parisiens de la haute société</strong> (faubourg Saint-Germain, milieux aristocratiques et bourgeois) dont il tire la matière de son œuvre. Les Guermantes, les Verdurin et Swann sont des portraits composites inspirés de personnages réels qu'il a côtoyés.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text">Il traduit l'esthète anglais <strong>John Ruskin</strong> (<em>La Bible d'Amiens</em>, 1904 ; <em>Sésame et les Lys</em>, 1906), ce qui affine profondément sa philosophie de la perception sensible et de la beauté. Cette expérience prépare directement la rédaction de <em>La Recherche</em>.</div>
            </div>
            <div class="point"><div class="point-dot dot-amber"></div>
              <div class="point-text">À partir de <strong>1909</strong>, il se retire définitivement du monde mondain et se consacre entièrement à son grand œuvre. Il travaille souvent la nuit, depuis son lit, dictant ou corrigeant sur des cahiers. Il ajoute des développements considérables jusqu'à sa mort, si bien que l'œuvre dépasse les 3 000 pages.</div>
            </div>
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text">Mort le <strong>18 novembre 1922</strong> à Paris d'une pneumonie aggravée par son asthme. Il n'avait pas achevé la révision des derniers tomes. Son frère Robert publiera les volumes posthumes. Proust aura consacré les treize dernières années de sa vie, en quasi-réclusion, à son unique chef-d'œuvre.</div>
            </div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">La mémoire involontaire — concept fondamental</div>
          <div class="info-box" style="border-left-color: var(--purple);">
            Au cœur de l'œuvre de Proust se trouve la notion de <strong>mémoire involontaire</strong> : une sensation présente (un goût, une odeur, une musique, une texture) peut déclencher involontairement et soudainement le souvenir vivant d'un passé perdu, avec une intensité et une plénitude que la mémoire volontaire — celle qui "cherche" — ne peut jamais atteindre.
            <br><br>
            L'exemple le plus célèbre : une <strong>madeleine trempée dans du thé</strong> fait resurgir spontanément le village de <strong>Combray</strong> tout entier, avec ses sons, ses odeurs, ses lumières — comme si le temps avait été aboli. Pour Proust, c'est la seule façon de <strong>vaincre le temps qui passe et efface</strong> : non pas en résistant à sa fuite, mais en le retrouvant intact dans la sensation présente. Le projet de <em>La Recherche</em> est de comprendre ces expériences et d'en faire la matière d'une œuvre d'art.
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Les 7 volumes d'À la recherche du temps perdu</div>
          <div class="figures-grid">
            <div class="figure-card"><div class="figure-nom">1. Du côté de chez Swann (1913)</div><div class="figure-ex">La madeleine, Combray, l'amour de Swann pour Odette, le côté de Méséglise.</div></div>
            <div class="figure-card"><div class="figure-nom">2. À l'ombre des jeunes filles en fleurs (1919)</div><div class="figure-ex">Prix Goncourt. L'adolescence, Balbec, la rencontre d'Albertine.</div></div>
            <div class="figure-card"><div class="figure-nom">3. Le Côté de Guermantes (1920–21)</div><div class="figure-ex">La haute société parisienne, le faubourg Saint-Germain, mort de la grand-mère.</div></div>
            <div class="figure-card"><div class="figure-nom">4. Sodome et Gomorrhe (1921–22)</div><div class="figure-ex">L'homosexualité, la jalousie, la mort de la mère d'Albertine.</div></div>
            <div class="figure-card"><div class="figure-nom">5. La Prisonnière (1923, posthume)</div><div class="figure-ex">La jalousie obsessionnelle du narrateur envers Albertine.</div></div>
            <div class="figure-card"><div class="figure-nom">6. Albertine disparue (1925, posthume)</div><div class="figure-ex">La mort d'Albertine, le deuil, l'oubli progressif.</div></div>
            <div class="figure-card"><div class="figure-nom">7. Le Temps retrouvé (1927, posthume)</div><div class="figure-ex">La révélation finale. L'art comme seule victoire sur le temps. Décision d'écrire.</div></div>
          </div>
        </div>
      </div>
    </div>

    <!-- FRISE PROUST -->
    <div class="bloc">
      <div class="bloc-titre">Frise chronologique</div>
      <div class="card">
        <div class="card-section">
          <div class="frise-legende">
            <div class="legende-item"><div class="legende-dot key"></div> Création littéraire</div>
            <div class="legende-item"><div class="legende-dot war"></div> Événement historique</div>
            <div class="legende-item"><div class="legende-dot pub"></div> Publication</div>
            <div class="legende-item"><div class="legende-dot life"></div> Vie personnelle</div>
          </div>
          <div class="frise">
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">10 juillet 1871</div>
              <div class="frise-titre">Naissance à Auteuil</div>
              <div class="frise-desc">Naissance de Marcel Proust, fils du Dr Adrien Proust et de Jeanne Weil.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1880</div>
              <div class="frise-titre">Premières crises d'asthme</div>
              <div class="frise-desc">À 9 ans, crise grave au Bois de Boulogne. La maladie marquera toute sa vie et son rapport au monde extérieur.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1882–1889</div>
              <div class="frise-titre">Lycée Condorcet</div>
              <div class="frise-desc">Brillant élève, il y développe ses premières amitiés mondaines et intellectuelles. Il commence à écrire pour la revue du lycée.</div>
            </div>
            <div class="frise-item"><div class="frise-dot war"></div>
              <div class="frise-date">1894–1906</div>
              <div class="frise-titre">Affaire Dreyfus</div>
              <div class="frise-desc">Proust est dreyfusard convaincu. La fracture sociale et politique de l'affaire divise les salons et nourrit directement la description de la société dans <em>La Recherche</em>.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1896</div>
              <div class="frise-titre">Les Plaisirs et les Jours</div>
              <div class="frise-desc">Premier recueil de nouvelles et poèmes en prose, préfacé par Anatole France. Passe inaperçu.</div>
            </div>
            <div class="frise-item"><div class="frise-dot key"></div>
              <div class="frise-date">1895–1900</div>
              <div class="frise-titre">Rédaction de Jean Santeuil</div>
              <div class="frise-desc">Roman autobiographique inachevé (publié posthumement en 1952). Première ébauche de <em>La Recherche</em> : on y trouve déjà les thèmes du temps, de l'enfance et de la mémoire.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1903–1905</div>
              <div class="frise-titre">Mort de ses parents</div>
              <div class="frise-desc">La mort de son père (1903) puis surtout de sa mère adorée (1905) plonge Proust dans un deuil profond. Il entre dans une clinique de repos. Cette perte nourrit directement les thèmes du deuil et de la disparition dans son œuvre.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">1906</div>
              <div class="frise-titre">Emménagement boulevard Haussmann</div>
              <div class="frise-desc">Proust s'installe dans l'appartement familial boulevard Haussmann, qu'il fait calfeutrer de liège pour s'isoler du bruit. C'est là qu'il rédigera l'essentiel de <em>La Recherche</em>.</div>
            </div>
            <div class="frise-item"><div class="frise-dot key"></div>
              <div class="frise-date">1909</div>
              <div class="frise-titre">Début de la Recherche</div>
              <div class="frise-desc">Proust commence la rédaction définitive d'<em>À la recherche du temps perdu</em>. Il se retire du monde des salons et travaille nuit et jour.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">Novembre 1913</div>
              <div class="frise-titre">Du côté de chez Swann</div>
              <div class="frise-desc">Refusé par la NRF (Gide l'avouera comme une erreur monumentale), publié à compte d'auteur chez Grasset. Contient la scène fondatrice de la madeleine.</div>
            </div>
            <div class="frise-item"><div class="frise-dot war"></div>
              <div class="frise-date">1914–1918</div>
              <div class="frise-titre">Première Guerre mondiale</div>
              <div class="frise-desc">Proust, trop malade pour combattre, reste à Paris. La Grande Guerre efface la Belle Époque — cette disparition d'un monde nourrit directement le thème de <em>Le Temps retrouvé</em>.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1919</div>
              <div class="frise-titre">Prix Goncourt</div>
              <div class="frise-desc"><em>À l'ombre des jeunes filles en fleurs</em> reçoit le prix Goncourt, non sans controverse. Reconnaissance nationale tardive mais éclatante. Proust a 48 ans.</div>
            </div>
            <div class="frise-item"><div class="frise-dot pub"></div>
              <div class="frise-date">1920–1922</div>
              <div class="frise-titre">Le Côté de Guermantes, Sodome et Gomorrhe</div>
              <div class="frise-desc">Publication des volumes 3 et 4. Proust corrige les épreuves depuis son lit, ajoutant sans cesse de nouveaux développements.</div>
            </div>
            <div class="frise-item"><div class="frise-dot life"></div>
              <div class="frise-date">18 novembre 1922</div>
              <div class="frise-titre">Mort à Paris</div>
              <div class="frise-desc">Proust meurt d'une pneumonie à 51 ans. Les trois derniers volumes sont publiés posthumement par son frère Robert (1923–1927).</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- MODERNISME -->
    <div class="bloc">
      <div class="bloc-titre">Mouvement littéraire</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Mouvement · Début XXe siècle</div>
          <div class="fiche-titre">Le Modernisme</div>
          <div class="fiche-sous">et la littérature de la conscience · 1900–1940 environ</div>
          <div class="tags" style="margin-top:8px;">
            <span class="tag tag-purple">Flux de conscience</span>
            <span class="tag tag-blue">Rupture avec le réalisme</span>
            <span class="tag tag-teal">Subjectivité</span>
            <span class="tag tag-amber">Temps intérieur</span>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Définition et contexte</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text"><strong>Rupture avec le réalisme et le naturalisme :</strong> Le modernisme littéraire (Virginia Woolf, James Joyce, Proust) rompt avec le roman du XIXe siècle qui décrivait le monde extérieur avec objectivité. Il tourne la caméra vers l'intérieur : la <strong>conscience, la mémoire, la perception subjective</strong> du temps deviennent le véritable sujet.</div>
            </div>
            <div class="point"><div class="point-dot dot-blue"></div>
              <div class="point-text"><strong>Le temps intérieur (durée bergsonienne) :</strong> Proust s'inspire du philosophe <strong>Henri Bergson</strong> (son cousin par alliance) qui distingue le temps mesuré (chronologique, extérieur) de la <em>durée</em> — le temps vécu intérieurement, élastique, subjectif. Chez Proust, quelques secondes peuvent générer des centaines de pages.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text"><strong>Le flux de conscience :</strong> Technique narrative qui abandonne la logique causale traditionnelle pour suivre le cours associatif de la pensée. Chez Proust : les longues <strong>phrases sinueuses</strong>, les digressions, les parenthèses sont la forme même de la conscience qui se déploie.</div>
            </div>
            <div class="point"><div class="point-dot dot-coral"></div>
              <div class="point-text"><strong>Contexte historique :</strong> La Belle Époque (1871–1914) puis la Première Guerre mondiale bouleversent les certitudes. La modernité industrielle, la psychanalyse freudienne (1900), la relativité einsteinienne (1905) remettent en question les visions stables du moi et du temps.</div>
            </div>
            <div class="point"><div class="point-dot dot-amber"></div>
              <div class="point-text"><strong>L'art comme connaissance :</strong> Pour Proust comme pour les modernistes, l'œuvre d'art n'imite pas la réalité — elle la <strong>révèle</strong>. Seul l'art peut saisir la vérité de l'expérience humaine que la science et la philosophie ne peuvent atteindre.</div>
            </div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Proust parmi les modernistes</div>
          <div class="symb-grid">
            <div class="symb-card"><div class="symb-titre">Marcel Proust (1871–1922) — France</div><div class="symb-texte">La mémoire involontaire, le temps intérieur, la phrase-fleuve. <em>À la recherche du temps perdu</em>.</div></div>
            <div class="symb-card"><div class="symb-titre">Virginia Woolf (1882–1941) — Angleterre</div><div class="symb-texte">Flux de conscience, impressionnisme littéraire. <em>Mrs Dalloway</em>, <em>La Promenade au phare</em>.</div></div>
            <div class="symb-card"><div class="symb-titre">James Joyce (1882–1941) — Irlande</div><div class="symb-texte">Monologue intérieur radical, polyphonie, mythe. <em>Ulysse</em> (1922), <em>Gens de Dublin</em>.</div></div>
            <div class="symb-card"><div class="symb-titre">Henri Bergson (1859–1941) — France</div><div class="symb-texte">Philosophe de la durée et de la mémoire. Influence directe sur Proust. Prix Nobel de littérature 1927.</div></div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">La phrase proustienne — caractéristiques</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text"><strong>Longueur et sinuosité :</strong> Les phrases de Proust peuvent s'étendre sur une page entière avec des subordonnées emboîtées, des incises et des parenthèses. Cette forme mime le fonctionnement de la conscience qui associe, nuance, revient sur elle-même.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text"><strong>La métaphore au cœur du style :</strong> Proust use abondamment de comparaisons et métaphores inattendues qui révèlent des analogies cachées entre les choses. Pour lui, la métaphore est <strong>le seul moyen d'atteindre la vérité</strong> des sensations.</div>
            </div>
            <div class="point"><div class="point-dot dot-amber"></div>
              <div class="point-text"><strong>La digression comme structure :</strong> Le récit proustien avance par digressions, cercles concentriques, retours en arrière. Ce n'est pas un récit linéaire mais une <strong>exploration spiralée</strong> du temps et de la mémoire.</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- DU CÔTÉ DE CHEZ SWANN -->
    <div class="bloc">
      <div class="bloc-titre">Le roman</div>
      <div class="card">
        <div class="card-header">
          <div class="fiche-numero">Volume I · 1913 · Éditions Grasset puis Gallimard</div>
          <div class="fiche-titre">Du côté de chez Swann</div>
          <div class="fiche-sous">Premier volume d'À la recherche du temps perdu · 3 parties</div>
          <div class="tags" style="margin-top:8px;">
            <span class="tag tag-purple">Mémoire involontaire</span>
            <span class="tag tag-blue">Temps et enfance</span>
            <span class="tag tag-teal">Amour et jalousie</span>
            <span class="tag tag-amber">Modernisme</span>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Structure en trois parties</div>
          <div class="symb-grid">
            <div class="symb-card">
              <div class="symb-titre">1. Combray</div>
              <div class="symb-texte">L'enfance du narrateur à Combray. La scène de la madeleine déclenche le souvenir du village entier. Les deux « côtés » : côté de Méséglise (Swann) et côté de Guermantes.</div>
            </div>
            <div class="symb-card">
              <div class="symb-titre">2. Un amour de Swann</div>
              <div class="symb-texte">Récit rétrospectif de la passion jalouse et destructrice de Swann pour Odette de Crécy, dans les milieux bourgeois des Verdurin. La sonate de Vinteuil comme « petite phrase » musicale.</div>
            </div>
            <div class="symb-card">
              <div class="symb-titre">3. Noms de pays : le nom</div>
              <div class="symb-texte">L'adolescence du narrateur aux Champs-Élysées. Amour pour Gilberte (fille de Swann). Le pouvoir des noms de lieux dans l'imagination.</div>
            </div>
          </div>
        </div>
        <div class="card-section">
          <div class="section-label">Thèmes majeurs</div>
          <div class="points">
            <div class="point"><div class="point-dot dot-purple"></div>
              <div class="point-text"><strong>Le temps et la mémoire :</strong> La madeleine est le symbole de la <strong>mémoire involontaire</strong>. Un goût suffit à ressusciter un monde entier. Proust montre que le passé n'est pas mort — il dort dans les sensations présentes.</div>
            </div>
            <div class="point"><div class="point-dot dot-coral"></div>
              <div class="point-text"><strong>L'amour comme jalousie :</strong> Dans « Un amour de Swann », l'amour n'est pas idéalisé — il est d'abord <strong>jalousie, souffrance, obsession</strong>. Swann aime Odette non pour ce qu'elle est mais parce qu'elle lui échappe. La célèbre formule : <em>« il avait souffert pour une femme qui n'était même pas son genre »</em>.</div>
            </div>
            <div class="point"><div class="point-dot dot-teal"></div>
              <div class="point-text"><strong>Les milieux sociaux :</strong> Proust décrit avec précision les <strong>rites, les hiérarchies et les snobismes</strong> des milieux bourgeois (les Verdurin) et aristocratiques (les Guermantes). La société est un théâtre où chacun joue un rôle.</div>
            </div>
            <div class="point"><div class="point-dot dot-blue"></div>
              <div class="point-text"><strong>L'art comme révélation :</strong> La <strong>sonate de Vinteuil</strong> (musicien fictif) est la première manifestation d'une expérience esthétique qui ouvre sur une réalité plus vraie que le quotidien — thème qui culminera dans <em>Le Temps retrouvé</em>.</div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div><!-- /container proust -->
  </div><!-- /inner-proust -->

</div><!-- /panel-autres -->


<footer>
  Fiches basées sur les analyses de commentairecompose.fr — Arthur Rimbaud, <em>Cahiers de Douai</em> (1870)
</footer>

<script>
// ---- DISCLAIMER MODAL ----
function toggleDisclaimerBtn() {
  var checked = document.getElementById('disclaimer-check').checked;
  var btn = document.getElementById('disclaimer-btn');
  btn.disabled = !checked;
  btn.style.background = checked ? '#534ab7' : '#e8e4db';
  btn.style.color = checked ? '#ffffff' : '#9c9890';
  btn.style.cursor = checked ? 'pointer' : 'not-allowed';
}
function closeDisclaimer() {
  var overlay = document.getElementById('disclaimer-overlay');
  overlay.style.opacity = '0';
  overlay.style.transition = 'opacity 0.3s ease';
  setTimeout(function() { overlay.style.display = 'none'; }, 300);
}

// ---- TAB SWITCHING (onglets principaux) ----
function switchTab(id) {
  document.querySelectorAll('.tab-panel').forEach(function(p) { p.classList.remove('active'); });
  document.querySelectorAll('.tab-btn').forEach(function(b) { b.classList.remove('active'); });
  var panel = document.getElementById('panel-' + id);
  if (panel) panel.classList.add('active');
  event.currentTarget.classList.add('active');
  window.scrollTo(0, 0);
}

// ---- INNER TAB SWITCHING (sous-onglets La Fontaine / Proust) ----
function switchInner(id, btn) {
  // Cacher tous les inner-panels du même parent
  var bar = btn.closest('.inner-tab-bar');
  var container = bar.parentElement;
  container.querySelectorAll('.inner-panel').forEach(function(p) { p.classList.remove('active'); });
  bar.querySelectorAll('.inner-tab-btn').forEach(function(b) { b.classList.remove('active'); });
  var panel = document.getElementById('inner-' + id);
  if (panel) panel.classList.add('active');
  btn.classList.add('active');
  window.scrollTo(0, 0);
}

// ---- ACCORDION ----
function toggleMvt(header) {
  var body = header.nextElementSibling;
  var arrow = header.querySelector('.mvt-arrow');
  var isOpen = body.classList.contains('open');
  body.classList.toggle('open', !isOpen);
  arrow.classList.toggle('open', !isOpen);
}

// ---- SUBNAV ACTIVE ON SCROLL ----
var sections = document.querySelectorAll('[id]');
var navLinks = document.querySelectorAll('#subnav a');
function updateNav() {
  var scrollY = window.scrollY + 110;
  var current = '';
  sections.forEach(function(s) {
    if (s.offsetTop <= scrollY) current = s.id;
  });
  navLinks.forEach(function(a) {
    a.classList.toggle('active', a.getAttribute('href') === '#' + current);
  });
}
window.addEventListener('scroll', updateNav, { passive: true });
updateNav();
</script>

</body>
</html>
