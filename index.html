<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Club Lounge — Table Manager</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Mono:wght@300;400&family=Noto+Serif+JP:wght@300;400;600&display=swap" rel="stylesheet">
<style>
/* ── Themes ──────────────────────────────────────────── */
:root {
  --bg:#0f0d0b; --surface:#1a1713; --surface2:#221f1a; --border:#2e2a24;
  --gold:#c9a84c; --gold-dim:#8a6e2f; --gold-light:#e8c97a;
  --cream:#f0e8d8; --cream-dim:#9a9186;
  --free:#1e2e1f; --free-border:#2d4a2f; --free-text:#6aaa6e;
  --occupied:#2e1a0e; --occupied-border:#7a3a12; --occupied-text:#e07040;
  --warning:#2e2510; --warning-border:#8a6a10; --warning-text:#d4a020;
  --danger:#2e0e0e; --danger-border:#8a1010; --danger-text:#e03030;
  --accent:#c9a84c; --radius:4px;
}
[data-theme="ocean"] {
  --bg:#090e14; --surface:#111922; --surface2:#19232e; --border:#1e2d3d;
  --gold:#4a9eca; --gold-dim:#2a6a9a; --gold-light:#7ac0e8;
  --cream:#d8eaf8; --cream-dim:#7a9ab2;
  --free:#0e1e2e; --free-border:#1a3a5a; --free-text:#4a9aca;
  --occupied:#1e0e20; --occupied-border:#5a1a7a; --occupied-text:#c060e0;
  --warning:#1e1a0e; --warning-border:#5a4a10; --warning-text:#c0a020;
  --danger:#1e0e0e; --danger-border:#7a1010; --danger-text:#e03030;
  --accent:#4a9eca;
}
[data-theme="beige"] {
  --bg:#f0e8d4; --surface:#e8dcc4; --surface2:#ddd0b4; --border:#c4b090;
  --gold:#8a5c20; --gold-dim:#b07c38; --gold-light:#5c3c10;
  --cream:#2c1c08; --cream-dim:#806040;
  --free:#d4ecd4; --free-border:#88c488; --free-text:#286028;
  --occupied:#f0dcc8; --occupied-border:#d09060; --occupied-text:#8a3810;
  --warning:#f0e8c0; --warning-border:#c8a030; --warning-text:#7a5010;
  --danger:#f0d0c8; --danger-border:#d05050; --danger-text:#901010;
  --accent:#8a5c20;
}

/* ── Reset & Base ─────────────────────────────────────── */
*{box-sizing:border-box;margin:0;padding:0;}
body{background:var(--bg);color:var(--cream);font-family:'DM Mono',monospace;font-weight:300;height:100vh;overflow:hidden;transition:background 0.3s,color 0.3s;}
body.lang-ja{font-family:'Noto Serif JP',serif;}
body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");pointer-events:none;z-index:9999;opacity:0.4;}

/* ── Header ───────────────────────────────────────────── */
header{display:flex;align-items:center;justify-content:space-between;padding:10px 20px;border-bottom:1px solid var(--border);background:var(--surface);flex-shrink:0;gap:10px;}
.logo{display:flex;align-items:center;gap:10px;white-space:nowrap;}
.logo-text{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:300;letter-spacing:0.14em;color:var(--gold);}
.logo-text span{font-style:italic;color:var(--gold-light);}
/* Logo image — white base, recolored via filter to match theme gold */
.logo-img{width:34px;height:34px;flex-shrink:0;
  filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(450%) hue-rotate(5deg) brightness(95%);
  transition:filter 0.3s;}
/* Per-theme filter overrides to match each --gold color */
[data-theme="ocean"]    .logo-img{filter:brightness(0) saturate(100%) invert(62%) sepia(60%) saturate(350%) hue-rotate(175deg) brightness(105%);}
[data-theme="beige"]    .logo-img{filter:brightness(0) saturate(100%) invert(22%) sepia(90%) saturate(700%) hue-rotate(20deg) brightness(60%);}
/* Custom logo color override via CSS var set by color editor */
.logo-img.custom-filter{filter:none!important;}
.header-right{display:flex;align-items:center;gap:10px;}
.clock{font-size:11px;color:var(--cream-dim);letter-spacing:0.05em;font-family:'DM Mono',monospace;white-space:nowrap;}
.stats{display:flex;gap:12px;}
.stat{display:flex;flex-direction:column;align-items:center;gap:1px;}
.stat-val{font-size:14px;color:var(--cream);font-family:'Cormorant Garamond',serif;font-weight:600;}
.stat-label{text-transform:uppercase;font-size:7px;color:var(--cream-dim);letter-spacing:0.08em;}
.settings-icon-btn{background:none;border:1px solid var(--border);color:var(--cream-dim);padding:5px 9px;border-radius:var(--radius);cursor:pointer;font-size:14px;transition:all 0.15s;line-height:1;}
.settings-icon-btn:hover{border-color:var(--gold-dim);color:var(--gold);}
.lang-divider{width:1px;height:18px;background:var(--border);}

/* ── Buttons ──────────────────────────────────────────── */
.btn{background:var(--surface2);border:1px solid var(--border);color:var(--cream);font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.05em;padding:5px 11px;cursor:pointer;border-radius:var(--radius);transition:all 0.15s;white-space:nowrap;}
.btn:hover{border-color:var(--gold-dim);color:var(--gold-light);}
.btn.active{background:var(--gold-dim);border-color:var(--gold);color:var(--bg);}
.btn.gold{background:var(--gold-dim);border-color:var(--gold);color:var(--cream);}
.btn.gold:hover{background:var(--gold);color:var(--bg);}
.btn.danger{background:#2a0e0e;border-color:#5a1a1a;color:#e05050;}
.btn.danger:hover{background:#3a1010;border-color:#8a2020;}
.btn.edit-active{background:#142030;border-color:#3a6a9a;color:#7abae8;}
.lang-btn{font-size:11px;padding:5px 9px;}

/* ── App layout ───────────────────────────────────────── */
.app{display:grid;grid-template-columns:1fr 310px;height:calc(100vh - 53px);}

/* ── Main area ────────────────────────────────────────── */
.main-area{display:flex;flex-direction:column;overflow:hidden;}
.mode-bar{display:flex;border-bottom:1px solid var(--border);background:var(--surface);flex-shrink:0;}
.mode-tab{padding:7px 16px;font-size:9px;letter-spacing:0.1em;text-transform:uppercase;cursor:pointer;border-bottom:2px solid transparent;color:var(--cream-dim);transition:all 0.15s;background:none;border-top:none;border-left:none;border-right:none;font-family:'DM Mono',monospace;}
.mode-tab:hover{color:var(--cream);}
.mode-tab.active{color:var(--gold);border-bottom-color:var(--gold);}

/* ── Grid view ────────────────────────────────────────── */
#gridView{padding:46px 16px 20px;width:100%;box-sizing:border-box;}
.legend{display:flex;gap:9px;flex-wrap:wrap;}
.legend-item{display:flex;align-items:center;gap:4px;font-size:8px;letter-spacing:0.06em;color:var(--cream-dim);text-transform:uppercase;}
.legend-dot{width:6px;height:6px;border-radius:50%;}
input[type=number]{background:var(--surface2);border:1px solid var(--border);color:var(--cream);font-family:'DM Mono',monospace;font-size:11px;padding:4px 6px;width:54px;border-radius:var(--radius);text-align:center;}
input[type=number]:focus{outline:none;border-color:var(--gold-dim);}
#tableGrid{display:grid;gap:7px;justify-items:center;}

/* ── Table card ───────────────────────────────────────── */
.table-card{width:100%;aspect-ratio:1.2;max-width:102px;border:1px solid;border-radius:var(--radius);cursor:pointer;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;transition:all 0.2s;position:relative;user-select:none;}
.table-card.free{background:var(--free);border-color:var(--free-border);}
.table-card.free:hover{border-color:var(--free-text);}
.table-card.occupied{background:var(--occupied);border-color:var(--occupied-border);}
.table-card.occupied:hover{border-color:var(--occupied-text);}
.table-card.warning{background:var(--warning);border-color:var(--warning-border);animation:pw 2s infinite;}
.table-card.danger-time{background:var(--danger);border-color:var(--danger-border);animation:pd 1s infinite;}
@keyframes pw{0%,100%{box-shadow:0 0 0 0 rgba(212,160,32,0);}50%{box-shadow:0 0 0 4px rgba(212,160,32,0.15);}}
@keyframes pd{0%,100%{box-shadow:0 0 0 0 rgba(224,48,48,0);}50%{box-shadow:0 0 0 5px rgba(224,48,48,0.2);}}
.table-num{font-family:'Cormorant Garamond',serif;font-size:25px;font-weight:600;line-height:1;}
.table-card.free .table-num{color:var(--free-text);}
.table-card.occupied .table-num{color:var(--occupied-text);}
.table-card.warning .table-num{color:var(--warning-text);}
.table-card.danger-time .table-num{color:var(--danger-text);}
.table-status{font-size:7px;letter-spacing:0.1em;text-transform:uppercase;}
.table-card.free .table-status{color:var(--free-text);opacity:0.7;}
.table-card.occupied .table-status{color:var(--occupied-text);}
.table-card.warning .table-status{color:var(--warning-text);}
.table-card.danger-time .table-status{color:var(--danger-text);}
.table-timer{font-size:10px;font-family:'DM Mono',monospace;}
.table-card.occupied .table-timer{color:var(--occupied-text);}
.table-card.warning .table-timer{color:var(--warning-text);}
.table-card.danger-time .table-timer{color:var(--danger-text);}
.table-guest{font-size:8px;color:var(--cream-dim);text-align:center;padding:0 4px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;max-width:100%;font-weight:400;}
.table-seats-badge{position:absolute;top:3px;right:4px;font-size:7px;opacity:0.5;}

/* ── Floor plan ───────────────────────────────────────── */
#floorView{flex:1;position:relative;overflow:hidden;width:100%;}
#floorCanvas{min-width:100%;min-height:100%;position:relative;background-color:var(--bg);
  background-image:linear-gradient(var(--border) 1px,transparent 1px),linear-gradient(90deg,var(--border) 1px,transparent 1px);
  background-size:40px 40px;}
.floor-table{position:absolute;border:1px solid;border-radius:6px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;user-select:none;transition:box-shadow 0.15s;z-index:2;overflow:hidden;}
.floor-table.free{background:var(--free);border-color:var(--free-border);}
.floor-table.free:hover{border-color:var(--free-text);}
.floor-table.occupied{background:var(--occupied);border-color:var(--occupied-border);}
.floor-table.occupied:hover{border-color:var(--occupied-text);}
.floor-table.warning{background:var(--warning);border-color:var(--warning-border);animation:pw 2s infinite;}
.floor-table.danger-time{background:var(--danger);border-color:var(--danger-border);animation:pd 1s infinite;}
.floor-table .ft-num{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:600;line-height:1;}
.floor-table.free .ft-num{color:var(--free-text);}
.floor-table.occupied .ft-num{color:var(--occupied-text);}
.floor-table.warning .ft-num{color:var(--warning-text);}
.floor-table.danger-time .ft-num{color:var(--danger-text);}
.floor-table .ft-timer{font-size:10px;font-family:'DM Mono',monospace;}
.floor-table.occupied .ft-timer{color:var(--occupied-text);}
.floor-table.warning .ft-timer{color:var(--warning-text);}
.floor-table.danger-time .ft-timer{color:var(--danger-text);}
.floor-table .ft-guest{font-size:10px;color:var(--cream-dim);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;max-width:90%;text-align:center;font-weight:400;}
.floor-table .ft-seats{position:absolute;top:3px;right:4px;font-size:8px;opacity:0.5;}
.floor-table.selected-token{box-shadow:0 0 0 2px var(--gold)!important;border-color:var(--gold)!important;}
.resize-handle{position:absolute;bottom:0;right:0;width:14px;height:14px;cursor:se-resize;display:flex;align-items:flex-end;justify-content:flex-end;padding:2px;}
.resize-handle svg{opacity:0.35;}
.resize-handle:hover svg{opacity:0.75;}
.floor-edit-bar{position:absolute;top:10px;left:10px;display:flex;gap:6px;z-index:10;flex-wrap:wrap;align-items:center;}
.floor-hint{position:absolute;bottom:10px;left:50%;transform:translateX(-50%);font-size:8px;color:var(--cream-dim);letter-spacing:0.08em;text-transform:uppercase;background:rgba(15,13,11,0.85);padding:4px 12px;border-radius:20px;border:1px solid var(--border);pointer-events:none;white-space:nowrap;}

/* ── Sidebar ──────────────────────────────────────────── */
.sidebar{display:flex;flex-direction:column;border-left:1px solid var(--border);overflow:hidden;}

/* Sidebar tabs */
.sidebar-tabs{display:flex;border-bottom:1px solid var(--border);flex-shrink:0;}
.sidebar-tab{flex:1;padding:7px 6px;font-size:8px;letter-spacing:0.1em;text-transform:uppercase;cursor:pointer;border-bottom:2px solid transparent;color:var(--cream-dim);transition:all 0.15s;background:none;border-top:none;border-left:none;border-right:none;font-family:'DM Mono',monospace;text-align:center;}
.sidebar-tab:hover{color:var(--cream);}
.sidebar-tab.active{color:var(--gold);border-bottom-color:var(--gold);}

/* Panels container — single scrollable column */
.sidebar-scroll{flex:1;overflow-y:auto;overflow-x:hidden;scroll-behavior:smooth;-webkit-overflow-scrolling:touch;min-height:0;}
/* Each tab div needs to let content flow naturally */
#tab-detail,#tab-guests,#tab-settings{min-height:0;}

/* Each panel section */
.s-section{border-bottom:1px solid var(--border);}
.s-section-head{display:flex;align-items:center;justify-content:space-between;padding:11px 14px;cursor:pointer;user-select:none;}
.s-section-title{font-family:'Cormorant Garamond',serif;font-size:13px;font-weight:300;letter-spacing:0.1em;color:var(--gold);text-transform:uppercase;font-style:italic;}
.s-section-arrow{font-size:10px;color:var(--cream-dim);transition:transform 0.2s;}
.s-section-arrow.open{transform:rotate(180deg);}
.s-section-body{padding:0 14px 14px;display:none;}
.s-section-body.open{display:block;}

.s-row{display:flex;align-items:center;gap:7px;margin-bottom:8px;flex-wrap:wrap;}
.s-label{font-size:8px;text-transform:uppercase;letter-spacing:0.1em;color:var(--cream-dim);min-width:70px;}
.s-label-full{font-size:8px;text-transform:uppercase;letter-spacing:0.1em;color:var(--cream-dim);margin-bottom:4px;}

.theme-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:4px;}
.theme-swatch{width:100%;aspect-ratio:1;border-radius:4px;border:2px solid transparent;cursor:pointer;transition:all 0.15s;position:relative;}
.theme-swatch:hover{transform:scale(1.08);}
.theme-swatch.active{border-color:var(--gold);}
.theme-swatch::after{content:'';position:absolute;inset:2px;border-radius:2px;}
.swatch-classic::after{background:linear-gradient(135deg,#1e2e1f 50%,#2e1a0e 50%);}
.swatch-ocean::after{background:linear-gradient(135deg,#0e1e2e 50%,#1e0e20 50%);}
.swatch-beige::after{background:linear-gradient(135deg,#c8b48a 50%,#d4b898 50%);}
.theme-name{font-size:8px;text-align:center;color:var(--cream-dim);margin-top:3px;letter-spacing:0.05em;}

/* ── Color editor ─────────────────────────────────────── */
.color-editor{margin-top:12px;}
.color-editor-title{font-size:8px;text-transform:uppercase;letter-spacing:0.1em;color:var(--cream-dim);margin-bottom:8px;}
.color-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:7px;gap:8px;}
.color-row-label{font-size:9px;color:var(--cream-dim);flex:1;white-space:nowrap;}
.color-row input[type=color]{width:32px;height:22px;border:1px solid var(--border);border-radius:3px;cursor:pointer;background:none;padding:0;outline:none;}
.color-row input[type=color]::-webkit-color-swatch-wrapper{padding:2px;}
.color-row input[type=color]::-webkit-color-swatch{border:none;border-radius:2px;}
.color-reset-btn{font-size:8px;color:var(--cream-dim);background:none;border:1px solid var(--border);border-radius:3px;padding:2px 6px;cursor:pointer;white-space:nowrap;}
.color-reset-btn:hover{color:var(--gold);border-color:var(--gold-dim);}

/* Guest list */
.guest-list{margin-top:2px;}
.guest-row{display:flex;align-items:center;gap:8px;padding:7px 0;border-bottom:1px solid var(--border);cursor:pointer;transition:background 0.1s;}
.guest-row:last-child{border-bottom:none;}
.guest-row:hover{background:var(--surface2);margin:0 -14px;padding:7px 14px;}
.guest-tnum{font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:600;color:var(--gold);min-width:28px;line-height:1;}
.guest-info{flex:1;min-width:0;}
.guest-name{font-size:10px;color:var(--cream);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
.guest-room{font-size:8px;color:var(--cream-dim);}
.guest-timer{font-size:9px;font-family:'DM Mono',monospace;white-space:nowrap;}
.guest-timer.warn{color:var(--warning-text);}
.guest-timer.over{color:var(--danger-text);}
.guest-empty{font-size:12px;color:var(--cream-dim);text-align:center;padding:24px 0;font-family:'Cormorant Garamond',serif;font-style:italic;}
.guest-status-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0;}

/* Detail section */
.detail-table-num{font-family:'Cormorant Garamond',serif;font-size:38px;font-weight:300;color:var(--gold-light);line-height:1;margin-bottom:3px;}
.detail-badge{display:inline-block;font-size:7px;letter-spacing:0.1em;text-transform:uppercase;padding:2px 6px;border-radius:2px;margin-bottom:10px;}
.badge-free{background:var(--free);color:var(--free-text);border:1px solid var(--free-border);}
.badge-occupied{background:var(--occupied);color:var(--occupied-text);border:1px solid var(--occupied-border);}
.badge-warning{background:var(--warning);color:var(--warning-text);border:1px solid var(--warning-border);}
.badge-danger{background:var(--danger);color:var(--danger-text);border:1px solid var(--danger-border);}
.field-group{margin-bottom:9px;}
.field-label{font-size:7px;text-transform:uppercase;letter-spacing:0.1em;color:var(--cream-dim);margin-bottom:3px;}
.field-input{width:100%;background:var(--surface2);border:1px solid var(--border);color:var(--cream);font-family:'DM Mono',monospace;font-size:11px;padding:6px 8px;border-radius:var(--radius);}
.field-input:focus{outline:none;border-color:var(--gold-dim);}
.field-row{display:grid;grid-template-columns:1fr 1fr;gap:7px;}
.timer-display{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:300;letter-spacing:0.05em;color:var(--cream);margin:5px 0;}
.timer-display.warn{color:var(--warning-text);}
.timer-display.over{color:var(--danger-text);}
.time-bar{height:2px;background:var(--border);border-radius:2px;margin:4px 0 9px;overflow:hidden;}
.time-bar-fill{height:100%;border-radius:2px;transition:width 1s linear,background 0.5s;}
.seated-at{font-size:8px;color:var(--cream-dim);margin-bottom:2px;}
.action-row{display:flex;gap:7px;margin-top:10px;flex-wrap:wrap;}
.action-row .btn{flex:1;text-align:center;font-size:10px;}

/* Modal */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,0.72);z-index:1000;align-items:center;justify-content:center;backdrop-filter:blur(2px);}
.modal-overlay.open{display:flex;}
.modal{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:20px;min-width:260px;max-width:340px;width:90%;}
.modal-title{font-family:'Cormorant Garamond',serif;font-size:16px;color:var(--gold);margin-bottom:10px;font-style:italic;}
.modal-actions{display:flex;gap:8px;margin-top:14px;justify-content:flex-end;}

::-webkit-scrollbar{width:3px;}
::-webkit-scrollbar-track{background:var(--surface);}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:2px;}

/* ── Zoom wrapper (grid & floor) ──────────────────────── */
.zoom-viewport{flex:1;overflow:hidden;position:relative;}
/* Grid viewport: allow native scroll when at 1x; touch pinch handled in JS */
#gridViewport{touch-action:pan-y;overflow-y:auto;overflow-x:hidden;}
/* When zoomed (JS adds .zoomed class), scroll within the scaled inner */
#gridViewport.zoomed{overflow:hidden;}
/* Floor viewport blocks all touch to enable pinch/drag */
#floorViewport{touch-action:none;}
.zoom-inner{transform-origin:0 0;will-change:transform;}
/* gridZoomInner: full width so grid can lay out correctly */
#gridZoomInner{width:100%;}

/* Legend fixed overlay — sits above zoom-inner, never moves */
.legend-overlay{position:absolute;top:12px;left:12px;z-index:15;display:flex;gap:8px;flex-wrap:wrap;background:rgba(15,13,11,0.82);padding:5px 10px;border-radius:6px;border:1px solid var(--border);pointer-events:none;}
[data-theme="light"] .legend-overlay,[data-theme="beige"] .legend-overlay{background:rgba(240,232,212,0.92);}
.legend{display:flex;gap:9px;flex-wrap:wrap;}
.legend-item{display:flex;align-items:center;gap:4px;font-size:8px;letter-spacing:0.06em;color:var(--cream-dim);text-transform:uppercase;}
.legend-dot{width:6px;height:6px;border-radius:50%;}

/* Desktop drag-to-pan cursor states */
.zoom-viewport.can-drag{cursor:grab;}
.zoom-viewport.dragging{cursor:grabbing!important;}

/* ── Zoom controls ────────────────────────────────────── */
.zoom-controls{position:absolute;bottom:12px;right:12px;display:flex;gap:5px;z-index:20;}
.zoom-btn{background:var(--surface);border:1px solid var(--border);color:var(--cream-dim);width:30px;height:30px;border-radius:50%;cursor:pointer;font-size:16px;line-height:1;display:flex;align-items:center;justify-content:center;transition:all 0.15s;}
.zoom-btn:hover{border-color:var(--gold-dim);color:var(--gold);}
.zoom-level{background:var(--surface);border:1px solid var(--border);color:var(--cream-dim);padding:0 8px;border-radius:12px;font-size:9px;display:flex;align-items:center;letter-spacing:0.05em;}

/* Mobile bottom spacer — keeps Android nav bar from covering content */
.mobile-spacer{height:160px;flex-shrink:0;}
@media(min-width:681px){.mobile-spacer{display:none;}}

/* Custom saved theme swatches */
.custom-theme-row{display:flex;align-items:center;gap:6px;margin-bottom:6px;}
.custom-swatch{width:28px;height:28px;border-radius:4px;border:2px solid transparent;cursor:pointer;flex-shrink:0;transition:all 0.15s;}
.custom-swatch:hover{transform:scale(1.1);}
.custom-swatch.active{border-color:var(--gold);}
.custom-theme-name{font-size:9px;color:var(--cream-dim);flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.custom-theme-del{font-size:10px;color:var(--cream-dim);background:none;border:none;cursor:pointer;padding:2px 4px;line-height:1;opacity:0.6;}
.custom-theme-del:hover{opacity:1;color:#e05050;}
.save-theme-row{display:flex;gap:6px;align-items:center;margin-top:8px;}
.save-theme-input{flex:1;background:var(--surface2);border:1px solid var(--border);color:var(--cream);font-family:'DM Mono',monospace;font-size:10px;padding:5px 8px;border-radius:var(--radius);}
.save-theme-input:focus{outline:none;border-color:var(--gold-dim);}

@media(max-width:680px){
  .app{grid-template-columns:1fr;grid-template-rows:1fr 46vh;}
  .sidebar{border-top:1px solid var(--border);border-left:none;min-height:0;}
  /* sidebar-scroll already has overflow-y:auto globally, just reinforce */
  .sidebar-scroll{overflow-y:auto!important;-webkit-overflow-scrolling:touch;}
  header{flex-wrap:wrap;gap:6px;}
}
</style>
</head>
<body>

<header>
  <div class="logo">
    <div class="logo-text">Club Lounge</div>
    <img class="logo-img" src="data:image/png;base64,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" alt="Club Lounge Logo">
  </div>
  <div class="header-right">
    <div class="stats">
      <div class="stat"><span class="stat-val" id="statFree">0</span><span class="stat-label" id="lbl-free">Free</span></div>
      <div class="stat"><span class="stat-val" id="statOccupied">0</span><span class="stat-label" id="lbl-seated">Seated</span></div>
      <div class="stat"><span class="stat-val" id="statTotal">0</span><span class="stat-label" id="lbl-tables">Tables</span></div>
    </div>
    <div class="clock" id="clock">--:--:--</div>
    <div class="lang-divider"></div>
    <button class="btn lang-btn active" id="btnEN" onclick="setLang('en')">EN</button>
    <button class="btn lang-btn" id="btnJA" onclick="setLang('ja')">日本語</button>
    <div class="lang-divider"></div>
    <button class="settings-icon-btn" onclick="openSettings()" title="Settings">⚙</button>
  </div>
</header>

<div class="app">
  <!-- Main -->
  <div class="main-area">
    <div class="mode-bar">
      <button class="mode-tab active" id="tabGrid" onclick="switchMode('grid')">Grid View</button>
      <button class="mode-tab" id="tabFloor" onclick="switchMode('floor')">Floor Plan</button>
    </div>

    <!-- Grid -->
    <div class="zoom-viewport" id="gridViewport">
      <!-- Legend fixed overlay — unaffected by zoom/pan -->
      <div class="legend-overlay">
        <div class="legend">
          <div class="legend-item"><div class="legend-dot" style="background:var(--free-border)"></div><span id="leg-free">Free</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--occupied-border)"></div><span id="leg-occ">Occupied</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--warning-border)"></div><span id="leg-near">Near limit</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--danger-border)"></div><span id="leg-over">Over limit</span></div>
        </div>
      </div>
      <div class="zoom-inner" id="gridZoomInner">
        <div id="gridView">
          <div id="tableGrid"></div>
        </div>
      </div>
      <div class="zoom-controls" id="gridZoomControls">
        <button class="zoom-btn" onclick="adjustZoom('grid',-0.2)">−</button>
        <span class="zoom-level" id="gridZoomLabel">100%</span>
        <button class="zoom-btn" onclick="adjustZoom('grid',0.2)">+</button>
        <button class="zoom-btn" onclick="resetZoom('grid')" title="Reset">⌂</button>
      </div>
    </div>

    <!-- Floor -->
    <div class="zoom-viewport" id="floorViewport" style="display:none;">
      <!-- Legend fixed overlay for floor too -->
      <div class="legend-overlay">
        <div class="legend">
          <div class="legend-item"><div class="legend-dot" style="background:var(--free-border)"></div><span id="leg-free2">Free</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--occupied-border)"></div><span id="leg-occ2">Occupied</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--warning-border)"></div><span id="leg-near2">Near limit</span></div>
          <div class="legend-item"><div class="legend-dot" style="background:var(--danger-border)"></div><span id="leg-over2">Over limit</span></div>
        </div>
      </div>
      <div class="zoom-inner" id="floorZoomInner">
        <div id="floorView">
          <div id="floorCanvas">
            <div class="floor-edit-bar" id="floorEditBar" style="display:none;">
              <button class="btn gold" id="btnAddTable" onclick="addFloorTable()">+ Add Table</button>
              <button class="btn danger" id="btnDeleteTable" onclick="deleteSelectedTable()" style="display:none;">Delete</button>
              <button class="btn" id="btnSnap" onclick="snapAllToGrid()">Snap to Grid</button>
            </div>
            <div class="floor-hint" id="floorHint"></div>
          </div>
        </div>
      </div>
      <div class="zoom-controls" id="floorZoomControls">
        <button class="zoom-btn" onclick="adjustZoom('floor',-0.2)">−</button>
        <span class="zoom-level" id="floorZoomLabel">100%</span>
        <button class="zoom-btn" onclick="adjustZoom('floor',0.2)">+</button>
        <button class="zoom-btn" onclick="resetZoom('floor')" title="Reset">⌂</button>
      </div>
    </div>
  </div>

  <!-- Sidebar -->
  <div class="sidebar">
    <div class="sidebar-tabs">
      <button class="sidebar-tab active" id="stab-detail" onclick="setSideTab('detail')" data-stab="detail">Detail</button>
      <button class="sidebar-tab" id="stab-guests" onclick="setSideTab('guests')" data-stab="guests">Guests</button>
      <button class="sidebar-tab" id="stab-settings" onclick="setSideTab('settings')" data-stab="settings">Settings</button>
    </div>

    <div class="sidebar-scroll" id="sidebarScroll">

      <!-- ── DETAIL TAB ── -->
      <div id="tab-detail">
        <div id="detailPanel" style="padding:14px;">
          <div class="detail-empty" id="emptyMsg" style="color:var(--cream-dim);font-size:14px;text-align:center;padding:36px 10px;font-style:italic;font-family:'Cormorant Garamond',serif;line-height:1.9;">Select a table<br>to view details</div>
        </div>
        <div class="mobile-spacer"></div>
      </div>

      <!-- ── GUESTS TAB ── -->
      <div id="tab-guests" style="display:none;padding:14px;">
        <div style="font-family:'Cormorant Garamond',serif;font-size:13px;font-style:italic;color:var(--gold);margin-bottom:10px;letter-spacing:0.1em;text-transform:uppercase;" id="lbl-guestList">Current Guests</div>
        <div class="guest-list" id="guestList"></div>
        <div class="mobile-spacer"></div>
      </div>

      <!-- ── SETTINGS TAB ── -->
      <div id="tab-settings" style="display:none;">

        <!-- Grid settings -->
        <div class="s-section">
          <div class="s-section-head" onclick="toggleSection('sec-grid')">
            <span class="s-section-title" id="lbl-gridSettings">Grid Settings</span>
            <span class="s-section-arrow open" id="arrow-sec-grid">▾</span>
          </div>
          <div class="s-section-body open" id="sec-grid">
            <div class="s-row">
              <span class="s-label" id="lbl-cols">Columns</span>
              <input type="number" id="colCount" value="5" min="2" max="10">
            </div>
            <div class="s-row">
              <span class="s-label" id="lbl-tableCount">Tables</span>
              <input type="number" id="tableCount" value="15" min="1" max="50">
            </div>
            <div class="s-row">
              <button class="btn gold" id="btnApply" onclick="applyGridSettings()" style="width:100%">Apply</button>
            </div>
          </div>
        </div>

        <!-- Timing -->
        <div class="s-section">
          <div class="s-section-head" onclick="toggleSection('sec-timing')">
            <span class="s-section-title" id="lbl-timingSettings">Timing</span>
            <span class="s-section-arrow open" id="arrow-sec-timing">▾</span>
          </div>
          <div class="s-section-body open" id="sec-timing">
            <div class="s-row">
              <span class="s-label" id="lbl-defLimit">Default Limit</span>
              <input type="number" id="defaultLimit" value="90" min="5" max="480" style="width:55px;">
              <span style="font-size:8px;color:var(--cream-dim);" id="lbl-min">min</span>
            </div>
          </div>
        </div>

        <!-- Layout editor -->
        <div class="s-section">
          <div class="s-section-head" onclick="toggleSection('sec-layout')">
            <span class="s-section-title" id="lbl-layoutSettings">Floor Layout</span>
            <span class="s-section-arrow open" id="arrow-sec-layout">▾</span>
          </div>
          <div class="s-section-body open" id="sec-layout">
            <div class="s-row">
              <span class="s-label" id="lbl-editLayout">Edit Mode</span>
              <button class="btn" id="btnEditMode" onclick="toggleEditMode()">Off</button>
            </div>
            <div class="s-row" id="floorEditBtns" style="display:none;">
              <button class="btn gold" id="btnAddTable2" onclick="addFloorTable()" style="flex:1">+ Add</button>
              <button class="btn danger" id="btnDeleteTable2" onclick="deleteSelectedTable()" style="flex:1;display:none;">Delete</button>
            </div>
            <div class="s-row" id="floorSnapRow" style="display:none;">
              <button class="btn" id="btnSnap2" onclick="snapAllToGrid()" style="width:100%">Snap to Grid</button>
            </div>
          </div>
        </div>

        <!-- Appearance / Colors -->
        <div class="s-section">
          <div class="s-section-head" onclick="toggleSection('sec-colors')">
            <span class="s-section-title" id="lbl-colorSettings">Color Theme</span>
            <span class="s-section-arrow open" id="arrow-sec-colors">▾</span>
          </div>
          <div class="s-section-body open" id="sec-colors">
            <div class="theme-grid" id="themeGrid">
              <div onclick="setTheme('classic')">
                <div class="theme-swatch swatch-classic active" id="sw-classic"></div>
                <div class="theme-name" id="tn-classic">Classic</div>
              </div>
              <div onclick="setTheme('ocean')">
                <div class="theme-swatch swatch-ocean" id="sw-ocean"></div>
                <div class="theme-name" id="tn-ocean">Ocean</div>
              </div>
              <div onclick="setTheme('beige')">
                <div class="theme-swatch swatch-beige" id="sw-beige"></div>
                <div class="theme-name" id="tn-beige">Beige</div>
              </div>
            </div>
            <!-- Color editor -->
            <div class="color-editor" id="colorEditor">
              <div class="color-editor-title" id="lbl-colorEditor">Customize Colors</div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-bg">Background</span>
                <input type="color" id="ce-bg" oninput="applyCustomColor('--bg',this.value)">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-surface">Surface</span>
                <input type="color" id="ce-surface" oninput="applyCustomColor('--surface',this.value);applyCustomColor('--surface2',shiftColor(this.value,-12))">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-accent">Accent / Gold</span>
                <input type="color" id="ce-accent" oninput="applyCustomColor('--gold',this.value);applyCustomColor('--gold-dim',shiftColor(this.value,-40));applyCustomColor('--gold-light',shiftColor(this.value,30))">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-text">Body Text</span>
                <input type="color" id="ce-text" oninput="applyCustomColor('--cream',this.value);applyCustomColor('--cream-dim',shiftColor(this.value,-60))">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-header-font">Header Font</span>
                <input type="color" id="ce-header-font" oninput="setHeaderFontColor(this.value)">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-logo">Logo Color</span>
                <input type="color" id="ce-logo" oninput="setLogoColor(this.value)">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-free">Free Table</span>
                <input type="color" id="ce-free" oninput="applyCustomColor('--free-border',this.value);applyCustomColor('--free-text',shiftColor(this.value,60));applyCustomColor('--free',shiftColor(this.value,-80))">
              </div>
              <div class="color-row">
                <span class="color-row-label" id="lbl-ce-occ">Occupied Table</span>
                <input type="color" id="ce-occ" oninput="applyCustomColor('--occupied-border',this.value);applyCustomColor('--occupied-text',shiftColor(this.value,60));applyCustomColor('--occupied',shiftColor(this.value,-80))">
              </div>
              <div style="margin-top:10px;padding-top:10px;border-top:1px solid var(--border);">
                <div class="color-editor-title" id="lbl-savedThemes">Saved Themes</div>
                <div id="savedThemesList"></div>
                <div class="save-theme-row">
                  <input class="save-theme-input" id="newThemeName" placeholder="Theme name…" maxlength="20">
                  <button class="btn gold" onclick="saveCurrentTheme()" id="btnSaveTheme" style="white-space:nowrap;font-size:9px;padding:5px 9px;">Save</button>
                </div>
              </div>
              <div style="margin-top:8px;">
                <button class="color-reset-btn" onclick="resetCustomColors()" id="btnResetColors">Reset to theme</button>
              </div>
            </div>
          </div>
        </div>
        <!-- Mobile spacer — prevents Android nav bar covering last items -->
        <div class="mobile-spacer"></div>

      </div><!-- /tab-settings -->
    </div><!-- /sidebar-scroll -->
  </div><!-- /sidebar -->
</div>

<!-- Release modal -->
<div class="modal-overlay" id="releaseModal">
  <div class="modal">
    <div class="modal-title" id="modal-title">Release Table?</div>
    <p style="font-size:10px;color:var(--cream-dim);line-height:1.7;" id="modal-body">This will clear all guest information and stop the timer for</p>
    <strong id="releaseTableNum" style="color:var(--cream);font-size:12px;display:block;margin-top:4px;"></strong>
    <div class="modal-actions">
      <button class="btn" id="btnCancel" onclick="closeModal()">Cancel</button>
      <button class="btn danger" id="btnRelease" onclick="confirmRelease()">Release Table</button>
    </div>
  </div>
</div>

<script>
// ══════════════════════════
// i18n
// ══════════════════════════
const STRINGS={
  en:{
    free:'Free',seated:'Seated',tables:'Tables',
    cols:'Columns',tableCount:'Tables',apply:'Apply',
    nearLimit:'Near limit',overLimit:'Over limit',occ:'Occupied',
    tabGrid:'Grid View',tabFloor:'Floor Plan',
    tabDetail:'Detail',tabGuests:'Guests',tabSettings:'Settings',
    settings:'Settings',editLayout:'Edit Mode',
    editOn:'On ✓',editOff:'Off',
    defLimit:'Default Limit',min:'min',
    addTable:'+ Add Table',deleteTable:'Delete',snapGrid:'Snap to Grid',
    hintEdit:'Drag to move  ·  Corner to resize  ·  Click to select',
    hintView:'Click a table to select it',
    available:'Available',occupied:'Occupied',nearLimitBadge:'Near Limit',overLimitBadge:'Over Limit',
    releaseTitle:'Release Table?',
    releaseBody:'This will clear all guest information and stop the timer for',
    cancel:'Cancel',release:'Release Table',
    seatGuests:'Seat Guests',releaseTable:'Release Table',
    guestName:'Guest Name',roomNumber:'Room Number',
    seats:'Seats',timeLimit:'Time Limit (min)',seatedAt:'Seated at',
    emptyMsg:'Select a table<br>to view details',
    guestList:'Current Guests',noGuests:'No guests seated',
    gridSettings:'Grid Settings',timingSettings:'Timing',
    layoutSettings:'Floor Layout',colorSettings:'Color Theme',
    themeClassic:'Classic',themeOcean:'Ocean',themeBeige:'Beige',
    colorEditor:'Customize Colors',
    ceBg:'Background',ceSurface:'Surface',ceAccent:'Accent / Gold',
    ceText:'Body Text',ceHeaderFont:'Header Font',ceLogo:'Logo Color',
    ceFree:'Free Table',ceOcc:'Occupied Table',
    resetColors:'Reset to theme',savedThemes:'Saved Themes',
    saveTheme:'Save',newThemePlaceholder:'Theme name…',
  },
  ja:{
    free:'空席',seated:'使用中',tables:'テーブル',
    cols:'列数',tableCount:'テーブル数',apply:'適用',
    nearLimit:'制限間近',overLimit:'制限超過',occ:'使用中',
    tabGrid:'グリッド',tabFloor:'フロア',
    tabDetail:'詳細',tabGuests:'ゲスト',tabSettings:'設定',
    settings:'設定',editLayout:'編集モード',
    editOn:'オン ✓',editOff:'オフ',
    defLimit:'制限時間',min:'分',
    addTable:'＋ テーブル追加',deleteTable:'削除',snapGrid:'グリッドに整列',
    hintEdit:'ドラッグで移動 · 角でリサイズ · クリックで選択',
    hintView:'テーブルをクリックして選択',
    available:'空席',occupied:'使用中',nearLimitBadge:'制限間近',overLimitBadge:'制限超過',
    releaseTitle:'テーブルを解放しますか？',
    releaseBody:'以下のゲスト情報とタイマーをリセットします：',
    cancel:'キャンセル',release:'テーブルを解放',
    seatGuests:'着席',releaseTable:'テーブルを解放',
    guestName:'ゲスト名',roomNumber:'部屋番号',
    seats:'席数',timeLimit:'制限時間（分）',seatedAt:'着席時刻',
    emptyMsg:'テーブルを選択してください',
    guestList:'現在のゲスト',noGuests:'着席中のゲストはいません',
    gridSettings:'グリッド設定',timingSettings:'時間設定',
    layoutSettings:'フロアレイアウト',colorSettings:'カラーテーマ',
    themeClassic:'クラシック',themeOcean:'オーシャン',themeBeige:'ベージュ',
    colorEditor:'カラーカスタマイズ',
    ceBg:'背景',ceSurface:'サーフェス',ceAccent:'アクセント',
    ceText:'本文テキスト',ceHeaderFont:'ヘッダーフォント',ceLogo:'ロゴカラー',
    ceFree:'空席テーブル',ceOcc:'使用中テーブル',
    resetColors:'テーマにリセット',savedThemes:'保存済みテーマ',
    saveTheme:'保存',newThemePlaceholder:'テーマ名…',
  }
};

let lang='en';
function s(k){return(STRINGS[lang]||STRINGS.en)[k]||k;}

function setLang(l){
  lang=l;
  document.getElementById('btnEN').classList.toggle('active',l==='en');
  document.getElementById('btnJA').classList.toggle('active',l==='ja');
  document.body.classList.toggle('lang-ja',l==='ja');
  applyStrings();renderGrid();renderFloor();renderDetail();renderGuestList();updateStats();save();
}

function applyStrings(){
  const ids={
    'lbl-free':'free','lbl-seated':'seated','lbl-tables':'tables',
    'lbl-cols':'cols','lbl-tableCount':'tableCount','btnApply':'apply',
    'leg-free':'free','leg-occ':'occ','leg-near':'nearLimit','leg-over':'overLimit',
    'tabGrid':'tabGrid','tabFloor':'tabFloor',
    'stab-detail':'tabDetail','stab-guests':'tabGuests','stab-settings':'tabSettings',
    'lbl-defLimit':'defLimit','lbl-min':'min',
    'btnAddTable':'addTable','btnDeleteTable':'deleteTable','btnSnap':'snapGrid',
    'btnAddTable2':'addTable','btnSnap2':'snapGrid',
    'modal-title':'releaseTitle','modal-body':'releaseBody',
    'btnCancel':'cancel','btnRelease':'release',
    'lbl-guestList':'guestList',
    'lbl-gridSettings':'gridSettings','lbl-timingSettings':'timingSettings',
    'lbl-layoutSettings':'layoutSettings','lbl-colorSettings':'colorSettings',
    'tn-classic':'themeClassic','tn-ocean':'themeOcean','tn-beige':'themeBeige',
    'lbl-colorEditor':'colorEditor',
    'lbl-ce-bg':'ceBg','lbl-ce-surface':'ceSurface','lbl-ce-accent':'ceAccent',
    'lbl-ce-text':'ceText','lbl-ce-header-font':'ceHeaderFont','lbl-ce-logo':'ceLogo',
    'lbl-ce-free':'ceFree','lbl-ce-occ':'ceOcc',
    'btnResetColors':'resetColors','lbl-savedThemes':'savedThemes','btnSaveTheme':'saveTheme',
    'lbl-editLayout':'editLayout',
  };
  Object.entries(ids).forEach(([id,key])=>{const el=document.getElementById(id);if(el)el.textContent=s(key);});
  // Mirror legend labels to floor overlay
  ['free','occ','near','over'].forEach(k=>{
    const src=document.getElementById('leg-'+k);
    const dst=document.getElementById('leg-'+k+'2');
    if(src&&dst)dst.textContent=src.textContent;
  });
  document.getElementById('emptyMsg').innerHTML=s('emptyMsg');
  document.getElementById('floorHint').textContent=editMode?s('hintEdit'):s('hintView');
  const eb=document.getElementById('btnEditMode');
  eb.textContent=editMode?s('editOn'):s('editOff');
  eb.className='btn '+(editMode?'edit-active':'');
}

// ══════════════════════════
// State
// ══════════════════════════
const SK='lasalle_v6';
let tables=[],cols=5;
let selectedId=null,pendingReleaseId=null;
let currentMode='grid',editMode=false,floorSelId=null;
let currentTheme='classic',currentSideTab='detail';

// ══════════════════════════
// Persistence
// ══════════════════════════
function save(){
  try{localStorage.setItem(SK,JSON.stringify({tables,cols,defaultLimit:getDefLimit(),lang,currentMode,currentTheme}));}catch(e){}
}
function load(){
  try{
    const d=JSON.parse(localStorage.getItem(SK)||'null');
    if(!d)return false;
    tables=d.tables||[];cols=d.cols||5;lang=d.lang||'en';
    currentMode=d.currentMode||'grid';currentTheme=d.currentTheme||'classic';
    document.getElementById('colCount').value=cols;
    document.getElementById('tableCount').value=tables.length;
    document.getElementById('defaultLimit').value=d.defaultLimit||90;
    return true;
  }catch(e){return false;}
}

// ══════════════════════════
// Theme
// ══════════════════════════
const THEMES=['classic','ocean','beige'];
function setTheme(t){
  currentTheme=t;
  document.documentElement.setAttribute('data-theme',t==='classic'?'':t);
  // Clear any inline custom CSS vars when switching themes
  const root=document.documentElement;
  ['--bg','--surface','--gold','--gold-dim','--gold-light','--cream',
   '--free','--free-border','--free-text','--occupied','--occupied-border','--occupied-text'].forEach(v=>{
    root.style.removeProperty(v);
  });
  THEMES.forEach(n=>{
    const sw=document.getElementById('sw-'+n);
    if(sw)sw.classList.toggle('active',n===t);
  });
  // Sync color pickers to current computed values
  setTimeout(syncColorPickers,50);
  save();
}

// ══════════════════════════
// Color Editor
// ══════════════════════════
function applyCustomColor(varName, value){
  document.documentElement.style.setProperty(varName, value);
}

function shiftColor(hex, amount){
  // Ensure valid 6-char hex
  hex = hex.replace('#','');
  if(hex.length===3) hex=hex[0]+hex[0]+hex[1]+hex[1]+hex[2]+hex[2];
  if(hex.length!==6) return '#888888';
  let r=parseInt(hex.slice(0,2),16),g=parseInt(hex.slice(2,4),16),b=parseInt(hex.slice(4,6),16);
  r=Math.max(0,Math.min(255,r+amount));
  g=Math.max(0,Math.min(255,g+amount));
  b=Math.max(0,Math.min(255,b+amount));
  return '#'+[r,g,b].map(x=>x.toString(16).padStart(2,'0')).join('');
}

function getCSSVar(name){
  return getComputedStyle(document.documentElement).getPropertyValue(name).trim();
}

function cssColorToHex(color){
  if(!color) return '#888888';
  color = color.trim();
  if(color.startsWith('#') && color.length===7) return color;
  if(color.startsWith('#') && color.length===4)
    return '#'+color[1]+color[1]+color[2]+color[2]+color[3]+color[3];
  const tmp=document.createElement('div');
  tmp.style.color=color;
  document.body.appendChild(tmp);
  const computed=getComputedStyle(tmp).color;
  document.body.removeChild(tmp);
  const m=computed.match(/\d+/g);
  if(!m||m.length<3) return '#888888';
  return '#'+m.slice(0,3).map(n=>parseInt(n).toString(16).padStart(2,'0')).join('');
}

function syncColorPickers(){
  const map={
    'ce-bg':'--bg','ce-surface':'--surface','ce-accent':'--gold',
    'ce-text':'--cream','ce-free':'--free-border','ce-occ':'--occupied-border'
  };
  Object.entries(map).forEach(([id,varName])=>{
    const el=document.getElementById(id);
    if(el) el.value=cssColorToHex(getCSSVar(varName));
  });
  // Header font: read from logo-text computed color
  const logoText=document.querySelector('.logo-text');
  const hfEl=document.getElementById('ce-header-font');
  if(hfEl&&logoText) hfEl.value=cssColorToHex(getComputedStyle(logoText).color);
  // Logo: read stored hex or derive from current filter (fallback to gold)
  const logoEl=document.getElementById('ce-logo');
  if(logoEl) logoEl.value=customLogoHex||cssColorToHex(getCSSVar('--gold'));
}

// Header font color — uses a CSS var --header-font-color if set, else --gold
let customHeaderFontHex='';
let customLogoHex='';

function setHeaderFontColor(hex){
  customHeaderFontHex=hex;
  document.documentElement.style.setProperty('--header-font-color', hex);
  // Apply to logo-text and logo-text span
  document.querySelectorAll('.logo-text,.logo-text span').forEach(el=>{
    el.style.color=hex;
  });
  // Also stat vals, clock etc use --cream — leave those to body text picker
}

function setLogoColor(hex){
  customLogoHex=hex;
  const img=document.querySelector('.logo-img');
  if(!img) return;
  // Convert hex to an SVG filter approximation — use a wrapper SVG filter trick
  // We convert the hex to RGB then build a colorMatrix filter
  const r=parseInt(hex.slice(1,3),16)/255;
  const g=parseInt(hex.slice(3,5),16)/255;
  const b=parseInt(hex.slice(5,7),16)/255;
  // formula: make image black then colorize: each channel = target * alpha
  img.style.filter=`brightness(0) saturate(100%) `+
    `invert(1) sepia(1) saturate(10) `+
    // approximate hue by using drop-shadow trick isn't ideal; use color-matrix approach:
    // Actually the cleanest approach: set to a known filter for the computed color
    // We'll compute hue-rotate from the hex color
    buildLogoFilter(hex);
}

function buildLogoFilter(hex){
  // Convert hex to HSL to get hue for hue-rotate
  const r=parseInt(hex.slice(1,3),16)/255;
  const g=parseInt(hex.slice(3,5),16)/255;
  const b=parseInt(hex.slice(5,7),16)/255;
  const max=Math.max(r,g,b),min=Math.min(r,g,b);
  let h=0,s=0,l=(max+min)/2;
  if(max!==min){
    const d=max-min;
    s=l>0.5?d/(2-max-min):d/(max+min);
    switch(max){
      case r:h=((g-b)/d+(g<b?6:0))/6;break;
      case g:h=((b-r)/d+2)/6;break;
      case b:h=((r-g)/d+4)/6;break;
    }
  }
  const hDeg=Math.round(h*360);
  const sBright=Math.round(s*100+50);
  const bright=Math.round(l*120+40);
  // Start from white logo (brightness(0) makes it black, then invert makes white)
  // Then sepia+saturate+hue-rotate gets us close to the target hue
  return `brightness(0) saturate(100%) invert(1) sepia(1) saturate(${sBright}%) hue-rotate(${hDeg}deg) brightness(${bright}%)`;
}

function getCurrentCustomColors(){
  // Snapshot all current CSS variable inline styles + custom overrides
  const vars=['--bg','--surface','--surface2','--border',
    '--gold','--gold-dim','--gold-light','--cream','--cream-dim',
    '--free','--free-border','--free-text',
    '--occupied','--occupied-border','--occupied-text',
    '--warning','--warning-border','--warning-text',
    '--danger','--danger-border','--danger-text'];
  const snapshot={};
  vars.forEach(v=>{
    const val=document.documentElement.style.getPropertyValue(v);
    if(val) snapshot[v]=val;
    else snapshot[v]=getCSSVar(v); // use computed
  });
  return snapshot;
}

// ── Saved custom themes ──────────────────────────────────
const CUSTOM_THEMES_KEY='cl_custom_themes_v1';
let customThemes=[]; // [{name,colors,headerFont,logoHex,baseTheme}]

function loadCustomThemes(){
  try{
    customThemes=JSON.parse(localStorage.getItem(CUSTOM_THEMES_KEY)||'[]');
  }catch(e){customThemes=[];}
  renderSavedThemesList();
}

function saveCurrentTheme(){
  const nameEl=document.getElementById('newThemeName');
  const name=(nameEl.value||'').trim();
  if(!name){nameEl.focus();return;}
  const entry={
    name,
    baseTheme:currentTheme,
    colors:getCurrentCustomColors(),
    headerFont:customHeaderFontHex,
    logoHex:customLogoHex
  };
  // Remove duplicate name if exists
  customThemes=customThemes.filter(t=>t.name!==name);
  customThemes.push(entry);
  try{localStorage.setItem(CUSTOM_THEMES_KEY,JSON.stringify(customThemes));}catch(e){}
  nameEl.value='';
  renderSavedThemesList();
}

function applyCustomTheme(idx){
  const t=customThemes[idx];
  if(!t) return;
  // First apply the base theme to reset
  document.documentElement.setAttribute('data-theme',t.baseTheme==='classic'?'':t.baseTheme);
  THEMES.forEach(n=>{
    const sw=document.getElementById('sw-'+n);
    if(sw) sw.classList.toggle('active',n===t.baseTheme);
  });
  // Then apply all custom color overrides
  const root=document.documentElement;
  Object.entries(t.colors).forEach(([k,v])=>{root.style.setProperty(k,v);});
  // Header font
  if(t.headerFont){
    customHeaderFontHex=t.headerFont;
    document.querySelectorAll('.logo-text,.logo-text span').forEach(el=>{el.style.color=t.headerFont;});
  }
  // Logo
  if(t.logoHex){
    customLogoHex=t.logoHex;
    const img=document.querySelector('.logo-img');
    if(img) img.style.filter=buildLogoFilter(t.logoHex);
  }
  setTimeout(syncColorPickers,50);
}

function deleteCustomTheme(idx){
  customThemes.splice(idx,1);
  try{localStorage.setItem(CUSTOM_THEMES_KEY,JSON.stringify(customThemes));}catch(e){}
  renderSavedThemesList();
}

function renderSavedThemesList(){
  const el=document.getElementById('savedThemesList');
  if(!el) return;
  if(!customThemes.length){
    el.innerHTML=`<div style="font-size:9px;color:var(--cream-dim);padding:4px 0;font-style:italic;">No saved themes yet</div>`;
    return;
  }
  el.innerHTML=customThemes.map((t,i)=>{
    // Swatch background: approximate from saved bg + surface colors
    const bg=t.colors['--bg']||'#111';
    const surf=t.colors['--surface']||'#222';
    const gold=t.colors['--gold']||'#888';
    return `<div class="custom-theme-row">
      <div class="custom-swatch" onclick="applyCustomTheme(${i})"
        style="background:linear-gradient(135deg,${bg} 50%,${surf} 50%);border-color:${gold}"></div>
      <span class="custom-theme-name" onclick="applyCustomTheme(${i})">${esc(t.name)}</span>
      <button class="custom-theme-del" onclick="deleteCustomTheme(${i})" title="Delete">✕</button>
    </div>`;
  }).join('');
}

function resetCustomColors(){
  const root=document.documentElement;
  ['--bg','--surface','--surface2','--border',
   '--gold','--gold-dim','--gold-light','--cream','--cream-dim',
   '--free','--free-border','--free-text',
   '--occupied','--occupied-border','--occupied-text'].forEach(v=>{
    root.style.removeProperty(v);
  });
  customHeaderFontHex='';customLogoHex='';
  // Reset header font and logo to CSS-driven defaults
  document.querySelectorAll('.logo-text,.logo-text span').forEach(el=>{el.style.color='';});
  const img=document.querySelector('.logo-img');
  if(img) img.style.filter='';
  setTimeout(syncColorPickers,50);
}

// ══════════════════════════
// Init
// ══════════════════════════
function init(){
  if(!load())buildTables(15,5);
  setTheme(currentTheme);
  setLang(lang);
  switchMode(currentMode);
  setSideTab(currentSideTab);
  renderGrid();renderFloor();renderGuestList();updateStats();startClock();
  loadCustomThemes();
  setTimeout(syncColorPickers,120);
  setInterval(tick,1000);
}

function getDefLimit(){return parseInt(document.getElementById('defaultLimit').value)||90;}

function buildTables(n,c){
  const lim=getDefLimit();
  const sp=[2,4,4,6,2,4,4,2,6,4,4,2,4,6,2,4,4,6,4,2];
  tables=Array.from({length:n},(_,i)=>({id:i+1,occupied:false,startTime:null,guest:'',room:'',limitMin:lim,seats:sp[i%20],fx:null,fy:null,fw:90,fh:75}));
  cols=c;
}

function applyGridSettings(){
  const nc=parseInt(document.getElementById('tableCount').value)||15;
  const ng=parseInt(document.getElementById('colCount').value)||5;
  const lim=getDefLimit();
  while(tables.length<nc){const id=tables.length+1;tables.push({id,occupied:false,startTime:null,guest:'',room:'',limitMin:lim,seats:4,fx:null,fy:null,fw:90,fh:75});}
  if(tables.length>nc)tables=tables.slice(0,nc);
  cols=ng;
  if(selectedId&&selectedId>nc)selectedId=null;
  autoPlace();renderGrid();renderFloor();renderGuestList();updateStats();save();
}

// ══════════════════════════
// Sidebar tabs
// ══════════════════════════
function setSideTab(tab){
  currentSideTab=tab;
  ['detail','guests','settings'].forEach(t=>{
    document.getElementById('stab-'+t).classList.toggle('active',t===tab);
    document.getElementById('tab-'+t).style.display=t===tab?'block':'none';
  });
  if(tab==='detail')renderDetail();
  if(tab==='guests')renderGuestList();
}

function openSettings(){
  setSideTab('settings');
  // scroll to settings section
  setTimeout(()=>{
    const scroll=document.getElementById('sidebarScroll');
    scroll.scrollTo({top:scroll.scrollHeight,behavior:'smooth'});
  },50);
}

// ══════════════════════════
// Accordion sections
// ══════════════════════════
function toggleSection(id){
  const body=document.getElementById(id);
  const arrow=document.getElementById('arrow-'+id);
  const open=body.classList.toggle('open');
  if(arrow)arrow.classList.toggle('open',open);
}

// ══════════════════════════
// Mode switch
// ══════════════════════════
function switchMode(m){
  currentMode=m;
  document.getElementById('gridViewport').style.display=m==='grid'?'flex':'none';
  document.getElementById('floorViewport').style.display=m==='floor'?'flex':'none';
  document.getElementById('tabGrid').classList.toggle('active',m==='grid');
  document.getElementById('tabFloor').classList.toggle('active',m==='floor');
  document.getElementById('floorHint').textContent=editMode?s('hintEdit'):s('hintView');
  save();
}

// ══════════════════════════
// Grid render
// ══════════════════════════
function renderGrid(){
  const g=document.getElementById('tableGrid');
  g.style.gridTemplateColumns=`repeat(${cols},1fr)`;
  g.innerHTML='';
  tables.forEach(t=>{
    const el=document.createElement('div');
    el.className='table-card '+tClass(t);el.id='tcard-'+t.id;
    el.innerHTML=cardHTML(t);el.onclick=()=>selectTable(t.id);
    g.appendChild(el);
  });
}

function cardHTML(t){
  const e=t.occupied?getElapsed(t):0;
  const g=(t.guest||t.room)?`<div class="table-guest">${[t.guest,t.room?'#'+t.room:''].filter(Boolean).join(' · ')}</div>`:'';
  return `<div class="table-seats-badge">${t.seats}p</div>
    <div class="table-num">${t.id}</div>
    <div class="table-status">${t.occupied?s('occupied'):s('available')}</div>
    ${t.occupied?`<div class="table-timer">${fmt(e)}</div>`:''}${g}`;
}

function updateCard(t){
  const el=document.getElementById('tcard-'+t.id);if(!el)return;
  el.className='table-card '+tClass(t);el.innerHTML=cardHTML(t);el.onclick=()=>selectTable(t.id);
}

function tClass(t){
  if(!t.occupied)return'free';
  const e=getElapsed(t),l=t.limitMin*60;
  return e>=l?'danger-time':e>=l*0.8?'warning':'occupied';
}

// ══════════════════════════
// Floor plan
// ══════════════════════════
function autoPlace(){
  const vp=document.getElementById('floorViewport');
  const W=Math.max(vp?vp.clientWidth:800,600);
  const H=Math.max(vp?vp.clientHeight:600,400);
  const PAD=20,TW=100,TH=80,GAP=12;
  const pr=Math.max(1,Math.floor((W-PAD*2)/(TW+GAP)));
  tables.forEach((t,i)=>{
    if(t.fx===null||t.fy===null){
      t.fx=PAD+(i%pr)*(TW+GAP);
      t.fy=PAD+Math.floor(i/pr)*(TH+GAP);
      t.fw=TW;t.fh=TH;
    }
  });
  // Size canvas to contain all tokens
  if(tables.length){
    const maxX=Math.max(...tables.map(t=>t.fx+t.fw))+PAD;
    const maxY=Math.max(...tables.map(t=>t.fy+t.fh))+PAD;
    const cvs=document.getElementById('floorCanvas');
    cvs.style.width=Math.max(W,maxX)+'px';
    cvs.style.height=Math.max(H,maxY)+'px';
  }
}

function renderFloor(){
  const cvs=document.getElementById('floorCanvas');
  cvs.querySelectorAll('.floor-table').forEach(e=>e.remove());
  autoPlace();
  tables.forEach(t=>cvs.appendChild(makeToken(t)));
  document.getElementById('floorEditBar').style.display=editMode?'flex':'none';
  document.getElementById('floorHint').textContent=editMode?s('hintEdit'):s('hintView');
}

function makeToken(t){
  const el=document.createElement('div');
  el.className='floor-table '+tClass(t)+(floorSelId===t.id?' selected-token':'');
  el.id='ftok-'+t.id;
  el.style.cssText=`left:${t.fx}px;top:${t.fy}px;width:${t.fw}px;height:${t.fh}px;`;
  el.innerHTML=tokInner(t);
  if(editMode){
    makeDraggable(el,t);makeResizable(el.querySelector('.resize-handle'),t,el);
    el.addEventListener('click',e=>{e.stopPropagation();floorSelect(t.id);});
  }else{
    el.style.cursor='pointer';
    el.addEventListener('click',e=>{e.stopPropagation();selectTable(t.id);});
  }
  return el;
}

function tokInner(t){
  const e=t.occupied?getElapsed(t):0;
  const g=(t.guest||t.room)?`<div class="ft-guest">${[t.guest,t.room?'#'+t.room:''].filter(Boolean).join(' · ')}</div>`:'';
  const rh=editMode?`<div class="resize-handle"><svg width="8" height="8" viewBox="0 0 8 8"><path d="M1 7L7 1M4 7L7 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/></svg></div>`:'';
  return `<div class="ft-seats">${t.seats}p</div><div class="ft-num">${t.id}</div>
    ${t.occupied?`<div class="ft-timer">${fmt(e)}</div>`:''}${g}${rh}`;
}

function refreshToken(t){
  const el=document.getElementById('ftok-'+t.id);if(!el)return;
  el.className='floor-table '+tClass(t)+(floorSelId===t.id?' selected-token':'');
  el.style.cssText=`left:${t.fx}px;top:${t.fy}px;width:${t.fw}px;height:${t.fh}px;`;
  el.innerHTML=tokInner(t);
  if(editMode){makeDraggable(el,t);makeResizable(el.querySelector('.resize-handle'),t,el);el.onclick=e=>{e.stopPropagation();floorSelect(t.id);};}
  else{el.style.cursor='pointer';el.onclick=e=>{e.stopPropagation();selectTable(t.id);};}
}

function makeDraggable(el,t){
  let sx,sy,sl,st,on=false;
  function dn(e){if(e.target.closest('.resize-handle'))return;e.stopPropagation();e.preventDefault();on=true;const p=e.touches?e.touches[0]:e;sx=p.clientX;sy=p.clientY;sl=t.fx;st=t.fy;window.addEventListener('mousemove',mv);window.addEventListener('mouseup',up);window.addEventListener('touchmove',mv,{passive:false});window.addEventListener('touchend',up);}
  function mv(e){if(!on)return;e.preventDefault();const p=e.touches?e.touches[0]:e;const r=document.getElementById('floorCanvas').getBoundingClientRect();t.fx=Math.max(0,Math.min(r.width-t.fw,sl+p.clientX-sx));t.fy=Math.max(0,Math.min(r.height-t.fh,st+p.clientY-sy));el.style.left=t.fx+'px';el.style.top=t.fy+'px';}
  function up(){on=false;window.removeEventListener('mousemove',mv);window.removeEventListener('mouseup',up);window.removeEventListener('touchmove',mv);window.removeEventListener('touchend',up);save();}
  el.addEventListener('mousedown',dn);el.addEventListener('touchstart',dn,{passive:false});
}

function makeResizable(handle,t,el){
  if(!handle)return;
  let sx,sy,sw,sh,on=false;
  function dn(e){e.stopPropagation();e.preventDefault();on=true;const p=e.touches?e.touches[0]:e;sx=p.clientX;sy=p.clientY;sw=t.fw;sh=t.fh;window.addEventListener('mousemove',mv);window.addEventListener('mouseup',up);window.addEventListener('touchmove',mv,{passive:false});window.addEventListener('touchend',up);}
  function mv(e){if(!on)return;e.preventDefault();const p=e.touches?e.touches[0]:e;t.fw=Math.max(65,sw+p.clientX-sx);t.fh=Math.max(55,sh+p.clientY-sy);el.style.width=t.fw+'px';el.style.height=t.fh+'px';}
  function up(){on=false;window.removeEventListener('mousemove',mv);window.removeEventListener('mouseup',up);window.removeEventListener('touchmove',mv);window.removeEventListener('touchend',up);save();}
  handle.addEventListener('mousedown',dn);handle.addEventListener('touchstart',dn,{passive:false});
}

function floorSelect(id){
  floorSelId=id;
  document.querySelectorAll('.floor-table').forEach(e=>e.classList.remove('selected-token'));
  const el=document.getElementById('ftok-'+id);if(el)el.classList.add('selected-token');
  updateDeleteBtns();selectedId=id;renderDetail();
  if(currentSideTab!=='detail')setSideTab('detail');
}

function updateDeleteBtns(){
  const show=editMode&&floorSelId?'inline-block':'none';
  document.getElementById('btnDeleteTable').style.display=show;
  document.getElementById('btnDeleteTable2').style.display=show;
}

function toggleEditMode(){
  editMode=!editMode;
  const btn=document.getElementById('btnEditMode');
  btn.textContent=editMode?s('editOn'):s('editOff');
  btn.className='btn '+(editMode?'edit-active':'');
  const showExtra=editMode?'flex':'none';
  document.getElementById('floorEditBtns').style.display=showExtra;
  document.getElementById('floorSnapRow').style.display=editMode?'flex':'none';
  if(editMode&&currentMode!=='floor')switchMode('floor');
  floorSelId=null;renderFloor();updateDeleteBtns();
  document.getElementById('floorHint').textContent=editMode?s('hintEdit'):s('hintView');
}

function addFloorTable(){
  const vp=document.getElementById('floorViewport');
  const z=zoomState['floor'];
  // Place new table at center of current viewport view, accounting for zoom/pan
  const vw=(vp?vp.clientWidth:800),vh=(vp?vp.clientHeight:600);
  const cx=(vw/2-z.tx)/z.scale,cy=(vh/2-z.ty)/z.scale;
  const id=tables.length?Math.max(...tables.map(t=>t.id))+1:1;
  tables.push({id,occupied:false,startTime:null,guest:'',room:'',limitMin:getDefLimit(),seats:4,fx:cx-45,fy:cy-38,fw:90,fh:75});
  document.getElementById('tableCount').value=tables.length;
  renderFloor();renderGrid();renderGuestList();updateStats();save();
}

function deleteSelectedTable(){
  if(!floorSelId)return;
  if(!confirm(`Delete Table ${floorSelId}?`))return;
  tables=tables.filter(t=>t.id!==floorSelId);
  if(selectedId===floorSelId){selectedId=null;renderDetail();}
  floorSelId=null;updateDeleteBtns();
  document.getElementById('tableCount').value=tables.length;
  renderFloor();renderGrid();renderGuestList();updateStats();save();
}

function snapAllToGrid(){
  const G=40;tables.forEach(t=>{t.fx=Math.round(t.fx/G)*G;t.fy=Math.round(t.fy/G)*G;});
  renderFloor();save();
}

document.getElementById('floorCanvas').addEventListener('click',()=>{
  if(editMode&&floorSelId){floorSelId=null;document.querySelectorAll('.floor-table').forEach(e=>e.classList.remove('selected-token'));updateDeleteBtns();}
});

// ══════════════════════════
// Guest list
// ══════════════════════════
function renderGuestList(){
  const el=document.getElementById('guestList');
  const occupied=tables.filter(t=>t.occupied).sort((a,b)=>a.startTime-b.startTime);
  if(!occupied.length){el.innerHTML=`<div class="guest-empty">${s('noGuests')}</div>`;return;}
  el.innerHTML=occupied.map(t=>{
    const e=getElapsed(t),l=t.limitMin*60,cls=tClass(t);
    const tc=cls==='danger-time'?'over':cls==='warning'?'warn':'';
    const dotColor=cls==='danger-time'?'var(--danger-text)':cls==='warning'?'var(--warning-text)':'var(--occupied-text)';
    const name=t.guest||'—';
    const room=t.room?`#${t.room}`:'';
    return `<div class="guest-row" onclick="selectTable(${t.id});setSideTab('detail')">
      <div class="guest-tnum">${t.id}</div>
      <div class="guest-info">
        <div class="guest-name">${esc(name)}</div>
        <div class="guest-room">${esc(room)}</div>
      </div>
      <div class="guest-timer ${tc}">${fmt(e)}</div>
      <div class="guest-status-dot" style="background:${dotColor}"></div>
    </div>`;
  }).join('');
}

// ══════════════════════════
// Detail panel
// ══════════════════════════
function selectTable(id){selectedId=id;if(currentSideTab==='detail')renderDetail();}

function renderDetail(){
  const panel=document.getElementById('detailPanel');
  if(!selectedId){panel.innerHTML=`<div class="detail-empty" id="emptyMsg" style="color:var(--cream-dim);font-size:14px;text-align:center;padding:36px 10px;font-style:italic;font-family:'Cormorant Garamond',serif;line-height:1.9;">${s('emptyMsg')}</div>`;return;}
  const t=tables.find(x=>x.id===selectedId);
  if(!t){panel.innerHTML=`<div style="color:var(--cream-dim);font-size:12px;padding:20px;text-align:center;">${s('emptyMsg')}</div>`;return;}
  const el=t.occupied?getElapsed(t):0;
  const lim=t.limitMin*60,pct=t.occupied?Math.min(100,(el/lim)*100):0;
  const cls=tClass(t),tc=cls==='danger-time'?'over':cls==='warning'?'warn':'';
  const bc=cls==='free'?'badge-free':cls==='occupied'?'badge-occupied':cls==='warning'?'badge-warning':'badge-danger';
  const bl=cls==='free'?s('available'):cls==='occupied'?s('occupied'):cls==='warning'?s('nearLimitBadge'):s('overLimitBadge');
  const bar=cls==='danger-time'?'#e03030':cls==='warning'?'#d4a020':'#e07040';

  let h=`<div class="detail-table-num">T${t.id}</div><div class="detail-badge ${bc}">${bl}</div>`;
  if(t.occupied)h+=`<div class="seated-at">${s('seatedAt')} ${fmtTs(t.startTime)}</div>
    <div class="timer-display ${tc}" id="detail-timer">${fmt(el)}</div>
    <div class="time-bar"><div class="time-bar-fill" id="detail-bar" style="width:${pct}%;background:${bar}"></div></div>`;
  h+=`<div class="field-group"><div class="field-label">${s('guestName')}</div>
    <input class="field-input" value="${esc(t.guest)}" placeholder="${s('guestName')}…" oninput="fld('guest',this.value)"></div>
    <div class="field-group"><div class="field-label">${s('roomNumber')}</div>
    <input class="field-input" value="${esc(t.room)}" placeholder="${s('roomNumber')}…" oninput="fld('room',this.value)"></div>
    <div class="field-row field-group">
      <div><div class="field-label">${s('seats')}</div>
        <input class="field-input" type="number" value="${t.seats}" min="1" max="20" oninput="fld('seats',parseInt(this.value)||2)"></div>
      <div><div class="field-label">${s('timeLimit')}</div>
        <input class="field-input" type="number" value="${t.limitMin}" min="5" max="480" oninput="fld('limitMin',parseInt(this.value)||60)"></div>
    </div>
    <div class="action-row">${!t.occupied
      ?`<button class="btn gold" onclick="seatTable(${t.id})">${s('seatGuests')}</button>`
      :`<button class="btn danger" onclick="showRelease(${t.id})">${s('releaseTable')}</button>`}
    </div>`;
  panel.innerHTML=h;
}

function fld(field,val){
  const t=tables.find(x=>x.id===selectedId);if(!t)return;
  t[field]=val;updateCard(t);refreshToken(t);renderGuestList();save();
}

function seatTable(id){
  const t=tables.find(x=>x.id===id);if(!t)return;
  t.occupied=true;t.startTime=Date.now();
  updateCard(t);refreshToken(t);updateStats();renderDetail();renderGuestList();save();
}

function showRelease(id){
  pendingReleaseId=id;
  document.getElementById('releaseTableNum').textContent='Table '+id;
  document.getElementById('releaseModal').classList.add('open');
}
function closeModal(){document.getElementById('releaseModal').classList.remove('open');pendingReleaseId=null;}
function confirmRelease(){
  if(!pendingReleaseId)return;
  const t=tables.find(x=>x.id===pendingReleaseId);
  if(t){t.occupied=false;t.startTime=null;t.guest='';t.room='';updateCard(t);refreshToken(t);updateStats();if(selectedId===pendingReleaseId)renderDetail();renderGuestList();}
  closeModal();save();
}

// ══════════════════════════
// Tick
// ══════════════════════════
function tick(){
  tables.forEach(t=>{if(t.occupied){updateCard(t);refreshToken(t);}});
  updateDetailTimer();
  if(currentSideTab==='guests')renderGuestList();
  updateStats();save();
}

function updateDetailTimer(){
  if(!selectedId)return;
  const t=tables.find(x=>x.id===selectedId);if(!t||!t.occupied)return;
  const el=getElapsed(t),lim=t.limitMin*60,pct=Math.min(100,(el/lim)*100);
  const cls=tClass(t),tc=cls==='danger-time'?'over':cls==='warning'?'warn':'';
  const bar=cls==='danger-time'?'#e03030':cls==='warning'?'#d4a020':'#e07040';
  const te=document.getElementById('detail-timer'),be=document.getElementById('detail-bar');
  if(te){te.textContent=fmt(el);te.className='timer-display '+tc;}
  if(be){be.style.width=pct+'%';be.style.background=bar;}
}

function updateStats(){
  const o=tables.filter(t=>t.occupied).length;
  document.getElementById('statFree').textContent=tables.length-o;
  document.getElementById('statOccupied').textContent=o;
  document.getElementById('statTotal').textContent=tables.length;
}

// ══════════════════════════
// Clock
// ══════════════════════════
function startClock(){
  const upd=()=>document.getElementById('clock').textContent=new Date().toLocaleTimeString(lang==='ja'?'ja-JP':'en-GB');
  upd();setInterval(upd,1000);
}

// ══════════════════════════
// Helpers
// ══════════════════════════
function getElapsed(t){return Math.floor((Date.now()-t.startTime)/1000);}
function fmt(sec){const h=Math.floor(sec/3600),m=Math.floor((sec%3600)/60),sc=sec%60;return h>0?`${h}:${p2(m)}:${p2(sc)}`:`${p2(m)}:${p2(sc)}`;}
function p2(n){return String(n).padStart(2,'0');}
function fmtTs(ts){if(!ts)return'—';return new Date(ts).toLocaleTimeString(lang==='ja'?'ja-JP':'en-GB',{hour:'2-digit',minute:'2-digit'});}
function esc(v){return(v||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');}

// ══════════════════════════
// Pinch / Zoom
// ══════════════════════════
const zoomState={
  grid:{scale:1,tx:0,ty:0},
  floor:{scale:1,tx:0,ty:0}
};
const ZOOM_MIN=0.3,ZOOM_MAX=4;

function getZoomEls(view){
  if(view==='grid') return{inner:document.getElementById('gridZoomInner'),vp:document.getElementById('gridViewport'),lbl:document.getElementById('gridZoomLabel')};
  return{inner:document.getElementById('floorZoomInner'),vp:document.getElementById('floorViewport'),lbl:document.getElementById('floorZoomLabel')};
}

function applyZoom(view){
  const z=zoomState[view];
  const{inner,lbl}=getZoomEls(view);
  inner.style.transform=`translate(${z.tx}px,${z.ty}px) scale(${z.scale})`;
  if(lbl) lbl.textContent=Math.round(z.scale*100)+'%';
  updateDragCursor(view);
  // On grid: when at 1x with no pan, restore native overflow scroll
  if(view==='grid'){
    const vp=document.getElementById('gridViewport');
    const isNeutral=(z.scale===1&&z.tx===0&&z.ty===0);
    vp.classList.toggle('zoomed',!isNeutral);
  }
}

function updateDragCursor(view){
  const{vp}=getZoomEls(view);
  // Show grab cursor when content is larger than viewport (i.e. can be panned)
  const z=zoomState[view];
  const canPan=z.scale>1||z.tx!==0||z.ty!==0;
  vp.classList.toggle('can-drag',canPan);
}

function clampTranslation(view){
  // keep content from being dragged completely off screen
  const z=zoomState[view];
  const{vp,inner}=getZoomEls(view);
  const vw=vp.clientWidth,vh=vp.clientHeight;
  const iw=inner.scrollWidth*z.scale,ih=inner.scrollHeight*z.scale;
  const maxTx=vw*0.8,minTx=vw-iw-vw*0.8;
  const maxTy=vh*0.8,minTy=vh-ih-vh*0.8;
  z.tx=Math.min(maxTx,Math.max(minTx,z.tx));
  z.ty=Math.min(maxTy,Math.max(minTy,z.ty));
}

function adjustZoom(view,delta){
  const z=zoomState[view];
  const{vp}=getZoomEls(view);
  const prev=z.scale;
  z.scale=Math.min(ZOOM_MAX,Math.max(ZOOM_MIN,z.scale+delta));
  // zoom toward center of viewport
  const cx=vp.clientWidth/2,cy=vp.clientHeight/2;
  const ratio=z.scale/prev;
  z.tx=cx-(cx-z.tx)*ratio;
  z.ty=cy-(cy-z.ty)*ratio;
  clampTranslation(view);
  applyZoom(view);
}

function resetZoom(view){
  zoomState[view]={scale:1,tx:0,ty:0};
  applyZoom(view);
}

function initPinchZoom(view){
  const{vp}=getZoomEls(view);

  // ── Pinch ──
  let touches={},pinchDist0=0,pinchScale0=1,pinchTx0=0,pinchTy0=0,pinchCx=0,pinchCy=0;
  let panStart=null,panTx0=0,panTy0=0,isPinching=false;

  function dist(t1,t2){return Math.hypot(t2.clientX-t1.clientX,t2.clientY-t1.clientY);}
  function midpoint(t1,t2){return{x:(t1.clientX+t2.clientX)/2,y:(t1.clientY+t2.clientY)/2};}

  vp.addEventListener('touchstart',e=>{
    Array.from(e.changedTouches).forEach(t=>{touches[t.identifier]=t;});
    const tc=Object.values(touches);
    if(tc.length===2){
      isPinching=true;
      const z=zoomState[view];
      pinchDist0=dist(tc[0],tc[1]);
      pinchScale0=z.scale;pinchTx0=z.tx;pinchTy0=z.ty;
      const mid=midpoint(tc[0],tc[1]);
      const r=vp.getBoundingClientRect();
      pinchCx=mid.x-r.left;pinchCy=mid.y-r.top;
    } else if(tc.length===1&&!isPinching){
      const r=vp.getBoundingClientRect();
      const z=zoomState[view];
      panStart={x:tc[0].clientX-r.left,y:tc[0].clientY-r.top};
      panTx0=z.tx;panTy0=z.ty;
    }
  },{passive:true});

  vp.addEventListener('touchmove',e=>{
    Array.from(e.changedTouches).forEach(t=>{touches[t.identifier]=t;});
    const tc=Object.values(touches);
    const z=zoomState[view];
    if(tc.length===2&&isPinching){
      e.preventDefault();
      const d=dist(tc[0],tc[1]);
      const newScale=Math.min(ZOOM_MAX,Math.max(ZOOM_MIN,pinchScale0*(d/pinchDist0)));
      const ratio=newScale/pinchScale0;
      z.scale=newScale;
      z.tx=pinchCx-(pinchCx-pinchTx0)*ratio;
      z.ty=pinchCy-(pinchCy-pinchTy0)*ratio;
      clampTranslation(view);applyZoom(view);
    } else if(tc.length===1&&panStart&&!isPinching){
      const r=vp.getBoundingClientRect();
      const cx=tc[0].clientX-r.left,cy=tc[0].clientY-r.top;
      z.tx=panTx0+(cx-panStart.x);
      z.ty=panTy0+(cy-panStart.y);
      clampTranslation(view);applyZoom(view);
    }
  },{passive:false});

  vp.addEventListener('touchend',e=>{
    Array.from(e.changedTouches).forEach(t=>{delete touches[t.identifier];});
    if(Object.values(touches).length<2)isPinching=false;
    if(Object.values(touches).length===0)panStart=null;
  });

  // ── Mouse wheel → normal scroll (no zoom) ──
  // gridView scrolls naturally via overflow-y:auto; floor plan: allow default scroll
  // No wheel listener needed — just let it scroll naturally.

  // ── Desktop mouse drag-to-pan ──
  // On grid at 1x (not zoomed), don't intercept mousedown so native scroll works
  let mousePanStart=null,mousePanTx0=0,mousePanTy0=0,mouseDragging=false;

  vp.addEventListener('mousedown',e=>{
    // only pan on left-click on the viewport background (not on table cards/buttons)
    if(e.button!==0)return;
    if(e.target.closest('.floor-table,.table-card,.btn,.zoom-btn,.zoom-level,.legend-overlay,.floor-edit-bar,.floor-hint,.resize-handle'))return;
    // On grid at 1x neutral, don't intercept (let native scroll work)
    const z=zoomState[view];
    if(view==='grid'&&z.scale===1&&z.tx===0&&z.ty===0)return;
    const zz=zoomState[view];
    mousePanStart={x:e.clientX,y:e.clientY};
    mousePanTx0=zz.tx;mousePanTy0=zz.ty;
    mouseDragging=false;
    vp.classList.add('dragging');
    window.addEventListener('mousemove',onMouseMove);
    window.addEventListener('mouseup',onMouseUp);
  });

  function onMouseMove(e){
    if(!mousePanStart)return;
    const dx=e.clientX-mousePanStart.x,dy=e.clientY-mousePanStart.y;
    if(!mouseDragging&&(Math.abs(dx)>3||Math.abs(dy)>3))mouseDragging=true;
    if(!mouseDragging)return;
    const z=zoomState[view];
    z.tx=mousePanTx0+dx;z.ty=mousePanTy0+dy;
    clampTranslation(view);applyZoom(view);
  }

  function onMouseUp(){
    mousePanStart=null;mouseDragging=false;
    vp.classList.remove('dragging');
    window.removeEventListener('mousemove',onMouseMove);
    window.removeEventListener('mouseup',onMouseUp);
  }

  // Show grab cursor only when zoomed in enough to be pannable
  updateDragCursor(view);
}

init();
initPinchZoom('grid');
initPinchZoom('floor');

// ── Keyboard +/- zoom ──
document.addEventListener('keydown',e=>{
  // Don't fire when typing in an input
  if(e.target.tagName==='INPUT'||e.target.tagName==='TEXTAREA')return;
  const view=currentMode; // 'grid' or 'floor'
  if(e.key==='+'||e.key==='='||e.key==='NumpadAdd'){
    e.preventDefault();adjustZoom(view,0.2);
  } else if(e.key==='-'||e.key==='_'||e.key==='NumpadSubtract'){
    e.preventDefault();adjustZoom(view,-0.2);
  } else if(e.key==='0'||e.key==='Numpad0'){
    e.preventDefault();resetZoom(view);
  }
});</script>
</body>
</html>
