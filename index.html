<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Planificador de Dieta — Entreno & Descanso</title>
<style>
  :root{
    --bg:#0f172a; --panel:#111827; --muted:#1f2937; --text:#e5e7eb; --accent:#60a5fa;
    --ok:#22c55e; --warn:#f59e0b; --bad:#ef4444; --card:#0b1220;
    --chip:#0b1b35; --chip-br:#244266; --soft:#0d1a2b;
  }
  *{box-sizing:border-box}
  body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Inter,Arial,sans-serif;background:linear-gradient(180deg,#0b1220,#0f172a);color:var(--text)}
  header{padding:20px 16px;border-bottom:1px solid #1f2937;position:sticky;top:0;background:#0f172a;z-index:10}
  h1{margin:0;font-size:20px;font-weight:700;letter-spacing:.3px}
  .wrap{display:grid;gap:16px;padding:16px;grid-template-columns:1.1fr 1.1fr 1fr}
  @media (max-width:1100px){.wrap{grid-template-columns:1fr}}
  .card{background:var(--panel);border:1px solid #1f2937;border-radius:16px;box-shadow:0 10px 30px rgba(0,0,0,.25)}
  .card header{position:unset;background:transparent;border:0;padding:16px 16px 0}
  .card .content{padding:16px}
  .row{display:flex;gap:10px;align-items:center;flex-wrap:wrap}
  .col{display:flex;flex-direction:column;gap:6px}
  label{font-size:12px;color:#a5b4fc}
  input,select,button,textarea{
    background:#0b1220;color:var(--text);border:1px solid #334155;border-radius:10px;padding:10px 12px;font-size:14px;outline:none
  }
  input[type="number"]{width:110px}
  button{cursor:pointer;transition:.2s;border-color:#3b82f6}
  button:hover{background:#0b2348}
  .btn-ghost{background:transparent;border-color:#334155}
  .grid{display:grid;gap:10px}
  .grid-2{grid-template-columns:1fr 1fr}
  .grid-3{grid-template-columns:repeat(3,1fr)}
  .list{display:flex;flex-direction:column;gap:10px}
  .item{background:var(--card);border:1px solid #203049;border-radius:12px;padding:10px}
  .pill{padding:2px 8px;border-radius:999px;border:1px solid #334155;background:#0b1220;font-size:12px}
  .tag{display:inline-flex;gap:6px;align-items:center;margin-right:6px}
  .muted{opacity:.8}
  .divider{height:1px;background:#203049;margin:10px 0}
  .right{margin-left:auto}
  .small{font-size:12px}
  .help{font-size:12px;opacity:.9}

  /* Totales */
  .totals{display:flex;gap:10px;flex-wrap:wrap;margin-top:10px}
  .totals .box{background:#0b1220;border:1px solid #334155;border-radius:10px;padding:8px 10px;min-width:120px}
  .ok{color:var(--ok)} .warn{color:var(--warn)} .bad{color:var(--bad)}

  /* Cajas cálculo */
  .calc-row{display:grid;grid-template-columns:1fr 1fr;gap:12px}
  .calc-box{background:var(--soft);border:1px solid #21314a;border-radius:14px;padding:12px}
  .calc-box .title{display:flex;align-items:center;gap:8px;font-weight:700;margin-bottom:8px}
  .chip{display:inline-flex;align-items:center;gap:6px;background:var(--chip);border:1px solid var(--chip-br);padding:6px 10px;border-radius:999px;font-size:12px}
  .statline{display:grid;grid-template-columns:auto 1fr;gap:6px 10px;align-items:center;font-size:13px}
  .statline span.key{color:#93c5fd}
  .mono{font-variant-numeric:tabular-nums}

  /* Volumen/Deficit layout */
  .plan-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
  .plan-card{background:#0b1220;border:1px solid #244266;border-radius:14px;padding:12px}
  .plan-card .head{display:flex;align-items:center;gap:8px;margin-bottom:8px}
  .plan-card .rows{display:grid;gap:8px}
  .plan-row{display:flex;gap:8px;align-items:center}
  .badge{font-size:11px;border:1px solid #2b3f5d;background:#0b1b35;padding:2px 8px;border-radius:999px}

  /* Dietas minimalistas */
  .diet-wrap{display:grid;gap:14px}
  .diet-card{background:#0b1220;border:1px solid #21314a;border-radius:14px;padding:12px}
  .diet-card header{display:flex;align-items:center;gap:10px;margin-bottom:8px}
  .diet-card header .subtitle{margin-left:auto;font-size:12px;color:#a5b4fc}
  .meal-list{display:grid;gap:10px;max-height:480px;overflow:auto;padding-right:4px}
  .meal-card{background:#0c1524;border:1px solid #1a2a43;border-radius:12px;padding:10px}
  .meal-card.alt{background:#0b1220}
  .meal-card header{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px}
  .meal-card .controls{display:flex;gap:8px;flex-wrap:wrap}
  .meal-items{display:grid;gap:8px}
  .meal-item{display:grid;grid-template-columns:1.2fr auto auto auto;gap:8px;align-items:center}
  .meal-item select{min-width:140px}
  .meal-item small{opacity:.8}
  .sticky-actions{position:sticky;bottom:12px;display:flex;gap:10px;justify-content:flex-end;background:transparent;padding:0 16px 16px}

  /* Tabla alimentos */
  table{width:100%;border-collapse:collapse}
  th,td{padding:8px;border-bottom:1px solid #1f2937;text-align:left}
  th{font-size:12px;color:#93c5fd}

  /* Impresión (PDF) */
  @media print{
    body{background:#fff;color:#000}
    header,.sticky-actions{display:none}
    .card{break-inside:avoid;box-shadow:none;border-color:#ddd}
    .meal-card{border-color:#ddd}
    .totals .box{border-color:#bbb;background:#fff}
  }
  /* Mejora visual del autocompletado */
  .autocomplete-list { position: absolute !important; z-index: 99999; background: var(--panel); border: 1px solid #244266; border-radius: 8px; max-height: 220px; overflow-y: auto; box-shadow: 0 6px 16px rgba(0,0,0,.5); }
  .autocomplete-list div { padding: 8px 10px; cursor: pointer; }
  .autocomplete-list div:hover { background: #1e293b; }

</style>
</head>
<body>
  <header class="row">
    <h1>Planificador de Dieta — Entreno & Descanso</h1>
    <div class="right profile">
      <label for="perfil">Perfil:</label>
      <input id="perfil" placeholder="Tu nombre" />
      <button id="btnCargar">Usar perfil</button>
      <button id="btnNuevo" class="btn-ghost">Nuevo</button>
      <button id="btnExpJSON" class="btn-ghost">Exportar JSON</button>
      <label for="impJSON" class="btn-ghost" style="cursor:pointer;">Importar JSON</label>
      <input id="impJSON" type="file" accept="application/json" style="display:none" />
      <span class="help">Autoguardado en tu navegador.</span>
    </div>
  </header>

  <section class="wrap">
    <!-- CALCULOS -->
    <div class="card" id="cardCalc">
      <header><h2>Cálculos</h2></header>
      <div class="content grid grid-3">
        <div class="col"><label>Edad</label><input type="number" id="edad" value="22" min="10" /></div>
        <div class="col"><label>Peso (kg)</label><input type="number" id="peso" step="0.1" value="88.8" /></div>
        <div class="col"><label>Altura (cm)</label><input type="number" id="altura" value="180" /></div>
        <div class="col"><label>Pasos/día</label><input type="number" id="pasos" value="2500" /></div>
        <div class="col"><label>Días de entreno/sem.</label><input type="number" id="diasEnt" value="4" min="0" max="7" /></div>
        <div class="col"><label>Sexo</label>
          <select id="sexo">
            <option value="m">Masculino</option>
            <option value="f">Femenino</option>
          </select>
        </div>

        <div style="grid-column:1/-1" class="item">
          <div class="row">
            <span class="pill">TMB: <span id="tmb" class="tag mono"></span></span>
            <span class="pill">FAD: <span id="fad" class="tag mono"></span></span>
            <span class="pill">TDEE: <span id="tdee" class="tag mono"></span></span>
          </div>
          <div class="divider"></div>

          <!-- MANTENIMIENTO -->
          <div class="calc-row">
            <div class="calc-box">
              <div class="title">🧩 Mantenimiento</div>
              <div class="statline">
                <span class="key">Kcal</span><span class="mono" id="mant"></span>
              </div>
            </div>
            <div class="calc-box">
              <div class="title">📌 Resumen rápido</div>
              <div class="statline">
                <span class="key">Entrenos/sem</span><span class="mono" id="res_dias"></span>
                <span class="key">Pasos/día</span><span class="mono" id="res_pasos"></span>
              </div>
            </div>
          </div>

          <div class="divider"></div>

          <!-- DEFICITS EN CAJAS SEPARADAS -->
          <div class="plan-grid">
            <div class="plan-card">
              <div class="head">🔥 Déficit moderado <span class="badge">ENT −20%</span> <span class="badge">DES −25%</span></div>
              <div class="rows">
                <div class="plan-row">
                  <span class="badge">ENT</span>
                  <span class="mono" id="modEnt"></span>
                </div>
                <div class="plan-row">
                  <span class="badge">DES</span>
                  <span class="mono" id="modDes"></span>
                </div>
              </div>
            </div>

            <div class="plan-card">
              <div class="head">⚡ Déficit agresivo <span class="badge">ENT −30%</span> <span class="badge">DES −33%</span></div>
              <div class="rows">
                <div class="plan-row">
                  <span class="badge">ENT</span>
                  <span class="mono" id="agrEnt"></span>
                </div>
                <div class="plan-row">
                  <span class="badge">DES</span>
                  <span class="mono" id="agrDes"></span>
                </div>
              </div>
            </div>
          </div>

          <div class="divider"></div>

          <!-- VOLUMEN EN CAJAS SEPARADAS -->
          <div class="plan-grid">
            <div class="plan-card">
              <div class="head">💪 Volumen moderado <span class="badge">ENT +10%</span> <span class="badge">DES +5%</span></div>
              <div class="rows">
                <div class="plan-row"><span class="badge">ENT</span><span class="mono" id="volModEnt"></span></div>
                <div class="plan-row"><span class="badge">DES</span><span class="mono" id="volModDes"></span></div>
              </div>
            </div>
            <div class="plan-card">
              <div class="head">🚀 Volumen agresivo <span class="badge">ENT +20%</span> <span class="badge">DES +15%</span></div>
              <div class="rows">
                <div class="plan-row"><span class="badge">ENT</span><span class="mono" id="volAgrEnt"></span></div>
                <div class="plan-row"><span class="badge">DES</span><span class="mono" id="volAgrDes"></span></div>
              </div>
            </div>
          </div>

          <div class="divider"></div>
          <div class="row">
            <label>Plan a aplicar:</label>
            <select id="plan">
              <option value="mant">Mantenimiento</option>
              <option value="def_mod">Déficit moderado</option>
              <option value="def_agr">Déficit agresivo</option>
              <option value="vol_mod">Volumen moderado</option>
              <option value="vol_agr">Volumen agresivo</option>
            </select>
            <button id="btnAplicarPlan">Aplicar plan a ENT & DES</button>
            <span class="small muted">Luego puedes editar kcal/macros manualmente.</span>
          </div>
        </div>
      </div>
    </div>

    <!-- ALIMENTOS -->
    <div class="card" id="cardFoods">
      <header><h2>Alimentos</h2></header>
      <div class="content">
        <div class="row">
          <input id="foodName" placeholder="Nombre del alimento" />
          <input id="foodP" type="number" step="0.1" placeholder="Proteína (g)" />
          <input id="foodC" type="number" step="0.1" placeholder="Carbohidratos (g)" />
          <input id="foodF" type="number" step="0.1" placeholder="Grasa (g)" />
          <input id="foodK" type="number" step="1" placeholder="Kcal (manual)" />
          <button id="addFood">Añadir</button>
        </div>
        <div class="divider"></div>
        <div class="list" id="foodsList"></div>
      </div>
    </div>

    <!-- DIETAS -->
    <div class="card" id="cardDiet">
      <header><h2>Dietas</h2></header>
      <div class="content">
        <div class="diet-wrap grid-2">
          <!-- ENTRENO -->
          <div class="diet-card">
            <header>
              <strong>ENTRENO</strong>
              <span class="subtitle">Objetivo: <span id="goalEnt"></span></span>
            </header>
            <div class="row" style="margin-bottom:6px">
              <input type="number" id="entKcal" placeholder="kcal" />
              <input type="number" id="entP" placeholder="P (g)" />
              <input type="number" id="entC" placeholder="C (g)" />
              <input type="number" id="entF" placeholder="G (g)" />
              <input type="number" id="entMeals" value="3" min="1" max="10" />
              <button id="entSetMeals">Definir comidas</button>
            </div>
            <div id="entMealsWrap" class="meal-list"></div>
            <div class="totals" id="entTotals"></div>
          </div>

          <!-- DESCANSO -->
          <div class="diet-card">
            <header>
              <strong>DESCANSO</strong>
              <span class="subtitle">Objetivo: <span id="goalDes"></span></span>
            </header>
            <div class="row" style="margin-bottom:6px">
              <input type="number" id="desKcal" placeholder="kcal" />
              <input type="number" id="desP" placeholder="P (g)" />
              <input type="number" id="desC" placeholder="C (g)" />
              <input type="number" id="desF" placeholder="G (g)" />
              <input type="number" id="desMeals" value="3" min="1" max="10" />
              <button id="desSetMeals">Definir comidas</button>
            </div>
            <div id="desMealsWrap" class="meal-list"></div>
            <div class="totals" id="desTotals"></div>
          </div>
        </div>

        <div class="sticky-actions">
            <button id="btnPDF">Exportar PDF de Dietas</button>
            <button id="btnLista">Lista de la compra</button>
        </div>
      </div>
    </div>
  </section>
<!-- Librerías necesarias para exportar PDF -->
<script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/jspdf@2.5.1/dist/jspdf.umd.min.js"></script>

<script>
/* =======================
   Helpers de estado/JSON
   ======================= */
const STORAGE_KEY = "diet_profiles_v2";
const $ = (s,ctx=document)=>ctx.querySelector(s);
const $$ = (s,ctx=document)=>Array.from(ctx.querySelectorAll(s));

function getAllProfiles(){
  try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {}; }
  catch { return {}; }
}
function saveAllProfiles(p){ localStorage.setItem(STORAGE_KEY, JSON.stringify(p)); }
function defaultState(name="default"){
  return {
    profile:name,
    calc:{edad:22,peso:70,altura:175,pasos:3000,diasEnt:3,sexo:'m'},
    objetivos:{
      entreno:{kcal:2000,p:150,c:180,f:60},
      descanso:{kcal:1800,p:150,c:120,f:60}
    },
    foods:[],
    diet:{
      entreno:{meals:[{name:"Desayuno",items:[]},{name:"Comida",items:[]},{name:"Cena",items:[]}]},
      descanso:{meals:[{name:"Desayuno",items:[]},{name:"Comida",items:[]},{name:"Cena",items:[]}]}
    }
  }
}

let state = null;
function loadProfile(name){
  const all = getAllProfiles();
  if(!all[name]) all[name] = defaultState(name);
  state = all[name];
  $("#perfil").value = name;
  renderAll();
  saveAllProfiles(all);
}
function saveState(){
  const all = getAllProfiles();
  all[state.profile] = state;
  saveAllProfiles(all);
}

/* =======================
   Cálculos (mismas fórmulas)
   ======================= */
// TMB Mifflin–St Jeor
function calcTMB({sexo,edad,peso,altura}){
  const s = (sexo==='m') ? 5 : -161;
  return Math.round((10*peso) + (6.25*altura) - (5*edad) + s);
}
// FAD calibrado (mantengo el anterior para reproducir tus números)
function calcFAD(pasos,diasEnt){
  let base =
    pasos < 3000 ? 1.25 :
    pasos < 5000 ? 1.30 :
    pasos < 8000 ? 1.40 :
    pasos < 11000 ? 1.55 : 1.7;
  base += Math.min(0.21, diasEnt * 0.035);
  return +(base.toFixed(2));
}
function kcalFromMacros(p,c,f){ return Math.round(p*4 + c*4 + f*9); }

// Construcción de objetivos por plan
function buildPlanTargets(calc){
  const {tdee, peso} = calc;
  const out = {
    mant: {ratio:{entreno:1.00, descanso:1.00}, pKg:{entreno:1.8, descanso:1.9}, fKg:{entreno:1.0, descanso:1.1}},
    def_mod: {ratio:{entreno:0.80, descanso:0.75}, pKg:{entreno:2.0, descanso:2.1}, fKg:{entreno:0.9, descanso:1.0}},
    def_agr: {ratio:{entreno:0.70, descanso:0.67}, pKg:{entreno:2.2, descanso:2.3}, fKg:{entreno:0.9, descanso:0.9}},
    vol_mod: {ratio:{entreno:1.10, descanso:1.05}, pKg:{entreno:1.8, descanso:1.9}, fKg:{entreno:1.0, descanso:1.1}},
    vol_agr: {ratio:{entreno:1.20, descanso:1.15}, pKg:{entreno:1.8, descanso:2.0}, fKg:{entreno:1.0, descanso:1.1}}
  };
  const plans = {};
  for(const key of Object.keys(out)){
    plans[key] = {entreno:{}, descanso:{}};
    ["entreno","descanso"].forEach(d=>{
      const kcal = Math.round(tdee * out[key].ratio[d]);
      const p = Math.round(peso * out[key].pKg[d]);
      const f = Math.round(peso * out[key].fKg[d]);
      const c = Math.max(0, Math.round((kcal - p*4 - f*9)/4));
      plans[key][d] = {kcal,p,c,f};
    });
  }
  return plans;
}

function computeAllCalcs(){
  const edad = +$("#edad").value;
  const peso = +$("#peso").value;
  const altura = +$("#altura").value;
  const pasos = +$("#pasos").value;
  const diasEnt = +$("#diasEnt").value;
  const sexo = $("#sexo").value;

  const tmb = calcTMB({sexo,edad,peso,altura});
  const fad = calcFAD(pasos,diasEnt);
  const tdee = +(tmb * fad).toFixed(2);

  const plans = buildPlanTargets({tmb,fad,tdee,peso});
  return {edad,peso,altura,pasos,diasEnt,sexo,tmb,fad,tdee,plans};
}

/* =======================
   Render
   ======================= */
function renderAll(){
  const c = state.calc;
  $("#edad").value=c.edad; $("#peso").value=c.peso; $("#altura").value=c.altura;
  $("#pasos").value=c.pasos; $("#diasEnt").value=c.diasEnt; $("#sexo").value=c.sexo;

  renderCalcsPanel();
  renderFoods();
  setGoalLabels();
  renderDiet("entreno");
  renderDiet("descanso");
  saveState();
}

function formatPlanLine(obj){
  return `${obj.kcal} kcal · P:${obj.p}g  G:${obj.f}g  C:${obj.c}g`;
}
function renderCalcsPanel(){
  const cal = computeAllCalcs();
  $("#tmb").textContent = cal.tmb + " kcal";
  $("#fad").textContent = cal.fad;
  $("#tdee").textContent = cal.tdee;
  $("#res_dias").textContent = state.calc.diasEnt + " días";
  $("#res_pasos").textContent = state.calc.pasos + " pasos";

  $("#mant").textContent = `${Math.round(cal.tdee)} kcal`;

  const P = cal.plans;
  $("#modEnt").textContent = formatPlanLine(P.def_mod.entreno);
  $("#modDes").textContent = formatPlanLine(P.def_mod.descanso);
  $("#agrEnt").textContent = formatPlanLine(P.def_agr.entreno);
  $("#agrDes").textContent = formatPlanLine(P.def_agr.descanso);

  $("#volModEnt").textContent = formatPlanLine(P.vol_mod.entreno);
  $("#volModDes").textContent = formatPlanLine(P.vol_mod.descanso);
  $("#volAgrEnt").textContent = formatPlanLine(P.vol_agr.entreno);
  $("#volAgrDes").textContent = formatPlanLine(P.vol_agr.descanso);
}

/* =======================
   Foods (kcal manual opcional)
   ======================= */
function foodKcalPer100(f){
  // Si tiene kcal manual, usa ese valor; si no, calcula por macros
  return (typeof f.kcal === 'number' && !isNaN(f.kcal)) ? Math.round(f.kcal) : kcalFromMacros(f.p,f.c,f.f);
}
function renderFoods() {
  const wrap = $("#foodsList");
  wrap.innerHTML = "";

  if (state.foods.length === 0) {
    wrap.innerHTML = `<div class="muted small">Aún no hay alimentos. Añade arriba (por 100 g).</div>`;
    return;
  }

  const tbl = document.createElement("table");
  tbl.innerHTML = `
    <thead>
      <tr>
        <th>Alimento</th>
        <th>P</th>
        <th>C</th>
        <th>G</th>
        <th>Kcal (100g)</th>
        <th>Acciones</th>
      </tr>
    </thead>`;
  const tb = document.createElement("tbody");

  state.foods.forEach((f, idx) => {
    const kcal = foodKcalPer100(f);
    const tr = document.createElement("tr");
    tr.innerHTML = `
      <td>${f.name}</td>
      <td>${f.p}</td>
      <td>${f.c}</td>
      <td>${f.f}</td>
      <td>${kcal}</td>
      <td>
        <button class="btn-ghost" id="editFood_${idx}">Editar</button>
        <button class="btn-ghost" id="delFood_${idx}">Borrar</button>
      </td>`;
    tb.appendChild(tr);
  });

  tbl.appendChild(tb);
  wrap.appendChild(tbl);

  // === BORRAR ===
  state.foods.forEach((_, idx) => {
    document.getElementById(`delFood_${idx}`).onclick = () => {
      if (!confirm("¿Eliminar este alimento?")) return;
      state.foods.splice(idx, 1);
      ["entreno", "descanso"].forEach((kind) => {
        state.diet[kind].meals.forEach((m) => {
          m.items = m.items.filter(
            (it) => state.foods.find((ff) => ff.id === it.foodId)
          );
        });
      });
      renderAll();
    };
  });

  // === EDITAR ===
  state.foods.forEach((f, idx) => {
    document.getElementById(`editFood_${idx}`).onclick = () => {
      const tr = wrap.querySelectorAll("tbody tr")[idx];
      const kcal = foodKcalPer100(f);

      // Cambiar celdas a inputs
      tr.innerHTML = `
        <td><input type="text" id="nameEdit_${idx}" value="${f.name}" style="width:160px; padding:6px 8px; border-radius:8px;"></td>
        <td><input type="number" step="0.1" id="pEdit_${idx}" value="${f.p}" style="width:70px; padding:6px 8px; border-radius:8px; text-align:center;"></td>
        <td><input type="number" step="0.1" id="cEdit_${idx}" value="${f.c}" style="width:70px; padding:6px 8px; border-radius:8px; text-align:center;"></td>
        <td><input type="number" step="0.1" id="fEdit_${idx}" value="${f.f}" style="width:70px; padding:6px 8px; border-radius:8px; text-align:center;"></td>
        <td><input type="number" step="1" id="kEdit_${idx}" value="${kcal}" style="width:80px; padding:6px 8px; border-radius:8px; text-align:center;"></td>
        <td style="white-space:nowrap;">
          <button class="btn-ghost" id="saveFood_${idx}" style="margin-right:4px;">Guardar</button>
          <button class="btn-ghost" id="cancelFood_${idx}">Cancelar</button>
        </td>`;

      // Guardar cambios
      document.getElementById(`saveFood_${idx}`).onclick = () => {
        const newName = $("#nameEdit_" + idx).value.trim();
        const newP = +$("#pEdit_" + idx).value;
        const newC = +$("#cEdit_" + idx).value;
        const newF = +$("#fEdit_" + idx).value;
        const newK = +$("#kEdit_" + idx).value;

        if (!newName || isNaN(newP) || isNaN(newC) || isNaN(newF)) {
          alert("Rellena correctamente todos los campos.");
          return;
        }

        // Actualizar el alimento
        state.foods[idx].name = newName;
        state.foods[idx].p = +newP.toFixed(1);
        state.foods[idx].c = +newC.toFixed(1);
        state.foods[idx].f = +newF.toFixed(1);
        if (!isNaN(newK)) state.foods[idx].kcal = newK;

        saveState();
        renderFoods();
        renderTotals("entreno");
        renderTotals("descanso");
      };

      // Cancelar edición
      document.getElementById(`cancelFood_${idx}`).onclick = () => {
        renderFoods();
      };
    };
  });
}


// Modifica el botón de añadir alimento para soportar "actualizar"
$("#addFood").onclick = () => {
  const name = $("#foodName").value.trim();
  const p = +$("#foodP").value;
  const c = +$("#foodC").value;
  const f = +$("#foodF").value;
  const kcalManual = $("#foodK").value.trim();

  if (!name || isNaN(p) || isNaN(c) || isNaN(f)) {
    alert("Rellena nombre y macros por 100 g.");
    return;
  }

  const kcal = kcalManual !== "" && !isNaN(+kcalManual) ? Math.round(+kcalManual) : undefined;

  const editIndex = $("#addFood").dataset.editIndex;

  if (editIndex !== undefined && editIndex !== "") {
    // Estamos editando
    const i = +editIndex;
    state.foods[i].name = name;
    state.foods[i].p = +p.toFixed(1);
    state.foods[i].c = +c.toFixed(1);
    state.foods[i].f = +f.toFixed(1);
    if (kcal) state.foods[i].kcal = kcal;

    delete $("#addFood").dataset.editIndex;
    $("#addFood").textContent = "Añadir";
  } else {
    // Añadir nuevo
    const id = "f_" + Math.random().toString(36).slice(2, 9);
    const food = { id, name, p: +p.toFixed(1), c: +c.toFixed(1), f: +f.toFixed(1) };
    if (kcal) food.kcal = kcal;
    state.foods.push(food);
  }

  // Limpiar inputs
  $("#foodName").value = $("#foodP").value = $("#foodC").value = $("#foodF").value = $("#foodK").value = "";
  $("#addFood").textContent = "Añadir";

  renderFoods();
  renderTotals("entreno");
  renderTotals("descanso");
  saveState();
};


/* =======================
   Dietas (UI minimal)
   ======================= */
function setGoalLabels(){
  const e = state.objetivos.entreno, d = state.objetivos.descanso;
  $("#goalEnt").textContent = `${e.kcal} kcal · P${e.p} C${e.c} G${e.f}`;
  $("#goalDes").textContent = `${d.kcal} kcal · P${d.p} C${d.c} G${d.f}`;
  $("#entKcal").value=e.kcal; $("#entP").value=e.p; $("#entC").value=e.c; $("#entF").value=e.f;
  $("#desKcal").value=d.kcal; $("#desP").value=d.p; $("#desC").value=d.c; $("#desF").value=d.f;
}

function renderDiet(kind){
  const area = kind==="entreno" ? $("#entMealsWrap") : $("#desMealsWrap");
  area.innerHTML="";
  const diet = state.diet[kind];
  const foods = state.foods;

  diet.meals.forEach((meal, mi)=>{
    const box = document.createElement("div");
    box.className="meal-card" + (mi%2 ? " alt" : "");
    const nameId = `${kind}-meal-${mi}-name`;
    box.innerHTML = `
      <header>
        <input id="${nameId}" value="${meal.name||('Comida '+(mi+1))}" />
        <div class="controls">
          <button class="btn-ghost" data-add="${mi}">Añadir alimento</button>
          <button class="btn-ghost" data-clear="${mi}">Vaciar</button>
          <button class="btn-ghost" data-remove="${mi}">Eliminar</button>
        </div>
      </header>
      <div class="meal-items" id="${kind}-meal-${mi}-list"></div>
    `;
    area.appendChild(box);

    const list = $(`#${kind}-meal-${mi}-list`);
meal.items.forEach((it, ii) => {
    const row = document.createElement("div");
    row.className = "meal-item";
    const selId = `${kind}-${mi}-${ii}-sel`;
    const qtyId = `${kind}-${mi}-${ii}-qty`;

    const note = foods.find(f => f.id === it.foodId) || { name: "", p: 0, c: 0, f: 0, kcal: 0 };

    row.innerHTML = `
      <div style="position:relative;flex:1;">
        <input type="text" id="${selId}" placeholder="Buscar alimento..." value="${note.name || ""}" 
          style="width:100%;padding:8px;border-radius:8px;">
        <div id="${selId}_list" class="autocomplete-list" 
          style="position:absolute;z-index:5;top:35px;left:0;right:0;background:#0b1220;
          border:1px solid #244266;border-radius:8px;max-height:180px;overflow:auto;display:none;"></div>
      </div>
      <input id="${qtyId}" type="number" step="1" value="${it.g || 100}" style="width:70px;text-align:center;" />
      <small>g</small>
      <button class="btn-ghost" id="${kind}-del-${mi}-${ii}">Eliminar</button>
    `;

    const input = row.querySelector(`#${selId}`);
    // === AUTOCOMPLETADO ===
    const listBox = row.querySelector(`#${selId}_list`);

    // Mueve la lista al <body> para que no se recorte dentro de contenedores con overflow
    document.body.appendChild(listBox);

    // 🔎 Mostrar resultados
    input.addEventListener("input", (e) => {
      const term = e.target.value.toLowerCase();
      const matches = foods.filter(f => f.name.toLowerCase().includes(term));

      listBox.innerHTML = matches.length
        ? matches.map(f => `<div data-id="${f.id}" style="padding:6px 10px;cursor:pointer;">${f.name}</div>`).join("")
        : "<div style='padding:6px;color:#999;'>Sin resultados</div>";

      // posición dinámica justo debajo del input
      const rect = input.getBoundingClientRect();
      listBox.style.position = "absolute";
      listBox.style.top = `${rect.bottom + window.scrollY}px`;
      listBox.style.left = `${rect.left + window.scrollX}px`;
      listBox.style.width = `${rect.width}px`;
      listBox.style.display = "block";
    });


    // 🖱 Selección
    listBox.addEventListener("click", (e) => {
      const opt = e.target.closest("[data-id]");
      if (!opt) return;
      const selected = foods.find(f => f.id === opt.dataset.id);
      if (!selected) return;
      it.foodId = selected.id;
      input.value = selected.name;
      listBox.style.display = "none";
      renderTotals(kind);
      saveState();
    });

    // Ocultar si clic fuera
    document.addEventListener("click", (e) => {
      if (!row.contains(e.target)) listBox.style.display = "none";
    });

    // Cantidad
    row.querySelector(`#${qtyId}`).addEventListener("input", (e) => {
      it.g = +e.target.value || 0;
      renderTotals(kind);
      saveState();
    });

    // Eliminar
    row.querySelector(`#${kind}-del-${mi}-${ii}`).onclick = () => {
      meal.items.splice(ii, 1);
      renderDiet(kind);
      renderTotals(kind);
      saveState();
    };

    // Añadir la fila
    list.appendChild(row);

    // 🎯 Foco automático al crear nuevo alimento
    if (ii === meal.items.length - 1) {
      setTimeout(() => input.focus(), 50);
    }
  });

    document.getElementById(nameId).oninput = (e)=>{ meal.name = e.target.value; saveState(); };
    box.querySelector("[data-add]").onclick = ()=>{
      if(foods.length===0){ 
        alert("Primero crea alimentos en el panel de Alimentos."); 
        return; 
      }
      // Crea item vacío sin preseleccionar ningún alimento
      meal.items.push({foodId: null, g: 100});
      renderDiet(kind);
      // tras render, enfoca el campo de búsqueda vacío
      setTimeout(() => {
        const inputs = area.querySelectorAll('input[placeholder="Buscar alimento..."]');
        if (inputs.length) inputs[inputs.length - 1].focus();
      }, 100);
      renderTotals(kind);
      saveState();
    };
    box.querySelector("[data-clear]").onclick = ()=>{
      if(confirm("¿Vaciar esta comida?")){ meal.items=[]; renderDiet(kind); renderTotals(kind); saveState(); }
    };
    box.querySelector("[data-remove]").onclick = ()=>{
      if(confirm("¿Eliminar esta comida?")){ diet.meals.splice(mi,1); renderDiet(kind); renderTotals(kind); saveState(); }
    };
  });

  renderTotals(kind);
}

function dietTotals(kind){
  const foods = state.foods;
  const d = state.diet[kind];
  let P=0,C=0,F=0,K=0;
  d.meals.forEach(m=>{
    m.items.forEach(it=>{
      const f = foods.find(x=>x.id===it.foodId);
      if(!f) return;
      const factor = (it.g||0)/100;
      P += f.p*factor; C += f.c*factor; F += f.f*factor;
      K += foodKcalPer100(f)*factor; // kcal por alimento (manual si existe)
    });
  });
  return {P:+P.toFixed(1), C:+C.toFixed(1), F:+F.toFixed(1), K:Math.round(K)};
}
function currentGoal(kind){ return state.objetivos[kind]; }
function macroClass(total, target){
  if(!target || target<=0) return "";
  const diff = Math.abs(total - target)/target;
  if(diff <= 0.05) return "ok";
  if(diff <= 0.25) return "warn";
  return "bad";
}
function renderTotals(kind){
  const t = dietTotals(kind);
  const g = currentGoal(kind);
  const area = (kind==="entreno") ? $("#entTotals") : $("#desTotals");
  area.innerHTML = "";
  [["kcal", t.K, g.kcal], ["Proteína", t.P, g.p], ["Carbos", t.C, g.c], ["Grasa", t.F, g.f]]
  .forEach(([label,total,target])=>{
    const b = document.createElement("div"); b.className="box";
    const cls = macroClass(total, target);
    b.innerHTML = `<div class="${cls}"><strong>${label}</strong><br class="mono">${Math.round(total)} / ${target}</div>`;
    area.appendChild(b);
  });
}

/* =======================
   Eventos UI
   ======================= */
// Perfil
$("#btnCargar").onclick = ()=>{
  const name = ($("#perfil").value||"default").trim();
  if(!name) return;
  loadProfile(name);
};
$("#btnNuevo").onclick = ()=>{
  const name = prompt("Nombre del nuevo perfil:");
  if(!name) return;
  const all = getAllProfiles();
  all[name] = defaultState(name);
  saveAllProfiles(all);
  loadProfile(name);
};

// Exportar/Importar JSON
$("#btnExpJSON").onclick = ()=>{
  const all = getAllProfiles();
  const blob = new Blob([JSON.stringify(all,null,2)], {type:"application/json"});
  const a = document.createElement("a");
  a.href = URL.createObjectURL(blob);
  a.download = "diet_profiles.json";
  a.click();
  URL.revokeObjectURL(a.href);
};
$("#impJSON").onchange = (e)=>{
  const file = e.target.files[0]; if(!file) return;
  const fr = new FileReader();
  fr.onload = ()=>{
    try{
      const data = JSON.parse(fr.result);
      saveAllProfiles(data);
      const first = Object.keys(data)[0] || "default";
      loadProfile(first);
      alert("Perfiles importados.");
    }catch(err){ alert("JSON inválido."); }
  };
  fr.readAsText(file);
};

// Inputs de cálculo → tiempo real
["edad","peso","altura","pasos","diasEnt","sexo"].forEach(id=>{
  document.getElementById(id).addEventListener("input", ()=>{
    state.calc = {
      edad:+$("#edad").value, peso:+$("#peso").value, altura:+$("#altura").value,
      pasos:+$("#pasos").value, diasEnt:+$("#diasEnt").value, sexo:$("#sexo").value
    };
    renderCalcsPanel(); saveState();
  });
});

// Aplicar plan a ENT & DES
$("#btnAplicarPlan").onclick = ()=>{
  const cal = computeAllCalcs();
  const plan = $("#plan").value;
  const targets = cal.plans[plan];
  state.objetivos.entreno = {...targets.entreno};
  state.objetivos.descanso = {...targets.descanso};
  setGoalLabels();
  renderTotals("entreno"); renderTotals("descanso");
  saveState();
};

// Alimentos (añadir con kcal manual opcional)
$("#addFood").onclick = ()=>{
  const name = $("#foodName").value.trim();
  const p = +$("#foodP").value, c = +$("#foodC").value, f = +$("#foodF").value;
  const kcalManual = $("#foodK").value.trim();
  if(!name || isNaN(p) || isNaN(c) || isNaN(f)) { alert("Rellena nombre y macros por 100 g."); return; }
  const id = "f_"+Math.random().toString(36).slice(2,9);
  const food = {id,name,p:+p.toFixed(1),c:+c.toFixed(1),f:+f.toFixed(1)};
  if(kcalManual !== "" && !isNaN(+kcalManual)) food.kcal = Math.round(+kcalManual);
  state.foods.push(food);
  $("#foodName").value = $("#foodP").value = $("#foodC").value = $("#foodF").value = $("#foodK").value = "";
  renderFoods(); renderTotals("entreno"); renderTotals("descanso"); saveState();
};

// Set meals count
$("#entSetMeals").onclick = ()=>{ const n = Math.max(1, Math.min(10, +$("#entMeals").value||3)); setMealsCount("entreno", n); };
$("#desSetMeals").onclick = ()=>{ const n = Math.max(1, Math.min(10, +$("#desMeals").value||3)); setMealsCount("descanso", n); };
function setMealsCount(kind, n){
  const meals = state.diet[kind].meals;
  while(meals.length<n) meals.push({name:`Comida ${meals.length+1}`,items:[]});
  while(meals.length>n) meals.pop();
  renderDiet(kind); saveState();
}

// Objetivos manuales en tiempo real
["entKcal","entP","entC","entF"].forEach(id=>{
  document.getElementById(id).addEventListener("input", ()=>{
    state.objetivos.entreno = {
      kcal:+$("#entKcal").value||0, p:+$("#entP").value||0,
      c:+$("#entC").value||0, f:+$("#entF").value||0
    };
    setGoalLabels(); renderTotals("entreno"); saveState();
  });
});
["desKcal","desP","desC","desF"].forEach(id=>{
  document.getElementById(id).addEventListener("input", ()=>{
    state.objetivos.descanso = {
      kcal:+$("#desKcal").value||0, p:+$("#desP").value||0,
      c:+$("#desC").value||0, f:+$("#desF").value||0
    };
    setGoalLabels(); renderTotals("descanso"); saveState();
  });
});

/* =======================
   Inicio
   ======================= */
window.addEventListener("beforeunload", saveState);
document.addEventListener("DOMContentLoaded", ()=>{
  const existing = Object.keys(getAllProfiles())[0] || "Alvaro";
  loadProfile(existing);
});
/* =======================
   Exportar PDF de dietas (limpio, en columnas + subtotales)
   ======================= */
function exportDietasPDF() {
  const { jsPDF } = window.jspdf;
  const pdf = new jsPDF("p", "mm", "a4");

  const M = 14;          // margen
  const LH = 7;          // alto de línea
  const PW = pdf.internal.pageSize.getWidth();

  // Columnas (usa sólo ASCII para evitar símbolos raros)
  const COLS = {
    name: M,
    qty: 125,
    kcal: 150,
    P: 172,
    C: 188,
    F: 204
  };

  function fmt(n, d = 0) { return (Number(n) || 0).toFixed(d); }
  function kcal100(f){ return typeof f.kcal === "number" ? f.kcal : Math.round(f.p*4 + f.c*4 + f.f*9); }
  function itemFrom(f, g){
    const factor = (g||0)/100;
    return {
      kcal: Math.round(kcal100(f) * factor),
      P: +(f.p * factor).toFixed(1),
      C: +(f.c * factor).toFixed(1),
      F: +(f.f * factor).toFixed(1)
    };
  }
  function hr(y){ pdf.setDrawColor(180); pdf.line(M, y, PW-M, y); }

  function header(title){
    let y = M;
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(18); pdf.setTextColor(20);
    pdf.text("Dieta - " + title, PW/2, y, {align:"center"}); y += 8;
    pdf.setFont("helvetica", "normal"); pdf.setFontSize(11); pdf.setTextColor(80);
    pdf.text(`Perfil: ${(document.getElementById("perfil").value||"Usuario")}  |  Fecha: ${new Date().toLocaleDateString()}`, PW/2, y, {align:"center"});
    y += 6; pdf.setTextColor(0);
    hr(y); y += 6;

    // Encabezado de tabla
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(11);
    pdf.text("Alimento", COLS.name, y);
    pdf.text("g", COLS.qty, y, {align:"right"});
    pdf.text("kcal", COLS.kcal, y, {align:"right"});
    pdf.text("P", COLS.P, y, {align:"right"});
    pdf.text("C", COLS.C, y, {align:"right"});
    pdf.text("G", COLS.F, y, {align:"right"});
    y += 3; hr(y); y += 6;
    return y;
  }

  function ensureSpace(y, linesNeeded=1){
    if (y + linesNeeded*LH > 285){
      pdf.addPage();
      y = header("Continuación");
    }
    return y;
  }

  function objetivoNutricional(kind, y){
    const g = state.objetivos[kind];
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(12);
    pdf.text("Objetivo nutricional", M, y); y += LH;
    pdf.setFont("courier", "normal"); pdf.setFontSize(11);
    pdf.text(`Kcal: ${g.kcal}  |  Proteínas: ${g.p}g  |  Carbohidratos: ${g.c}g  |  Grasas: ${g.f}g`, M, y);
    y += LH; hr(y); y += 4;
    return y;
  }

  function drawRow(name, g, kcal, P, C, F, y){
    // corta nombre a una anchura razonable (ASCII, sin elipsis unicode)
    const maxChars = 42;
    const clean = (name||"").toString();
    const label = clean.length>maxChars ? clean.slice(0,maxChars-3)+"..." : clean;

    pdf.setFont("helvetica", "normal"); pdf.setFontSize(11);
    pdf.text(label, COLS.name, y);

    pdf.setFont("courier", "normal"); // columnas numéricas monoespaciadas
    pdf.text(fmt(g,0), COLS.qty, y, {align:"right"});
    pdf.text(fmt(kcal,0), COLS.kcal, y, {align:"right"});
    pdf.text(fmt(P,1), COLS.P, y, {align:"right"});
    pdf.text(fmt(C,1), COLS.C, y, {align:"right"});
    pdf.text(fmt(F,1), COLS.F, y, {align:"right"});
  }

  function mealBlock(meal, foods, y, idx){
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(12);
    pdf.text(`${idx+1}. ${meal.name||("Comida "+(idx+1))}`, M, y); y += LH;

    let tot = {kcal:0,P:0,C:0,F:0};

    if (!meal.items.length){
      pdf.setFont("helvetica", "italic"); pdf.setFontSize(11); pdf.setTextColor(120);
      pdf.text("(sin alimentos)", M+4, y); pdf.setTextColor(0); y += LH;
    }else{
      meal.items.forEach(it=>{
        const f = foods.find(x=>x.id===it.foodId);
        if(!f) return;
        const g = Number(it.g)||0;
        const m = itemFrom(f, g);
        y = ensureSpace(y);
        drawRow(f.name, g, m.kcal, m.P, m.C, m.F, y);
        y += LH;
        tot.kcal += m.kcal; tot.P += m.P; tot.C += m.C; tot.F += m.F;
      });
    }

    // Subtotal de la comida
    y = ensureSpace(y);
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(11);
    pdf.text("Subtotal comida:", M, y);
    pdf.setFont("courier", "bold");
    pdf.text(fmt(tot.kcal,0), COLS.kcal, y, {align:"right"});
    pdf.text(fmt(tot.P,1), COLS.P, y, {align:"right"});
    pdf.text(fmt(tot.C,1), COLS.C, y, {align:"right"});
    pdf.text(fmt(tot.F,1), COLS.F, y, {align:"right"});
    y += LH; hr(y); y += 5;

    return { y, tot };
  }

  function section(kind, tituloPagina){
    let y = header(tituloPagina);
    y = objetivoNutricional(kind, y);

    const diet = state.diet[kind];
    const foods = state.foods;
    let grand = {kcal:0,P:0,C:0,F:0};

    diet.meals.forEach((meal, i)=>{
      const r = mealBlock(meal, foods, y, i);
      y = r.y;
      grand.kcal += r.tot.kcal; grand.P += r.tot.P; grand.C += r.tot.C; grand.F += r.tot.F;
      y = ensureSpace(y, 3);
    });

    // Totales del día
    pdf.setFont("helvetica", "bold"); pdf.setFontSize(12);
    pdf.text("Totales del día", M, y); y += LH;
    pdf.setFont("courier", "bold"); pdf.setFontSize(11);
    pdf.text(`Kcal: ${fmt(grand.kcal,0)}  |  P: ${fmt(grand.P,1)}g  |  C: ${fmt(grand.C,1)}g  |  G: ${fmt(grand.F,1)}g`, M, y);
  }

  // Página 1: ENT | Página 2: DES
  section("entreno", "Día de Entrenamiento");
  pdf.addPage();
  section("descanso", "Día de Descanso");

  // Pie
  pdf.setFont("helvetica","italic"); pdf.setFontSize(9); pdf.setTextColor(120);
  pdf.text("Generado automáticamente — Planificador de Dieta", PW/2, 293, {align:"center"});
  pdf.setTextColor(0);

  pdf.save("Dieta_Personalizada.pdf");
}

document.getElementById("btnPDF").addEventListener("click", exportDietasPDF);

/* =======================
   🛒 Exportar Lista de la Compra
   ======================= */
function exportListaCompra() {
  const { jsPDF } = window.jspdf;
  const pdf = new jsPDF("p", "mm", "a4");
  const M = 14, LH = 7, PW = pdf.internal.pageSize.getWidth();
  function fmt(n, d = 0) { return (Number(n) || 0).toFixed(d); }

  // === Pide número de días ===
  let dias = parseInt(prompt("¿Para cuántos días quieres la lista de la compra?", "7"));
  if (isNaN(dias) || dias <= 0) dias = 7;

  // === Reúne todos los alimentos de entreno y descanso ===
  const foods = state.foods;
  const lista = {}; // { nombre: gramos }

  ["entreno", "descanso"].forEach(kind => {
    state.diet[kind].meals.forEach(meal => {
      meal.items.forEach(it => {
        const f = foods.find(x => x.id === it.foodId);
        if (!f) return;
        const g = Number(it.g) || 0;
        if (!lista[f.name]) lista[f.name] = 0;
        lista[f.name] += g;
      });
    });
  });

  // === Multiplica por número de días ===
  Object.keys(lista).forEach(k => lista[k] *= dias);

  // === Generar PDF ===
  pdf.setFont("helvetica", "bold"); pdf.setFontSize(18);
  pdf.text("Lista de la compra", PW / 2, M, { align: "center" });
  pdf.setFont("helvetica", "normal"); pdf.setFontSize(11);
  pdf.text(`Perfil: ${(document.getElementById("perfil").value || "Usuario")}  |  ${new Date().toLocaleDateString()}`, PW / 2, M + 8, { align: "center" });
  pdf.line(M, M + 10, PW - M, M + 10);

  let y = M + 18;
  pdf.setFont("helvetica", "bold");
  pdf.text("Alimento", M, y);
  pdf.text("Cantidad (g)", PW - M, y, { align: "right" });
  y += LH;
  pdf.line(M, y - 4, PW - M, y - 4);

  pdf.setFont("helvetica", "normal");
  Object.entries(lista).forEach(([nombre, gramos]) => {
    if (y > 280) { pdf.addPage(); y = M; }
    const label = nombre.length > 45 ? nombre.slice(0, 42) + "..." : nombre;
    pdf.text(label, M, y);
    pdf.text(fmt(gramos, 0), PW - M, y, { align: "right" });
    y += LH;
  });

  y += 6;
  pdf.setFont("helvetica", "italic"); pdf.setFontSize(10); pdf.setTextColor(120);
  pdf.text(`Cantidad total calculada para ${dias} día(s)`, PW / 2, y, { align: "center" });
  y += 6;
  pdf.text("Generado automáticamente — Planificador de Dieta", PW / 2, 293, { align: "center" });

  pdf.save(`Lista_Compra_${dias}dias.pdf`);
}

// Vincular botón
document.getElementById("btnLista").addEventListener("click", exportListaCompra);


/* =======================
   🔘 AUTOCOMPLETAR MACROS (por dieta)
   ======================= */

// Inserta los botones junto al de "Definir comidas"
function addAutoButtons() {
  const entRow = $("#entSetMeals").closest(".row");
  const desRow = $("#desSetMeals").closest(".row");

  if (entRow && !$("#btnAutoEnt")) {
    const btnEnt = document.createElement("button");
    btnEnt.id = "btnAutoEnt";
    btnEnt.textContent = "⚙️ Autocompletar ENT";
    btnEnt.className = "btnAuto";
    btnEnt.title = "Ajustar automáticamente macros y kcal del día de entreno";
    btnEnt.onclick = () => autoCompleteMacros("entreno");
    entRow.appendChild(btnEnt);
  }

  if (desRow && !$("#btnAutoDes")) {
    const btnDes = document.createElement("button");
    btnDes.id = "btnAutoDes";
    btnDes.textContent = "⚙️ Autocompletar DES";
    btnDes.className = "btnAuto";
    btnDes.title = "Ajustar automáticamente macros y kcal del día de descanso";
    btnDes.onclick = () => autoCompleteMacros("descanso");
    desRow.appendChild(btnDes);
  }
}

// 💅 Estilo visual del botón (azul brillante con glow)
const style = document.createElement("style");
style.textContent = `
  .btnAuto {
    background: linear-gradient(135deg, #2563eb, #3b82f6);
    border: 1px solid #60a5fa;
    color: white;
    font-weight: 600;
    border-radius: 10px;
    padding: 10px 14px;
    cursor: pointer;
    box-shadow: 0 0 10px rgba(59,130,246,0.4);
    transition: all 0.25s ease;
  }
  .btnAuto:hover {
    background: linear-gradient(135deg, #1d4ed8, #2563eb);
    box-shadow: 0 0 16px rgba(96,165,250,0.7);
    transform: translateY(-1px);
  }
`;
document.head.appendChild(style);

// ======= Lógica principal =======
function autoCompleteMacros(kind){
  const totals = dietTotals(kind);
  const goal = currentGoal(kind);
  const diffKcal = goal.kcal - totals.K;

  if(Math.abs(diffKcal) < 10){
    alert(`✅ ${kind.toUpperCase()} ya está equilibrada.`);
    return;
  }

  const foods = state.foods;
  const meals = state.diet[kind].meals;

  // Recoge todos los alimentos usados en la dieta
  let items = [];
  meals.forEach((m,mi)=>{
    m.items.forEach((it,ii)=>{
      const f = foods.find(ff=>ff.id===it.foodId);
      if(f && it.g>0) items.push({mi,ii,it,f});
    });
  });

  if(items.length===0){
    alert(`No hay alimentos en la dieta de ${kind}.`);
    return;
  }

  // Calcular kcal por alimento
  items.forEach(o=>{
    o.kcal = foodKcalPer100(o.f) * (o.it.g/100);
  });

  // Desviaciones por macro
  const diffP = goal.p - totals.P;
  const diffC = goal.c - totals.C;
  const diffF = goal.f - totals.F;

  // Clasificar alimentos según su macro dominante
  const proteinFoods = items.filter(o=>o.f.p>o.f.c && o.f.p>o.f.f);
  const carbFoods    = items.filter(o=>o.f.c>o.f.p && o.f.c>o.f.f);
  const fatFoods     = items.filter(o=>o.f.f>o.f.p && o.f.f>o.f.c);

  function adjustGroup(group, diff){
    if(!group.length || diff===0) return;
    const perItem = diff / group.length;
    group.forEach(o=>{
      const currentG = o.it.g;
      const macroPer100 = (o.f.p>o.f.c && o.f.p>o.f.f)? o.f.p :
                          (o.f.c>o.f.p && o.f.c>o.f.f)? o.f.c : o.f.f;
      const adj = (perItem / macroPer100) * 100; // gramos a añadir o restar
      o.it.g = Math.max(0, Math.round(currentG + adj));
    });
  }

  // Ajustes lógicos macro a macro
  adjustGroup(proteinFoods, diffP);
  adjustGroup(carbFoods, diffC);
  adjustGroup(fatFoods, diffF);

  // Ajuste fino final según kcal totales
  const newTotals = dietTotals(kind);
  if(newTotals.K > 0){
    const kcalRatio = goal.kcal / newTotals.K;
    items.forEach(o=>{
      o.it.g = Math.max(0, Math.round(o.it.g * kcalRatio));

    });
  }

  renderDiet(kind);
  renderTotals(kind);
  saveState();

  alert(`⚙️ ${kind.toUpperCase()} ajustada automáticamente a sus macros y kcal objetivo.`);
}

// Iniciar los botones al cargar
document.addEventListener("DOMContentLoaded", addAutoButtons);

</script>

</body>
</html>
