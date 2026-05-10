<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MIS 432 — Ingredient Recommender</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>

  <style>
    /* =====================================================
       CSS VARIABLES — all colors and values in one place
    ===================================================== */
    :root {
      --bg:          #f5f0e8;
      --surface:     #fffdf7;
      --border:      #d9d0bc;
      --border-dark: #b8ad98;
      --ink:         #1a1612;
      --ink-mid:     #5a5040;
      --ink-light:   #9a8f7a;
      --accent:      #2d5a27;
      --accent-light:#4a8c42;
      --warm:        #c4651a;
      --warm-light:  #e8892a;
      --red:         #8b2020;
      --weak-color:  #8b6914;
      --mod-color:   #c4651a;
      --strong-color:#2d5a27;
      --radius:      4px;
      --font-head:   'Playfair Display', Georgia, serif;
      --font-body:   'DM Mono', 'Courier New', monospace;
    }

    /* =====================================================
       RESET + BASE
    ===================================================== */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--ink);
      font-family: var(--font-body);
      font-size: 13px;
      line-height: 1.6;
      min-height: 100vh;
    }

    /* Subtle paper texture overlay */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='4' height='4'%3E%3Crect width='4' height='4' fill='none'/%3E%3Ccircle cx='1' cy='1' r='0.4' fill='%23b8a88a' opacity='0.3'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 0;
    }

    /* =====================================================
       LAYOUT
    ===================================================== */
    .app {
      position: relative;
      z-index: 1;
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 28px 60px;
    }

    /* =====================================================
       HEADER
    ===================================================== */
    header {
      padding: 44px 0 32px;
      border-bottom: 2px solid var(--ink);
      margin-bottom: 36px;
    }

    .header-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }

    h1 {
      font-family: var(--font-head);
      font-size: 38px;
      font-weight: 900;
      line-height: 1.1;
      letter-spacing: -1px;
      color: var(--ink);
    }

    h1 em {
      font-style: italic;
      color: var(--accent);
    }

    .subtitle {
      font-size: 11px;
      color: var(--ink-light);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-top: 8px;
    }

    .badge {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      padding: 5px 12px;
      border: 1px solid var(--border-dark);
      border-radius: 2px;
      color: var(--ink-mid);
      background: var(--surface);
      white-space: nowrap;
      margin-top: 6px;
    }

    /* =====================================================
       MAIN GRID
    ===================================================== */
    .main-grid {
      display: grid;
      grid-template-columns: 300px 1fr;
      gap: 32px;
      align-items: start;
    }

    @media (max-width: 780px) {
      .main-grid { grid-template-columns: 1fr; }
    }

    /* =====================================================
       SECTION LABELS
    ===================================================== */
    .section-label {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--ink-light);
      margin-bottom: 10px;
      padding-bottom: 6px;
      border-bottom: 1px solid var(--border);
    }

    /* =====================================================
       LEFT PANEL — Controls
    ===================================================== */
    .controls-panel {
      background: var(--surface);
      border: 1px solid var(--border-dark);
      border-radius: var(--radius);
      padding: 24px;
      position: sticky;
      top: 24px;
    }

    /* Ingredient dropdown */
    .control-group {
      margin-bottom: 24px;
    }

    .control-label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--ink-mid);
      display: block;
      margin-bottom: 8px;
    }

    select {
      width: 100%;
      padding: 10px 12px;
      font-family: var(--font-body);
      font-size: 13px;
      color: var(--ink);
      background: var(--bg);
      border: 1px solid var(--border-dark);
      border-radius: var(--radius);
      appearance: none;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%235a5040' stroke-width='1.5' fill='none' stroke-linecap='round'/%3E%3C/svg%3E");
      background-repeat: no-repeat;
      background-position: right 12px center;
      cursor: pointer;
      transition: border-color 0.15s;
    }

    select:focus {
      outline: none;
      border-color: var(--accent);
    }

    /* Connection strength filter buttons */
    .filter-buttons {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .filter-btn {
      width: 100%;
      padding: 9px 14px;
      font-family: var(--font-body);
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.04em;
      border-radius: var(--radius);
      border: 1px solid;
      cursor: pointer;
      text-align: left;
      transition: all 0.15s;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .filter-btn .dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      flex-shrink: 0;
    }

    /* Weak button */
    .filter-btn.weak {
      background: rgba(139,105,20,0.07);
      border-color: rgba(139,105,20,0.3);
      color: var(--weak-color);
    }
    .filter-btn.weak .dot { background: var(--weak-color); }
    .filter-btn.weak:hover,
    .filter-btn.weak.active {
      background: rgba(139,105,20,0.15);
      border-color: var(--weak-color);
    }

    /* Moderate button */
    .filter-btn.moderate {
      background: rgba(196,101,26,0.07);
      border-color: rgba(196,101,26,0.3);
      color: var(--mod-color);
    }
    .filter-btn.moderate .dot { background: var(--mod-color); }
    .filter-btn.moderate:hover,
    .filter-btn.moderate.active {
      background: rgba(196,101,26,0.15);
      border-color: var(--mod-color);
    }

    /* Strong button */
    .filter-btn.strong {
      background: rgba(45,90,39,0.07);
      border-color: rgba(45,90,39,0.3);
      color: var(--strong-color);
    }
    .filter-btn.strong .dot { background: var(--strong-color); }
    .filter-btn.strong:hover,
    .filter-btn.strong.active {
      background: rgba(45,90,39,0.15);
      border-color: var(--strong-color);
    }

    /* Show all button */
    .filter-btn.all {
      background: transparent;
      border-color: var(--border-dark);
      color: var(--ink-mid);
    }
    .filter-btn.all .dot { background: var(--ink-light); }
    .filter-btn.all:hover,
    .filter-btn.all.active {
      background: var(--bg);
      border-color: var(--ink);
      color: var(--ink);
    }

    /* Ingredient grid in left panel */
    .ingredient-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 4px;
    }

    .ingredient-chip {
      font-size: 11px;
      padding: 3px 9px;
      border-radius: 2px;
      background: var(--bg);
      border: 1px solid var(--border);
      color: var(--ink-mid);
      cursor: pointer;
      transition: all 0.12s;
    }

    .ingredient-chip:hover {
      border-color: var(--accent);
      color: var(--accent);
    }

    .ingredient-chip.selected {
      background: var(--accent);
      border-color: var(--accent);
      color: white;
    }

    /* =====================================================
       RIGHT PANEL — Results
    ===================================================== */
    .results-panel {
      min-height: 400px;
    }

    /* Empty state */
    .empty-state {
      background: var(--surface);
      border: 1px dashed var(--border-dark);
      border-radius: var(--radius);
      padding: 60px 32px;
      text-align: center;
    }

    .empty-icon {
      font-size: 36px;
      display: block;
      margin-bottom: 16px;
    }

    .empty-title {
      font-family: var(--font-head);
      font-size: 20px;
      color: var(--ink-mid);
      margin-bottom: 8px;
    }

    .empty-sub {
      font-size: 12px;
      color: var(--ink-light);
      line-height: 1.8;
    }

    /* Results header */
    .results-header {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      margin-bottom: 16px;
      flex-wrap: wrap;
      gap: 8px;
    }

    .results-title {
      font-family: var(--font-head);
      font-size: 22px;
      font-weight: 700;
      color: var(--ink);
    }

    .results-title span {
      color: var(--accent);
      font-style: italic;
    }

    .results-meta {
      font-size: 11px;
      color: var(--ink-light);
    }

    /* Recommendation cards */
    .rec-list {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .rec-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 18px 20px;
      border-left: 4px solid var(--border);
      animation: cardIn 0.25s ease both;
      transition: border-color 0.15s, box-shadow 0.15s;
    }

    .rec-card:hover {
      box-shadow: 0 2px 12px rgba(0,0,0,0.06);
    }

    @keyframes cardIn {
      from { opacity: 0; transform: translateY(6px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .rec-card.strength-weak     { border-left-color: var(--weak-color); }
    .rec-card.strength-moderate { border-left-color: var(--mod-color); }
    .rec-card.strength-strong   { border-left-color: var(--strong-color); }
    .rec-card.hidden            { display: none; }

    .rec-card-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 12px;
      margin-bottom: 10px;
    }

    .rec-left {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .rec-rank {
      font-family: var(--font-head);
      font-size: 26px;
      font-weight: 900;
      color: var(--border-dark);
      line-height: 1;
      width: 28px;
      flex-shrink: 0;
    }

    .rec-name {
      font-family: var(--font-head);
      font-size: 18px;
      font-weight: 700;
      color: var(--ink);
      line-height: 1.2;
    }

    /* Strength badge */
    .strength-badge {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      padding: 3px 9px;
      border-radius: 2px;
      border: 1px solid;
      flex-shrink: 0;
    }

    .strength-badge.weak     { color: var(--weak-color);   border-color: rgba(139,105,20,0.4); background: rgba(139,105,20,0.08); }
    .strength-badge.moderate { color: var(--mod-color);    border-color: rgba(196,101,26,0.4); background: rgba(196,101,26,0.08); }
    .strength-badge.strong   { color: var(--strong-color); border-color: rgba(45,90,39,0.4);   background: rgba(45,90,39,0.08); }

    /* Score bars */
    .rec-scores {
      display: flex;
      gap: 20px;
      margin-bottom: 10px;
      flex-wrap: wrap;
    }

    .score-item {
      display: flex;
      flex-direction: column;
      gap: 3px;
    }

    .score-label {
      font-size: 9px;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--ink-light);
    }

    .score-value {
      font-size: 14px;
      font-weight: 500;
      color: var(--ink);
    }

    .score-bar-bg {
      width: 80px;
      height: 3px;
      background: var(--border);
      border-radius: 2px;
      overflow: hidden;
    }

    .score-bar-fill {
      height: 100%;
      border-radius: 2px;
      transition: width 0.4s ease;
    }

    .fill-sim   { background: var(--accent); }
    .fill-match { background: var(--warm); }

    /* Explanation text */
    .rec-explanation {
      font-size: 12px;
      color: var(--ink-mid);
      line-height: 1.7;
      padding-top: 10px;
      border-top: 1px solid var(--border);
    }

    .rec-explanation strong {
      color: var(--ink);
    }

    /* No results message */
    .no-results {
      text-align: center;
      padding: 40px;
      color: var(--ink-light);
      font-size: 13px;
      background: var(--surface);
      border: 1px dashed var(--border);
      border-radius: var(--radius);
    }
  </style>
</head>
<body>
<div class="app">

  <!-- =====================================================
       HEADER
  ===================================================== -->
  <header>
    <div class="header-top">
      <div>
        <h1>Ingredient<br><em>Recommender</em></h1>
        <p class="subtitle">MIS 432 · Recipe Ingredient Graph · Western Washington University</p>
      </div>
      <div class="badge">Collaborative Filtering Demo</div>
    </div>
  </header>

  <div class="main-grid">

    <!-- ===================================================
         LEFT PANEL: Controls
         Dropdown to pick an ingredient, filter buttons
         to narrow by connection strength, and a quick
         visual grid of all ingredients in the catalog.
    =================================================== -->
    <div class="controls-panel">

      <!-- Ingredient selector dropdown -->
      <div class="control-group">
        <div class="section-label">Select Ingredient</div>
        <select id="ingredient-select">
          <option value="">— Choose an ingredient —</option>
          <option>Tomato</option>
          <option>Garlic</option>
          <option>Parmesan</option>
          <option>Olive Oil</option>
          <option>Chicken</option>
          <option>Rice</option>
          <option>Cheese</option>
          <option>Tortilla</option>
          <option>Onion</option>
          <option>Beans</option>
          <option>Eggs</option>
        </select>
      </div>

      <!-- Connection strength filter -->
      <div class="control-group">
        <div class="section-label">Filter by Strength</div>
        <div class="filter-buttons">
          <button class="filter-btn all active" onclick="setFilter('all')">
            <span class="dot"></span> Show All
          </button>
          <button class="filter-btn weak" onclick="setFilter('weak')">
            <span class="dot"></span> Weak only (0.1)
          </button>
          <button class="filter-btn moderate" onclick="setFilter('moderate')">
            <span class="dot"></span> Moderate only (0.5)
          </button>
          <button class="filter-btn strong" onclick="setFilter('strong')">
            <span class="dot"></span> Strong only (0.9)
          </button>
        </div>
      </div>

      <!-- Quick-click ingredient grid -->
      <div class="control-group">
        <div class="section-label">Quick Select</div>
        <div class="ingredient-grid" id="chip-grid">
          <!-- Chips injected by JS -->
        </div>
      </div>

    </div>

    <!-- ===================================================
         RIGHT PANEL: Results
         Shows top 5 recommended ingredients with their
         similarity score, connection strength, match score,
         and a plain-English explanation sentence.
    =================================================== -->
    <div class="results-panel">
      <div id="results-container">
        <div class="empty-state">
          <span class="empty-icon">🌿</span>
          <div class="empty-title">Select an ingredient to begin</div>
          <div class="empty-sub">
            Choose any ingredient from the dropdown or quick-select grid.<br>
            The system will find your top 5 substitution matches<br>
            using cosine similarity and connection strength scoring.
          </div>
        </div>
      </div>
    </div>

  </div>
</div>

<script>
// =====================================================
// DATA: The complete ingredient graph
// Each entry defines a relationship between two items,
// what type of connection it is, and how strong it is.
// This mirrors the DataFrame we built in Python Step 01.
// =====================================================
const GRAPH = [
  // Cuisine connections (strength 0.1)
  { a: "Tomato",    b: "Italian",  type: "cuisine", strength: 0.1 },
  { a: "Garlic",    b: "Italian",  type: "cuisine", strength: 0.1 },
  { a: "Parmesan",  b: "Italian",  type: "cuisine", strength: 0.1 },
  { a: "Olive Oil", b: "Italian",  type: "cuisine", strength: 0.1 },
  { a: "Onion",     b: "Italian",  type: "cuisine", strength: 0.1 },
  { a: "Chicken",   b: "Mexican",  type: "cuisine", strength: 0.1 },
  { a: "Rice",      b: "Mexican",  type: "cuisine", strength: 0.1 },
  { a: "Tortilla",  b: "Mexican",  type: "cuisine", strength: 0.1 },
  { a: "Cheese",    b: "Mexican",  type: "cuisine", strength: 0.1 },
  { a: "Beans",     b: "Mexican",  type: "cuisine", strength: 0.1 },
  { a: "Onion",     b: "Mexican",  type: "cuisine", strength: 0.1 },

  // Flavor connections (strength 0.5)
  { a: "Garlic",    b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Chicken",   b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Rice",      b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Tortilla",  b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Onion",     b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Beans",     b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Eggs",      b: "Savory",   type: "flavor",  strength: 0.5 },
  { a: "Chicken",   b: "Spicy",    type: "flavor",  strength: 0.5 },
  { a: "Beans",     b: "Spicy",    type: "flavor",  strength: 0.5 },
  { a: "Parmesan",  b: "Salty",    type: "flavor",  strength: 0.5 },
  { a: "Cheese",    b: "Salty",    type: "flavor",  strength: 0.5 },
  { a: "Tomato",    b: "Salty",    type: "flavor",  strength: 0.5 },
  { a: "Onion",     b: "Salty",    type: "flavor",  strength: 0.5 },
  { a: "Cheese",    b: "Rich",     type: "flavor",  strength: 0.5 },
  { a: "Eggs",      b: "Rich",     type: "flavor",  strength: 0.5 },
  { a: "Olive Oil", b: "Rich",     type: "flavor",  strength: 0.5 },

  // Direct pairings (strength 0.9)
  { a: "Tomato",    b: "Garlic",    type: "pairing", strength: 0.9 },
  { a: "Garlic",    b: "Olive Oil", type: "pairing", strength: 0.9 },
  { a: "Chicken",   b: "Rice",      type: "pairing", strength: 0.9 },
  { a: "Cheese",    b: "Tortilla",  type: "pairing", strength: 0.9 },
  { a: "Rice",      b: "Beans",     type: "pairing", strength: 0.9 },
  { a: "Eggs",      b: "Cheese",    type: "pairing", strength: 0.9 },
  { a: "Onion",     b: "Garlic",    type: "pairing", strength: 0.9 },
];

const INGREDIENTS = [
  "Tomato","Garlic","Parmesan","Olive Oil","Chicken",
  "Rice","Cheese","Tortilla","Onion","Beans","Eggs"
];

const CUISINES = ["Italian","Mexican"];
const FLAVORS  = ["Savory","Spicy","Salty","Rich"];

let currentFilter = "all";

// =====================================================
// FEATURE ENGINEERING (mirrors Python Step 02)
//
// For each ingredient, compute the same four features
// we built in Python so cosine similarity works the
// same way here as it did in Colab.
// =====================================================
function buildFeatures() {
  const features = {};

  for (const ing of INGREDIENTS) {
    // Get all connections this ingredient is part of
    const myEdges = GRAPH.filter(e => e.a === ing || e.b === ing);

    const cuisineEdges = myEdges.filter(e => e.type === "cuisine");
    const flavorEdges  = myEdges.filter(e => e.type === "flavor");
    const pairingEdges = myEdges.filter(e => e.type === "pairing");

    // substitution_score: sum of all connection strengths
    const substitution_score = myEdges.reduce((s, e) => s + e.strength, 0);

    // strong_match_rate: fraction of connections that are pairings (0.9)
    const strong_match_rate = myEdges.length > 0
      ? pairingEdges.length / myEdges.length
      : 0;

    // flavor_diversity: how many unique flavor profiles connected
    const connectedFlavors = new Set(
      flavorEdges.map(e => e.a === ing ? e.b : e.a).filter(x => FLAVORS.includes(x))
    );

    // cuisine_diversity: how many unique cuisines connected
    const connectedCuisines = new Set(
      cuisineEdges.map(e => e.a === ing ? e.b : e.a).filter(x => CUISINES.includes(x))
    );

    features[ing] = {
      substitution_score,
      strong_match_rate,
      flavor_diversity:  connectedFlavors.size,
      cuisine_diversity: connectedCuisines.size,
    };
  }
  return features;
}

// =====================================================
// COSINE SIMILARITY (mirrors Python Step 03 Part B)
//
// Compares the direction of two feature vectors.
// Returns a score from 0.0 (nothing in common)
// to 1.0 (identical feature profiles).
// =====================================================
function cosineSim(vecA, vecB) {
  const keys = ["substitution_score","strong_match_rate","flavor_diversity","cuisine_diversity"];
  let dot = 0, magA = 0, magB = 0;
  for (const k of keys) {
    dot  += vecA[k] * vecB[k];
    magA += vecA[k] * vecA[k];
    magB += vecB[k] * vecB[k];
  }
  if (magA === 0 || magB === 0) return 0;
  return dot / (Math.sqrt(magA) * Math.sqrt(magB));
}

// =====================================================
// SHARED CONNECTION LOOKUP (mirrors Python Step 03 Part C)
//
// For any two ingredients, find what they share:
// shared cuisines, shared flavors, direct pairing.
// =====================================================
function getSharedConnections(ingA, ingB) {
  // Everything ingA connects to
  const aTargets = new Set(
    GRAPH.filter(e => e.a === ingA || e.b === ingA)
         .map(e => e.a === ingA ? e.b : e.a)
  );
  // Everything ingB connects to
  const bTargets = new Set(
    GRAPH.filter(e => e.a === ingB || e.b === ingB)
         .map(e => e.a === ingB ? e.b : e.a)
  );

  const sharedCuisines = CUISINES.filter(c => aTargets.has(c) && bTargets.has(c));
  const sharedFlavors  = FLAVORS.filter(f  => aTargets.has(f)  && bTargets.has(f));

  // Direct pairing check
  const directPair = GRAPH.some(e =>
    (e.a === ingA && e.b === ingB && e.type === "pairing") ||
    (e.a === ingB && e.b === ingA && e.type === "pairing")
  );

  return { sharedCuisines, sharedFlavors, directPair };
}

// =====================================================
// MATCH SCORE (mirrors Python Step 03 Part D)
// shared cuisine = 2 pts, shared flavor = 3 pts,
// direct pairing = 4 pts
// =====================================================
function getMatchScore(sharedCuisines, sharedFlavors, directPair) {
  return (sharedCuisines.length * 2) + (sharedFlavors.length * 3) + (directPair ? 4 : 0);
}

// =====================================================
// CONNECTION STRENGTH (mirrors Python Step 03 Part E)
// =====================================================
function getStrength(sharedCuisines, sharedFlavors, directPair) {
  if (directPair)          return 0.9;
  if (sharedFlavors.length) return 0.5;
  if (sharedCuisines.length) return 0.1;
  return 0.1;
}

function strengthLabel(s) {
  if (s >= 0.9) return "strong";
  if (s >= 0.5) return "moderate";
  return "weak";
}

function strengthText(s) {
  if (s >= 0.9) return "Strong";
  if (s >= 0.5) return "Moderate";
  return "Weak";
}

// =====================================================
// EXPLANATION GENERATOR (mirrors Python Step 03 Part F)
// Writes a plain-English sentence for each recommendation
// =====================================================
function getExplanation(target, match, sharedCuisines, sharedFlavors, directPair) {
  const parts = [];
  if (directPair)
    parts.push(`<strong>${target}</strong> and <strong>${match}</strong> are directly paired together in cooking`);
  if (sharedFlavors.length)
    parts.push(`both share a <strong>${sharedFlavors.join(" and ")}</strong> flavor profile`);
  if (sharedCuisines.length)
    parts.push(`both are used in <strong>${sharedCuisines.join(" and ")}</strong> cuisine`);
  if (!parts.length)
    return `<strong>${match}</strong> has a similar overall connection profile to <strong>${target}</strong> in the graph.`;
  return parts.join(", and ") + ".";
}

// =====================================================
// MAIN: Get top 5 recommendations for a target ingredient
// =====================================================
const FEATURES = buildFeatures();

function getRecommendations(target) {
  const targetVec = FEATURES[target];
  const results = [];

  for (const ing of INGREDIENTS) {
    if (ing === target) continue;
    const sim = cosineSim(targetVec, FEATURES[ing]);
    const { sharedCuisines, sharedFlavors, directPair } = getSharedConnections(target, ing);
    const matchScore = getMatchScore(sharedCuisines, sharedFlavors, directPair);
    const strength   = getStrength(sharedCuisines, sharedFlavors, directPair);
    const explanation = getExplanation(target, ing, sharedCuisines, sharedFlavors, directPair);

    results.push({ ing, sim, matchScore, strength, explanation });
  }

  // Sort by connection strength first, then match score as tiebreaker, then similarity
  return results.sort((a, b) =>
    b.strength - a.strength ||
    b.matchScore - a.matchScore ||
    b.sim - a.sim
  ).slice(0, 5);
}

// =====================================================
// RENDER: Build and display recommendation cards
// =====================================================
function renderResults(target) {
  const container = document.getElementById("results-container");

  if (!target) {
    container.innerHTML = `
      <div class="empty-state">
        <span class="empty-icon">🌿</span>
        <div class="empty-title">Select an ingredient to begin</div>
        <div class="empty-sub">
          Choose any ingredient from the dropdown or quick-select grid.<br>
          The system will find your top 5 substitution matches<br>
          using cosine similarity and connection strength scoring.
        </div>
      </div>`;
    return;
  }

  const recs = getRecommendations(target);
  const maxSim   = Math.max(...recs.map(r => r.sim));
  const maxMatch = Math.max(...recs.map(r => r.matchScore)) || 1;

  let html = `
    <div class="results-header">
      <div class="results-title">Matches for <span>${target}</span></div>
      <div class="results-meta">top 5 · sorted by connection strength</div>
    </div>
    <div class="rec-list">`;

  recs.forEach((rec, i) => {
    const sl    = strengthLabel(rec.strength);
    const st    = strengthText(rec.strength);
    const simPct   = Math.round((rec.sim / maxSim) * 100);
    const matchPct = Math.round((rec.matchScore / maxMatch) * 100);
    const hidden = currentFilter !== "all" && currentFilter !== sl ? "hidden" : "";

    html += `
      <div class="rec-card strength-${sl} ${hidden}" style="animation-delay:${i*0.06}s">
        <div class="rec-card-top">
          <div class="rec-left">
            <div class="rec-rank">${i+1}</div>
            <div class="rec-name">${rec.ing}</div>
          </div>
          <span class="strength-badge ${sl}">${st} · ${rec.strength}</span>
        </div>

        <div class="rec-scores">
          <div class="score-item">
            <span class="score-label">Similarity</span>
            <span class="score-value">${rec.sim.toFixed(3)}</span>
            <div class="score-bar-bg"><div class="score-bar-fill fill-sim" style="width:${simPct}%"></div></div>
          </div>
          <div class="score-item">
            <span class="score-label">Match Score</span>
            <span class="score-value">${rec.matchScore} pts</span>
            <div class="score-bar-bg"><div class="score-bar-fill fill-match" style="width:${matchPct}%"></div></div>
          </div>
          <div class="score-item">
            <span class="score-label">Conn. Strength</span>
            <span class="score-value">${rec.strength}</span>
          </div>
        </div>

        <div class="rec-explanation">Why: ${rec.explanation}</div>
      </div>`;
  });

  html += `</div>`;

  // Show a "none match filter" message if all cards are hidden
  const visibleCount = recs.filter(r =>
    currentFilter === "all" || strengthLabel(r.strength) === currentFilter
  ).length;

  if (visibleCount === 0) {
    html += `<div class="no-results" style="margin-top:10px">
      No recommendations match the selected strength filter for <strong>${target}</strong>.
      Try a different filter or ingredient.
    </div>`;
  }

  container.innerHTML = html;
}

// =====================================================
// FILTER: Toggle connection strength filter buttons
// =====================================================
function setFilter(filter) {
  currentFilter = filter;

  // Update active button styles
  document.querySelectorAll(".filter-btn").forEach(btn => btn.classList.remove("active"));
  document.querySelector(`.filter-btn.${filter === "all" ? "all" : filter}`).classList.add("active");

  // Show or hide cards based on filter
  document.querySelectorAll(".rec-card").forEach(card => {
    if (filter === "all") {
      card.classList.remove("hidden");
    } else {
      const isMatch = card.classList.contains(`strength-${filter}`);
      card.classList.toggle("hidden", !isMatch);
    }
  });

  // Check if anything is visible
  const target = document.getElementById("ingredient-select").value;
  if (target) {
    const visible = document.querySelectorAll(".rec-card:not(.hidden)").length;
    const existing = document.querySelector(".no-results");
    if (visible === 0 && !existing) {
      const list = document.querySelector(".rec-list");
      if (list) {
        const msg = document.createElement("div");
        msg.className = "no-results";
        msg.style.marginTop = "10px";
        msg.innerHTML = `No recommendations match the selected strength filter for <strong>${target}</strong>. Try a different filter or ingredient.`;
        list.after(msg);
      }
    } else if (visible > 0 && existing) {
      existing.remove();
    }
  }
}

// =====================================================
// BUILD: Quick-select chip grid in left panel
// =====================================================
function buildChips() {
  const grid = document.getElementById("chip-grid");
  for (const ing of INGREDIENTS) {
    const chip = document.createElement("div");
    chip.className = "ingredient-chip";
    chip.textContent = ing;
    chip.onclick = () => {
      document.getElementById("ingredient-select").value = ing;
      document.querySelectorAll(".ingredient-chip").forEach(c => c.classList.remove("selected"));
      chip.classList.add("selected");
      renderResults(ing);
    };
    grid.appendChild(chip);
  }
}

// =====================================================
// EVENT: Dropdown change handler
// =====================================================
document.getElementById("ingredient-select").addEventListener("change", function() {
  const val = this.value;
  document.querySelectorAll(".ingredient-chip").forEach(c => {
    c.classList.toggle("selected", c.textContent === val);
  });
  renderResults(val);
});

// =====================================================
// INIT
// =====================================================
buildChips();
</script>
</body>
</html>
