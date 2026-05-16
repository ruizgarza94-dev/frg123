[index.html.txt](https://github.com/user-attachments/files/27852479/index.html.txt)
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Generador Automático Infinito — Johan Monetiza</title>
<style>
  :root {
    --bg: #0d0d1a;
    --panel: #14142b;
    --panel2: #1c1c35;
    --text: #ffffff;
    --muted: rgba(255,255,255,0.74);
    --soft: rgba(255,255,255,0.50);
    --pink: #ff3e7f;
    --green: #2ecc71;
    --gold: #ffd700;
    --purple: #8b5cf6;
    --cyan: #00e5ff;
    --red: #ff4444;
    --orange: #ff9a3c;
    --shadow: 0 20px 50px rgba(0,0,0,0.36);
    --radius: 22px;
  }
  * { box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    margin: 0;
    font-family: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    background:
      radial-gradient(circle at 0% 0%, rgba(255,62,127,0.12), transparent 28%),
      radial-gradient(circle at 100% 100%, rgba(0,229,255,0.12), transparent 24%),
      linear-gradient(180deg, #0d0d1a 0%, #101022 100%);
    color: var(--text);
    min-height: 100vh;
  }
  .wrap { max-width: 1380px; margin: 0 auto; padding: 26px 18px 70px; }
  .hero {
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, rgba(255,62,127,0.18), rgba(139,92,246,0.16));
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 30px;
    padding: 30px 26px 26px;
    box-shadow: var(--shadow);
    text-align: center;
  }
  .hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.03), transparent);
    pointer-events: none;
  }
  .title {
    margin: 0 auto;
    text-align: center;
    font-size: clamp(2.2rem, 5.3vw, 5.2rem);
    line-height: 0.92;
    font-weight: 1000;
    text-transform: uppercase;
    letter-spacing: .04em;
    max-width: 1100px;
    background: linear-gradient(180deg, #fff8d8 0%, var(--gold) 32%, var(--orange) 60%, var(--pink) 100%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    text-shadow:
      0 1px 0 rgba(255,255,255,0.34),
      0 4px 0 rgba(139,92,246,0.26),
      0 7px 0 rgba(255,62,127,0.22),
      0 18px 28px rgba(0,0,0,0.45);
    filter: drop-shadow(0 12px 26px rgba(255,62,127,0.28));
  }
  .subtitle {
    max-width: 960px;
    margin: 14px auto 0;
    color: var(--muted);
    font-size: 1rem;
    line-height: 1.68;
  }
  .hero-pills {
    display: flex; justify-content: center; flex-wrap: wrap; gap: 10px;
    margin-top: 18px;
  }
  .hero-pill {
    padding: 9px 14px; border-radius: 999px;
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.08);
    color: var(--muted); font-size: .83rem; font-weight: 900;
  }
  .grid-top {
    display: grid; grid-template-columns: 1.08fr .92fr; gap: 20px;
    margin-top: 22px;
  }
  .panel {
    background: rgba(20,20,43,0.95);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
  }
  .pad { padding: 20px; }
  .section-title {
    margin: 0 0 14px;
    font-size: 1.07rem;
    font-weight: 900;
    letter-spacing: .02em;
  }
  .steps { display: grid; gap: 12px; }
  .step {
    display: flex; gap: 12px; align-items: flex-start;
    background: var(--panel2);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px;
    padding: 12px 14px;
  }
  .step-num {
    width: 30px; height: 30px; border-radius: 999px; display: grid; place-items: center;
    background: linear-gradient(135deg, var(--pink), var(--purple));
    font-weight: 900; flex: 0 0 30px;
  }
  .step b { display: block; margin-bottom: 3px; }
  .step span { color: var(--soft); font-size: .91rem; line-height: 1.52; }
  .quick {
    display: grid; grid-template-columns: repeat(2,1fr); gap: 12px;
  }
  .quick .card {
    background: var(--panel2);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px;
    padding: 14px;
  }
  .k { color: var(--soft); font-size: .76rem; text-transform: uppercase; letter-spacing: .08em; }
  .v { margin-top: 6px; font-weight: 900; line-height: 1.42; }
  .selectors {
    margin-top: 22px;
    display: grid;
    grid-template-columns: repeat(5, minmax(0,1fr));
    gap: 14px;
  }
  .control {
    background: rgba(20,20,43,0.96);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 18px;
    padding: 14px;
    box-shadow: var(--shadow);
  }
  .control label {
    display: block;
    margin-bottom: 8px;
    color: var(--soft);
    font-size: .74rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    font-weight: 900;
  }
  select {
    width: 100%;
    background: var(--panel2);
    border: 1px solid rgba(255,255,255,0.10);
    color: #fff;
    border-radius: 12px;
    padding: 11px 12px;
    font-size: .93rem;
    font-weight: 800;
    outline: none;
  }
  select:focus { border-color: var(--pink); }
  .cta-row {
    display: flex; gap: 12px; flex-wrap: wrap;
    margin-top: 18px;
  }
  .btn {
    border: none; border-radius: 999px; padding: 14px 22px;
    font-weight: 900; cursor: pointer; font-size: .94rem;
    transition: transform .18s ease, box-shadow .18s ease, opacity .18s ease;
  }
  .btn:hover { transform: translateY(-2px); }
  .btn-main {
    background: linear-gradient(135deg, var(--pink), var(--purple));
    color: #fff; box-shadow: 0 15px 36px rgba(255,62,127,0.28);
  }
  .btn-green {
    background: linear-gradient(135deg, var(--green), var(--cyan));
    color: #042028; box-shadow: 0 15px 36px rgba(0,229,255,0.20);
  }
  .btn-alt {
    background: rgba(255,255,255,0.08);
    color: #fff; border: 1px solid rgba(255,255,255,0.11);
  }
  .btn-gold {
    background: linear-gradient(135deg, var(--gold), var(--orange));
    color: #241503; box-shadow: 0 15px 36px rgba(255,215,0,0.18);
  }
  .layout {
    display: grid; grid-template-columns: 360px 1fr; gap: 20px;
    align-items: start; margin-top: 22px;
  }
  .sticky { position: sticky; top: 16px; }
  .story-title-box {
    background: linear-gradient(135deg, rgba(255,62,127,0.14), rgba(139,92,246,0.10));
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 20px;
    padding: 18px;
    margin-bottom: 18px;
  }
  .story-title {
    font-size: 1.22rem;
    font-weight: 1000;
    line-height: 1.35;
    margin: 0;
  }
  .premise {
    color: var(--muted);
    line-height: 1.62;
    font-size: .95rem;
    margin-top: 10px;
  }
  .char-list { display: grid; gap: 12px; }
  .char-card {
    background: var(--panel2);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px; padding: 14px;
  }
  .char-name { font-weight: 1000; color: var(--gold); margin-bottom: 8px; }
  .char-role {
    display: inline-flex; padding: 4px 10px; border-radius: 999px; font-size: .72rem;
    font-weight: 900; margin-left: 6px; background: rgba(255,255,255,0.08); color: var(--muted);
  }
  .char-desc { color: var(--muted); font-size: .9rem; line-height: 1.6; }
  .mini-box {
    margin-top: 16px;
    background: linear-gradient(135deg, rgba(46,204,113,0.12), rgba(0,229,255,0.08));
    border: 1px solid rgba(46,204,113,0.22);
    border-radius: 16px;
    padding: 14px;
  }
  .summary-row {
    display: flex; justify-content: space-between; gap: 10px;
    padding: 8px 0; border-bottom: 1px dashed rgba(255,255,255,0.08);
    font-size: .88rem;
  }
  .summary-row:last-child { border-bottom: 0; }
  .summary-row span:first-child { color: var(--soft); }
  .tabs { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 16px; }
  .tab {
    background: rgba(255,255,255,0.07); color: var(--muted);
    border: 1px solid rgba(255,255,255,0.08); padding: 10px 15px;
    border-radius: 12px; cursor: pointer; font-weight: 900;
  }
  .tab.active {
    color: #fff; border-color: var(--pink);
    background: linear-gradient(135deg, rgba(255,62,127,0.26), rgba(139,92,246,0.18));
  }
  .tab-panel { display: none; }
  .tab-panel.visible { display: block; }
  .scene-card {
    background: rgba(20,20,43,0.98);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 18px; overflow: hidden; margin-bottom: 16px;
  }
  .scene-head {
    display: flex; align-items: center; justify-content: space-between; gap: 12px;
    padding: 14px 16px;
    background: linear-gradient(90deg, rgba(255,62,127,0.12), transparent);
    border-bottom: 1px solid rgba(255,255,255,0.06);
  }
  .scene-number {
    width: 34px; height: 34px; border-radius: 999px; display: grid; place-items: center;
    background: var(--pink); color: #fff; font-weight: 1000; flex: 0 0 34px;
  }
  .scene-head-text { flex: 1; }
  .scene-title-line { font-weight: 1000; line-height: 1.35; }
  .scene-meta { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 7px; }
  .pill {
    display: inline-flex; align-items: center; gap: 6px; padding: 6px 10px;
    border-radius: 999px; background: rgba(255,255,255,0.08); color: var(--muted);
    font-size: .74rem; font-weight: 900;
  }
  .scene-body { padding: 16px; }
  .label {
    color: var(--gold); font-size: .76rem; letter-spacing: .08em; text-transform: uppercase;
    font-weight: 1000; margin-bottom: 8px;
  }
  .label.cyan { color: var(--cyan); }
  .prompt-box {
    position: relative; background: rgba(0,0,0,0.22);
    border: 1px solid rgba(255,255,255,0.06); border-left: 4px solid var(--gold);
    border-radius: 14px; padding: 14px 70px 14px 14px;
    color: var(--muted); line-height: 1.7; font-size: .92rem;
  }
  .prompt-box.cyan { border-left-color: var(--cyan); }
  .copy {
    position: absolute; top: 10px; right: 10px; border: 1px solid rgba(255,255,255,0.12);
    background: rgba(255,255,255,0.08); color: #fff; border-radius: 10px;
    padding: 7px 10px; font-size: .74rem; font-weight: 900; cursor: pointer;
  }
  .copy:hover { border-color: var(--pink); background: rgba(255,62,127,0.20); }
  .narration {
    margin-top: 12px; background: linear-gradient(135deg, rgba(139,92,246,0.14), rgba(0,229,255,0.08));
    border: 1px solid rgba(139,92,246,0.20); border-radius: 14px; padding: 12px 14px;
    color: #fff; font-style: italic; line-height: 1.66;
  }
  .hook-grid, .summary-grid, .combo-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 12px;
  }
  .hook, .summary-item, .combo-item {
    background: var(--panel2); border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px; padding: 14px; color: var(--muted); line-height: 1.6;
  }
  .summary-item b, .combo-item b { color: #fff; }
  .lipsync-list { display: grid; gap: 12px; }
  .lip-card {
    background: var(--panel2); border: 1px solid rgba(255,255,255,0.07);
    border-radius: 16px; padding: 14px;
  }
  .lip-card b { display: block; margin-bottom: 8px; }
  .toolbar {
    display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 16px;
  }
  .footer-note {
    margin-top: 20px; text-align: center; color: var(--soft); font-size: .88rem;
  }
  @media (max-width: 1200px) {
    .selectors { grid-template-columns: repeat(3, minmax(0,1fr)); }
  }
  @media (max-width: 980px) {
    .grid-top, .layout { grid-template-columns: 1fr; }
    .sticky { position: static; }
    .selectors { grid-template-columns: repeat(2, minmax(0,1fr)); }
  }
  @media (max-width: 640px) {
    .selectors, .quick { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>
  <div class="wrap">
    <section class="hero">
      <h1 class="title">Generador Automático Infinito<br>Johan Monetiza</h1>
      <p class="subtitle">
        Genera historias completamente nuevas con coherencia narrativa total, manteniendo el mismo formato Johan, el estilo glossy premium 3D,
        prompts de imagen y video en inglés, lipsync en español, hooks virales, resumen por escena y personajes visualmente consistentes con un solo clic.
      </p>
      <div class="hero-pills">
        <span class="hero-pill">⚡ Título viral automático</span>
        <span class="hero-pill">🎬 10 a 15 escenas</span>
        <span class="hero-pill">🖼️ FREEPIK IMAGEN</span>
        <span class="hero-pill">🎥 KLING VIDEO</span>
        <span class="hero-pill">🎙️ LIPSYNC en español</span>
        <span class="hero-pill">🎯 Hooks + Resumen + Personajes</span>
      </div>

      <div class="grid-top">
        <div class="panel pad">
          <h2 class="section-title">Cómo funciona</h2>
          <div class="steps">
            <div class="step"><div class="step-num">1</div><div><b>Selecciona tu universo</b><span>Elige espada y rosa, invernadero del revés, academia de eclipse, laboratorio de tormenta, escenario de neón, bosque dorado o jardín miniatura.</span></div></div>
            <div class="step"><div class="step-num">2</div><div><b>Define los roles</b><span>Selecciona protagonista, rival, protector, emoción, conflicto, escenario, final y cantidad de escenas cinematográficas.</span></div></div>
            <div class="step"><div class="step-num">3</div><div><b>Genera la historia</b><span>El sistema crea automáticamente una premisa coherente, de 10 a 15 escenas, prompts completos, hooks por escena, resumen y todos los lipsync en orden.</span></div></div>
          </div>
        </div>

        <div class="panel pad">
          <h2 class="section-title">Qué genera</h2>
          <div class="quick">
            <div class="card"><div class="k">Universos</div><div class="v">7 bases narrativas</div></div>
            <div class="card"><div class="k">Escenas</div><div class="v" id="quickScenes">10 a 15 escenas</div></div>
            <div class="card"><div class="k">Formato</div><div class="v">FREEPIK + KLING + LIPSYNC</div></div>
            <div class="card"><div class="k">Estilo</div><div class="v">Glossy 3D premium Johan</div></div>
          </div>
        </div>
      </div>
    </section>

    <section class="selectors">
      <div class="control"><label>Universo</label><select id="universe"></select></div>
      <div class="control"><label>Protagonista</label><select id="protagonist"></select></div>
      <div class="control"><label>Rival / Villano</label><select id="rival"></select></div>
      <div class="control"><label>Protector</label><select id="protector"></select></div>
      <div class="control"><label>Emoción dominante</label><select id="emotion"></select></div>
      <div class="control"><label>Conflicto principal</label><select id="conflict"></select></div>
      <div class="control"><label>Escenario</label><select id="scenario"></select></div>
      <div class="control"><label>Tipo de final</label><select id="ending"></select></div>
      <div class="control"><label>Número de escenas</label><select id="sceneCount"></select></div>
      <div class="control"><label>Estilo visual</label><select id="visualStyle"></select></div>
    </section>

    <div class="cta-row">
      <button class="btn btn-main" id="generateBtn">⚡ Generar historia</button>
      <button class="btn btn-green" id="randomBtn">🎲 Generar historia aleatoria</button>
      <button class="btn btn-alt" id="copyAllBtn">📋 Copiar historia completa</button>
      <button class="btn btn-gold" id="copyLipsBtn">🎙️ Copiar todos los lipsync</button>
    </div>

    <section class="layout">
      <aside class="sticky">
        <div class="story-title-box">
          <h2 class="story-title" id="storyTitle">Genera una historia nueva</h2>
          <div class="premise" id="premise">Selecciona tus variables o usa el botón aleatorio para crear una nueva historia con coherencia completa.</div>
        </div>

        <div class="panel pad">
          <h2 class="section-title">Prompt base de personajes</h2>
          <div class="char-list" id="charactersOut"></div>
        </div>

        <div class="mini-box">
          <div class="summary-row"><span>Universo</span><span id="sumUniverse">—</span></div>
          <div class="summary-row"><span>Conflicto</span><span id="sumConflict">—</span></div>
          <div class="summary-row"><span>Emoción</span><span id="sumEmotion">—</span></div>
          <div class="summary-row"><span>Final</span><span id="sumEnding">—</span></div>
          <div class="summary-row"><span>Escenas</span><span id="sumScenes">—</span></div>
        </div>
      </aside>

      <main>
        <div class="panel pad">
          <div class="tabs">
            <button class="tab active" data-tab="scenes">🎬 Escenas</button>
            <button class="tab" data-tab="hooks">🎯 Hooks</button>
            <button class="tab" data-tab="summary">🧾 Resumen</button>
            <button class="tab" data-tab="lipsync">🎙️ Lipsync</button>
            <button class="tab" data-tab="ideas">⚡ Ideas rápidas</button>
          </div>

          <div class="tab-panel visible" id="tab-scenes">
            <div class="toolbar">
              <button class="btn btn-alt" onclick="copyByType('image')">📋 Copiar prompts de imagen</button>
              <button class="btn btn-alt" onclick="copyByType('video')">📋 Copiar prompts de video</button>
            </div>
            <div id="scenesOut"></div>
          </div>

          <div class="tab-panel" id="tab-hooks"><div class="hook-grid" id="hooksOut"></div></div>
          <div class="tab-panel" id="tab-summary"><div class="summary-grid" id="storySummaryOut"></div></div>
          <div class="tab-panel" id="tab-lipsync"><div class="lipsync-list" id="lipsyncOut"></div></div>
          <div class="tab-panel" id="tab-ideas"><div class="combo-grid" id="comboOut"></div></div>
        </div>
      </main>
    </section>

    <div class="footer-note">Generador automático infinito listo para usar. Todo en un solo HTML y con estilo Johan.</div>
  </div>



<script>
const VISUAL_STYLES = [
  "Premium glossy 3D cartoon animation, same style as reference",
  "Premium glossy 3D cartoon animation with stronger cinematic lighting, luxe reflections and iconic close-ups",
  "Premium glossy 3D cartoon animation with moody neon contrast, emotional depth of field and sensual tension",
  "Premium glossy 3D cartoon animation with ultra polished surfaces, premium toy-like finish and dramatic atmosphere"
];
const UNIVERSES = {
  "espadaRosa": {
    "name": "La Espada y la Rosa",
    "mood": "duelos nocturnos, aristocracia podrida, deseo contenido y valentía enmascarada",
    "moodEn": "moonlit duels, rotten aristocracy, restrained desire and masked courage",
    "theme": {
      "symbolEs": "la rosa de terciopelo",
      "placeEs": "el mercado viejo",
      "secretEs": "la máscara negra",
      "symbolEn": "the velvet rose",
      "placeEn": "the old market",
      "secretEn": "the black mask"
    },
    "titleTemplates": [
      "{P} y la rosa que hizo caer a {R}",
      "{R} quiso humillar a {P}… y {T} respondió con una espada",
      "La noche en que {P} vio la máscara de {T} y dejó de obedecer",
      "{P} convirtió una humillación en el escándalo más elegante del mercado viejo"
    ],
    "characters": {
      "frambuesaMarquesa": {
        "emoji": "🍓",
        "name": "La Frambuesa Marquesa",
        "role": "Protagonista",
        "desc": "Humanized female raspberry marchioness in a glossy premium 3D cartoon style. Deep wine-red berry head with tiny glossy drupelets, huge half-lidded feminine eyes, beauty mark, long lashes, sculpted velvet corset gown, satin gloves, elegant heels, proud but wounded posture, subtle sensual charisma, premium cinematic finish."
      },
      "peraMensajera": {
        "emoji": "🍐",
        "name": "La Pera Mensajera",
        "role": "Protagonista",
        "desc": "Humanized female pear messenger in a glossy premium 3D cartoon style. Smooth pale-green pear-shaped head, alert amber eyes, soft blush, fitted cream blouse, high-waist riding skirt, ankle boots, hidden rebellious energy, graceful but fast body language, polished heroic silhouette."
      },
      "melonEnmascarado": {
        "emoji": "🍈",
        "name": "El Melón Enmascarado",
        "role": "Protector",
        "desc": "Humanized male melon vigilante in a glossy premium 3D cartoon style. Pale green melon head with subtle stripe texture, sharp golden eyes behind a black domino mask, fitted white shirt slightly open at the collar, emerald cape, dark sword belt, dangerous gentleman aura, premium glossy lighting."
      },
      "uvaEspadachina": {
        "emoji": "🍇",
        "name": "La Uva Espadachina",
        "role": "Protectora",
        "desc": "Humanized female grape swordswoman in a glossy premium 3D cartoon style. Sleek purple grape-cluster silhouette, confident almond eyes, dark plum leather jacket over a fitted duel corset, polished boots, silver rapier, poised stance, alluring and fearless energy."
      },
      "pimientoDuque": {
        "emoji": "🌶️",
        "name": "El Pimiento Duque",
        "role": "Rival",
        "desc": "Humanized male red pepper duke in a glossy premium 3D cartoon style. Long glossy crimson pepper head, sculpted arrogant brows, predatory smile, rich black-and-red aristocratic suit, jeweled cane, possessive posture, manipulative upper-class villain charisma."
      }
    },
    "protagonists": [
      "frambuesaMarquesa",
      "peraMensajera"
    ],
    "rivals": [
      "pimientoDuque"
    ],
    "protectors": [
      "melonEnmascarado",
      "uvaEspadachina"
    ],
    "scenarios": [
      {
        "label": "balcón colonial con rosas y faroles",
        "prompt": "moonlit colonial balcony filled with velvet roses, stone arches, warm lanterns and charged social tension"
      },
      {
        "label": "plaza del mercado viejo con máscaras y miradas",
        "prompt": "old market plaza at night with masquerade guests, glowing lanterns, polished cobblestone and scandalous tension"
      },
      {
        "label": "pasillo secreto de hacienda con espadas y pétalos",
        "prompt": "secret hacienda corridor with crossed swords, fallen petals, candlelight and aristocratic danger"
      }
    ],
    "conflicts": [
      "una rosa anónima y una espada escondida convierten un baile elegante en un duelo emocional",
      "el rival expone la deuda de la protagonista delante de todos para forzar un compromiso humillante",
      "una identidad enmascarada protege a la protagonista justo cuando el escándalo social está a punto de destruirla"
    ],
    "endings": [
      "romántico",
      "venganza elegante",
      "cliffhanger"
    ],
    "ideaSeeds": [
      "Frambuesa marquesa + melón enmascarado + duque pimiento celoso + balcón con beso no dado",
      "Pera mensajera atrapada entre un compromiso forzado y un protector con espada",
      "Uva espadachina defendiendo a una protagonista humillada en plena plaza colonial",
      "Pimiento duque desenmascarado por una rosa y un rumor viral frente a toda la corte"
    ]
  },
  "invernaderoReves": {
    "name": "El Invernadero del Revés",
    "mood": "misterio adolescente, portales orgánicos, deseo peligroso y rumores que deforman la realidad",
    "moodEn": "teen mystery, organic portals, dangerous desire and rumors that distort reality",
    "theme": {
      "symbolEs": "la luz roja del portal",
      "placeEs": "el invernadero del revés",
      "secretEs": "la grieta luminosa",
      "symbolEn": "the red portal glow",
      "placeEn": "the upside greenhouse",
      "secretEn": "the glowing rift"
    },
    "titleTemplates": [
      "{P} abrió el portal y nadie volvió a reconocer a {R}",
      "Cuando {R} salió del invernadero, {P} ya no era la misma",
      "{T} sintió la grieta antes que todos… y {P} pagó el precio",
      "La noche roja en que {P} dejó de huir del revés"
    ],
    "characters": {
      "moraElectrica": {
        "emoji": "🫐",
        "name": "La Mora Eléctrica",
        "role": "Protagonista",
        "desc": "Humanized female blackberry hero in a glossy premium 3D cartoon style. Dark violet berry head with electric magenta reflections, oversized emotional eyes, varsity jacket over a fitted black dress, silver bracelets, nervous but magnetic aura, polished cinematic textures and subtle dangerous beauty."
      },
      "duraznoSismico": {
        "emoji": "🍑",
        "name": "El Durazno Sísmico",
        "role": "Protagonista",
        "desc": "Humanized male peach teen in a glossy premium 3D cartoon style. Soft peach-toned head with velvety shine, anxious but kind eyes, bomber jacket, layered chains, ripped dark jeans, vulnerable hero energy, soft lips, premium emotional close-up appeal."
      },
      "kiwiPunk": {
        "emoji": "🥝",
        "name": "El Kiwi Punk",
        "role": "Protector",
        "desc": "Humanized male kiwi rebel in a glossy premium 3D cartoon style. Fuzzy kiwi head with green inner glow details, intense eyes, black leather jacket, fingerless gloves, skater stance, protective bad-boy attitude, glossy premium finish and grounded strength."
      },
      "maizCientifico": {
        "emoji": "🌽",
        "name": "El Maíz Científico",
        "role": "Protector",
        "desc": "Humanized male corn scientist in a glossy premium 3D cartoon style. Golden kernel-textured head, clear glasses, long lab coat, rolled sleeves, warm worried gaze, precise hands, mentor energy, polished stylized anatomy and smart cinematic presence."
      },
      "calabazaReves": {
        "emoji": "🎃",
        "name": "La Calabaza del Revés",
        "role": "Rival",
        "desc": "Humanized female pumpkin queen from another dimension in a glossy premium 3D cartoon style. Glowing orange pumpkin head with dark vine crown, shadow-purple eyes, torn luxury cape, eerie regal posture, seductive menace, ominous premium reflections and supernatural authority."
      }
    },
    "protagonists": [
      "moraElectrica",
      "duraznoSismico"
    ],
    "rivals": [
      "calabazaReves"
    ],
    "protectors": [
      "kiwiPunk",
      "maizCientifico"
    ],
    "scenarios": [
      {
        "label": "invernadero rojo con enredaderas vivas",
        "prompt": "red-lit greenhouse with living vines, wet glass, glowing spores and a breathing portal in the background"
      },
      {
        "label": "laboratorio escolar con luces rotas y semillas brillantes",
        "prompt": "school lab with broken lights, glowing seeds, overturned tables and paranormal tension"
      },
      {
        "label": "estacionamiento nocturno con neblina y alarma lejana",
        "prompt": "night parking lot wrapped in fog, distant sirens, red emergency light and supernatural suspense"
      }
    ],
    "conflicts": [
      "el portal empieza a copiar los peores rumores del pueblo y usa la vergüenza de la protagonista para abrirse más",
      "el rival sale del invernadero sabiendo exactamente qué herida emocional usar contra la protagonista",
      "una cinta grabada cerca de la grieta revela que alguien muy cercano alimentó el monstruo sin querer"
    ],
    "endings": [
      "shock",
      "cliffhanger",
      "redentor"
    ],
    "ideaSeeds": [
      "Mora eléctrica + kiwi punk protector + portal rojo que imita rumores crueles",
      "Durazno sísmico atrapado entre la grieta luminosa y una calabaza que lo conoce demasiado bien",
      "Maíz científico descubriendo que el monstruo responde a la vergüenza pública del protagonista",
      "Escena viral en estacionamiento con neblina, cinta encontrada y protector rebelde en primer plano"
    ]
  },
  "academiaEclipse": {
    "name": "La Academia del Eclipse Negro",
    "mood": "gótica, elegante y venenosa, con sarcasmo brillante, deseo reprimido y jerarquías crueles",
    "moodEn": "gothic, elegant and venomous, filled with sharp sarcasm, repressed desire and cruel hierarchies",
    "theme": {
      "symbolEs": "el vals del eclipse",
      "placeEs": "la academia de mármol oscuro",
      "secretEs": "el cuervo de medianoche",
      "symbolEn": "the eclipse waltz",
      "placeEn": "the dark marble academy",
      "secretEn": "the midnight raven"
    },
    "titleTemplates": [
      "{P} bailó una sola vez y destruyó el imperio social de {R}",
      "El vals prohibido de {P} en la academia del eclipse",
      "{R} quiso exhibir a {P}… pero {T} leyó la verdad primero",
      "Lo que {P} vio bajo la luna negra cambió toda la academia"
    ],
    "characters": {
      "uvaCuervo": {
        "emoji": "🍇",
        "name": "La Uva Cuervo",
        "role": "Protagonista",
        "desc": "Humanized female gothic grape prodigy in a glossy premium 3D cartoon style. Deep purple grape-cluster head, porcelain skin accents, heavy-lashed eyes, black lace academy uniform, silver rings, sharp posture, elegant deadpan attitude, polished gothic luxury finish."
      },
      "cerezaFuneraria": {
        "emoji": "🍒",
        "name": "La Cereza Funeraria",
        "role": "Protagonista",
        "desc": "Humanized female cherry gothic debutante in a glossy premium 3D cartoon style. Twin cherry shape with glossy scarlet shine, melancholic eyes, fitted black satin dress with ruby details, delicate gloves, mysterious beauty, soft but dangerous grace."
      },
      "kiwiViolinista": {
        "emoji": "🥝",
        "name": "El Kiwi Violinista",
        "role": "Protector",
        "desc": "Humanized male kiwi violinist in a glossy premium 3D cartoon style. Fuzzy olive-brown kiwi head, calm intense eyes, tailored dark school blazer, open collar, violin case on the shoulder, quiet protector energy, polished romantic silhouette."
      },
      "maizDirector": {
        "emoji": "🌽",
        "name": "El Maíz Director",
        "role": "Protector",
        "desc": "Humanized male corn headmaster in a glossy premium 3D cartoon style. Tall golden kernel crown, long dark academic coat, stern brows, sharp cheek contours, silver cane, unreadable but watchful authority, premium gothic lighting."
      },
      "peraPrefecta": {
        "emoji": "🍐",
        "name": "La Pera Prefecta",
        "role": "Rival",
        "desc": "Humanized female pear prefect in a glossy premium 3D cartoon style. Glossy pale-green pear head, perfect hairline, cold symmetrical eyes, immaculate academy uniform with emerald sash, cruel social queen energy, poised posture and weaponized elegance."
      }
    },
    "protagonists": [
      "uvaCuervo",
      "cerezaFuneraria"
    ],
    "rivals": [
      "peraPrefecta"
    ],
    "protectors": [
      "kiwiViolinista",
      "maizDirector"
    ],
    "scenarios": [
      {
        "label": "salón gótico del baile de eclipse",
        "prompt": "gothic academy ballroom under eclipse light, black roses, polished marble and cruel social glamour"
      },
      {
        "label": "biblioteca de cuervos y vitrales violetas",
        "prompt": "raven library with violet stained glass, endless books, candlelight and dangerous silence"
      },
      {
        "label": "jardín funerario con estatuas y niebla",
        "prompt": "grave garden with angel statues, low mist, moonlit hedges and aristocratic tension"
      }
    ],
    "conflicts": [
      "un vals prohibido enciende rumores, humillación social y una cercanía que nadie puede negar",
      "la rival organiza una exposición pública para destruir la reputación de la protagonista frente a toda la academia",
      "una nota firmada por el cuervo de medianoche demuestra que la protagonista no era el verdadero monstruo del escándalo"
    ],
    "endings": [
      "venganza elegante",
      "romántico",
      "shock"
    ],
    "ideaSeeds": [
      "Uva cuervo + kiwi violinista + prefecta de pera humillada en el baile de eclipse",
      "Cereza funeraria atrapada entre un rumor gótico y una mirada demasiado cercana en la biblioteca",
      "Director de maíz revelando una prueba brutal en pleno salón de mármol",
      "Jardín con niebla, confesión tensa y un vals que termina en escándalo viral"
    ]
  },
  "laboratorioTormenta": {
    "name": "Corazón de Laboratorio",
    "mood": "creación prohibida, deseo de pertenecer, juicio social y tormentas que despiertan la verdad",
    "moodEn": "forbidden creation, desire to belong, public judgment and storms that awaken the truth",
    "theme": {
      "symbolEs": "el rayo verde",
      "placeEs": "el laboratorio sobre la torre",
      "secretEs": "la costura de cristal",
      "symbolEn": "the green lightning strike",
      "placeEn": "the tower laboratory",
      "secretEn": "the crystal seam"
    },
    "titleTemplates": [
      "{P} despertó con un rayo… y el pueblo quiso llamarla monstruo",
      "La tormenta que unió a {P} con {T} y humilló a {R}",
      "{R} organizó el juicio perfecto… hasta que {P} habló",
      "Nadie imaginó lo que escondía el corazón de laboratorio de {P}"
    ],
    "characters": {
      "manzanaTormenta": {
        "emoji": "🍎",
        "name": "La Manzana de Tormenta",
        "role": "Protagonista",
        "desc": "Humanized female apple creation in a glossy premium 3D cartoon style. Bright crimson apple head with elegant seam details, luminous green eyes, white stitched satin dress, lightning reflections on glossy skin, vulnerable mouth, graceful but newly awakened posture, premium dramatic finish."
      },
      "coliflorDoctora": {
        "emoji": "🥦",
        "name": "La Coliflor Doctora",
        "role": "Protectora",
        "desc": "Humanized female cauliflower doctor in a glossy premium 3D cartoon style. Soft ivory florets, intelligent tired eyes, long dark scientific coat, belted waist, leather gloves, guilt and brilliance in the same face, composed creator energy with refined cinematic polish."
      },
      "cerezaSutura": {
        "emoji": "🍒",
        "name": "La Cereza Sutura",
        "role": "Protectora",
        "desc": "Humanized female cherry seamstress in a glossy premium 3D cartoon style. Twin glossy cherries with delicate stitch motifs, warm ruby eyes, burgundy fitted tailoring apron over a romantic dress, quick hands, loyal compassion, elegant emotional presence."
      },
      "maizTesla": {
        "emoji": "🌽",
        "name": "El Maíz Tesla",
        "role": "Protector",
        "desc": "Humanized male corn electrician in a glossy premium 3D cartoon style. Golden kernel head with blue spark reflections, rolled-up sleeves, utility belt, intense but gentle eyes, strong shoulders, storm-lit protector aura, glossy premium materials."
      },
      "cebollaFiscal": {
        "emoji": "🧅",
        "name": "La Cebolla Fiscal",
        "role": "Rival",
        "desc": "Humanized female onion prosecutor in a glossy premium 3D cartoon style. Layered pearl-purple onion head, razor-sharp eyes, high-collar black legal suit, pointed shoulders, cruelly composed mouth, elite moralist villain energy and polished dramatic authority."
      }
    },
    "protagonists": [
      "manzanaTormenta"
    ],
    "rivals": [
      "cebollaFiscal"
    ],
    "protectors": [
      "coliflorDoctora",
      "cerezaSutura",
      "maizTesla"
    ],
    "scenarios": [
      {
        "label": "laboratorio de torre con bobinas y lluvia",
        "prompt": "storm tower laboratory with electric coils, green lightning, wet windows and forbidden beauty"
      },
      {
        "label": "salón del pueblo con juicio y candelabros",
        "prompt": "village hall with chandeliers, polished wood, judgmental crowd and dramatic candlelight"
      },
      {
        "label": "azotea bajo tormenta con relámpagos verdes",
        "prompt": "rooftop under a violent storm, green lightning, soaked stone and emotionally charged danger"
      }
    ],
    "conflicts": [
      "la protagonista intenta bailar y mostrarse humana, pero el pueblo convierte ese momento en una humillación cruel",
      "la rival usa un juicio público para llamar monstruo a la protagonista y destruir a quien la creó",
      "una costura de cristal y un cuaderno escondido revelan quién fabricó realmente la tragedia"
    ],
    "endings": [
      "trágico",
      "redentor",
      "shock"
    ],
    "ideaSeeds": [
      "Manzana de tormenta humillada en un baile del pueblo y salvada por una doctora brillante",
      "Cereza sutura cosiendo el vestido roto de la protagonista justo antes del juicio público",
      "Cebolla fiscal cayendo ante una prueba imposible en medio del laboratorio bajo lluvia",
      "Azotea con relámpagos verdes, beso no dado y verdad gritada frente al pueblo"
    ]
  },
  "escenarioNeon": {
    "name": "Rey del Escenario de Neón",
    "mood": "fama, coreografías peligrosas, celos mediáticos y deseo contenido detrás del brillo",
    "moodEn": "fame, dangerous choreography, media jealousy and restrained desire behind the glow",
    "theme": {
      "symbolEs": "el paso imposible",
      "placeEs": "el escenario de neón",
      "secretEs": "la cinta perdida del ensayo",
      "symbolEn": "the impossible step",
      "placeEn": "the neon stage",
      "secretEn": "the lost rehearsal tape"
    },
    "titleTemplates": [
      "{P} volvió al escenario… y {R} perdió el control en vivo",
      "El paso imposible de {P} que convirtió la venganza en leyenda",
      "{R} filtró la cinta… pero {T} cambió la coreografía de la noche",
      "La última mirada de {P} antes de hacer temblar el neón"
    ],
    "characters": {
      "mangoLunar": {
        "emoji": "🥭",
        "name": "El Mango Lunar",
        "role": "Protagonista",
        "desc": "Humanized male mango pop icon in a glossy premium 3D cartoon style. Golden-orange mango head with moonlit highlights, sharp soulful eyes, black sequined jacket, fitted pants, iconic glove, magnetic stage stance, sensual but elegant charisma and premium spotlight reflections."
      },
      "cerezaCoreografa": {
        "emoji": "🍒",
        "name": "La Cereza Coreógrafa",
        "role": "Protagonista",
        "desc": "Humanized female cherry choreographer in a glossy premium 3D cartoon style. Twin scarlet cherry silhouette, intense dancer eyes, structured black-red rehearsal outfit, long gloves, high boots, athletic grace, commanding sensual energy and premium polished anatomy."
      },
      "limonSeguridad": {
        "emoji": "🍋",
        "name": "El Limón Seguridad",
        "role": "Protector",
        "desc": "Humanized male lemon bodyguard in a glossy premium 3D cartoon style. Bright lemon head, stern but kind eyes, fitted black suit, earpiece, broad shoulders, controlled calm, protective aura and glossy stage-side cinematic finish."
      },
      "cocoManager": {
        "emoji": "🥥",
        "name": "El Coco Manager",
        "role": "Rival",
        "desc": "Humanized male coconut manager in a glossy premium 3D cartoon style. Split-shell coconut head with polished dark texture, expensive ivory suit, calculating eyes, sleek slicked-back style cues, manipulative executive posture, elegant but cold villain presence."
      },
      "duraznoInfluencer": {
        "emoji": "🍑",
        "name": "El Durazno Influencer",
        "role": "Rival",
        "desc": "Humanized male peach social-media rival in a glossy premium 3D cartoon style. Velvety peach head, dazzling smile, designer street-lux outfit, jeweled shades, vain body language, seductive self-obsession and glossy camera-ready perfection."
      }
    },
    "protagonists": [
      "mangoLunar",
      "cerezaCoreografa"
    ],
    "rivals": [
      "cocoManager",
      "duraznoInfluencer"
    ],
    "protectors": [
      "limonSeguridad",
      "cerezaCoreografa"
    ],
    "scenarios": [
      {
        "label": "escenario de neón con humo y gritos del público",
        "prompt": "neon concert stage with crowd lights, drifting smoke, reflective floor and explosive performance energy"
      },
      {
        "label": "backstage de espejos con maquillaje corrido",
        "prompt": "mirror-filled backstage corridor with smeared makeup, costume racks and emotionally dangerous glamour"
      },
      {
        "label": "azotea del estadio con ciudad brillante",
        "prompt": "stadium rooftop overlooking a glowing city, wind-blown fabric, neon spill light and intimate aftershow tension"
      }
    ],
    "conflicts": [
      "una cinta filtrada del ensayo intenta arruinar el regreso del protagonista justo antes del show más importante",
      "el rival quiere controlar la carrera y el cuerpo de la estrella con manipulación, chantaje y vergüenza pública",
      "la coreografía final esconde una respuesta emocional que puede humillar al traidor frente a todo el estadio"
    ],
    "endings": [
      "redentor",
      "humillante para el rival",
      "cliffhanger"
    ],
    "ideaSeeds": [
      "Mango lunar + cereza coreógrafa + coco manager caído en vivo ante todo el estadio",
      "Durazno influencer saboteando un regreso y terminando expuesto por una cinta inesperada",
      "Limón seguridad mirando desde backstage hasta decidir intervenir con una verdad brutal",
      "Azotea del estadio con abrazo tenso, lluvia de flashes y promesa de segunda parte"
    ]
  },
  "bosqueDorado": {
    "name": "Bosque Dorado de los Forajidos",
    "mood": "rebelión elegante, robo justo, flechas románticas y humillación para el poder corrupto",
    "moodEn": "elegant rebellion, righteous theft, romantic arrows and humiliation for corrupt power",
    "theme": {
      "symbolEs": "la flecha de miel",
      "placeEs": "el bosque dorado",
      "secretEs": "el botín del mercado",
      "symbolEn": "the honey arrow",
      "placeEn": "the golden forest",
      "secretEn": "the stolen market tribute"
    },
    "titleTemplates": [
      "{P} robó una sola moneda… y se convirtió en el terror elegante de {R}",
      "Cuando {T} apuntó su flecha por {P}, el bosque dorado cambió de dueño",
      "{R} quiso cobrar humillación… y terminó pagando con orgullo",
      "La rebelión de {P} bajo los árboles de oro"
    ],
    "characters": {
      "peraArquera": {
        "emoji": "🍐",
        "name": "La Pera Arquera",
        "role": "Protagonista",
        "desc": "Humanized female pear archer in a glossy premium 3D cartoon style. Smooth green pear head, fierce emerald eyes, fitted hooded forest outfit, leather bracers, bow on her back, athletic elegance, protective sensual confidence and polished heroic detail."
      },
      "arandanoPrincipe": {
        "emoji": "🫐",
        "name": "El Arándano Príncipe",
        "role": "Protagonista",
        "desc": "Humanized male blueberry prince in a glossy premium 3D cartoon style. Glossy midnight-blue berry head, thoughtful royal eyes, dark velvet riding coat, hidden crest, restrained nobility, soft vulnerability and premium cinematic grace."
      },
      "aguacateForajido": {
        "emoji": "🥑",
        "name": "El Aguacate Forajido",
        "role": "Protector",
        "desc": "Humanized male avocado outlaw in a glossy premium 3D cartoon style. Dark green avocado head with lighter face area, intense protective eyes, rugged forest coat, open collar, leather straps, quiet bad-boy warmth, tall silhouette and premium polished finish."
      },
      "lechugaSanadora": {
        "emoji": "🥬",
        "name": "La Lechuga Sanadora",
        "role": "Protectora",
        "desc": "Humanized female lettuce healer in a glossy premium 3D cartoon style. Layered emerald lettuce head, calm luminous eyes, flowing cream-green cloak, herb satchel, gentle hands, soft wise beauty and polished magical realism energy."
      },
      "limonSheriff": {
        "emoji": "🍋",
        "name": "El Limón Sheriff",
        "role": "Rival",
        "desc": "Humanized male lemon sheriff in a glossy premium 3D cartoon style. Bright yellow lemon head, cruel narrowed eyes, expensive military-green coat, polished badge, riding boots, rigid posture, smug authority and premium villain shine."
      }
    },
    "protagonists": [
      "peraArquera",
      "arandanoPrincipe"
    ],
    "rivals": [
      "limonSheriff"
    ],
    "protectors": [
      "aguacateForajido",
      "lechugaSanadora"
    ],
    "scenarios": [
      {
        "label": "bosque dorado con hojas brillantes y arcos tensos",
        "prompt": "golden forest with glowing leaves, stretched bowstrings, warm sunset haze and outlaw tension"
      },
      {
        "label": "mercado saqueado con guardias y gritos",
        "prompt": "looted market square with banners, guards, scattered fruit tribute and public outrage"
      },
      {
        "label": "casa del árbol rebelde con mapas y velas",
        "prompt": "rebel treehouse filled with maps, candles, stolen tribute and intimate planning energy"
      }
    ],
    "conflicts": [
      "el sheriff humilla a los pobres del mercado y obliga al protagonista a robar delante de todos",
      "una flecha marcada y un botín escondido revelan que el verdadero ladrón no era quien todos creían",
      "el protector arriesga su libertad por la protagonista justo cuando el bosque se llena de cazadores"
    ],
    "endings": [
      "romántico",
      "venganza elegante",
      "redentor"
    ],
    "ideaSeeds": [
      "Pera arquera + aguacate forajido + sheriff limón humillado con una flecha frente al mercado",
      "Arándano príncipe escondiendo su identidad mientras roba para salvar al pueblo",
      "Lechuga sanadora curando una herida íntima en la casa del árbol antes del gran robo",
      "Mercado saqueado, beso interrumpido y botín que demuestra una verdad imposible de negar"
    ]
  },
  "astroJardin": {
    "name": "El Príncipe del Jardín Miniatura",
    "mood": "poesía emocional, orgullo delicado, viajes entre asteroides y amor que se entiende demasiado tarde",
    "moodEn": "emotional poetry, delicate pride, asteroid travel and love understood too late",
    "theme": {
      "symbolEs": "la rosa diminuta",
      "placeEs": "el jardín de los asteroides",
      "secretEs": "la ruta de semillas",
      "symbolEn": "the tiny rose",
      "placeEn": "the asteroid garden",
      "secretEn": "the seed trail"
    },
    "titleTemplates": [
      "{P} dejó su rosa… y descubrió demasiado tarde lo que valía",
      "El jardín miniatura donde {P} aprendió a mirar de verdad",
      "{R} intentó reírse de {P} frente a las estrellas… y el silencio lo venció",
      "La despedida de {P} que convirtió una herida en universo"
    ],
    "characters": {
      "duraznoPrincipe": {
        "emoji": "🍑",
        "name": "El Durazno Príncipe",
        "role": "Protagonista",
        "desc": "Humanized male peach prince in a glossy premium 3D cartoon style. Velvety peach head with warm blush, wide reflective eyes, tiny golden scarf, tailored celestial coat, gentle posture, innocent but growing emotional depth, premium dreamy lighting."
      },
      "tomateRosa": {
        "emoji": "🍅",
        "name": "La Tomate Rosa",
        "role": "Protagonista",
        "desc": "Humanized female rose-tomato diva in a glossy premium 3D cartoon style. Glossy pink-red tomato head with petal-like top leaves, proud luminous eyes, romantic sculpted dress, delicate heels, dramatic vanity mixed with fragility, premium poetic glow."
      },
      "kiwiViajero": {
        "emoji": "🥝",
        "name": "El Kiwi Viajero",
        "role": "Protector",
        "desc": "Humanized male kiwi traveler in a glossy premium 3D cartoon style. Fuzzy kiwi head, dusty cloak, wise amused eyes, traveler boots, seed compass, calm protective body language, nomad charm and polished cosmic finish."
      },
      "maizAstral": {
        "emoji": "🌽",
        "name": "La Maíz Astral",
        "role": "Protectora",
        "desc": "Humanized female cosmic corn astronomer in a glossy premium 3D cartoon style. Golden kernel crown with star-like sparkle, flowing midnight cape, observant eyes, luminous charts, elegant serene posture and premium celestial sheen."
      },
      "cocoMeteorito": {
        "emoji": "🥥",
        "name": "El Coco Meteorito",
        "role": "Rival",
        "desc": "Humanized male coconut merchant in a glossy premium 3D cartoon style. Dark shell-textured head with sharp metallic accents, jeweled space coat, sly smile, greedy cosmic trader energy, polished villain glamour and cold confidence."
      }
    },
    "protagonists": [
      "duraznoPrincipe",
      "tomateRosa"
    ],
    "rivals": [
      "cocoMeteorito"
    ],
    "protectors": [
      "kiwiViajero",
      "maizAstral"
    ],
    "scenarios": [
      {
        "label": "asteroide pequeño con una rosa y tres volcanes",
        "prompt": "tiny asteroid garden with one proud rose, three miniature volcanoes, starlight and poetic loneliness"
      },
      {
        "label": "mercado cósmico de faroles flotantes",
        "prompt": "cosmic market with floating lanterns, drifting seeds, glowing stalls and bittersweet wonder"
      },
      {
        "label": "desierto estelar con constelaciones bajas",
        "prompt": "star desert with low constellations, silver sand, wind trails and fragile emotional distance"
      }
    ],
    "conflicts": [
      "un malentendido orgulloso hace que la protagonista deje a quien ama justo antes de un viaje sin regreso claro",
      "el rival quiere comprar la rosa diminuta y humilla públicamente su valor frente a todo el mercado cósmico",
      "una ruta de semillas revela que el verdadero abandono no fue físico, sino emocional"
    ],
    "endings": [
      "poético",
      "romántico",
      "redentor"
    ],
    "ideaSeeds": [
      "Durazno príncipe + tomate rosa + kiwi viajero + despedida entre estrellas",
      "Maíz astral guiando a un protagonista herido hacia una verdad delicada y fuerte",
      "Coco meteorito intentando comprar amor y quedando humillado en el mercado cósmico",
      "Asteroide pequeño, mirada final y una rosa que vale más que cualquier tesoro"
    ]
  }
};
const EMOTIONS = {
  "atraccion": {
    "es": "atracción peligrosa, miradas largas, cercanía tensa y deseo contenido",
    "en": "dangerous attraction, lingering eye contact, charged closeness and restrained desire"
  },
  "celos": {
    "es": "celos elegantes, orgullo herido y rabia contenida detrás de una sonrisa",
    "en": "elegant jealousy, bruised pride and controlled rage behind a polished smile"
  },
  "tristeza": {
    "es": "tristeza devastadora, silencio pesado y corazón roto a plena vista",
    "en": "devastating sadness, heavy silence and heartbreak exposed in public"
  },
  "venganza": {
    "es": "venganza fría, inteligente y deliciosamente humillante",
    "en": "cold, intelligent revenge with a deliciously humiliating payoff"
  },
  "suspenso": {
    "es": "suspenso asfixiante, presión social y peligro emocional inminente",
    "en": "suffocating suspense, social pressure and imminent emotional danger"
  },
  "ternura": {
    "es": "ternura inesperada, protección sincera y química suave pero poderosa",
    "en": "unexpected tenderness, sincere protection and soft but powerful chemistry"
  },
  "verguenza": {
    "es": "vergüenza pública intensa, exposición dolorosa y dignidad en riesgo",
    "en": "intense public shame, painful exposure and dignity at risk"
  },
  "enojo": {
    "es": "enojo explosivo, energía de choque y palabras capaces de romperlo todo",
    "en": "explosive anger, collision energy and words sharp enough to break everything"
  }
};
const CONFLICT_ARCHETYPES = [
  "una carta, cinta, flor o prueba oculta cae en las manos equivocadas y enciende el escándalo",
  "una humillación elegante frente al público obliga al protagonista a dejar de fingir fortaleza",
  "el rival usa cercanía, estatus y manipulación emocional para intentar recuperar el control",
  "un secreto de identidad, origen o lealtad estalla en el peor momento posible",
  "la presencia del protector cambia por completo la jerarquía del conflicto social",
  "la protagonista descubre demasiado tarde que el rumor viral venía de alguien que decía amarla"
];
const ENDINGS = {
  "redentor": {
    "es": "redentor, poderoso y emocional, con la dignidad del protagonista restaurada",
    "en": "redemptive, powerful and emotional, restoring the protagonist's dignity"
  },
  "romántico": {
    "es": "romántico, cálido y protector, con una elección basada en paz y respeto",
    "en": "romantic, warm and protective, built on peace, tenderness and respect"
  },
  "trágico": {
    "es": "trágico y melancólico, con una victoria costosa y una herida que no cierra del todo",
    "en": "tragic and melancholic, with a costly victory and wounds that do not fully close"
  },
  "cliffhanger": {
    "es": "abierto con cliffhanger, dejando una nueva amenaza o revelación para la siguiente parte",
    "en": "open-ended with a cliffhanger, leaving a fresh threat or revelation for the next part"
  },
  "shock": {
    "es": "de shock total, con una revelación que cambia todo en el último momento",
    "en": "full shock ending with a revelation that changes everything at the last second"
  },
  "venganza elegante": {
    "es": "de venganza elegante, con humillación inteligente para quien causó el daño",
    "en": "elegant revenge with smart humiliation for the one who caused the damage"
  },
  "humillante para el rival": {
    "es": "humillante para el rival, que termina derrotado ante todos",
    "en": "humiliating for the rival, who ends up defeated in front of everyone"
  },
  "humillante para la protagonista": {
    "es": "amargo y humillante para la protagonista, obligándola a aprender una lección dura",
    "en": "bitter and humiliating for the protagonist, forcing a hard emotional lesson"
  },
  "poético": {
    "es": "poético y melancólico, con una verdad delicada que deja eco emocional",
    "en": "poetic and melancholic, leaving behind a delicate truth and emotional afterglow"
  }
};
const FULL_SCENE_BLUEPRINTS = [
  {
    "name": "Hook viral",
    "type": "CON DIÁLOGO — Golpe inicial",
    "beat": "an explosive opening drenched in public humiliation, sharp chemistry and instant scandal",
    "cam": "fast push-in from dramatic wide shot to a tense medium close-up",
    "motion": "rival steps forward, protagonist freezes for half a beat, the crowd turns and fabric reacts to the wind",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival"
    ],
    "summary": "{R} invade {SC} y abre la historia con una frase cruel que deja a {P} en el centro del escándalo.",
    "hook": "La humillaron en el primer segundo… y todos se quedaron mirando.",
    "direction": "{R} corners {P} in front of a frozen crowd, invading personal space with sharp body language and intense eye contact."
  },
  {
    "name": "La mirada que delata todo",
    "type": "CON DIÁLOGO — La herida respira",
    "beat": "the protagonist tries to stay composed while hidden desire, shame and pride collide",
    "cam": "slow emotional push-in from medium shot to close-up",
    "motion": "shaky breathing, trembling fingers, wet eyes and a stubborn chin refusing to collapse",
    "speaker": "protagonist",
    "activeRoles": [
      "protagonist",
      "rival"
    ],
    "summary": "{P} intenta sostener la compostura, pero la tensión íntima bajo la superficie se vuelve imposible de esconder.",
    "hook": "No era solo pelea: había una energía peligrosa que nadie supo ignorar.",
    "direction": "{P} holds eye contact while shaky breathing, trembling fingers and a stubborn chin reveal hidden vulnerability."
  },
  {
    "name": "El rival marca territorio",
    "type": "CON DIÁLOGO — La amenaza toma forma",
    "beat": "the rival escalates the conflict and makes the whole place feel like a stage they own",
    "cam": "slow lateral pan following the rival's dominant movement",
    "motion": "rival circles the protagonist, straightens clothing, points subtly and controls the spacing",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival"
    ],
    "summary": "{R} marca territorio con una amenaza elegante y hace sentir que todo el lugar le pertenece.",
    "hook": "{R} creyó que podía seguir mandando con una sola mirada.",
    "direction": "{R} circles around {P} as if claiming the scene, forcing everyone to witness the imbalance of power."
  },
  {
    "name": "Humillación elegante",
    "type": "CON DIÁLOGO — La burla arde",
    "beat": "social humiliation spreads and the protagonist feels the sting of public exposure",
    "cam": "tight medium shot with a slow zoom and background whispers",
    "motion": "crowd whispers, shoulders tighten, a forced smile cracks and the body absorbs the blow",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival"
    ],
    "summary": "La burla se vuelve pública y {P} siente el peso de la vergüenza mientras el rumor corre como fuego.",
    "hook": "Pensaron que {P} iba a bajar la cabeza… justo antes de que todo cambiara.",
    "direction": "{P} absorbs the public sting while whispers spread, shoulders tighten and the camera catches the flush of humiliation."
  },
  {
    "name": "Entrada del protector",
    "type": "CON DIÁLOGO — Cambia el tablero",
    "beat": "the protector enters and instantly rewrites the emotional hierarchy of the scene",
    "cam": "heroic reveal pan from the rival to the protector",
    "motion": "protector enters calmly, steps between them, coat and hair settle with cinematic weight",
    "speaker": "protector",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "{T} entra sin anunciarse y el equilibrio emocional de la historia cambia en un instante.",
    "hook": "Apareció en silencio… y el aire dejó de sentirse seguro para el rival.",
    "direction": "{T} enters the frame with quiet authority, placing their body between {P} and {R} without breaking elegance."
  },
  {
    "name": "El gesto cercano",
    "type": "CON DIÁLOGO — Tensión sugerente",
    "beat": "a subtle protective gesture creates intimacy, safety and restrained sensual tension",
    "cam": "intimate medium close-up with shallow depth of field",
    "motion": "small lean-in, controlled hand movement, breath proximity and a charged pause",
    "speaker": "protector",
    "activeRoles": [
      "protagonist",
      "protector"
    ],
    "summary": "Un gesto cercano entre {P} y {T} despierta una tensión nueva: cuidado, deseo contenido y confianza.",
    "hook": "Una sola cercanía hizo más ruido que todos los gritos.",
    "direction": "{T} leans closer to {P} just enough to create safety, intimacy and restrained sensual tension without any explicit contact."
  },
  {
    "name": "Plan secreto",
    "type": "CON DIÁLOGO — La verdad empieza a moverse",
    "beat": "the protagonist and protector uncover a clue, secret plan or hidden proof against the rival",
    "cam": "over-the-shoulder reveal moving into a secretive two-shot",
    "motion": "a hidden note, tape, flower or object changes hands while eyes dart and breathing stays tight",
    "speaker": "protagonist",
    "activeRoles": [
      "protagonist",
      "protector"
    ],
    "summary": "{P} y {T} descubren una pista, una prueba o un secreto que puede destruir a {R}.",
    "hook": "La verdad no llegó gritando: llegó en forma de prueba.",
    "direction": "{P} and {T} exchange a secret plan, a found clue or a hidden message while the world around them turns suspicious."
  },
  {
    "name": "Primer giro inesperado",
    "type": "CON DIÁLOGO — El rival aún respira",
    "beat": "when the heroes think they have control, the rival reveals a deeper card and regains momentum",
    "cam": "snap zoom to the rival's face followed by reaction cuts",
    "motion": "rival smirks, reveals an object or secret, crowd reacts and the protagonist recoils",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "Cuando todo parece controlado, un giro inesperado demuestra que {R} todavía guarda una carta peligrosa.",
    "hook": "Creían que el rival había perdido… hasta que lanzó la herida exacta.",
    "direction": "{R} suddenly reveals a sharper move, exposing a secret or manipulating the crowd to regain emotional control."
  },
  {
    "name": "Noche de tensión máxima",
    "type": "CON DIÁLOGO — Punto de no retorno",
    "beat": "the atmosphere becomes unbearably charged and every glance feels irreversible",
    "cam": "slow circular dolly around the three characters",
    "motion": "breath syncs, half steps collide, eyes lock and no one dares to blink first",
    "speaker": "protagonist",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "La noche alcanza su punto más alto de tensión y cada mirada parece una decisión irreversible.",
    "hook": "Lo que pasó después fue demasiado íntimo para ser un simple conflicto.",
    "direction": "{P}, {R} and {T} share the same charged frame; every glance, breath and half-step feels like a point of no return."
  },
  {
    "name": "La traición se revela",
    "type": "CON DIÁLOGO — Máscara rota",
    "beat": "the betrayal surfaces completely and the rival's polished performance begins to crack",
    "cam": "rapid push-in to the reveal object, then reaction close-ups",
    "motion": "hands shake, posture cracks, the rival tries to recover and fails in front of the crowd",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "La traición se revela por completo y el teatro emocional de {R} queda al descubierto.",
    "hook": "La mentira estaba impecable… hasta que alguien tiró del hilo correcto.",
    "direction": "{R} loses the mask as the betrayal surfaces, hands shaking, posture cracking and polished confidence slipping away."
  },
  {
    "name": "Caída o humillación final",
    "type": "CON DIÁLOGO — El fondo duele",
    "beat": "the protagonist hits emotional bottom or faces the final social humiliation before transforming",
    "cam": "slow drop from eye level to a low emotional angle",
    "motion": "tears, clenched jaw, a bent posture that slowly straightens into resolve",
    "speaker": "protagonist",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "{P} toca fondo o enfrenta la humillación final, pero ese dolor le da la fuerza que antes no tenía.",
    "hook": "La peor caída de {P} fue también su manera de levantarse.",
    "direction": "{P} reaches the emotional bottom, then straightens up with tears, anger or calm determination transforming the body language."
  },
  {
    "name": "La prueba imposible",
    "type": "CON DIÁLOGO — Verdad total",
    "beat": "the protector presents undeniable proof and the lie collapses in public",
    "cam": "centered medium-wide shot tightening toward the evidence",
    "motion": "proof is displayed, the crowd gasps, the rival freezes and silence floods the frame",
    "speaker": "protector",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "{T} muestra la prueba imposible de negar y deja a {R} sin refugio frente a todos.",
    "hook": "Una sola prueba bastó para destruir un personaje entero.",
    "direction": "{T} presents undeniable proof, forcing the crowd to watch the collapse of the lie in real time."
  },
  {
    "name": "Decisión que rompe el destino",
    "type": "CON DIÁLOGO — Corte final",
    "beat": "the protagonist makes the irreversible choice that finally ends the emotional trap",
    "cam": "cinematic push-in centered on the protagonist's decisive gesture",
    "motion": "one final step, a lifted chin, a hand released or taken and a voice that no longer shakes",
    "speaker": "protagonist",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "{P} toma la decisión definitiva y corta la historia por el lugar donde más dolía.",
    "hook": "La frase final de {P} cambió el destino de todos.",
    "direction": "{P} makes the final choice with a powerful gesture, a decisive step and a voice that no longer trembles."
  },
  {
    "name": "Consecuencia emocional",
    "type": "CON DIÁLOGO — El perdedor entiende",
    "beat": "the emotional winner and loser are now visible and the defeat lands with full weight",
    "cam": "slow pull-back widening the space between characters",
    "motion": "rival remains isolated, breathing broken, while the new alliance holds center frame",
    "speaker": "rival",
    "activeRoles": [
      "protagonist",
      "rival",
      "protector"
    ],
    "summary": "El perdedor procesa la derrota y entiende, demasiado tarde, que la historia ya no le pertenece.",
    "hook": "Lo más fuerte no fue el grito… fue la cara del que se quedó sin control.",
    "direction": "{R} is left isolated inside the frame while {P} and {T} occupy the emotional center with new power dynamics."
  },
  {
    "name": "Cierre Johan",
    "type": "CON DIÁLOGO — Eco viral",
    "beat": "the final image leaves a strong lesson, emotional aftershock and sequel potential",
    "cam": "epic final pull-back with dramatic light shaping the last tableau",
    "motion": "the survivors walk away, hold eye contact or leave a symbolic object behind as the atmosphere seals the ending",
    "speaker": "narrator",
    "activeRoles": [
      "protagonist",
      "protector"
    ],
    "summary": "La historia cierra con eco viral, una lección emocional clara y una imagen imposible de olvidar.",
    "hook": "Y ahí fue cuando la herida se convirtió en leyenda.",
    "direction": "{P} and {T}, or the surviving cast, leave behind an unforgettable final tableau filled with aftershock, dignity and cinematic closure."
  }
];
const SCENE_MAPS = {
  "10": [
    0,
    1,
    2,
    3,
    4,
    7,
    9,
    11,
    12,
    14
  ],
  "11": [
    0,
    1,
    2,
    3,
    4,
    5,
    7,
    9,
    11,
    12,
    14
  ],
  "12": [
    0,
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    9,
    11,
    12,
    14
  ],
  "13": [
    0,
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    8,
    9,
    11,
    12,
    14
  ],
  "14": [
    0,
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    8,
    9,
    10,
    11,
    12,
    14
  ],
  "15": [
    0,
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    8,
    9,
    10,
    11,
    12,
    13,
    14
  ]
};
const VOICE_BANK = {
  "protagonist": [
    "No pienso seguir respirando culpa solo para que {R} se sienta poderoso.",
    "Si esta noche tengo que perder algo, prefiero perder el miedo antes que volver a perderme a mí.",
    "Te di silencio demasiado tiempo, pero ya no voy a esconder lo que sentí en {PLACE}.",
    "Usaste {SYMBOL} para hacerme temblar, pero hoy lo miro de frente y ya no me controla."
  ],
  "rival": [
    "No conviertas esto en un espectáculo, {P}, porque todavía sé exactamente dónde te duele.",
    "Todo este lugar me vio construir tu historia; no me vas a borrar con una sola mirada.",
    "Si te vas con {T}, conviertes mi orgullo en guerra y no pienso fingir calma.",
    "Nadie me deja como villano en {PLACE} sin escuchar primero lo que todavía tengo para decir."
  ],
  "protector": [
    "Baja la voz y da un paso atrás. No vuelvas a usar la vergüenza para tocar lo que ya no te pertenece.",
    "Respira, {P}. No necesitas demostrar nada mientras yo esté mirando de frente.",
    "Hoy se termina tu teatro, {R}. La cercanía no te pertenece solo porque la exijas.",
    "No voy a dejar que conviertas {SYMBOL} en otra cicatriz para {P}."
  ],
  "narrator": [
    "En {PLACE}, la herida dejó de ser secreto y se volvió una verdad imposible de esconder.",
    "Esa noche no ganó quien gritó más; ganó quien por fin sostuvo su propia mirada.",
    "Hay historias que nacen del escándalo y terminan convertidas en leyenda emocional.",
    "Lo viral no fue la caída: fue el instante en que {P} dejó de temblar delante de {R}."
  ]
};
const GLOBAL_IDEA_SEEDS = [
  "Fresa pasiva + melón bad boy + pimiento aristócrata + una rosa que delata todo",
  "Durazno influencer + coco manager rival + limón seguridad silencioso + cinta filtrada",
  "Pera desesperada + kiwi protector + calabaza del revés + portal emocional",
  "Manzana de tormenta + cereza sutura + cebolla fiscal cruel + baile bajo relámpagos",
  "Tomate rosa orgullosa + durazno príncipe + maíz astral + despedida con eco poético",
  "Arándano príncipe + aguacate forajido + sheriff de limón + mercado robado al amanecer",
  "Uva gótica + pera perfecta + kiwi violinista + humillación en un vals de eclipse",
  "Mora eléctrica + durazno sísmico + mentor de maíz + prueba escondida entre enredaderas"
];

const selects = {
  universe: document.getElementById('universe'),
  protagonist: document.getElementById('protagonist'),
  rival: document.getElementById('rival'),
  protector: document.getElementById('protector'),
  emotion: document.getElementById('emotion'),
  conflict: document.getElementById('conflict'),
  scenario: document.getElementById('scenario'),
  ending: document.getElementById('ending'),
  sceneCount: document.getElementById('sceneCount'),
  visualStyle: document.getElementById('visualStyle')
};

let currentStory = null;

function titleCase(text) {
  return text.charAt(0).toUpperCase() + text.slice(1);
}

function randomOf(arr) {
  return arr[Math.floor(Math.random() * arr.length)];
}

function shuffleCopy(arr) {
  const copy = [...arr];
  for (let i = copy.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [copy[i], copy[j]] = [copy[j], copy[i]];
  }
  return copy;
}

function uniqueChars(arr) {
  const seen = new Set();
  return arr.filter(char => {
    if (!char || seen.has(char.name)) return false;
    seen.add(char.name);
    return true;
  });
}

function applyTemplate(text, data) {
  return String(text).replace(/\{(\w+)\}/g, (_, key) => data[key] ?? ('{' + key + '}'));
}

function populateUniverseOptions() {
  Object.entries(UNIVERSES).forEach(([key, uni]) => {
    const opt = document.createElement('option');
    opt.value = key;
    opt.textContent = uni.name;
    selects.universe.appendChild(opt);
  });
}

function populateSceneCounts() {
  [10, 11, 12, 13, 14, 15].forEach(n => {
    const opt = document.createElement('option');
    opt.value = String(n);
    opt.textContent = `${n} escenas`;
    selects.sceneCount.appendChild(opt);
  });
  selects.sceneCount.value = '12';
}

function populateVisualStyles() {
  VISUAL_STYLES.forEach((style, idx) => {
    const opt = document.createElement('option');
    opt.value = style;
    opt.textContent = idx === 0 ? 'Glossy 3D Premium Base' : `Variación ${idx}`;
    selects.visualStyle.appendChild(opt);
  });
}

function populateEmotionOptions() {
  Object.keys(EMOTIONS).forEach(key => {
    const opt = document.createElement('option');
    opt.value = key;
    opt.textContent = titleCase(key);
    selects.emotion.appendChild(opt);
  });
  selects.emotion.value = 'suspenso';
}

function fillSelect(select, ids, chars) {
  select.innerHTML = '';
  ids.forEach(id => {
    const c = chars[id];
    const opt = document.createElement('option');
    opt.value = id;
    opt.textContent = `${c.emoji} ${c.name}`;
    select.appendChild(opt);
  });
}

function fillArraySelect(select, arr) {
  select.innerHTML = '';
  arr.forEach((item, idx) => {
    const opt = document.createElement('option');
    opt.value = String(idx);
    opt.textContent = typeof item === 'string' ? item : item.label;
    select.appendChild(opt);
  });
}

function getArrayItem(arr, value) {
  const idx = Number(value);
  if (!Number.isNaN(idx) && arr[idx] !== undefined) return arr[idx];
  return arr[0];
}

function refreshControls() {
  const uni = UNIVERSES[selects.universe.value];
  fillSelect(selects.protagonist, uni.protagonists, uni.characters);
  fillSelect(selects.rival, uni.rivals, uni.characters);
  fillSelect(selects.protector, uni.protectors, uni.characters);
  fillArraySelect(selects.scenario, uni.scenarios);
  fillArraySelect(selects.conflict, [...uni.conflicts, ...CONFLICT_ARCHETYPES]);
  fillArraySelect(selects.ending, [...new Set([...uni.endings, ...Object.keys(ENDINGS)])]);
}

function getTemplateDataEs(uni, protagonist, rival, protector, scenario) {
  return {
    P: protagonist.name,
    R: rival.name,
    T: protector.name,
    U: uni.name,
    SC: scenario.label,
    PLACE: uni.theme.placeEs,
    SYMBOL: uni.theme.symbolEs,
    SECRET: uni.theme.secretEs
  };
}

function buildTitle(uni, protagonist, rival, protector, scenario, endingKey) {
  const data = getTemplateDataEs(uni, protagonist, rival, protector, scenario);
  return applyTemplate(randomOf(uni.titleTemplates), data);
}

function buildPremise(uni, protagonist, rival, protector, emotion, conflict, scenario, ending) {
  return `${protagonist.name} entra en ${uni.name}, un universo de ${uni.mood}, donde ${conflict}. Todo estalla en ${scenario.label}, mientras ${rival.name} intenta dominar la narrativa con estatus, cercanía y presión emocional. ${protector.name} altera la energía con presencia magnética, protección real y una tensión sugerente que nunca cruza lo explícito. La historia crece con ${emotion.es} y termina con un cierre ${ending.es}.`;
}

function getBlueprints(count) {
  const map = SCENE_MAPS[String(count)] || SCENE_MAPS['15'];
  return map.map(idx => FULL_SCENE_BLUEPRINTS[idx]);
}

function selectSceneCharacters(blueprint, protagonist, rival, protector) {
  const roleMap = { protagonist, rival, protector };
  return uniqueChars(blueprint.activeRoles.map(role => roleMap[role]));
}

function chooseVoice(role, data) {
  const safeRole = VOICE_BANK[role] ? role : 'narrator';
  const line = applyTemplate(randomOf(VOICE_BANK[safeRole]), data);
  if (safeRole === 'protagonist') return { label: `${data.P} habla`, line };
  if (safeRole === 'rival') return { label: `${data.R} habla`, line };
  if (safeRole === 'protector') return { label: `${data.T} habla`, line };
  return { label: 'Narración de cierre', line };
}

function buildImagePrompt(scene, context) {
  const emotional = scene.index === context.count ? context.ending.en : context.emotion.en;
  const castLock = context.cast.map(char => `${char.name}: ${char.desc}`).join(' ');
  const activeCast = scene.characters.map(char => char.name).join(', ');
  return `A ${context.style}. ${context.scenario.prompt}. Universe mood: ${context.uni.moodEn}. Character consistency lock: ${castLock} Active characters in this scene: ${activeCast}. Story beat: ${scene.blueprint.beat}. Scene direction: ${scene.direction}. Emotional tone: ${emotional}. Include subtle sensual tension through eye contact, elegant closeness and charged body language, with no explicit content. Premium glossy materials, expressive faces, cinematic composition, dramatic lighting, polished stylized anatomy, strong depth of field, strict continuity of wardrobe and colors, vertical 9:16.`;
}

function buildVideoPrompt(scene, context) {
  const emotional = scene.index === context.count ? context.ending.en : context.emotion.en;
  const castLock = context.cast.map(char => `${char.name}: ${char.desc}`).join(' ');
  return `${context.style}. ${context.scenario.prompt}. Continuity lock: ${castLock} Scene ${scene.index} — ${scene.blueprint.name}. Camera: ${scene.blueprint.cam}. Motion: ${scene.blueprint.motion}. Direction: ${scene.direction}. Emotional direction: ${emotional}. Preserve exact face shapes, colors, outfits, accessories and scale in every shot. Cinematic timing, premium glossy finish, clean motion, viral vertical framing, 9:16.`;
}

function buildIdeaCombos(uni, protagonist, rival, protector) {
  const moodKeys = Object.keys(EMOTIONS);
  const selectedScenario = randomOf(uni.scenarios).label;
  const endingKeys = uni.endings.length ? uni.endings : Object.keys(ENDINGS);
  const pool = [
    `Combo actual: ${protagonist.name} + ${protector.name} + ${rival.name} + giro en ${selectedScenario}.`,
    `Parte 2: ${protagonist.name} regresa con final ${ENDINGS[randomOf(endingKeys)].es}.`,
    `Versión alternativa: cambia la emoción dominante a ${titleCase(randomOf(moodKeys))} y sube la tensión social.`,
    `Nueva humillación viral: ${protagonist.name} enfrenta otra trampa preparada por ${rival.name} en ${randomOf(uni.scenarios).label}.`,
    ...uni.ideaSeeds,
    ...GLOBAL_IDEA_SEEDS
  ];
  return Array.from(new Set(shuffleCopy(pool))).slice(0, 10);
}

function buildStory() {
  const uni = UNIVERSES[selects.universe.value];
  const protagonist = uni.characters[selects.protagonist.value];
  const rival = uni.characters[selects.rival.value];
  const protector = uni.characters[selects.protector.value];
  const emotion = EMOTIONS[selects.emotion.value];
  const conflict = getArrayItem([...uni.conflicts, ...CONFLICT_ARCHETYPES], selects.conflict.value);
  const scenario = getArrayItem(uni.scenarios, selects.scenario.value);
  const endingOptions = [...new Set([...uni.endings, ...Object.keys(ENDINGS)])];
  const endingKey = getArrayItem(endingOptions, selects.ending.value);
  const ending = ENDINGS[endingKey] || { es: endingKey, en: endingKey };
  const count = parseInt(selects.sceneCount.value, 10);
  const style = selects.visualStyle.value;
  const cast = uniqueChars([protagonist, rival, protector]);
  const templateData = getTemplateDataEs(uni, protagonist, rival, protector, scenario);

  const title = buildTitle(uni, protagonist, rival, protector, scenario, endingKey);
  const premise = buildPremise(uni, protagonist, rival, protector, emotion, conflict, scenario, ending);
  const blueprints = getBlueprints(count);

  const scenes = blueprints.map((blueprint, idx) => {
    const index = idx + 1;
    const sceneData = { ...templateData, IDX: String(index) };
    const direction = applyTemplate(blueprint.direction, sceneData);
    const summary = applyTemplate(blueprint.summary, sceneData);
    const hook = applyTemplate(blueprint.hook, sceneData);
    const voice = chooseVoice(blueprint.speaker, sceneData);
    const scene = {
      index,
      blueprint,
      type: blueprint.type,
      duration: '~10 segundos',
      characters: selectSceneCharacters(blueprint, protagonist, rival, protector),
      direction,
      summary,
      hook,
      voiceLabel: voice.label,
      lipsync: voice.line
    };
    scene.imagePrompt = buildImagePrompt(scene, { uni, protagonist, rival, protector, emotion, scenario, ending, count, style, cast });
    scene.videoPrompt = buildVideoPrompt(scene, { uni, protagonist, rival, protector, emotion, scenario, ending, count, style, cast });
    return scene;
  });

  const hooks = scenes.map(scene => ({
    title: `ESCENA ${scene.index} — ${scene.blueprint.name}`,
    text: scene.hook
  }));

  const storySummary = [
    { title: 'Premisa', text: premise },
    ...scenes.map(scene => ({
      title: `ESCENA ${scene.index} — ${scene.blueprint.name}`,
      text: scene.summary
    })),
    { title: 'Cierre', text: `Final ${ending.es}.` }
  ];

  const ideaCombos = buildIdeaCombos(uni, protagonist, rival, protector);

  currentStory = {
    uni,
    protagonist,
    rival,
    protector,
    emotion,
    conflict,
    scenario,
    endingKey,
    ending,
    count,
    style,
    title,
    premise,
    scenes,
    hooks,
    storySummary,
    ideaCombos,
    cast
  };
  renderStory();
}

function escapeHtml(str) {
  return String(str)
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/"/g, '&quot;')
    .replace(/'/g, '&#039;');
}

function renderStory() {
  if (!currentStory) return;
  const { uni, protagonist, rival, protector, emotion, conflict, ending, count, title, premise, scenes, hooks, storySummary, ideaCombos, cast } = currentStory;

  document.getElementById('storyTitle').textContent = title;
  document.getElementById('premise').textContent = premise;
  document.getElementById('sumUniverse').textContent = uni.name;
  document.getElementById('sumConflict').textContent = conflict;
  document.getElementById('sumEmotion').textContent = emotion.es;
  document.getElementById('sumEnding').textContent = ending.es;
  document.getElementById('sumScenes').textContent = `${count} escenas`;
  document.getElementById('quickScenes').textContent = `${count} escenas actuales`;

  const charsOut = document.getElementById('charactersOut');
  charsOut.innerHTML = '';
  const roleNames = {
    [protagonist.name]: 'Protagonista',
    [rival.name]: 'Rival',
    [protector.name]: protagonist.name === protector.name ? 'Protagonista / Protector' : 'Protector'
  };
  cast.forEach(char => {
    charsOut.insertAdjacentHTML('beforeend', `
      <div class="char-card">
        <div class="char-name">${char.emoji} ${char.name}<span class="char-role">${roleNames[char.name] || char.role || 'Personaje'}</span></div>
        <div class="char-desc">${escapeHtml(char.desc)}</div>
      </div>
    `);
  });

  const scenesOut = document.getElementById('scenesOut');
  scenesOut.innerHTML = '';
  scenes.forEach(scene => {
    scenesOut.insertAdjacentHTML('beforeend', `
      <div class="scene-card">
        <div class="scene-head">
          <div class="scene-number">${scene.index}</div>
          <div class="scene-head-text">
            <div class="scene-title-line">${scene.blueprint.name}</div>
            <div class="scene-meta">
              <span class="pill">${scene.type}</span>
              <span class="pill">${scene.duration}</span>
              <span class="pill">${scene.characters.map(c => c.emoji + ' ' + c.name).join(' + ')}</span>
            </div>
          </div>
        </div>
        <div class="scene-body">
          <div class="label">FREEPIK IMAGEN — ESCENA ${scene.index}</div>
          <div class="prompt-box">
            <button class="copy" data-text="${encodeURIComponent(scene.imagePrompt)}" onclick="copyEncoded(this)">Copiar</button>
            ${escapeHtml(scene.imagePrompt)}
          </div>
          <div style="height:12px"></div>
          <div class="label cyan">KLING VIDEO — ESCENA ${scene.index}</div>
          <div class="prompt-box cyan">
            <button class="copy" data-text="${encodeURIComponent(scene.videoPrompt)}" onclick="copyEncoded(this)">Copiar</button>
            ${escapeHtml(scene.videoPrompt)}
          </div>
          <div class="narration"><b>LIPSYNC — ${scene.voiceLabel}:</b><br>${escapeHtml(scene.lipsync)}</div>
        </div>
      </div>
    `);
  });

  const hooksOut = document.getElementById('hooksOut');
  hooksOut.innerHTML = hooks.map(item => `<div class="hook"><b>${escapeHtml(item.title)}</b><br>${escapeHtml(item.text)}</div>`).join('');

  const sumOut = document.getElementById('storySummaryOut');
  sumOut.innerHTML = storySummary.map(item => `<div class="summary-item"><b>${escapeHtml(item.title)}</b><br>${escapeHtml(item.text)}</div>`).join('');

  const lipOut = document.getElementById('lipsyncOut');
  lipOut.innerHTML = scenes.map(scene => `<div class="lip-card"><b>ESCENA ${scene.index} — ${escapeHtml(scene.voiceLabel)}</b>${escapeHtml(scene.lipsync)}</div>`).join('');

  const comboOut = document.getElementById('comboOut');
  comboOut.innerHTML = ideaCombos.map(item => `<div class="combo-item"><b>Idea rápida</b><br>${escapeHtml(item)}</div>`).join('');
}

function flashCopied(btn) {
  const old = btn.textContent;
  btn.textContent = 'Copiado';
  setTimeout(() => btn.textContent = old, 1200);
}

function fallbackCopy(text) {
  const area = document.createElement('textarea');
  area.value = text;
  area.setAttribute('readonly', '');
  area.style.position = 'fixed';
  area.style.opacity = '0';
  area.style.pointerEvents = 'none';
  document.body.appendChild(area);
  area.focus();
  area.select();
  try { document.execCommand('copy'); } catch (e) {}
  document.body.removeChild(area);
}

function copyText(btn, text) {
  if (navigator.clipboard && navigator.clipboard.writeText) {
    navigator.clipboard.writeText(text).then(() => {
      flashCopied(btn);
    }).catch(() => {
      fallbackCopy(text);
      flashCopied(btn);
    });
    return;
  }
  fallbackCopy(text);
  flashCopied(btn);
}

function copyEncoded(btn) {
  const raw = btn.dataset.text || '';
  copyText(btn, decodeURIComponent(raw));
}

function copyByType(type) {
  if (!currentStory) return;
  const text = currentStory.scenes.map(scene => type === 'image'
    ? `ESCENA ${scene.index}\n${scene.imagePrompt}`
    : `ESCENA ${scene.index}\n${scene.videoPrompt}`
  ).join('\n\n');
  navigator.clipboard.writeText(text);
}

function copyAllStory() {
  if (!currentStory) return;
  const { title, premise, protagonist, rival, protector, scenes, hooks, storySummary, cast } = currentStory;
  const chars = cast.map(c => `${c.emoji} ${c.name}\n${c.desc}`).join('\n\n');
  const summaryText = storySummary.map(item => `${item.title}\n${item.text}`).join('\n\n');
  const sceneText = scenes.map(scene => `ESCENA ${scene.index} — ${scene.blueprint.name}\nTIPO: ${scene.type}\nPERSONAJES: ${scene.characters.map(c => c.emoji + ' ' + c.name).join(' + ')}\n\nFREEPIK IMAGEN:\n${scene.imagePrompt}\n\nKLING VIDEO:\n${scene.videoPrompt}\n\nLIPSYNC — ${scene.voiceLabel}:\n${scene.lipsync}`).join('\n\n────────────────────────────────────────\n\n');
  const hookText = hooks.map(item => `• ${item.title}: ${item.text}`).join('\n');
  const allLips = scenes.map(scene => `ESCENA ${scene.index} — ${scene.voiceLabel}\n${scene.lipsync}`).join('\n\n');
  const content = `GENERADOR DE PROMPTS JOHAN MONETIZA\n\nHistoria: ${title}\n\nPREMISA:\n${premise}\n\nPERSONAJES BASE:\n${chars}\n\nRESUMEN DE ESCENAS:\n\n${summaryText}\n\nESCENAS:\n\n${sceneText}\n\nHOOKS VIRALES:\n${hookText}\n\nTODOS LOS LIPSYNC:\n${allLips}`;
  navigator.clipboard.writeText(content);
}

function copyAllLipsync() {
  if (!currentStory) return;
  const text = currentStory.scenes.map(scene => `ESCENA ${scene.index} — ${scene.voiceLabel}\n${scene.lipsync}`).join('\n\n');
  navigator.clipboard.writeText(text);
}

function randomizeSelections() {
  const universeKeys = Object.keys(UNIVERSES);
  selects.universe.value = randomOf(universeKeys);
  refreshControls();

  const uni = UNIVERSES[selects.universe.value];
  const conflictOptions = [...uni.conflicts, ...CONFLICT_ARCHETYPES];
  const endingOptions = [...new Set([...uni.endings, ...Object.keys(ENDINGS)])];

  selects.protagonist.value = randomOf(uni.protagonists);
  selects.rival.value = randomOf(uni.rivals);
  selects.protector.value = randomOf(uni.protectors);
  selects.emotion.value = randomOf(Object.keys(EMOTIONS));
  selects.conflict.value = String(Math.floor(Math.random() * conflictOptions.length));
  selects.scenario.value = String(Math.floor(Math.random() * uni.scenarios.length));
  selects.ending.value = String(Math.floor(Math.random() * endingOptions.length));
  selects.sceneCount.value = randomOf(['10','11','12','13','14','15']);
  selects.visualStyle.value = randomOf(VISUAL_STYLES);

  buildStory();
}

function setupTabs() {
  document.querySelectorAll('.tab').forEach(tab => {
    tab.addEventListener('click', () => {
      document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
      tab.classList.add('active');
      const target = tab.dataset.tab;
      document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('visible'));
      document.getElementById('tab-' + target).classList.add('visible');
    });
  });
}

populateUniverseOptions();
populateSceneCounts();
populateVisualStyles();
populateEmotionOptions();
selects.universe.value = 'espadaRosa';
refreshControls();
selects.visualStyle.value = VISUAL_STYLES[0];
setupTabs();
buildStory();

selects.universe.addEventListener('change', refreshControls);
document.getElementById('generateBtn').addEventListener('click', buildStory);
document.getElementById('randomBtn').addEventListener('click', randomizeSelections);
document.getElementById('copyAllBtn').addEventListener('click', copyAllStory);
document.getElementById('copyLipsBtn').addEventListener('click', copyAllLipsync);
window.copyText = copyText;
window.copyEncoded = copyEncoded;
window.copyByType = copyByType;
</script>


</body>
</html>
