<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Repositorio de Proyectos · Talento Humano · Banco del Austro</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0B1330; --panel:#141F45; --panel-2:#1A2850; --border:#273669;
  --text:#F2F4FB; --muted:#93A0C8; --accent:#F7A026;
  --accent-soft:rgba(247,160,38,.14); --red:#E3272E;
  --st-todo:#F97316; --st-doing:#FBBF24; --st-done:#34D399;
  --radius:14px;
  --mono:'JetBrains Mono',ui-monospace,SFMono-Regular,Menlo,Consolas,monospace;
  --sans:'Inter',-apple-system,'Segoe UI',Roboto,sans-serif;
}
*{margin:0;padding:0;box-sizing:border-box}
body{
  font-family:var(--sans);
  background:
    radial-gradient(1200px 600px at 85% -10%, rgba(247,160,38,.07), transparent 60%),
    radial-gradient(900px 500px at -10% 110%, rgba(52,211,153,.05), transparent 60%),
    var(--bg);
  color:var(--text); min-height:100dvh; font-size:15px; line-height:1.55;
}
::selection{background:rgba(247,160,38,.35)}
::-webkit-scrollbar{width:8px;height:8px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:4px}
button{font-family:inherit;cursor:pointer;border:none;background:none;color:inherit}
button:focus-visible,a:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible{
  outline:none;box-shadow:0 0 0 2px var(--bg),0 0 0 4px var(--accent);border-radius:6px
}
a{color:var(--accent)}

/* ============ HEADER ============ */
.topbar{position:sticky;top:0;z-index:50;display:flex;align-items:center;gap:18px;flex-wrap:wrap;
  padding:12px 24px;background:rgba(11,19,48,.88);backdrop-filter:blur(10px);border-bottom:1px solid var(--border)}
.brand{display:flex;align-items:center;gap:12px;min-width:0}
.brand-mark{display:flex;gap:3px;align-items:flex-end;flex:none}
.brand-mark i{display:block;width:7px;border-radius:2px;transform:skewX(-14deg)}
.brand-mark i:nth-child(1){height:14px;background:var(--accent)}
.brand-mark i:nth-child(2){height:22px;background:var(--red)}
.brand-mark i:nth-child(3){height:30px;background:var(--text)}
.brand-text b{font-size:15px;font-weight:800;display:block;white-space:nowrap}
.brand-text span{font-family:var(--mono);font-size:10px;letter-spacing:.22em;text-transform:uppercase;color:var(--accent);display:block}

.nav{display:flex;gap:4px;margin-left:8px}
.nav-btn{
  font-family:var(--mono);font-size:11px;font-weight:500;letter-spacing:.12em;text-transform:uppercase;
  color:var(--muted);padding:9px 16px;border-radius:9px;position:relative;transition:all .15s ease
}
.nav-btn:hover{color:var(--text);background:var(--accent-soft)}
.nav-btn.active{color:var(--accent)}
.nav-btn.active::after{content:"";position:absolute;left:14px;right:14px;bottom:3px;height:2px;background:var(--accent);border-radius:1px}

.actions{display:flex;gap:8px;margin-left:auto;flex-wrap:wrap}
.btn{display:inline-flex;align-items:center;gap:7px;font-family:var(--mono);font-size:11px;font-weight:500;
  letter-spacing:.1em;text-transform:uppercase;padding:9px 16px;border-radius:999px;
  border:1px solid var(--border);color:var(--text);background:transparent;transition:all .15s ease}
.btn:hover{border-color:var(--accent);background:var(--accent-soft);transform:translateY(-1px)}
.btn.primary{background:var(--accent);border-color:var(--accent);color:#1A1206;font-weight:700}
.btn.primary:hover{background:#ffb94a;border-color:#ffb94a}
.btn.danger:hover{border-color:var(--red);background:rgba(227,39,46,.12);color:#ff8f93}
.btn svg{width:13px;height:13px}

/* ============ LAYOUT ============ */
main{padding:22px 24px 48px;max-width:1600px;margin:0 auto}
.view{display:none}
.view.active{display:block;animation:rise .3s ease-out}
@keyframes rise{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}

.view-title{display:flex;align-items:baseline;gap:14px;margin-bottom:18px;flex-wrap:wrap}
.view-title h1{font-size:20px;font-weight:800;letter-spacing:-.01em}
.view-title span{font-family:var(--mono);font-size:10px;letter-spacing:.18em;text-transform:uppercase;color:var(--muted)}

/* ============ STATS ============ */
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:10px;margin-bottom:18px}
.stat{background:var(--panel);border:1px solid var(--border);border-radius:12px;padding:14px 16px}
.stat b{font-family:var(--mono);font-size:26px;font-weight:700;display:block;line-height:1.1}
.stat span{font-family:var(--mono);font-size:9px;letter-spacing:.16em;text-transform:uppercase;color:var(--muted)}
.stat.s-todo b{color:var(--st-todo)} .stat.s-doing b{color:var(--st-doing)}
.stat.s-done b{color:var(--st-done)} .stat.s-avg b{color:var(--accent)}

/* ============ DASHBOARD CHARTS ============ */
.charts{display:grid;grid-template-columns:minmax(300px,380px) 1fr;gap:16px;margin-bottom:18px}
@media (max-width:900px){.charts{grid-template-columns:1fr}}
.panel{background:var(--panel);border:1px solid var(--border);border-radius:var(--radius);padding:18px;min-width:0}
.panel h2{font-family:var(--mono);font-size:11px;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:var(--muted);margin-bottom:16px}

.donut-wrap{display:flex;align-items:center;gap:22px;flex-wrap:wrap}
.donut{position:relative;width:170px;height:170px;flex:none}
.donut svg{width:100%;height:100%;transform:rotate(-90deg)}
.donut circle{fill:none;stroke-width:14}
.donut .ring{stroke:var(--panel-2)}
.donut .seg{transition:stroke-dasharray .5s ease,stroke-dashoffset .5s ease}
.donut-center{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center}
.donut-center b{font-family:var(--mono);font-size:30px;font-weight:700;color:var(--accent);line-height:1}
.donut-center span{font-family:var(--mono);font-size:9px;letter-spacing:.16em;text-transform:uppercase;color:var(--muted);margin-top:4px}
.legend{display:flex;flex-direction:column;gap:10px;flex:1;min-width:140px}
.legend-row{display:flex;align-items:center;gap:10px;font-size:13px}
.legend-dot{width:10px;height:10px;border-radius:50%;flex:none}
.legend-row b{font-family:var(--mono);margin-left:auto;font-size:14px}
.legend-row .lpct{font-family:var(--mono);font-size:11px;color:var(--muted);min-width:40px;text-align:right}

.bars{display:flex;align-items:flex-end;gap:14px;height:220px;padding-top:10px}
.bar-col{flex:1;display:flex;flex-direction:column;align-items:center;gap:8px;height:100%;min-width:0;
  cursor:pointer;border-radius:10px;padding:6px 4px;transition:background .15s ease;border:1px solid transparent}
.bar-col:hover{background:var(--accent-soft)}
.bar-col.selected{border-color:var(--accent);background:var(--accent-soft)}
.bar-col .bval{font-family:var(--mono);font-size:13px;font-weight:700}
.bar-track{flex:1;width:100%;max-width:56px;display:flex;align-items:flex-end}
.bar-rect{width:100%;border-radius:6px 6px 3px 3px;background:linear-gradient(180deg,var(--accent),#c97a12);
  min-height:3px;transition:height .5s ease;position:relative}
.bar-col.selected .bar-rect{box-shadow:0 0 18px rgba(247,160,38,.35)}
.bar-name{font-family:var(--mono);font-size:9px;letter-spacing:.06em;text-transform:uppercase;color:var(--muted);
  text-align:center;line-height:1.4;max-width:100%;overflow:hidden;overflow-wrap:anywhere;
  display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical}
.bar-col .bhint{font-size:10px;color:var(--accent);opacity:0;transition:opacity .15s ease}
.bar-col:hover .bhint,.bar-col.selected .bhint{opacity:1}

/* ============ FILTROS + DETALLE ============ */
.filters{display:flex;gap:10px;flex-wrap:wrap;align-items:center;margin-bottom:14px}
.filters label{font-family:var(--mono);font-size:10px;letter-spacing:.14em;text-transform:uppercase;color:var(--muted)}
.filters select{
  font:inherit;font-size:13px;color:var(--text);background:var(--bg);border:1px solid var(--border);
  border-radius:9px;padding:8px 12px;cursor:pointer;transition:border-color .15s ease
}
.filters select:hover,.filters select:focus{border-color:var(--accent);outline:none}
.filters .clear-f{font-size:11px;color:var(--muted);text-decoration:underline;text-underline-offset:3px}
.filters .clear-f:hover{color:var(--accent)}

.task-row{
  display:flex;align-items:center;gap:14px;flex-wrap:wrap;
  background:var(--bg);border:1px solid var(--border);border-radius:11px;padding:12px 16px;margin-bottom:8px
}
.task-row .tname{flex:1;min-width:180px}
.task-row .tname b{font-size:14px;font-weight:600;display:block}
.task-row .tname span{font-size:12px;color:var(--muted)}
.task-row .trange{display:flex;align-items:center;gap:10px;min-width:220px;flex:none}
.task-row output{font-family:var(--mono);font-size:14px;font-weight:700;color:var(--accent);min-width:46px;text-align:right}
.detail-empty{border:1px dashed var(--border);border-radius:12px;padding:26px;text-align:center;color:var(--muted);font-size:13px}
.detail-head{display:flex;align-items:center;gap:10px;margin-bottom:12px}
.detail-head b{font-size:15px}
.detail-head .close-x{margin-left:auto}

input[type=range]{flex:1;appearance:none;height:4px;background:var(--panel-2);border-radius:2px;cursor:pointer;min-width:110px}
input[type=range]::-webkit-slider-thumb{appearance:none;width:16px;height:16px;border-radius:50%;background:var(--accent);border:3px solid var(--bg);box-shadow:0 0 0 1px var(--accent);cursor:grab}
input[type=range]::-moz-range-thumb{width:12px;height:12px;border-radius:50%;background:var(--accent);border:3px solid var(--bg);cursor:grab}

/* ============ PILLS (compartidas) ============ */
.pill{display:inline-flex;align-items:center;gap:6px;font-family:var(--mono);font-size:9px;font-weight:700;
  letter-spacing:.12em;text-transform:uppercase;padding:4px 10px;border-radius:999px;border:1px solid currentColor;flex:none}
.pill i{width:6px;height:6px;border-radius:50%;background:currentColor;animation:pulse 1.6s ease-in-out infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.35}}
.pill.todo{color:var(--st-todo);background:rgba(249,115,22,.1)}
.pill.doing{color:var(--st-doing);background:rgba(251,191,36,.1)}
.pill.done{color:var(--st-done);background:rgba(52,211,153,.1)}

/* ============ VISTA PROYECTOS (tablero) ============ */
.areas{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(270px,1fr));align-items:start}
.area{background:var(--panel);border:1px solid var(--border);border-radius:var(--radius);display:flex;flex-direction:column;overflow:hidden}
.area-head{padding:14px 16px 12px;border-bottom:1px solid var(--border);background:var(--panel-2)}
.area-head-row{display:flex;align-items:center;gap:8px}
.area-name{font-size:13px;font-weight:700;text-transform:uppercase;flex:1;min-width:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.area-name-input{flex:1;min-width:0;font:inherit;font-size:13px;font-weight:700;text-transform:uppercase;
  background:var(--bg);border:1px solid var(--accent);border-radius:6px;color:var(--text);padding:3px 8px}
.icon-btn{display:inline-flex;align-items:center;justify-content:center;width:28px;height:28px;border-radius:8px;color:var(--muted);flex:none;transition:all .15s ease}
.icon-btn:hover{background:var(--accent-soft);color:var(--accent)}
.icon-btn svg{width:14px;height:14px}
.count-pill{font-family:var(--mono);font-size:10px;font-weight:700;background:var(--bg);border:1px solid var(--border);border-radius:999px;padding:3px 9px;color:var(--muted);flex:none}
.area-progress{display:flex;align-items:center;gap:10px;margin-top:10px}
.bar{flex:1;height:4px;background:var(--bg);border-radius:2px;overflow:hidden}
.bar-fill{height:100%;border-radius:2px;background:var(--accent);transition:width .4s ease}
.area-progress b{font-family:var(--mono);font-size:11px;color:var(--muted);min-width:38px;text-align:right}
.area-body{padding:12px;display:flex;flex-direction:column;gap:10px;min-height:120px}
.card{background:var(--bg);border:1px solid var(--border);border-radius:12px;padding:12px 14px;display:flex;flex-direction:column;gap:8px;transition:all .15s ease}
.card:hover{border-color:#3a4d8f;transform:translateY(-2px)}
.card-top{display:flex;align-items:center;justify-content:space-between;gap:8px}
.card-num{font-family:var(--mono);font-size:10px;color:var(--muted);letter-spacing:.1em}
.card-title{font-size:14px;font-weight:600;line-height:1.35;word-break:break-word}
.card-owner{font-size:12px;color:var(--muted)}
.card-bar{display:flex;align-items:center;gap:10px}
.card-bar b{font-family:var(--mono);font-size:12px;font-weight:700;min-width:40px;text-align:right}
.card .bar-fill.todo{background:var(--st-todo)} .card .bar-fill.doing{background:var(--st-doing)} .card .bar-fill.done{background:var(--st-done)}
.card-foot{display:flex;align-items:center;gap:6px;flex-wrap:wrap;border-top:1px dashed var(--border);padding-top:9px}
.doc-chip{display:inline-flex;align-items:center;gap:5px;font-size:11px;font-weight:500;color:var(--text);
  background:var(--panel-2);border:1px solid var(--border);border-radius:7px;padding:4px 9px;text-decoration:none;max-width:170px;transition:all .15s ease}
.doc-chip:hover{border-color:var(--accent);color:var(--accent)}
.doc-chip span{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.doc-chip svg{width:11px;height:11px;flex:none}
.card-actions{display:flex;gap:4px;margin-left:auto}
.mini-btn{display:inline-flex;align-items:center;gap:5px;font-family:var(--mono);font-size:10px;letter-spacing:.08em;
  text-transform:uppercase;color:var(--muted);padding:5px 9px;border-radius:7px;transition:all .15s ease}
.mini-btn:hover{background:var(--accent-soft);color:var(--accent)}
.mini-btn.del:hover{background:rgba(227,39,46,.12);color:#ff8f93}
.mini-btn svg{width:12px;height:12px}
.add-card{border:1px dashed var(--border);border-radius:12px;background:transparent;padding:14px;
  display:flex;align-items:center;justify-content:center;gap:8px;font-family:var(--mono);font-size:11px;
  letter-spacing:.1em;text-transform:uppercase;color:var(--muted);transition:all .15s ease}
.add-card:hover{border-color:var(--accent);color:var(--accent);background:var(--accent-soft)}
.empty{border:1px dashed var(--border);border-radius:12px;padding:20px 14px;text-align:center;font-size:12px;color:var(--muted)}

/* ============ VISTA ACTAS ============ */
.actas-head{display:flex;align-items:center;gap:12px;margin-bottom:16px;flex-wrap:wrap}
.actas-head .spacer{flex:1}
.acta-row{
  display:flex;align-items:center;gap:14px;flex-wrap:wrap;
  background:var(--panel);border:1px solid var(--border);border-radius:12px;padding:14px 18px;margin-bottom:10px;
  transition:border-color .15s ease
}
.acta-row:hover{border-color:#3a4d8f}
.acta-ico{width:38px;height:38px;border-radius:10px;background:var(--accent-soft);color:var(--accent);
  display:flex;align-items:center;justify-content:center;flex:none}
.acta-ico svg{width:18px;height:18px}
.acta-info{flex:1;min-width:200px}
.acta-info b{font-size:14px;font-weight:600;display:block}
.acta-info span{font-family:var(--mono);font-size:11px;color:var(--muted)}
.acta-actions{display:flex;gap:6px;flex-wrap:wrap}

/* ============ MODALES ============ */
.overlay{position:fixed;inset:0;z-index:100;background:rgba(5,9,24,.7);backdrop-filter:blur(6px);
  display:flex;align-items:center;justify-content:center;padding:20px;opacity:0;pointer-events:none;transition:opacity .2s ease}
.overlay.open{opacity:1;pointer-events:auto}
.modal{background:var(--panel);border:1px solid var(--border);border-radius:16px;width:100%;max-width:480px;
  max-height:88dvh;overflow:auto;transform:scale(.95) translateY(8px);transition:transform .2s ease;box-shadow:0 24px 60px rgba(0,0,0,.5)}
.overlay.open .modal{transform:none}
.modal-head{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:16px 20px;border-bottom:1px solid var(--border)}
.modal-head h2{font-size:15px;font-weight:700}
.modal-head .kicker{font-family:var(--mono);font-size:9px;letter-spacing:.2em;text-transform:uppercase;color:var(--accent);display:block;margin-bottom:2px}
.modal-body{padding:18px 20px;display:flex;flex-direction:column;gap:14px}
.field{display:flex;flex-direction:column;gap:6px}
.field label{font-family:var(--mono);font-size:10px;letter-spacing:.14em;text-transform:uppercase;color:var(--muted)}
.field input[type=text],.field input[type=url],.field input[type=date],.field select,.field textarea{
  font:inherit;font-size:14px;color:var(--text);background:var(--bg);border:1px solid var(--border);
  border-radius:9px;padding:10px 12px;width:100%;transition:border-color .15s ease;color-scheme:dark}
.field textarea{resize:vertical;min-height:90px;font-size:13px;line-height:1.6}
.field input:focus,.field select:focus,.field textarea:focus{border-color:var(--accent);outline:none}
.field input[type=file]{font-size:12px;color:var(--muted);background:var(--bg);border:1px dashed var(--border);border-radius:9px;padding:9px 12px;width:100%;cursor:pointer}
.field input[type=file]::file-selector-button{font-family:var(--mono);font-size:10px;letter-spacing:.08em;text-transform:uppercase;
  background:var(--accent-soft);color:var(--accent);border:1px solid var(--accent);border-radius:7px;padding:6px 12px;margin-right:10px;cursor:pointer}
.field .hint{font-size:11px;color:var(--muted)}
.range-row{display:flex;align-items:center;gap:14px}
.range-row output{font-family:var(--mono);font-size:18px;font-weight:700;color:var(--accent);min-width:56px;text-align:right}
.status-opts{display:grid;grid-template-columns:repeat(3,1fr);gap:8px}
.status-opt{border:1px solid var(--border);border-radius:10px;padding:10px 6px;text-align:center;font-family:var(--mono);
  font-size:10px;font-weight:700;letter-spacing:.06em;text-transform:uppercase;color:var(--muted);
  display:flex;flex-direction:column;align-items:center;gap:6px;transition:all .15s ease}
.status-opt i{width:8px;height:8px;border-radius:50%;background:currentColor}
.status-opt[data-status="por-iniciar"].active{color:var(--st-todo);border-color:var(--st-todo);background:rgba(249,115,22,.1)}
.status-opt[data-status="en-proceso"].active{color:var(--st-doing);border-color:var(--st-doing);background:rgba(251,191,36,.1)}
.status-opt[data-status="completo"].active{color:var(--st-done);border-color:var(--st-done);background:rgba(52,211,153,.1)}
.modal-foot{display:flex;justify-content:flex-end;gap:8px;padding:14px 20px;border-top:1px solid var(--border)}
.doc-list{display:flex;flex-direction:column;gap:8px;max-height:240px;overflow:auto}
.doc-row{display:flex;align-items:center;gap:10px;background:var(--bg);border:1px solid var(--border);border-radius:9px;padding:9px 12px}
.doc-row svg{width:14px;height:14px;color:var(--accent);flex:none}
.doc-row a{flex:1;font-size:13px;font-weight:500;color:var(--text);text-decoration:none;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.doc-row a:hover{color:var(--accent);text-decoration:underline}
.doc-file-btn{flex:1;font-size:13px;font-weight:500;color:var(--text);text-align:left;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;transition:color .15s ease}
.doc-file-btn:hover{color:var(--accent);text-decoration:underline}
.doc-row .icon-btn{width:24px;height:24px}
.doc-row .icon-btn:hover{color:#ff8f93;background:rgba(227,39,46,.12)}

.toast-wrap{position:fixed;bottom:20px;right:20px;z-index:200;display:flex;flex-direction:column;gap:8px}
.toast{background:var(--panel-2);border:1px solid var(--accent);border-radius:10px;font-family:var(--mono);
  font-size:12px;padding:11px 16px;color:var(--text);animation:toastIn .25s ease-out;box-shadow:0 8px 24px rgba(0,0,0,.4)}
@keyframes toastIn{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}
.toast.out{opacity:0;transform:translateY(6px);transition:all .3s ease}

footer{padding:18px 24px;border-top:1px solid var(--border);font-family:var(--mono);font-size:10px;
  letter-spacing:.14em;text-transform:uppercase;color:var(--muted);display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap}

@media (max-width:760px){
  .topbar{padding:12px 14px;gap:10px}
  main{padding:14px 14px 40px}
  .nav{margin-left:0;width:100%}
  .nav-btn{flex:1;text-align:center;padding:9px 8px}
  .actions{margin-left:0}
  .task-row .trange{width:100%}
}
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important}
}
</style>
</head>
<body>

<header class="topbar">
  <div class="brand">
    <div class="brand-mark" aria-hidden="true"><i></i><i></i><i></i></div>
    <div class="brand-text"><b>banco del austro</b><span>Talento Humano</span></div>
  </div>

  <nav class="nav">
    <button class="nav-btn active" type="button" data-view="dashboard">Dashboard</button>
    <button class="nav-btn" type="button" data-view="proyectos">Proyectos</button>
    <button class="nav-btn" type="button" data-view="actas">Actas</button>
  </nav>

  <div class="actions">
    <button class="btn" id="btnSummary" type="button">Resumen</button>
    <button class="btn" id="btnExport" type="button">Exportar</button>
    <button class="btn" id="btnImport" type="button">Importar</button>
    <input type="file" id="importFile" accept=".json,application/json" hidden>
  </div>
</header>

<main>

  <!-- ================= VISTA: DASHBOARD ================= -->
  <section class="view active" id="view-dashboard">
    <div class="view-title">
      <h1>Avance general de proyectos</h1>
      <span>Visión ejecutiva · clic en una barra para ver sus tareas</span>
    </div>

    <div class="stats" id="stats"></div>

    <div class="charts">
      <div class="panel">
        <h2>Estado de proyectos</h2>
        <div class="donut-wrap">
          <div class="donut" id="donut"></div>
          <div class="legend" id="legend"></div>
        </div>
      </div>
      <div class="panel">
        <h2>Proyectos por área</h2>
        <div class="bars" id="bars"></div>
      </div>
    </div>

    <div class="panel">
      <h2>Detalle de tareas</h2>
      <div class="filters">
        <label for="fArea">Área</label>
        <select id="fArea"></select>
        <label for="fEstado">Estado</label>
        <select id="fEstado">
          <option value="todos">Todos</option>
          <option value="por-iniciar">Por iniciar</option>
          <option value="en-proceso">En proceso</option>
          <option value="completo">Completo</option>
        </select>
        <button class="clear-f" id="fClear" type="button">limpiar filtros</button>
        <button class="btn primary" id="btnNuevaTarea" type="button" style="margin-left:auto">+ Nueva tarea</button>
      </div>
      <div id="taskDetail"></div>
    </div>
  </section>

  <!-- ================= VISTA: PROYECTOS ================= -->
  <section class="view" id="view-proyectos">
    <div class="view-title">
      <h1>Tablero por área</h1>
      <span>Gestiona proyectos, avances y documentos</span>
    </div>
    <div class="areas" id="areas"></div>
  </section>

  <!-- ================= VISTA: ACTAS ================= -->
  <section class="view" id="view-actas">
    <div class="view-title">
      <h1>Actas de reunión</h1>
      <span>Registro y descarga de actas</span>
    </div>
    <div class="actas-head">
      <div class="filters" style="margin:0">
        <label for="fActaArea">Área</label>
        <select id="fActaArea"></select>
      </div>
      <div class="spacer"></div>
      <button class="btn primary" id="btnNuevaActa" type="button">+ Nueva acta</button>
    </div>
    <div id="actasList"></div>
  </section>

</main>

<footer>
  <span>Uso interno · Talento Humano</span>
  <span>Datos guardados en este navegador · Usa "Exportar" para respaldar</span>
</footer>

<!-- Modal: proyecto -->
<div class="overlay" id="projectOverlay" role="dialog" aria-modal="true">
  <div class="modal">
    <div class="modal-head">
      <div><span class="kicker" id="projectKicker">Nuevo proyecto</span><h2 id="projectModalTitle">Añadir proyecto</h2></div>
      <button class="icon-btn" type="button" data-close aria-label="Cerrar">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6 6 18M6 6l12 12"/></svg>
      </button>
    </div>
    <div class="modal-body">
      <div class="field"><label for="pArea">Área a la que pertenece</label>
        <select id="pArea"></select></div>
      <div class="field"><label for="pName">Nombre del proyecto / actividad</label>
        <input type="text" id="pName" placeholder="Ej.: Actualización del manual de inducción" maxlength="120"></div>
      <div class="field"><label for="pOwner">Responsable</label>
        <input type="text" id="pOwner" placeholder="Ej.: María Fernanda R." maxlength="60"></div>
      <div class="field"><label>Estado</label>
        <div class="status-opts" id="statusOpts">
          <button type="button" class="status-opt" data-status="por-iniciar"><i></i>Por iniciar</button>
          <button type="button" class="status-opt" data-status="en-proceso"><i></i>En proceso</button>
          <button type="button" class="status-opt" data-status="completo"><i></i>Completo</button>
        </div></div>
      <div class="field"><label for="pPct">Avance</label>
        <div class="range-row"><input type="range" id="pPct" min="0" max="100" step="5" value="0"><output id="pPctOut">0%</output></div>
        <span class="hint">El estado se ajusta solo: 0% por iniciar · 1–99% en proceso · 100% completo</span></div>
    </div>
    <div class="modal-foot">
      <button class="btn" type="button" data-close>Cancelar</button>
      <button class="btn primary" type="button" id="pSave">Guardar proyecto</button>
    </div>
  </div>
</div>

<!-- Modal: documentos -->
<div class="overlay" id="docsOverlay" role="dialog" aria-modal="true">
  <div class="modal">
    <div class="modal-head">
      <div><span class="kicker">Documentos de seguimiento</span><h2 id="docsModalTitle">Documentos</h2></div>
      <button class="icon-btn" type="button" data-close aria-label="Cerrar">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6 6 18M6 6l12 12"/></svg>
      </button>
    </div>
    <div class="modal-body">
      <div class="doc-list" id="docList"></div>
      <div class="field">
        <label for="dFile">Subir archivo desde tu PC</label>
        <input type="file" id="dFile" accept=".pdf,.doc,.docx,.xls,.xlsx,.ppt,.pptx,.png,.jpg,.jpeg,.txt,.csv">
        <span class="hint">PDF, Word, Excel, imágenes... Se guarda en este navegador (máx. recomendado 20 MB).</span>
      </div>
      <div style="display:flex;align-items:center;gap:10px;font-family:var(--mono);font-size:10px;letter-spacing:.14em;text-transform:uppercase;color:var(--muted)">
        <span style="flex:1;height:1px;background:var(--border)"></span>o pega un enlace<span style="flex:1;height:1px;background:var(--border)"></span>
      </div>
      <div class="field">
        <label for="dName">Nombre del documento</label>
        <input type="text" id="dName" placeholder="Ej.: Acta de reunión 12-nov" maxlength="100">
      </div>
      <div class="field">
        <label for="dUrl">Enlace (SharePoint / OneDrive / carpeta)</label>
        <input type="url" id="dUrl" placeholder="https://bancodelaustro-my.sharepoint.com/...">
        <span class="hint">El enlace es ideal para documentos que todo el equipo debe ver actualizados.</span>
      </div>
    </div>
    <div class="modal-foot">
      <button class="btn" type="button" data-close>Cerrar</button>
      <button class="btn" type="button" id="dUpload">Subir archivo</button>
      <button class="btn primary" type="button" id="dAdd">Añadir enlace</button>
    </div>
  </div>
</div>

<!-- Modal: acta -->
<div class="overlay" id="actaOverlay" role="dialog" aria-modal="true">
  <div class="modal">
    <div class="modal-head">
      <div><span class="kicker">Acta de reunión</span><h2>Nueva acta</h2></div>
      <button class="icon-btn" type="button" data-close aria-label="Cerrar">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6 6 18M6 6l12 12"/></svg>
      </button>
    </div>
    <div class="modal-body">
      <div class="field"><label for="aTitulo">Título de la reunión</label>
        <input type="text" id="aTitulo" placeholder="Ej.: Comité de Talento Humano — semanal" maxlength="120"></div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px">
        <div class="field"><label for="aFecha">Fecha</label><input type="date" id="aFecha"></div>
        <div class="field"><label for="aArea">Área</label><select id="aArea"></select></div>
      </div>
      <div class="field"><label for="aAsistentes">Asistentes</label>
        <input type="text" id="aAsistentes" placeholder="Ej.: M. Rojas, J. Andrade, C. Medina" maxlength="200"></div>
      <div class="field"><label for="aAcuerdos">Acuerdos y compromisos</label>
        <textarea id="aAcuerdos" placeholder="1. Revisar avance del manual de inducción...&#10;2. Enviar encuesta de clima antes del viernes..."></textarea></div>
      <div class="field"><label for="aUrl">Enlace del archivo firmado (opcional)</label>
        <input type="url" id="aUrl" placeholder="https://bancodelaustro-my.sharepoint.com/...">
        <span class="hint">Si el acta firmada está en SharePoint, pega el enlace y quedará a un clic.</span></div>
    </div>
    <div class="modal-foot">
      <button class="btn" type="button" data-close>Cancelar</button>
      <button class="btn primary" type="button" id="aSave">Guardar acta</button>
    </div>
  </div>
</div>

<!-- Modal: confirmar -->
<div class="overlay" id="confirmOverlay" role="dialog" aria-modal="true">
  <div class="modal" style="max-width:380px">
    <div class="modal-head"><div><span class="kicker">Confirmar</span><h2>¿Eliminar?</h2></div></div>
    <div class="modal-body"><p style="font-size:13px;color:var(--muted)" id="confirmText">Esta acción no se puede deshacer.</p></div>
    <div class="modal-foot">
      <button class="btn" type="button" data-close>Cancelar</button>
      <button class="btn danger" type="button" id="confirmYes">Sí, eliminar</button>
    </div>
  </div>
</div>

<div class="toast-wrap" id="toasts"></div>

<script>
(function(){
"use strict";

/* ================= ESTADO ================= */
const KEY="ba_th_repo_v2";
const STATUS={
  "por-iniciar":{label:"Por iniciar",cls:"todo",color:"#F97316"},
  "en-proceso":{label:"En proceso",cls:"doing",color:"#FBBF24"},
  "completo":{label:"Completo",cls:"done",color:"#34D399"}
};
const uid=()=>Date.now().toString(36)+Math.random().toString(36).slice(2,7);

function seed(){return{areas:[
{id:uid(),name:"Reclutamiento y Selección",projects:[
{id:uid(),name:"Manual de inducción 2026",owner:"M. Fernanda R.",status:"en-proceso",pct:60,docs:[{id:uid(),name:"Borrador v2",url:"https://bancodelaustro.sharepoint.com"}]},
{id:uid(),name:"Perfil de puestos críticos",owner:"J. Andrade",status:"por-iniciar",pct:0,docs:[]}]},
{id:uid(),name:"Capacitación y Desarrollo",projects:[
{id:uid(),name:"Plan anual de capacitación",owner:"C. Medina",status:"en-proceso",pct:35,docs:[]}]},
{id:uid(),name:"Compensación y Beneficios",projects:[
{id:uid(),name:"Estudio salarial anual",owner:"P. Salazar",status:"completo",pct:100,docs:[{id:uid(),name:"Informe final",url:"https://bancodelaustro.sharepoint.com"}]}]},
{id:uid(),name:"Bienestar y Clima Laboral",projects:[
{id:uid(),name:"Encuesta de clima Q1",owner:"L. Torres",status:"por-iniciar",pct:0,docs:[]}]},
{id:uid(),name:"Evaluación y Desempeño",projects:[
{id:uid(),name:"Ciclo de evaluación 360°",owner:"A. Villacís",status:"en-proceso",pct:80,docs:[]}]}
],actas:[
{id:uid(),titulo:"Comité de Talento Humano — semanal",fecha:new Date().toISOString().slice(0,10),
area:"Reclutamiento y Selección",asistentes:"M. Fernanda R., J. Andrade",
acuerdos:"1. Revisar avance del manual de inducción 2026.\n2. Definir perfiles de puestos críticos antes de fin de mes.",
url:""}
]};}

let state;
try{
  const raw=localStorage.getItem(KEY)||localStorage.getItem("ba_th_repo_v1");
  state=raw?JSON.parse(raw):seed();
  if(!state||!Array.isArray(state.areas))state=seed();
  if(!Array.isArray(state.actas))state.actas=[];
}catch(e){state=seed();}

const save=()=>localStorage.setItem(KEY,JSON.stringify(state));
const esc=s=>String(s).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));
const statusFromPct=v=>v<=0?"por-iniciar":v>=100?"completo":"en-proceso";
const fmtSize=b=>b<1024?b+" B":b<1048576?(b/1024).toFixed(1)+" KB":(b/1048576).toFixed(1)+" MB";

/* ================= ARCHIVOS (IndexedDB) ================= */
const DB={
  open(){return new Promise((res,rej)=>{
    const r=indexedDB.open("ba_th_files",1);
    r.onupgradeneeded=()=>r.result.createObjectStore("files");
    r.onsuccess=()=>res(r.result);r.onerror=()=>rej(r.error);});},
  async put(id,blob){const db=await this.open();return new Promise((res,rej)=>{
    const tx=db.transaction("files","readwrite");tx.objectStore("files").put(blob,id);
    tx.oncomplete=res;tx.onerror=()=>rej(tx.error);});},
  async get(id){const db=await this.open();return new Promise((res,rej)=>{
    const rq=db.transaction("files").objectStore("files").get(id);
    rq.onsuccess=()=>res(rq.result);rq.onerror=()=>rej(rq.error);});},
  async del(id){const db=await this.open();return new Promise((res,rej)=>{
    const tx=db.transaction("files","readwrite");tx.objectStore("files").delete(id);
    tx.oncomplete=res;tx.onerror=()=>rej(tx.error);});}
};
async function downloadFileDoc(d){
  try{
    const blob=await DB.get(d.id);
    if(!blob){toast("Archivo no encontrado en este navegador");return;}
    const a=document.createElement("a");
    a.href=URL.createObjectURL(blob);a.download=d.name;a.click();
    setTimeout(()=>URL.revokeObjectURL(a.href),4000);
    toast("Descargando "+d.name);
  }catch(e){toast("No se pudo leer el archivo");}
}

function toast(msg){const w=document.getElementById("toasts");const el=document.createElement("div");
el.className="toast";el.textContent=msg;w.appendChild(el);
setTimeout(()=>{el.classList.add("out");setTimeout(()=>el.remove(),320);},2400);}

const IC={
doc:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 3H6a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V9z"/><path d="M14 3v6h6"/></svg>',
edit:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 3a2.8 2.8 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5z"/></svg>',
trash:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 6h18M8 6V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2m3 0v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6"/></svg>',
link:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M10 13a5 5 0 0 0 7.5.5l3-3a5 5 0 0 0-7-7l-1.7 1.7"/><path d="M14 11a5 5 0 0 0-7.5-.5l-3 3a5 5 0 0 0 7 7l1.7-1.7"/></svg>',
down:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3v12m0 0 4-4m-4 4-4-4"/><path d="M4 17v2a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2v-2"/></svg>',
x:'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6 6 18M6 6l12 12"/></svg>'};

function allProjects(){return state.areas.flatMap(a=>a.projects.map(p=>({...p,areaId:a.id,areaName:a.name})));}
function areaAvg(a){if(!a.projects.length)return 0;return Math.round(a.projects.reduce((s,p)=>s+p.pct,0)/a.projects.length);}

/* ================= ROUTER ================= */
const navBtns=document.querySelectorAll(".nav-btn");
function showView(v){
  document.querySelectorAll(".view").forEach(s=>s.classList.toggle("active",s.id==="view-"+v));
  navBtns.forEach(b=>b.classList.toggle("active",b.dataset.view===v));
  if(location.hash!=="#"+v) history.replaceState(null,"","#"+v);
}
navBtns.forEach(b=>b.addEventListener("click",()=>showView(b.dataset.view)));
const initial=(location.hash||"#dashboard").slice(1);
showView(["dashboard","proyectos","actas"].includes(initial)?initial:"dashboard");

/* ================= DASHBOARD ================= */
const statsEl=document.getElementById("stats");
const statHTML=(n,l,c)=>`<div class="stat ${c}"><b>${n}</b><span>${l}</span></div>`;
let selectedArea="todas", selectedEstado="todos";

function counts(){
  let todo=0,doing=0,done=0,sum=0,total=0;
  allProjects().forEach(p=>{total++;sum+=p.pct;
    if(p.status==="por-iniciar")todo++;else if(p.status==="en-proceso")doing++;else done++;});
  return{total,todo,doing,done,avg:total?Math.round(sum/total):0};
}

function renderStats(){
  const c=counts();
  statsEl.innerHTML=statHTML(c.total,"Proyectos","")+statHTML(c.todo,"Por iniciar","s-todo")+
    statHTML(c.doing,"En proceso","s-doing")+statHTML(c.done,"Completos","s-done")+statHTML(c.avg+"%","Avance global","s-avg");
}

function renderDonut(){
  const c=counts();
  const R=15.9155, parts=[
    {k:"por-iniciar",n:c.todo},{k:"en-proceso",n:c.doing},{k:"completo",n:c.done}
  ];
  let offset=25;
  const segs=parts.map(p=>{
    const frac=c.total?p.n/c.total*100:0;
    const s=`<circle class="seg" cx="21" cy="21" r="${R}" stroke="${STATUS[p.k].color}"
      stroke-dasharray="${frac} ${100-frac}" stroke-dashoffset="${offset}"></circle>`;
    offset-=frac; return s;
  }).join("");
  document.getElementById("donut").innerHTML=
    `<svg viewBox="0 0 42 42"><circle class="ring" cx="21" cy="21" r="${R}"></circle>${c.total?segs:""}</svg>
     <div class="donut-center"><b>${c.avg}%</b><span>avance</span></div>`;
  document.getElementById("legend").innerHTML=parts.map(p=>{
    const pct=c.total?Math.round(p.n/c.total*100):0;
    return`<div class="legend-row"><span class="legend-dot" style="background:${STATUS[p.k].color}"></span>
      ${STATUS[p.k].label}<span class="lpct">${pct}%</span><b>${p.n}</b></div>`;
  }).join("");
}

function renderBars(){
  const max=Math.max(1,...state.areas.map(a=>a.projects.length));
  document.getElementById("bars").innerHTML=state.areas.map(a=>{
    const n=a.projects.length, h=Math.round(n/max*100);
    const sel=a.id===selectedArea?" selected":"";
    return`<div class="bar-col${sel}" data-area-bar="${a.id}" role="button" tabindex="0" title="Ver tareas de ${esc(a.name)}">
      <span class="bval">${n}</span>
      <div class="bar-track"><div class="bar-rect" style="height:${h}%"></div></div>
      <span class="bar-name">${esc(a.name)}</span>
      <span class="bhint">${a.id===selectedArea?"▲ viendo tareas":"ver tareas"}</span>
    </div>`;
  }).join("");
}

function renderAreaFilter(){
  const sel=document.getElementById("fArea");
  sel.innerHTML=`<option value="todas">Todas las áreas</option>`+
    state.areas.map(a=>`<option value="${a.id}">${esc(a.name)}</option>`).join("");
  sel.value=[...sel.options].some(o=>o.value===selectedArea)?selectedArea:"todas";
  selectedArea=sel.value;
}

function renderTaskDetail(){
  const wrap=document.getElementById("taskDetail");
  let list=allProjects();
  if(selectedArea!=="todas")list=list.filter(p=>p.areaId===selectedArea);
  if(selectedEstado!=="todos")list=list.filter(p=>p.status===selectedEstado);
  if(!list.length){
    wrap.innerHTML=`<div class="detail-empty">No hay tareas con esos filtros.<br>
      ${selectedArea==="todas"?"Tip: haz clic en una barra del gráfico para ver el detalle de un área.":"Prueba limpiando los filtros."}</div>`;
    return;
  }
  wrap.innerHTML=list.map(p=>{
    const st=STATUS[p.status];
    return`<div class="task-row" data-area="${p.areaId}" data-id="${p.id}">
      <div class="tname"><b>${esc(p.name)}</b><span>${esc(p.areaName)}${p.owner?" · "+esc(p.owner):""}</span></div>
      <span class="pill ${st.cls}"><i></i>${st.label}</span>
      <div class="trange">
        <input type="range" min="0" max="100" step="5" value="${p.pct}" data-range aria-label="Avance de ${esc(p.name)}">
        <output>${p.pct}%</output>
      </div>
    </div>`;
  }).join("");
}

/* Actualización en vivo del % desde el detalle */
document.getElementById("taskDetail").addEventListener("input",e=>{
  const r=e.target.closest("[data-range]");if(!r)return;
  r.nextElementSibling.textContent=r.value+"%";
});
document.getElementById("taskDetail").addEventListener("change",e=>{
  const r=e.target.closest("[data-range]");if(!r)return;
  const row=r.closest(".task-row");
  const a=state.areas.find(x=>x.id===row.dataset.area);
  const p=a.projects.find(x=>x.id===row.dataset.id);
  p.pct=+r.value; p.status=statusFromPct(p.pct);
  save(); renderDashboard(); renderBoard();
  toast(`Avance actualizado: ${p.pct}%`);
});

/* Filtros */
document.getElementById("fArea").addEventListener("change",e=>{selectedArea=e.target.value;renderBars();renderTaskDetail();});
document.getElementById("fEstado").addEventListener("change",e=>{selectedEstado=e.target.value;renderTaskDetail();});
document.getElementById("fClear").addEventListener("click",()=>{
  selectedArea="todas";selectedEstado="todos";
  document.getElementById("fEstado").value="todos";
  renderAreaFilter();renderBars();renderTaskDetail();
});

/* Clic en barras */
document.getElementById("bars").addEventListener("click",e=>{
  const col=e.target.closest("[data-area-bar]");if(!col)return;
  selectedArea=col.dataset.areaBar===selectedArea?"todas":col.dataset.areaBar;
  renderAreaFilter();renderBars();renderTaskDetail();
  document.getElementById("taskDetail").scrollIntoView({behavior:"smooth",block:"nearest"});
});
document.getElementById("bars").addEventListener("keydown",e=>{
  if(e.key==="Enter"||e.key===" "){const col=e.target.closest("[data-area-bar]");if(col){e.preventDefault();col.click();}}
});

function renderDashboard(){renderStats();renderDonut();renderBars();renderAreaFilter();renderTaskDetail();}

/* ================= TABLERO DE PROYECTOS ================= */
const areasEl=document.getElementById("areas");

function renderBoard(){
  areasEl.innerHTML=state.areas.map(a=>{
    const avg=areaAvg(a);
    const cards=a.projects.length?a.projects.map((p,i)=>cardHTML(a,p,i)).join("")
      :`<div class="empty">Sin proyectos aún.<br>Añade el primero con el botón de abajo.</div>`;
    return`<section class="area" data-area="${a.id}">
      <div class="area-head"><div class="area-head-row">
        <span class="area-name" title="${esc(a.name)}">${esc(a.name)}</span>
        <button class="icon-btn" type="button" data-act="rename-area" title="Renombrar área" aria-label="Renombrar área">${IC.edit}</button>
        <span class="count-pill">${a.projects.length}</span></div>
        <div class="area-progress"><div class="bar"><div class="bar-fill" style="width:${avg}%"></div></div><b>${avg}%</b></div></div>
      <div class="area-body">${cards}
        <button class="add-card" type="button" data-act="add-project">+ Añadir proyecto</button></div>
    </section>`;
  }).join("");
}

function cardHTML(a,p,i){
  const st=STATUS[p.status]||STATUS["por-iniciar"];
  const docs=p.docs.map(d=>d.type==="file"
    ?`<button class="doc-chip" type="button" data-chip-file="${d.id}" title="Descargar ${esc(d.name)}">${IC.down}<span>${esc(d.name)}</span></button>`
    :`<a class="doc-chip" href="${esc(d.url)}" target="_blank" rel="noopener" title="${esc(d.url)}">${IC.doc}<span>${esc(d.name)}</span></a>`).join("");
  return`<article class="card" data-id="${p.id}">
    <div class="card-top"><span class="card-num">#${String(i+1).padStart(2,"0")}</span>
      <span class="pill ${st.cls}"><i></i>${st.label}</span></div>
    <h3 class="card-title">${esc(p.name)}</h3>
    <div class="card-owner">${p.owner?"Resp.: "+esc(p.owner):"Sin responsable asignado"}</div>
    <div class="card-bar"><div class="bar"><div class="bar-fill ${st.cls}" style="width:${p.pct}%"></div></div><b>${p.pct}%</b></div>
    <div class="card-foot">${docs}
      <div class="card-actions">
        <button class="mini-btn" type="button" data-act="docs">${IC.link} Docs ${p.docs.length?`(${p.docs.length})`:""}</button>
        <button class="mini-btn" type="button" data-act="edit">${IC.edit} Editar</button>
        <button class="mini-btn del" type="button" data-act="del" aria-label="Eliminar proyecto">${IC.trash}</button>
      </div></div>
  </article>`;
}

/* ================= ACTAS ================= */
const actasList=document.getElementById("actasList");
let actaAreaFilter="todas";

function renderActaFilter(){
  const sel=document.getElementById("fActaArea");
  sel.innerHTML=`<option value="todas">Todas las áreas</option>`+
    state.areas.map(a=>`<option value="${a.id}"${a.id===actaAreaFilter?" selected":""}>${esc(a.name)}</option>`).join("");
}
document.getElementById("fActaArea").addEventListener("change",e=>{actaAreaFilter=e.target.value;renderActas();});

function renderActas(){
  renderActaFilter();
  let list=[...state.actas].sort((a,b)=>b.fecha.localeCompare(a.fecha));
  if(actaAreaFilter!=="todas"){
    const name=state.areas.find(a=>a.id===actaAreaFilter)?.name;
    list=list.filter(x=>x.area===name);
  }
  actasList.innerHTML=list.length?list.map(x=>`
    <div class="acta-row" data-id="${x.id}">
      <div class="acta-ico">${IC.doc}</div>
      <div class="acta-info">
        <b>${esc(x.titulo)}</b>
        <span>${esc(x.fecha)} · ${esc(x.area||"General")}${x.asistentes?" · "+esc(x.asistentes):""}</span>
      </div>
      <div class="acta-actions">
        <button class="mini-btn" type="button" data-acta="download">${IC.down} Descargar</button>
        ${x.url?`<a class="mini-btn" href="${esc(x.url)}" target="_blank" rel="noopener">${IC.link} Abrir enlace</a>`:""}
        <button class="mini-btn del" type="button" data-acta="del" aria-label="Eliminar acta">${IC.trash}</button>
      </div>
    </div>`).join("")
  :`<div class="empty">Sin actas registradas.<br>Crea la primera con "+ Nueva acta" y descárgala cuando la necesites.</div>`;
}

actasList.addEventListener("click",e=>{
  const btn=e.target.closest("[data-acta]");if(!btn)return;
  const row=btn.closest(".acta-row");
  const acta=state.actas.find(x=>x.id===row.dataset.id);
  if(btn.dataset.acta==="download")downloadActa(acta);
  if(btn.dataset.acta==="del"){
    askConfirm(`Se eliminará el acta "${acta.titulo}".`,()=>{
      state.actas=state.actas.filter(x=>x.id!==acta.id);
      save();renderActas();toast("Acta eliminada");});
  }
});

function downloadActa(x){
  const txt=
`ACTA DE REUNIÓN — TALENTO HUMANO
BANCO DEL AUSTRO
================================================

Título:      ${x.titulo}
Fecha:       ${x.fecha}
Área:        ${x.area||"General"}
Asistentes:  ${x.asistentes||"—"}

ACUERDOS Y COMPROMISOS
------------------------------------------------
${x.acuerdos||"Sin acuerdos registrados."}

${x.url?`Archivo firmado: ${x.url}`:""}
================================================
Generado desde el Repositorio de Proyectos TH`;
  const blob=new Blob([txt],{type:"text/plain;charset=utf-8"});
  const a=document.createElement("a");
  a.href=URL.createObjectURL(blob);
  a.download="Acta_"+x.titulo.replace(/[^\wáéíóúñ ]/gi,"").trim().replace(/\s+/g,"_")+".txt";
  a.click();URL.revokeObjectURL(a.href);
  toast("Acta descargada (.txt)");
}

/* Modal nueva acta */
document.getElementById("btnNuevaActa").addEventListener("click",()=>{
  document.getElementById("aTitulo").value="";
  document.getElementById("aFecha").value=new Date().toISOString().slice(0,10);
  document.getElementById("aAsistentes").value="";
  document.getElementById("aAcuerdos").value="";
  document.getElementById("aUrl").value="";
  const sel=document.getElementById("aArea");
  sel.innerHTML=`<option value="">General</option>`+state.areas.map(a=>`<option>${esc(a.name)}</option>`).join("");
  openOverlay("actaOverlay");
});
document.getElementById("aSave").addEventListener("click",()=>{
  const titulo=document.getElementById("aTitulo").value.trim();
  if(!titulo){toast("Ponle un título al acta");document.getElementById("aTitulo").focus();return;}
  state.actas.push({
    id:uid(), titulo,
    fecha:document.getElementById("aFecha").value||new Date().toISOString().slice(0,10),
    area:document.getElementById("aArea").value,
    asistentes:document.getElementById("aAsistentes").value.trim(),
    acuerdos:document.getElementById("aAcuerdos").value.trim(),
    url:document.getElementById("aUrl").value.trim()
  });
  save();renderActas();
  closeOverlay(document.getElementById("actaOverlay"));
  toast("Acta guardada");
});

/* ================= MODALES GENÉRICOS ================= */
function openOverlay(id){const ov=document.getElementById(id);ov.classList.add("open");
const first=ov.querySelector("input,button.primary");if(first)setTimeout(()=>first.focus(),60);}
function closeOverlay(ov){ov.classList.remove("open");}
document.querySelectorAll(".overlay").forEach(ov=>{
  ov.addEventListener("click",e=>{if(e.target===ov)closeOverlay(ov);});
  ov.querySelectorAll("[data-close]").forEach(b=>b.addEventListener("click",()=>closeOverlay(ov)));});
document.addEventListener("keydown",e=>{if(e.key==="Escape"){const o=document.querySelector(".overlay.open");if(o)closeOverlay(o);}});

/* ================= PROYECTO: añadir / editar ================= */
let editing=null;
const statusOpts=document.getElementById("statusOpts"),pPct=document.getElementById("pPct"),pPctOut=document.getElementById("pPctOut");
let curStatus="por-iniciar";
function setStatusUI(s){curStatus=s;statusOpts.querySelectorAll(".status-opt").forEach(b=>b.classList.toggle("active",b.dataset.status===s));}
statusOpts.addEventListener("click",e=>{const b=e.target.closest(".status-opt");if(!b)return;
setStatusUI(b.dataset.status);
const preset={"por-iniciar":0,"en-proceso":50,"completo":100}[b.dataset.status];
pPct.value=preset;pPctOut.textContent=preset+"%";});
pPct.addEventListener("input",()=>{pPctOut.textContent=pPct.value+"%";setStatusUI(statusFromPct(+pPct.value));});

function openProjectModal(areaId,projectId){
  editing={areaId,projectId:projectId||null};
  const isEdit=!!projectId;
  document.getElementById("projectKicker").textContent=isEdit?"Editar proyecto":"Nuevo proyecto";
  document.getElementById("projectModalTitle").textContent=isEdit?"Editar proyecto":"Añadir proyecto";
  let p={name:"",owner:"",status:"por-iniciar",pct:0};
  if(isEdit){const a=state.areas.find(x=>x.id===areaId);p=a.projects.find(x=>x.id===projectId);}
  const selArea=document.getElementById("pArea");
  selArea.innerHTML=state.areas.map(a=>`<option value="${a.id}">${esc(a.name)}</option>`).join("");
  selArea.value=areaId;
  document.getElementById("pName").value=p.name;
  document.getElementById("pOwner").value=p.owner||"";
  pPct.value=p.pct;pPctOut.textContent=p.pct+"%";setStatusUI(p.status);
  openOverlay("projectOverlay");
}
document.getElementById("pSave").addEventListener("click",()=>{
  const name=document.getElementById("pName").value.trim();
  if(!name){toast("Escribe el nombre del proyecto");document.getElementById("pName").focus();return;}
  const owner=document.getElementById("pOwner").value.trim(),pct=+pPct.value;
  const destId=document.getElementById("pArea").value;
  const dest=state.areas.find(x=>x.id===destId)||state.areas[0];
  if(editing.projectId){
    const orig=state.areas.find(x=>x.id===editing.areaId);
    const p=orig.projects.find(x=>x.id===editing.projectId);
    Object.assign(p,{name,owner,pct,status:curStatus});
    if(dest.id!==orig.id){ /* mover de área */
      orig.projects=orig.projects.filter(x=>x.id!==p.id);
      dest.projects.push(p);
      toast("Proyecto movido a "+dest.name);
    }else toast("Proyecto actualizado");
  }else{
    dest.projects.push({id:uid(),name,owner,pct,status:curStatus,docs:[]});
    toast("Proyecto añadido a "+dest.name);
  }
  save();renderBoard();renderDashboard();
  closeOverlay(document.getElementById("projectOverlay"));
});
document.getElementById("btnNuevaTarea").addEventListener("click",()=>{
  const areaId=selectedArea!=="todas"?selectedArea:state.areas[0].id;
  openProjectModal(areaId,null);
});

/* ================= DOCUMENTOS ================= */
let docsCtx=null;
function openDocsModal(areaId,projectId){docsCtx={areaId,projectId};renderDocList();
document.getElementById("dName").value="";document.getElementById("dUrl").value="";openOverlay("docsOverlay");}
function renderDocList(){
  const a=state.areas.find(x=>x.id===docsCtx.areaId);
  const p=a.projects.find(x=>x.id===docsCtx.projectId);
  document.getElementById("docsModalTitle").textContent=p.name;
  const list=document.getElementById("docList");
  list.innerHTML=p.docs.length?p.docs.map(d=>{
    const isFile=d.type==="file";
    const main=isFile
      ?`<button class="doc-file-btn" type="button" data-open-file title="Descargar ${esc(d.name)}">${esc(d.name)}</button>`
      :`<a href="${esc(d.url)}" target="_blank" rel="noopener" title="${esc(d.url)}">${esc(d.name)}</a>`;
    return`<div class="doc-row" data-doc="${d.id}">
      ${isFile?IC.down:IC.doc}
      ${main}
      ${isFile&&d.size?`<span style="font-family:var(--mono);font-size:10px;color:var(--muted);flex:none">${fmtSize(d.size)}</span>`:""}
      <button class="icon-btn" type="button" data-del-doc aria-label="Eliminar documento">${IC.trash}</button></div>`;
  }).join("")
  :`<div class="empty">Sin documentos todavía.<br>Sube un archivo o agrega un enlace de SharePoint para el seguimiento.</div>`;
}
document.getElementById("docList").addEventListener("click",async e=>{
  const openBtn=e.target.closest("[data-open-file]");
  if(openBtn){
    const row=openBtn.closest(".doc-row");
    const a=state.areas.find(x=>x.id===docsCtx.areaId);
    const p=a.projects.find(x=>x.id===docsCtx.projectId);
    const d=p.docs.find(x=>x.id===row.dataset.doc);
    if(d)downloadFileDoc(d);
    return;
  }
  const btn=e.target.closest("[data-del-doc]");if(!btn)return;
  const row=btn.closest(".doc-row");
  const a=state.areas.find(x=>x.id===docsCtx.areaId);
  const p=a.projects.find(x=>x.id===docsCtx.projectId);
  const d=p.docs.find(x=>x.id===row.dataset.doc);
  if(d&&d.type==="file")await DB.del(d.id).catch(()=>{});
  p.docs=p.docs.filter(x=>x.id!==row.dataset.doc);
  save();renderDocList();renderBoard();toast("Documento eliminado");
});
document.getElementById("dAdd").addEventListener("click",()=>{
  const name=document.getElementById("dName").value.trim();
  let url=document.getElementById("dUrl").value.trim();
  if(!name){toast("Ponle un nombre al documento");document.getElementById("dName").focus();return;}
  if(!url){toast("Falta el enlace del documento");document.getElementById("dUrl").focus();return;}
  if(!/^https?:\/\//i.test(url))url="https://"+url;
  const a=state.areas.find(x=>x.id===docsCtx.areaId);
  const p=a.projects.find(x=>x.id===docsCtx.projectId);
  p.docs.push({id:uid(),name,url,type:"link"});
  save();renderDocList();renderBoard();
  document.getElementById("dName").value="";document.getElementById("dUrl").value="";document.getElementById("dName").focus();
  toast("Enlace añadido");
});
document.getElementById("dUpload").addEventListener("click",async()=>{
  const input=document.getElementById("dFile");
  const file=input.files[0];
  if(!file){toast("Primero elige un archivo de tu PC");input.focus();return;}
  if(file.size>25*1048576){toast("El archivo pesa más de 25 MB, mejor súbelo a SharePoint y pega el enlace");return;}
  const a=state.areas.find(x=>x.id===docsCtx.areaId);
  const p=a.projects.find(x=>x.id===docsCtx.projectId);
  const id=uid();
  try{
    await DB.put(id,file);
    p.docs.push({id,name:file.name,size:file.size,type:"file"});
    save();renderDocList();renderBoard();
    input.value="";
    toast("Archivo subido: "+file.name);
  }catch(e){toast("No se pudo guardar el archivo");}
});

/* ================= CONFIRMAR ================= */
let confirmCb=null;
function askConfirm(text,cb){document.getElementById("confirmText").textContent=text;confirmCb=cb;openOverlay("confirmOverlay");}
document.getElementById("confirmYes").addEventListener("click",()=>{
  closeOverlay(document.getElementById("confirmOverlay"));if(confirmCb)confirmCb();confirmCb=null;});

/* ================= EVENTOS TABLERO ================= */
areasEl.addEventListener("click",e=>{
  const chip=e.target.closest("[data-chip-file]");
  if(chip){
    const cardEl=e.target.closest(".card");
    const areaEl=e.target.closest(".area");
    const a=state.areas.find(x=>x.id===areaEl.dataset.area);
    const p=a.projects.find(x=>x.id===cardEl.dataset.id);
    const d=p.docs.find(x=>x.id===chip.dataset.chipFile);
    if(d)downloadFileDoc(d);
    return;
  }
  const actBtn=e.target.closest("[data-act]");if(!actBtn)return;
  const areaEl=e.target.closest(".area"),areaId=areaEl.dataset.area,cardEl=e.target.closest(".card"),act=actBtn.dataset.act;
  if(act==="add-project")openProjectModal(areaId,null);
  if(act==="rename-area")startRename(areaEl,areaId);
  if(act==="edit"&&cardEl)openProjectModal(areaId,cardEl.dataset.id);
  if(act==="docs"&&cardEl)openDocsModal(areaId,cardEl.dataset.id);
  if(act==="del"&&cardEl){
    const a=state.areas.find(x=>x.id===areaId);
    const p=a.projects.find(x=>x.id===cardEl.dataset.id);
    askConfirm(`Se eliminará "${p.name}" y sus ${p.docs.length} documento(s) vinculados.`,()=>{
      a.projects=a.projects.filter(x=>x.id!==p.id);
      save();renderBoard();renderDashboard();toast("Proyecto eliminado");});
  }
});

function startRename(areaEl,areaId){
  const a=state.areas.find(x=>x.id===areaId);
  const span=areaEl.querySelector(".area-name");
  const input=document.createElement("input");
  input.type="text";input.className="area-name-input";input.value=a.name;input.maxLength=60;
  span.replaceWith(input);input.focus();input.select();
  let done=false;
  const finish=ok=>{if(done)return;done=true;
    if(ok&&input.value.trim()){a.name=input.value.trim();save();renderDashboard();renderActas();toast("Área renombrada");}
    renderBoard();};
  input.addEventListener("keydown",e=>{if(e.key==="Enter")finish(true);if(e.key==="Escape")finish(false);});
  input.addEventListener("blur",()=>finish(true));
}

/* ================= EXPORTAR / IMPORTAR / RESUMEN ================= */
document.getElementById("btnExport").addEventListener("click",()=>{
  const blob=new Blob([JSON.stringify(state,null,2)],{type:"application/json"});
  const a=document.createElement("a");a.href=URL.createObjectURL(blob);
  a.download="repositorio_proyectos_TH.json";a.click();URL.revokeObjectURL(a.href);
  toast("Respaldo descargado (.json)");
});
document.getElementById("btnImport").addEventListener("click",()=>document.getElementById("importFile").click());
document.getElementById("importFile").addEventListener("change",e=>{
  const file=e.target.files[0];if(!file)return;
  const reader=new FileReader();
  reader.onload=()=>{try{
    const data=JSON.parse(reader.result);
    if(!data||!Array.isArray(data.areas))throw new Error("formato");
    if(!Array.isArray(data.actas))data.actas=[];
    state=data;save();renderDashboard();renderBoard();renderActas();
    toast("Datos importados correctamente");
  }catch(err){toast("Archivo no válido");}e.target.value="";};
  reader.readAsText(file);
});
document.getElementById("btnSummary").addEventListener("click",()=>{
  const lines=["REPOSITORIO DE PROYECTOS · TALENTO HUMANO",""];
  state.areas.forEach(a=>{
    lines.push(`▸ ${a.name} — avance ${areaAvg(a)}% (${a.projects.length} proyectos)`);
    a.projects.forEach(p=>lines.push(`   · ${p.name} — ${STATUS[p.status].label}, ${p.pct}%${p.owner?` (${p.owner})`:""}`));
  });
  if(state.actas.length){lines.push("","ACTAS REGISTRADAS: "+state.actas.length);}
  navigator.clipboard.writeText(lines.join("\n")).then(
    ()=>toast("Resumen copiado al portapapeles"),()=>toast("No se pudo copiar"));
});

/* ================= INIT ================= */
renderDashboard();
renderBoard();
renderActas();
})();
</script>
</body>
</html>
