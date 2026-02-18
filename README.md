index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kozi Desert — Master Growth Playbook 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Playfair+Display:ital@0;1&family=DM+Mono:wght@300;400;500&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
--bg:#080C12;--bg2:#0C1018;--bg3:#10161E;--bg4:#141C26;--bg5:#18222E;
--accent:#5B9BD5;--accent2:#7BB8F0;--accent-dim:#0F2035;
--cream:#E8F0F8;--muted:#4A6080;--muted2:#6A84A8;--border:#1A2638;--border2:#243450;
--green:#4A9E78;--red:#C4604A;--gold:#C9A96E;
--phase1:#3A6EA8;--phase2:#5B9BD5;--phase3:#7BB8F0;--phase4:#A8D4FF;
--safety:#4A9E78;--balanced:#C9A96E;--aggressive:#C4604A;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--cream);font-family:'DM Sans',sans-serif;font-weight:300;line-height:1.6;overflow-x:hidden;transition:background 0.4s,color 0.4s}
body::after{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E");pointer-events:none;z-index:9999}

nav{position:fixed;top:0;left:0;right:0;z-index:500;background:rgba(8,12,18,0.95);backdrop-filter:blur(16px);border-bottom:1px solid var(--border);height:52px;display:flex;align-items:center;justify-content:space-between;padding:0 28px}
.nav-brand{font-family:'Bebas Neue',sans-serif;font-size:18px;letter-spacing:0.12em;color:var(--accent)}
.nav-center{display:flex;gap:2px;list-style:none}
.nav-center a{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.12em;text-transform:uppercase;color:var(--muted2);text-decoration:none;padding:5px 8px;transition:color 0.2s;white-space:nowrap}
.nav-center a:hover{color:var(--accent)}
@media(max-width:900px){.nav-center{display:none}}
.nav-right{display:flex;align-items:center;gap:6px;margin-left:12px}
.theme-dot{width:18px;height:18px;border-radius:50%;border:2px solid var(--border2);cursor:pointer;transition:border-color 0.2s;flex-shrink:0}
.theme-dot:hover,.theme-dot.on{border-color:var(--accent2)}
.td-blue{background:#080C12}.td-sand{background:#0A0908}.td-slate{background:#0D0F14}

.wrap{max-width:1080px;margin:0 auto;padding:0 32px}
.section{max-width:1080px;margin:0 auto;padding:0 32px 80px}
.sec-label{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.25em;color:var(--accent);text-transform:uppercase;margin-bottom:8px}
.sec-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(30px,5vw,54px);letter-spacing:0.04em;line-height:1;margin-bottom:36px;color:var(--cream)}

/* HERO */
.hero{padding:130px 32px 70px;max-width:1080px;margin:0 auto;opacity:0;animation:fadeUp 0.9s ease 0.1s forwards}
.hero-eyebrow{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.25em;color:var(--accent);text-transform:uppercase;margin-bottom:20px;display:flex;align-items:center;gap:12px}
.hero-eyebrow::after{content:'';display:block;height:1px;width:60px;background:var(--accent);opacity:0.4}
.hero h1{font-family:'Bebas Neue',sans-serif;font-size:clamp(52px,9vw,120px);line-height:0.88;letter-spacing:0.02em;margin-bottom:28px}
.hero h1 em{font-style:italic;font-family:'Playfair Display',serif;color:var(--accent);font-size:0.78em}
.hero-sub{font-size:15px;color:var(--muted2);max-width:520px;line-height:1.8;font-weight:300;margin-bottom:36px}
.pills{display:flex;gap:10px;flex-wrap:wrap}
.pill{background:var(--bg4);border:1px solid var(--border2);padding:9px 18px;font-family:'DM Mono',monospace;font-size:11px;letter-spacing:0.1em;color:var(--muted2);text-transform:uppercase}
.pill span{color:var(--accent)}

/* CARDS generic */
.card{background:var(--bg2);border:1px solid var(--border);padding:22px 24px;position:relative;overflow:hidden}
.card-label{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.18em;text-transform:uppercase;color:var(--muted);margin-bottom:6px}
.card-val{font-family:'Bebas Neue',sans-serif;font-size:38px;letter-spacing:0.02em;line-height:1;color:var(--accent);margin-bottom:4px}
.card-sub{font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:0.06em}

/* GRID helpers */
.g2{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
@media(max-width:700px){.g2,.g3,.g4{grid-template-columns:1fr}}
@media(max-width:900px){.g4{grid-template-columns:repeat(2,1fr)}}

/* TIMELINE */
.timeline{position:relative;margin-bottom:0}
.timeline::before{content:'';position:absolute;left:20px;top:0;bottom:0;width:1px;background:linear-gradient(to bottom,var(--accent),transparent)}
.phase{position:relative;padding-left:56px;margin-bottom:4px;opacity:0;transform:translateX(-20px);transition:opacity 0.6s,transform 0.6s}
.phase.vis{opacity:1;transform:translateX(0)}
.phase-dot{position:absolute;left:12px;top:28px;width:16px;height:16px;border-radius:50%;border:2px solid var(--accent);background:var(--bg);z-index:2}
.phase-dot::after{content:'';position:absolute;inset:3px;border-radius:50%;background:var(--accent)}
.phase-card{background:var(--bg2);border:1px solid var(--border);padding:26px 30px;margin-bottom:3px;cursor:pointer;transition:border-color 0.3s;position:relative;overflow:hidden}
.phase-card:hover{border-color:var(--border2)}
.phase-card::before{content:'';position:absolute;left:0;top:0;bottom:0;width:3px}
.ph1 .phase-card::before{background:var(--phase1)}
.ph2 .phase-card::before{background:var(--phase2)}
.ph3 .phase-card::before{background:var(--phase3)}
.ph4 .phase-card::before{background:var(--phase4)}
.ph-header{display:flex;align-items:flex-start;justify-content:space-between;gap:20px;flex-wrap:wrap}
.ph-num{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.2em;text-transform:uppercase;color:var(--muted);margin-bottom:4px}
.ph-name{font-family:'Bebas Neue',sans-serif;font-size:28px;letter-spacing:0.04em;line-height:1;margin-bottom:6px}
.ph1 .ph-name{color:var(--phase1)}.ph2 .ph-name{color:var(--phase2)}.ph3 .ph-name{color:var(--phase3)}.ph4 .ph-name{color:var(--phase4)}
.ph-period{font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:0.1em}
.ph-stats{display:flex;gap:20px;flex-wrap:wrap}
.st{text-align:right}
.st-v{font-family:'Bebas Neue',sans-serif;font-size:26px;line-height:1;letter-spacing:0.02em}
.ph1 .st-v{color:var(--phase1)}.ph2 .st-v{color:var(--phase2)}.ph3 .st-v{color:var(--phase3)}.ph4 .st-v{color:var(--phase4)}
.st-l{font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);letter-spacing:0.1em;text-transform:uppercase}
.ph-toggle{font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:0.15em;text-transform:uppercase;margin-top:14px;display:flex;align-items:center;gap:8px;user-select:none}
.arr{display:inline-block;transition:transform 0.3s}.arr.open{transform:rotate(180deg)}
.ph-body{max-height:0;overflow:hidden;transition:max-height 0.6s ease,padding 0.3s}
.ph-body.open{max-height:3000px;padding-top:22px}
.ph-div{height:1px;background:var(--border);margin-bottom:22px}
.ph-cols{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-bottom:18px}
@media(max-width:700px){.ph-cols{grid-template-columns:1fr}}
.pc{background:var(--bg3);border:1px solid var(--border);padding:16px 18px}
.ct{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.2em;text-transform:uppercase;color:var(--accent);margin-bottom:10px;padding-bottom:8px;border-bottom:1px solid var(--border)}
.ci{font-size:13px;font-weight:300;color:var(--muted2);line-height:1.7;margin-bottom:7px;padding-left:12px;position:relative}
.ci::before{content:'—';position:absolute;left:0;color:var(--muted);font-family:'DM Mono',monospace;font-size:10px}
.ci strong{color:var(--cream);font-weight:400}
.cg2{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;margin-bottom:18px}
@media(max-width:600px){.cg2{grid-template-columns:1fr}}
.cb{background:var(--bg4);border:1px solid var(--border);padding:14px 18px;position:relative}
.cb::after{content:attr(data-type);position:absolute;top:10px;right:12px;font-family:'DM Mono',monospace;font-size:8px;letter-spacing:0.15em;text-transform:uppercase;color:var(--muted)}
.cn{font-family:'DM Mono',monospace;font-size:11px;color:var(--accent);letter-spacing:0.1em;margin-bottom:5px;text-transform:uppercase}
.cd{font-size:12px;color:var(--muted2);line-height:1.7;font-weight:300}
.cd strong{color:var(--cream);font-weight:400}
.brief{background:var(--bg3);border:1px solid var(--border);padding:18px 22px;margin-bottom:14px}
.bt{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.2em;text-transform:uppercase;color:var(--accent);margin-bottom:12px}
.br{display:flex;gap:14px;margin-bottom:7px;align-items:flex-start}
.bk{font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:0.08em;min-width:76px;text-transform:uppercase;padding-top:2px}
.bv{font-size:13px;color:var(--muted2);font-weight:300;line-height:1.6}
.bv strong{color:var(--cream);font-weight:400}
.bb-wrap{margin-bottom:18px}
.bb-lbl{display:flex;justify-content:space-between;font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:0.1em;margin-bottom:5px;text-transform:uppercase}
.bb-lbl span{color:var(--accent)}
.bb{height:4px;background:var(--bg5);border-radius:2px;overflow:hidden;margin-bottom:3px}
.bbf{height:100%;border-radius:2px;background:linear-gradient(to right,var(--phase1),var(--accent2));transform-origin:left;transform:scaleX(0);transition:transform 0.8s ease}
.bbf.go{transform:scaleX(1)}

/* IMAGE ADS SECTION */
.img-ad-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-bottom:24px}
@media(max-width:600px){.img-ad-grid{grid-template-columns:1fr}}
.img-ad-card{background:var(--bg2);border:1px solid var(--border);padding:20px 22px;border-left:3px solid var(--accent)}
.img-ad-title{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.15em;text-transform:uppercase;color:var(--accent);margin-bottom:8px}
.img-ad-body{font-size:13px;color:var(--muted2);line-height:1.8;font-weight:300}
.img-ad-body strong{color:var(--cream);font-weight:400}

/* REVENUE PROJECTION */
.rev-tabs{display:flex;gap:6px;margin-bottom:24px;flex-wrap:wrap}
.rtab{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.12em;text-transform:uppercase;padding:7px 16px;border:1px solid var(--border);background:transparent;color:var(--muted);cursor:pointer;transition:all 0.2s}
.rtab.safety.on,.rtab.safety:hover{border-color:var(--safety);color:var(--safety);background:rgba(74,158,120,0.1)}
.rtab.balanced.on,.rtab.balanced:hover{border-color:var(--balanced);color:var(--balanced);background:rgba(201,169,110,0.1)}
.rtab.aggressive.on,.rtab.aggressive:hover{border-color:var(--aggressive);color:var(--aggressive);background:rgba(196,96,74,0.1)}
.rtab.all.on,.rtab.all:hover{border-color:var(--accent);color:var(--accent);background:rgba(91,155,213,0.1)}
.rev-summary{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:28px}
@media(max-width:600px){.rev-summary{grid-template-columns:1fr}}
.rsc{background:var(--bg2);border:1px solid var(--border);padding:20px 22px;position:relative}
.rsc::before{content:'';position:absolute;top:0;left:0;right:0;height:2px}
.rsc.safety::before{background:var(--safety)}.rsc.balanced::before{background:var(--balanced)}.rsc.aggressive::before{background:var(--aggressive)}
.rsc-name{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.18em;text-transform:uppercase;margin-bottom:4px}
.rsc.safety .rsc-name{color:var(--safety)}.rsc.balanced .rsc-name{color:var(--balanced)}.rsc.aggressive .rsc-name{color:var(--aggressive)}
.rsc-val{font-family:'Bebas Neue',sans-serif;font-size:36px;line-height:1;letter-spacing:0.02em;margin-bottom:4px}
.rsc.safety .rsc-val{color:var(--safety)}.rsc.balanced .rsc-val{color:var(--balanced)}.rsc.aggressive .rsc-val{color:var(--aggressive)}
.rsc-meta{font-family:'DM Mono',monospace;font-size:10px;color:var(--muted);line-height:1.7}
.rsc-meta span{color:var(--cream)}
.chart-area{background:var(--bg2);border:1px solid var(--border);padding:28px 20px 20px;margin-bottom:24px;position:relative}
.chart-lbl{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.18em;text-transform:uppercase;color:var(--muted);margin-bottom:22px}
.chart-inner{position:relative;height:260px;padding-left:48px;padding-bottom:26px}
.chart-grid{position:absolute;inset:0 0 26px 48px;display:flex;flex-direction:column;justify-content:space-between;pointer-events:none}
.cg-line{width:100%;height:1px;background:var(--border);position:relative}
.cg-line-lbl{position:absolute;right:calc(100% + 52px);top:-8px;font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);white-space:nowrap}
.chart-svg{position:absolute;inset:0 0 26px 48px;width:calc(100% - 48px);height:calc(100% - 26px);overflow:visible}
.x-lbls{position:absolute;bottom:0;left:48px;right:0;display:flex;justify-content:space-between}
.xl{font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);letter-spacing:0.08em;text-transform:uppercase;flex:1;text-align:center}
.tip{position:absolute;background:var(--bg4);border:1px solid var(--border);padding:10px 14px;font-family:'DM Mono',monospace;font-size:11px;pointer-events:none;opacity:0;transition:opacity 0.15s;z-index:50;min-width:170px}
.tip.show{opacity:1}
.tip-mo{color:var(--muted);font-size:9px;letter-spacing:0.15em;text-transform:uppercase;margin-bottom:6px}
.tip-row{display:flex;justify-content:space-between;gap:14px;margin-bottom:3px;font-size:11px}
.ts{color:var(--safety)}.tb{color:var(--balanced)}.ta{color:var(--aggressive)}
.anim-path{stroke-dasharray:3000;stroke-dashoffset:3000;animation:draw 2s ease forwards}
@keyframes draw{to{stroke-dashoffset:0}}

/* REV TABLE */
.rev-table-wrap{overflow-x:auto}
table{width:100%;border-collapse:collapse;font-family:'DM Mono',monospace;font-size:11px}
thead tr{background:var(--bg4)}
thead th{padding:10px 14px;text-align:left;font-size:9px;letter-spacing:0.15em;color:var(--muted);font-weight:400;text-transform:uppercase;border:1px solid var(--border);border-top:none}
tbody tr{transition:background 0.2s}
tbody tr:hover{background:var(--bg3)}
tbody td{padding:9px 14px;border:1px solid var(--border);border-top:none;letter-spacing:0.04em;color:var(--muted2)}
td.mo{color:var(--muted);font-size:9px;letter-spacing:0.12em;text-transform:uppercase}
td.ts2{color:var(--safety)}td.tb2{color:var(--balanced)}td.ta2{color:var(--aggressive)}
.tot-row{background:var(--bg4)!important}
.tot-row td{border-top:1px solid var(--accent)!important;font-size:13px}

/* STORE CHECKLIST */
.checklist-cats{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:24px}
@media(max-width:700px){.checklist-cats{grid-template-columns:1fr}}
.chk-cat{background:var(--bg2);border:1px solid var(--border);padding:20px 22px}
.chk-cat-title{font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.2em;text-transform:uppercase;margin-bottom:14px;padding-bottom:8px;border-bottom:1px solid var(--border)}
.chk-cat.crit .chk-cat-title{color:var(--aggressive)}
.chk-cat.imp .chk-cat-title{color:var(--balanced)}
.chk-cat.growth .chk-cat-title{color:var(--safety)}
.chk-item{display:flex;align-items:flex-start;gap:10px;margin-bottom:9px;cursor:pointer}
.chk-box{width:16px;height:16px;border:1px solid var(--border2);flex-shrink:0;margin-top:2px;display:flex;align-items:center;justify-content:center;transition:all 0.2s}
.chk-item.done .chk-box{background:var(--accent);border-color:var(--accent)}
.chk-item.done .chk-box::after{content:'✓';color:#fff;font-size:10px;font-weight:700}
.chk-item.done .chk-txt{text-decoration:line-through;color:var(--muted)}
.chk-txt{font-size:12px;color:var(--muted2);font-weight:300;line-height:1.5}
.chk-txt strong{color:var(--cream);font-weight:400}

/* EMAIL FLOWS */
.email-flows{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:32px}
@media(max-width:700px){.email-flows{grid-template-columns:1fr}}
.fc{background:var(--bg2);border:1px solid var(--border);padding:20px;position:relative}
.fc-num{font-family:'Bebas Neue',sans-serif;font-size:46px;color:var(--bg4);position:absolute;top:10px;right:14px;line-height:1;user-select:none}
.fc-name{font-family:'DM Mono',monospace;font-size:10px;color:var(--accent);letter-spacing:0.15em;text-transform:uppercase;margin-bottom:8px}
.fc-trig{font-size:10px;color:var(--muted);font-family:'DM Mono',monospace;letter-spacing:0.05em;margin-bottom:10px;padding:4px 8px;background:var(--bg4);display:inline-block}
.fc-steps{list-style:none;margin-top:8px}
.fc-step{font-size:12px;color:var(--muted2);padding:5px 0;border-bottom:1px solid var(--border);display:flex;gap:10px;align-items:flex-start;font-weight:300}
.fc-step:last-child{border-bottom:none}
.st-time{font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);letter-spacing:0.08em;min-width:44px;padding-top:2px}

/* CONTENT CALENDAR */
.cal{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;margin-bottom:22px}
@media(max-width:600px){.cal{grid-template-columns:repeat(3,1fr)}}
.cal-day{background:var(--bg3);border:1px solid var(--border);padding:10px 8px;text-align:center}
.cal-dn{font-family:'DM Mono',monospace;font-size:8px;color:var(--muted);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:5px}
.cal-type{font-size:11px;color:var(--cream);font-weight:300;line-height:1.4}
.cal-plat{font-family:'DM Mono',monospace;font-size:8px;color:var(--accent);margin-top:4px;letter-spacing:0.05em}

/* SCALING RULES */
.rules{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-bottom:32px}
@media(max-width:600px){.rules{grid-template-columns:1fr}}
.rule{background:var(--bg2);border:1px solid var(--border);padding:22px 24px}
.rule-icon{font-size:26px;margin-bottom:8px;display:block}
.rule-title{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.15em;color:var(--accent);text-transform:uppercase;margin-bottom:8px}
.rule-body{font-size:13px;color:var(--muted2);line-height:1.8;font-weight:300}
.rule-body strong{color:var(--cream);font-weight:400}
.rule-trig{margin-top:10px;padding:8px 12px;background:var(--bg4);border-left:2px solid var(--accent);font-family:'DM Mono',monospace;font-size:10px;color:var(--muted2);letter-spacing:0.05em;line-height:1.6}
.rule-trig strong{color:var(--accent)}

/* KPI */
.kpi-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:32px}
@media(max-width:700px){.kpi-grid{grid-template-columns:repeat(2,1fr)}}
.kpi{background:var(--bg2);border:1px solid var(--border);padding:18px 20px;text-align:center}
.kpi-lbl{font-family:'DM Mono',monospace;font-size:8px;letter-spacing:0.18em;text-transform:uppercase;color:var(--muted);margin-bottom:7px}
.kpi-val{font-family:'Bebas Neue',sans-serif;font-size:30px;letter-spacing:0.02em;color:var(--accent);line-height:1;margin-bottom:4px}
.kpi-desc{font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);letter-spacing:0.05em}

/* AI OPTIMIZATION */
.ai-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-bottom:32px}
@media(max-width:600px){.ai-grid{grid-template-columns:1fr}}
.ai-card{background:var(--bg2);border:1px solid var(--border);padding:22px 24px}
.ai-card-title{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:0.15em;text-transform:uppercase;color:var(--accent2);margin-bottom:10px}
.ai-card-body{font-size:13px;color:var(--muted2);line-height:1.8;font-weight:300}
.ai-card-body strong{color:var(--cream);font-weight:400}
.ai-tag{display:inline-block;font-family:'DM Mono',monospace;font-size:9px;letter-spacing:0.1em;text-transform:uppercase;padding:3px 8px;background:var(--accent-dim);color:var(--accent2);margin-top:8px;margin-right:4px}

/* RESOURCES */
.res-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-bottom:32px}
@media(max-width:700px){.res-grid{grid-template-columns:1fr}}
.res-card{background:var(--bg2);border:1px solid var(--border);padding:20px 22px;text-decoration:none;display:block;transition:border-color 0.2s,background 0.2s;cursor:pointer}
.res-card:hover{border-color:var(--border2);background:var(--bg3)}
.res-cat{font-family:'DM Mono',monospace;font-size:8px;letter-spacing:0.2em;text-transform:uppercase;color:var(--accent);margin-bottom:6px}
.res-title{font-size:14px;color:var(--cream);font-weight:400;margin-bottom:6px;line-height:1.4}
.res-desc{font-size:12px;color:var(--muted);font-weight:300;line-height:1.6}
.res-link{font-family:'DM Mono',monospace;font-size:9px;color:var(--accent2);letter-spacing:0.08em;margin-top:10px;display:block}

/* FOOTER */
footer{border-top:1px solid var(--border);padding:32px;max-width:1080px;margin:0 auto;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:14px}
.foot-brand{font-family:'Bebas Neue',sans-serif;font-size:20px;letter-spacing:0.1em;color:var(--accent)}
.foot-note{font-family:'DM Mono',monospace;font-size:9px;color:var(--muted);letter-spacing:0.1em;text-transform:uppercase}
.info-box{background:var(--bg2);border:1px solid var(--border);border-left:3px solid var(--accent);padding:22px 26px;margin-bottom:32px}
.info-box p{font-size:14px;color:var(--muted2);line-height:1.9;font-weight:300;max-width:740px}
.info-box p strong{color:var(--cream);font-weight:400}

@keyframes fadeUp{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:translateY(0)}}
.fade-s{opacity:0;transform:translateY(18px);transition:opacity 0.7s,transform 0.7s}
.fade-s.vis{opacity:1;transform:translateY(0)}
::-webkit-scrollbar{width:5px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:3px}
</style>
</head>
<body>

<nav>
  <div class="nav-brand">KOZIDESERT</div>
  <ul class="nav-center">
    <li><a href="#phases">Phases</a></li>
    <li><a href="#image-ads">Image Ads</a></li>
    <li><a href="#revenue">Revenue</a></li>
    <li><a href="#store">Store</a></li>
    <li><a href="#email">Email</a></li>
    <li><a href="#content">Content</a></li>
    <li><a href="#scaling">Scaling</a></li>
    <li><a href="#ai">AI Optimization</a></li>
    <li><a href="#resources">Resources</a></li>
  </ul>
  <div class="nav-right">
    <div class="theme-dot td-blue on" onclick="setTheme('blue')" title="Blue"></div>
    <div class="theme-dot td-sand" onclick="setTheme('sand')" title="Sand"></div>
    <div class="theme-dot td-slate" onclick="setTheme('slate')" title="Slate"></div>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-eyebrow">2026 Master Growth Playbook</div>
  <h1>THE KOZI<br><em>Master</em><br>PLAYBOOK</h1>
  <p class="hero-sub">Everything in one place. Meta campaign strategy, image ad playbook, store optimization checklist, email flows, compounding revenue projections, AI search optimization, and learning resources — built specifically for Kozi Desert.</p>
  <div class="pills">
    <div class="pill">Start Budget: <span>$500/mo</span></div>
    <div class="pill">Method: <span>Balanced Compound</span></div>
    <div class="pill">Creative: <span>Image Ads (Phase 1)</span></div>
    <div class="pill">Target ROAS: <span>2x → 3.5x</span></div>
    <div class="pill">Projected Year: <span>$28K–$36K</span></div>
  </div>
</div>

<!-- PHASES -->
<div class="section" id="phases">
  <div class="sec-label">Campaign Structure</div>
  <div class="sec-title">THE 4 PHASES</div>
  <div class="timeline">

    <!-- PH1 -->
    <div class="phase ph1" id="ph1">
      <div class="phase-dot"></div>
      <div class="phase-card" onclick="tp('pb1','a1')">
        <div class="ph-header">
          <div>
            <div class="ph-num">Phase 01</div>
            <div class="ph-name">IGNITION</div>
            <div class="ph-period">Feb – Mar 2026 · Months 1–2</div>
          </div>
          <div class="ph-stats">
            <div class="st"><div class="st-v">$500</div><div class="st-l">Mo. Spend</div></div>
            <div class="st"><div class="st-v">0.8%</div><div class="st-l">Target CVR</div></div>
            <div class="st"><div class="st-v">1.5x</div><div class="st-l">Target ROAS</div></div>
          </div>
        </div>
        <div class="ph-toggle"><span>View full strategy</span><span class="arr" id="a1">↓</span></div>
        <div class="ph-body" id="pb1">
          <div class="ph-div"></div>
          <div class="ph-cols">
            <div class="pc"><div class="ct">Objective</div>
              <div class="ci"><strong>Pixel training.</strong> You need 50+ purchase events before Meta's algo can optimize. Every sale teaches it who your buyer is.</div>
              <div class="ci"><strong>Audience building.</strong> Build 1,000+ warm website visitors to retarget in Phase 2.</div>
              <div class="ci"><strong>First sales.</strong> Even 3–5 orders gives you data on which products convert cold.</div>
            </div>
            <div class="pc"><div class="ct">Hero Products</div>
              <div class="ci"><strong>Oasis Heavyweight Crew ($80)</strong> — lowest friction price, unisex, broadest appeal. Lead product.</div>
              <div class="ci"><strong>Kozi Core Hoodie ($75)</strong> — second ad set, test alongside Oasis.</div>
              <div class="ci"><strong>Canyon Vest ($97)</strong> — only if above perform. Don't spread budget thin in Phase 1.</div>
            </div>
            <div class="pc"><div class="ct">Audience Targeting</div>
              <div class="ci"><strong>Broad (18–34, US/CA/UK)</strong> — Let Advantage+ find buyers. Don't over-restrict.</div>
              <div class="ci">Interests: <strong>Aime Leon Dore, Reigning Champ, Carhartt WIP, Noah NYC, Kith</strong></div>
              <div class="ci">Behavior: <strong>Online shoppers, engaged with fashion brands in past 30 days</strong></div>
              <div class="ci">Exclude: <strong>existing customers</strong> from cold campaigns.</div>
            </div>
          </div>
          <div class="cg2">
            <div class="cb" data-type="Cold Traffic"><div class="cn">Campaign 1 — Traffic</div><div class="cd"><strong>Budget:</strong> $10/day · <strong>Format:</strong> Static image 4:5<br>Lead with your best on-body lifestyle shot. Show the Oasis Crew worn in a minimal desert-tone setting. Clean, premium, thumb-stopping.<br><strong>CTA:</strong> "Shop the Drop" → Product page</div></div>
            <div class="cb" data-type="Conversion"><div class="cn">Campaign 2 — Catalogue Sales</div><div class="cd"><strong>Budget:</strong> $6/day · <strong>Format:</strong> Advantage+ Catalogue<br>Auto-serves your products to likely buyers. Connect Shopify → Meta Sales Channel first. Let the algorithm pick the product.<br><strong>CTA:</strong> "Shop Now"</div></div>
            <div class="cb" data-type="Retargeting"><div class="cn">Campaign 3 — Retargeting</div><div class="cd"><strong>Budget:</strong> $0 Month 1 → $4/day Month 2<br>Starts empty. By Week 3 you have 200–400 site visitors. Hit them with a lifestyle image + 30% off hook. Different creative than cold.<br><strong>Audience:</strong> Website visitors 0–30 days</div></div>
            <div class="cb" data-type="Email Capture"><div class="cn">Campaign 4 — Lead Gen</div><div class="cd"><strong>Budget:</strong> $0 Month 1 → $3/day Month 2<br>Meta Lead Ad — email in exchange for 30% off. Feeds Klaviyo directly. This audience converts 3–5x better than cold traffic once warmed via email sequence.<br><strong>CTA:</strong> "Unlock 30% Off"</div></div>
          </div>
          <div class="brief">
            <div class="bt">Phase 1 Image Ad Creative Brief</div>
            <div class="br"><div class="bk">Format</div><div class="bv"><strong>4:5 portrait</strong> for feed. <strong>9:16</strong> for stories/reels placement. Shoot on iPhone — authenticity works in streetwear.</div></div>
            <div class="br"><div class="bk">Shot 1</div><div class="bv">On-body lifestyle — person wearing the Oasis Crew outdoors, warm desert tones, natural light. Not posed. Moving or candid.</div></div>
            <div class="br"><div class="bk">Shot 2</div><div class="bv">Close-up fabric texture — the 400gsm weight looks premium on camera. Show the drape and density.</div></div>
            <div class="br"><div class="bk">Shot 3</div><div class="bv">Full outfit shot on clean/concrete surface or minimal urban background. Walking away from camera works well.</div></div>
            <div class="br"><div class="bk">Golden Hr</div><div class="bv">Shoot at golden hour — warm light = free brand photography that matches the Kozi Desert aesthetic perfectly.</div></div>
            <div class="br"><div class="bk">Text</div><div class="bv">Minimal. Headline only: <strong>"OASIS CREW — $80 · KOZIDESERT.COM"</strong> Bottom of frame. Clean white text.</div></div>
            <div class="br"><div class="bk">Copy</div><div class="bv">First line = value prop immediately: <strong>"400gsm French terry. Built to outlast your wardrobe rotation."</strong> Don't bury the hook.</div></div>
            <div class="br"><div class="bk">Variants</div><div class="bv">Make <strong>3 image variants</strong> per ad set with different hero shots. Kill weakest 2 by Day 5. Scale the winner.</div></div>
          </div>
          <div class="bb-wrap">
            <div class="bb-lbl">Budget Split — Phase 1 ($500/mo · $16.60/day) <span></span></div>
            <div class="bb-lbl" style="font-size:9px">Traffic + Catalogue <span>60% — $300</span></div>
            <div class="bb"><div class="bbf" style="width:60%"></div></div>
            <div class="bb-lbl" style="font-size:9px">Retargeting + Lead Gen (from Month 2) <span>25% — $125</span></div>
            <div class="bb"><div class="bbf" style="width:25%"></div></div>
            <div class="bb-lbl" style="font-size:9px">Creative Testing Buffer <span>15% — $75</span></div>
            <div class="bb"><div class="bbf" style="width:15%"></div></div>
          </div>
        </div>
      </div>
    </div>

    <!-- PH2 -->
    <div class="phase ph2">
      <div class="phase-dot"></div>
      <div class="phase-card" onclick="tp('pb2','a2')">
        <div class="ph-header">
          <div><div class="ph-num">Phase 02</div><div class="ph-name">MOMENTUM</div><div class="ph-period">Apr – Jun 2026 · Months 3–5</div></div>
          <div class="ph-stats">
            <div class="st"><div class="st-v">$700</div><div class="st-l">Mo. Spend</div></div>
            <div class="st"><div class="st-v">1.8%</div><div class="st-l">Target CVR</div></div>
            <div class="st"><div class="st-v">2.2x</div><div class="st-l">Target ROAS</div></div>
          </div>
        </div>
        <div class="ph-toggle"><span>View full strategy</span><span class="arr" id="a2">↓</span></div>
        <div class="ph-body" id="pb2">
          <div class="ph-div"></div>
          <div class="ph-cols">
            <div class="pc"><div class="ct">What Changes</div>
              <div class="ci">Switch main campaign from <strong>Traffic → Purchase objective.</strong> Pixel now has enough data.</div>
              <div class="ci"><strong>Lookalike audiences</strong> available once you hit 100+ buyers. Create 1% LAL from purchasers.</div>
              <div class="ci">Email revenue starts contributing. <strong>Factor email into total ROAS</strong> — it's not free, factor Klaviyo cost.</div>
            </div>
            <div class="pc"><div class="ct">New Campaigns</div>
              <div class="ci"><strong>Lookalike Campaign (1%)</strong> — best performing once pixel trained. Budget: $200/mo.</div>
              <div class="ci"><strong>UGC/Review Ads</strong> — any customer photos run as ads. Converts 40% better than studio content.</div>
              <div class="ci"><strong>Cross-sell retargeting</strong> — buyers of Oasis Crew get served Nomad Bomber or Outline Zip.</div>
            </div>
            <div class="pc"><div class="ct">Creative Strategy Shift</div>
              <div class="ci"><strong>Add video if possible</strong> — even 15-sec iPhone clip of someone putting on the piece. Reels-style.</div>
              <div class="ci"><strong>Flat lay with context</strong> — concrete floor, sand, rough textures. Intentional styling around the piece.</div>
              <div class="ci"><strong>Refresh Phase 1 winners</strong> — same image, different headline copy. New angle, same visual.</div>
            </div>
          </div>
          <div class="bb-wrap">
            <div class="bb-lbl">Budget Split — Phase 2 (~$700/mo) <span></span></div>
            <div class="bb-lbl" style="font-size:9px">Lookalike (1%) Purchase Campaign <span>35% — $245</span></div>
            <div class="bb"><div class="bbf" style="width:35%"></div></div>
            <div class="bb-lbl" style="font-size:9px">Cold Traffic / Catalogue <span>30% — $210</span></div>
            <div class="bb"><div class="bbf" style="width:30%"></div></div>
            <div class="bb-lbl" style="font-size:9px">Retargeting 7d + 30d <span>25% — $175</span></div>
            <div class="bb"><div class="bbf" style="width:25%"></div></div>
            <div class="bb-lbl" style="font-size:9px">Lead Gen (email growth) <span>10% — $70</span></div>
            <div class="bb"><div class="bbf" style="width:10%"></div></div>
          </div>
        </div>
      </div>
    </div>

    <!-- PH3 -->
    <div class="phase ph3">
      <div class="phase-dot"></div>
      <div class="phase-card" onclick="tp('pb3','a3')">
        <div class="ph-header">
          <div><div class="ph-num">Phase 03</div><div class="ph-name">SCALE</div><div class="ph-period">Jul – Sep 2026 · Months 6–8</div></div>
          <div class="ph-stats">
            <div class="st"><div class="st-v">$1,200</div><div class="st-l">Mo. Spend</div></div>
            <div class="st"><div class="st-v">2.5%</div><div class="st-l">Target CVR</div></div>
            <div class="st"><div class="st-v">2.8x</div><div class="st-l">Target ROAS</div></div>
          </div>
        </div>
        <div class="ph-toggle"><span>View full strategy</span><span class="arr" id="a3">↓</span></div>
        <div class="ph-body" id="pb3">
          <div class="ph-div"></div>
          <div class="ph-cols">
            <div class="pc"><div class="ct">Horizontal Scaling</div>
              <div class="ci">Don't raise budget on existing sets — <strong>duplicate winners</strong> into new ad sets with slightly different audiences. Avoids saturation.</div>
              <div class="ci">Expand LAL: <strong>1% → 2% → 3%</strong> lookalikes from buyer list.</div>
              <div class="ci">Open new markets — <strong>Australia, Germany, Netherlands</strong> all have strong streetwear demand and lower CPMs than US.</div>
            </div>
            <div class="pc"><div class="ct">Vertical Scaling</div>
              <div class="ci">Raise budget on winning sets by <strong>max 20% every 3–4 days.</strong> Larger jumps reset learning.</div>
              <div class="ci">ROAS holds above 2.5x for 7 days → scale 20%. Drops below 1.8x for 3 days → cut 20%.</div>
              <div class="ci">Set <strong>automated rules</strong> in Meta: pause sets spending $15+ with 0 purchases in 24h.</div>
            </div>
            <div class="pc"><div class="ct">New Revenue Levers</div>
              <div class="ci"><strong>Influencer seeding</strong> — 2–3 pieces to micro-influencers (5K–50K) in streetwear/minimal fashion. No payment, just product. Use content as ads.</div>
              <div class="ci"><strong>Bundle offers</strong> — Crew + Pants bundle increases AOV from $110 → $160+.</div>
              <div class="ci"><strong>SMS marketing</strong> — Postscript or SMSBump. SMS converts at 8–12% vs email's 2–4%.</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- PH4 -->
    <div class="phase ph4">
      <div class="phase-dot"></div>
      <div class="phase-card" onclick="tp('pb4','a4')">
        <div class="ph-header">
          <div><div class="ph-num">Phase 04</div><div class="ph-name">PEAK SEASON</div><div class="ph-period">Oct – Dec 2026 · Months 9–11</div></div>
          <div class="ph-stats">
            <div class="st"><div class="st-v">$2,000+</div><div class="st-l">Mo. Spend</div></div>
            <div class="st"><div class="st-v">3.0%</div><div class="st-l">Target CVR</div></div>
            <div class="st"><div class="st-v">3.5x</div><div class="st-l">Target ROAS</div></div>
          </div>
        </div>
        <div class="ph-toggle"><span>View full strategy</span><span class="arr" id="a4">↓</span></div>
        <div class="ph-body" id="pb4">
          <div class="ph-div"></div>
          <div class="ph-cols">
            <div class="pc"><div class="ct">Q4 Is Everything</div>
              <div class="ci">Oct–Dec = <strong>30–40% of annual revenue</strong> for fashion brands. Higher CPMs, but conversion rates are at their peak.</div>
              <div class="ci"><strong>Start Q4 prep in September</strong> — stockpile creatives, build email segments, plan BFCM offer now.</div>
              <div class="ci">Your email list built over 8 months is your <strong>most valuable asset</strong> — free to send, highest converting.</div>
            </div>
            <div class="pc"><div class="ct">BFCM Strategy</div>
              <div class="ci"><strong>Black Friday:</strong> 25–30% sitewide. Email to list at midnight. Run ads Nov 20 – Dec 2.</div>
              <div class="ci"><strong>Don't discount hero items</strong> — offer bundles or free shipping instead. Protects brand equity.</div>
              <div class="ci"><strong>Gift messaging from Dec 1–20.</strong> Target gift-buyers not just fashion fans — different creative, different copy angle.</div>
            </div>
            <div class="pc"><div class="ct">Ad Strategy Q4</div>
              <div class="ci"><strong>Double best ad sets only</strong> — Q4 is not the time for creative testing. Run what's proven from Phase 2–3.</div>
              <div class="ci"><strong>Retargeting budget → 40%</strong> of total. Warm audience converts 5–8% in Q4 because purchase intent peaks.</div>
              <div class="ci"><strong>Set daily budget cap</strong> — Meta spends aggressively in Q4. Cap at 2x normal daily to control costs.</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- IMAGE ADS -->
<div class="section fade-s" id="image-ads">
  <div class="sec-label">Current Creative Constraint</div>
  <div class="sec-title">IMAGE AD STRATEGY</div>
  <div class="info-box" style="margin-bottom:24px">
    <p><strong>Image ads can absolutely scale a fashion brand.</strong> The gap between image and video closes significantly with the right creative. For premium streetwear specifically, a well-shot image often outperforms a mediocre video. The key is understanding that your ad image and your product page image serve different jobs — one stops a scroll, the other closes a sale.</p>
  </div>
  <div class="img-ad-grid">
    <div class="img-ad-card">
      <div class="img-ad-title">On-Body Lifestyle Shots</div>
      <div class="img-ad-body">Your best performer. <strong>Person wearing the piece in a real environment</strong> — dry landscape, minimal urban, natural light. Not posed. Candid or walking. The desert/nomad aesthetic gives you a strong visual identity that stands out in a feed full of white-background studio shots. Shoot golden hour for that warm, on-brand tone.</div>
    </div>
    <div class="img-ad-card">
      <div class="img-ad-title">Fabric Texture Close-Ups</div>
      <div class="img-ad-body"><strong>400gsm shows on camera</strong> — the weight and density of your French terry is a selling point. A cropped, close-up shot of the fabric texture communicates premium quality without a single word. Pair with a simple overlay: <strong>"400gsm. Built different."</strong> This works especially well for knits and heavyweight pieces.</div>
    </div>
    <div class="img-ad-card">
      <div class="img-ad-title">Contextual Flat Lay</div>
      <div class="img-ad-body">Never on a bed or table. <strong>Concrete floor, sand surface, rough stone</strong> — textures that match the Kozi Desert world. The piece folded or laid intentionally with minimal props (a worn watch, sunglasses, nothing cheap). This works for introducing new products before lifestyle content is shot.</div>
    </div>
    <div class="img-ad-card">
      <div class="img-ad-title">Clean Product on White/Off-White</div>
      <div class="img-ad-body">The baseline testing format. <strong>Use for your first week</strong> to establish a CTR baseline before layering in lifestyle shots. Communicates the product clearly, works well for catalogue ads, and tells you if the product itself is compelling before the creative does the heavy lifting.</div>
    </div>
    <div class="img-ad-card">
      <div class="img-ad-title">Ad Copy Structure</div>
      <div class="img-ad-body"><strong>Headline:</strong> Product name + price. "Oasis Heavyweight Crew — $80." Direct, no fluff.<br><strong>First line:</strong> Value prop before the "see more" cut. "400gsm French terry. Built to outlast your wardrobe rotation." <strong>This line does the most work.</strong><br>Body copy can expand but most cold traffic won't read past line 2.</div>
    </div>
    <div class="img-ad-card">
      <div class="img-ad-title">Shooting Checklist</div>
      <div class="img-ad-body">• <strong>iPhone is fine</strong> — authenticity matters in streetwear<br>• <strong>Golden hour</strong> — warm light = free on-brand photography<br>• <strong>4:5 ratio</strong> for feed, <strong>9:16</strong> for stories/reels placement<br>• Shoot <strong>20–30 frames</strong> per outfit, pick best 3<br>• <strong>3 variants per ad set</strong>, kill 2 weakest by Day 5<br>• Repurpose every ad image as an organic post too</div>
    </div>
  </div>
</div>

<!-- REVENUE PROJECTION -->
<div class="section fade-s" id="revenue">
  <div class="sec-label">Compounding Scenarios</div>
  <div class="sec-title">REVENUE PROJECTIONS</div>
  <div class="rev-tabs">
    <button class="rtab all on" onclick="filterChart('all',this)">ALL SCENARIOS</button>
    <button class="rtab safety" onclick="filterChart('safety',this)">SAFETY 20%</button>
    <button class="rtab balanced" onclick="filterChart('balanced',this)">BALANCED 50%</button>
    <button class="rtab aggressive" onclick="filterChart('aggressive',this)">AGGRESSIVE 80%</button>
  </div>
  <div class="rev-summary">
    <div class="rsc safety"><div class="rsc-name">Safety — 20% Reinvest</div><div class="rsc-val" id="sv">—</div><div class="rsc-meta">Total ad spend: <span id="ss">—</span><br>Final mo spend: <span id="sf">—</span><br>Avg ROAS: ~2.1x · Low risk</div></div>
    <div class="rsc balanced"><div class="rsc-name">Balanced — 50% Reinvest</div><div class="rsc-val" id="bv">—</div><div class="rsc-meta">Total ad spend: <span id="bs">—</span><br>Final mo spend: <span id="bf">—</span><br>Avg ROAS: ~2.3x · Recommended</div></div>
    <div class="rsc aggressive"><div class="rsc-name">Aggressive — 80% Reinvest</div><div class="rsc-val" id="av">—</div><div class="rsc-meta">Total ad spend: <span id="as">—</span><br>Final mo spend: <span id="af">—</span><br>Avg ROAS: ~2.5x · High ceiling</div></div>
  </div>
  <div class="chart-area">
    <div class="chart-lbl">MONTHLY REVENUE BY SCENARIO — HOVER FOR DETAILS</div>
    <div class="chart-inner" id="chartInner">
      <div class="chart-grid" id="chartGrid"></div>
      <svg class="chart-svg" id="chartSvg" viewBox="0 0 100 100" preserveAspectRatio="none"></svg>
      <div class="x-lbls" id="xLbls"></div>
      <div class="tip" id="tip"></div>
    </div>
  </div>
  <div class="rev-table-wrap">
    <table><thead><tr>
      <th>Month</th>
      <th style="color:var(--safety)">Safety Spend</th><th style="color:var(--safety)">Safety Rev</th>
      <th style="color:var(--balanced)">Balanced Spend</th><th style="color:var(--balanced)">Balanced Rev</th>
      <th style="color:var(--aggressive)">Aggr Spend</th><th style="color:var(--aggressive)">Aggr Rev</th>
    </tr></thead><tbody id="revTbody"></tbody></table>
  </div>
</div>

<!-- STORE CHECKLIST -->
<div class="section fade-s" id="store">
  <div class="sec-label">Before You Scale</div>
  <div class="sec-title">STORE OPTIMIZATION CHECKLIST</div>
  <p style="font-size:14px;color:var(--muted2);margin-bottom:28px;font-weight:300">Click items to mark as done. Fix Critical before running any ads. Fix Important within Week 1–2.</p>
  <div class="checklist-cats">
    <div class="chk-cat crit">
      <div class="chk-cat-title">🔴 Critical — Before Ads</div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Reviews</strong> — Install Loox or Judge.me. Get min 5–10 reviews per product. This is #1.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Product Descriptions</strong> — Rewrite spec sheets as storytelling. "Who it's for, what it feels like, why it exists."</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Return Policy</strong> — Make it clear and confident. "30-day returns, no questions asked" not vague language.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Shipping Timeframes</strong> — Add estimated delivery windows by region. "US: 5–8 days."</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Trust Badges</strong> — Secure Checkout, Free Returns, Worldwide Shipping — directly below Add to Cart.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Klaviyo Email Flows</strong> — Welcome, Abandoned Cart, Post-Purchase set up and live before first ad spend.</div></div>
    </div>
    <div class="chk-cat imp">
      <div class="chk-cat-title">🟡 Important — Week 1–2</div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Our Story Page</strong> — Brand narrative, desert philosophy, who started Kozi Desert and why. Make it feel human.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Homepage Hero Value Prop</strong> — One clear sentence above the fold for first-time visitors from ads.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Sticky Add to Cart (Mobile)</strong> — 80%+ of Meta traffic is mobile. ATC must always be visible.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Logo Filename</strong> — Currently "insert_some_code_here_5" — rename to kozidesert-logo.png in Shopify files.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Page Speed</strong> — Product pages have 17 images. Install TinyIMG to auto-compress. Every second costs 20% of visitors.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Instagram Feed on Homepage</strong> — Shows the brand is alive. Builds trust for cold traffic from ads.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Favicon</strong> — Make sure it's your logo, not the default Shopify icon.</div></div>
    </div>
    <div class="chk-cat growth">
      <div class="chk-cat-title">🟢 Growth — AI & SEO</div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>ChatGPT Merchant Feed</strong> — Register at chatgpt.com/merchants. Submit product feed. Early mover advantage is real.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Meta Titles & Descriptions</strong> — Write proper SEO copy for every product page in Shopify → Edit SEO.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Schema Markup</strong> — Install TinyIMG or SEO King app to enhance structured data for AI indexing.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Collection Page Descriptions</strong> — Add a short paragraph to each collection page for Google and AI search.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Blog / Content Hub</strong> — Start with 3–4 articles: "How to style a heavyweight crew", "What makes 400gsm worth it."</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Review Presence Off-Site</strong> — Get listed on Trustpilot, Google Business. Brands with Trustpilot profiles have 3x higher AI recommendation chance.</div></div>
      <div class="chk-item" onclick="toggleChk(this)"><div class="chk-box"></div><div class="chk-txt"><strong>Reddit/Quora Presence</strong> — Answer questions in streetwear/fashion niches. Brands mentioned on Reddit have 4x higher ChatGPT citation rate.</div></div>
    </div>
  </div>
</div>

<!-- EMAIL -->
<div class="section fade-s" id="email">
  <div class="sec-label">Retention & Revenue</div>
  <div class="sec-title">EMAIL FLOWS</div>
  <div class="email-flows">
    <div class="fc"><div class="fc-num">01</div><div class="fc-name">Welcome Series</div><div class="fc-trig">Trigger: Email signup (popup)</div>
      <ul class="fc-steps">
        <li class="fc-step"><div class="st-time">Instant</div><div>Send 30% discount code + brand story. Short, sharp. Who is Kozi Desert and why it exists.</div></li>
        <li class="fc-step"><div class="st-time">Day 2</div><div>Bestseller showcase — Oasis Crew, Core Hoodie, Canyon Vest. Single product per email.</div></li>
        <li class="fc-step"><div class="st-time">Day 5</div><div>Social proof — show any reviews, Instagram posts, real people in the pieces.</div></li>
        <li class="fc-step"><div class="st-time">Day 9</div><div>Last chance — "Your 30% code expires in 48 hours." Urgency close.</div></li>
      </ul>
    </div>
    <div class="fc"><div class="fc-num">02</div><div class="fc-name">Abandoned Cart</div><div class="fc-trig">Trigger: Add to cart → no purchase (1hr)</div>
      <ul class="fc-steps">
        <li class="fc-step"><div class="st-time">1 hr</div><div>"You left something behind." Clean email, product image, direct link to cart. No discount yet.</div></li>
        <li class="fc-step"><div class="st-time">24 hrs</div><div>Address objections — sizing? Free returns. Price? Quality breakdown. Shipping timeline.</div></li>
        <li class="fc-step"><div class="st-time">72 hrs</div><div>Final email — 10% off this order only. Subject: "Okay, we'll meet you halfway."</div></li>
      </ul>
    </div>
    <div class="fc"><div class="fc-num">03</div><div class="fc-name">Post-Purchase</div><div class="fc-trig">Trigger: Order confirmed</div>
      <ul class="fc-steps">
        <li class="fc-step"><div class="st-time">Day 1</div><div>Order confirmation + brand message. "You just copped something built to last."</div></li>
        <li class="fc-step"><div class="st-time">Day 7</div><div>Shipping update + styling guide. How to wear what they bought. Builds brand relationship.</div></li>
        <li class="fc-step"><div class="st-time">Day 14</div><div>Review request. One click. Offer giveaway entry as incentive.</div></li>
        <li class="fc-step"><div class="st-time">Day 30</div><div>Cross-sell — "Complete the look." Complementary pieces to what they bought.</div></li>
      </ul>
    </div>
  </div>
</div>

<!-- CONTENT CALENDAR -->
<div class="section fade-s" id="content">
  <div class="sec-label">Organic Growth</div>
  <div class="sec-title">WEEKLY CONTENT CALENDAR</div>
  <div class="cal">
    <div class="cal-day"><div class="cal-dn">Mon</div><div class="cal-type">Product showcase</div><div class="cal-plat">IG Reel + TikTok</div></div>
    <div class="cal-day"><div class="cal-dn">Tue</div><div class="cal-type">Outfit inspo static</div><div class="cal-plat">IG Feed</div></div>
    <div class="cal-day"><div class="cal-dn">Wed</div><div class="cal-type">Behind the brand</div><div class="cal-plat">IG Stories</div></div>
    <div class="cal-day"><div class="cal-dn">Thu</div><div class="cal-type">Fabric close-up</div><div class="cal-plat">TikTok</div></div>
    <div class="cal-day"><div class="cal-dn">Fri</div><div class="cal-type">"How I style it"</div><div class="cal-plat">IG Reel + TikTok</div></div>
    <div class="cal-day"><div class="cal-dn">Sat</div><div class="cal-type">UGC repost / poll</div><div class="cal-plat">IG Stories</div></div>
    <div class="cal-day"><div class="cal-dn">Sun</div><div class="cal-type">Drop teaser / restock</div><div class="cal-plat">IG + Email</div></div>
  </div>
  <div style="background:var(--bg2);border:1px solid var(--border);padding:22px 26px">
    <div class="ct" style="margin-bottom:14px">Content Rules for Kozi Desert</div>
    <div class="g2">
      <div class="ci"><strong>Desert aesthetic always.</strong> Dry landscapes, warm tones, minimal backgrounds. Every post should feel like the same world.</div>
      <div class="ci"><strong>No cheap-looking flats.</strong> Never on a bed or table. Worn on body, in motion, or on a premium surface only.</div>
      <div class="ci"><strong>Captions = brand voice.</strong> Short, lowercase, intentional. "built for the in-between." "not for everyone."</div>
      <div class="ci"><strong>Repurpose everything.</strong> Every ad image → organic post. Every organic post → ad test candidate. Nothing is single-use.</div>
    </div>
  </div>
</div>

<!-- SCALING RULES -->
<div class="section fade-s" id="scaling">
  <div class="sec-label">Decision Framework</div>
  <div class="sec-title">SCALING RULES</div>
  <div class="rules">
    <div class="rule"><span class="rule-icon">📈</span><div class="rule-title">When to Scale Up</div><div class="rule-body">Ad set in learning phase <strong>7+ days</strong>, ROAS holding above target, <strong>25–50+ purchase events</strong> in period. These three conditions must all be true.<br><br>Don't scale on gut feeling — scale on data only.</div><div class="rule-trig"><strong>Action:</strong> Increase budget max 20% every 3–4 days. Never double overnight — resets learning for 5–7 days.</div></div>
    <div class="rule"><span class="rule-icon">📉</span><div class="rule-title">When to Scale Down</div><div class="rule-body">ROAS below <strong>1.5x for 3 consecutive days</strong>, CTR below <strong>0.8%</strong> (creative fatigue), or CPM above <strong>$18</strong> (audience saturation). Act fast — don't wait hoping it recovers.</div><div class="rule-trig"><strong>Action:</strong> Cut 20–30% or pause the set. Refresh creative before reactivating. Kill ad sets, not campaigns.</div></div>
    <div class="rule"><span class="rule-icon">🎯</span><div class="rule-title">Creative Rotation Rule</div><div class="rule-body">Always keep <strong>3 active creative variants</strong> per campaign. When one drops below 0.8% CTR, replace it. Never run a single creative — you'll hit fatigue in 2–3 weeks and performance collapses with no backup.</div><div class="rule-trig"><strong>Action:</strong> Every 2 weeks, introduce 1 new variant. Kill worst performer. Always testing something new.</div></div>
    <div class="rule"><span class="rule-icon">💰</span><div class="rule-title">Compound Reinvestment Rule</div><div class="rule-body">Balanced (50%): monthly profit = Revenue – COGS – Ad Spend. Take 50%, add to next month's budget. Do this <strong>after month closes</strong>, not mid-month — budget changes disrupt the learning phase.</div><div class="rule-trig"><strong>Action:</strong> Month closes → profit calc → 50% to next month ads → 50% is yours. Consistent, sustainable.</div></div>
  </div>
  <div class="info-box">
    <p><strong>The One Rule That Overrides Everything:</strong> Don't scale what's broken. CVR below 1% = site problem. CTR below 0.8% = creative problem. Fix the fundamentals first, then pour fuel on it. Spend never fixes fundamentals.</p>
  </div>
</div>

<!-- KPIs -->
<div class="section fade-s" id="kpis">
  <div class="sec-label">Performance Benchmarks</div>
  <div class="sec-title">KPIs TO TRACK WEEKLY</div>
  <div class="kpi-grid">
    <div class="kpi"><div class="kpi-lbl">Min. ROAS Target</div><div class="kpi-val">1.8x</div><div class="kpi-desc">Below this → pause & fix</div></div>
    <div class="kpi"><div class="kpi-lbl">Target CTR</div><div class="kpi-val">1.5%+</div><div class="kpi-desc">Below 0.8% = creative fatigue</div></div>
    <div class="kpi"><div class="kpi-lbl">Target CVR</div><div class="kpi-val">1.5%+</div><div class="kpi-desc">Below 0.8% = site problem</div></div>
    <div class="kpi"><div class="kpi-lbl">Target AOV</div><div class="kpi-val">$105+</div><div class="kpi-desc">Improve with bundles</div></div>
    <div class="kpi"><div class="kpi-lbl">Max CPM</div><div class="kpi-val">$18</div><div class="kpi-desc">Above = audience saturation</div></div>
    <div class="kpi"><div class="kpi-lbl">Email Open Rate</div><div class="kpi-val">28%+</div><div class="kpi-desc">Below 20% = fix subject lines</div></div>
    <div class="kpi"><div class="kpi-lbl">Cart Abandon Rate</div><div class="kpi-val">&lt;70%</div><div class="kpi-desc">Above 75% = trust issue</div></div>
    <div class="kpi"><div class="kpi-lbl">Repeat Purchase %</div><div class="kpi-val">15%+</div><div class="kpi-desc">By Month 6 target</div></div>
  </div>
</div>

<!-- AI OPTIMIZATION -->
<div class="section fade-s" id="ai">
  <div class="sec-label">Future-Proofing</div>
  <div class="sec-title">AI SEARCH OPTIMIZATION</div>
  <div class="info-box" style="margin-bottom:24px">
    <p>AI tools like ChatGPT, Perplexity, and Google's AI Overviews are becoming the new search for shoppers. Brands optimized for AI recommendation get visibility without paying for every click. The foundation is the same as SEO but the tactics are different — here's what actually moves the needle for Kozi Desert specifically.</p>
  </div>
  <div class="ai-grid">
    <div class="ai-card">
      <div class="ai-card-title">ChatGPT Shopping Feed</div>
      <div class="ai-card-body">Register at <strong>chatgpt.com/merchants</strong> and submit a product feed. This is a direct pipeline into ChatGPT Shopping recommendations. Most small brands haven't done this yet — genuine early mover advantage.<span class="ai-tag">Do This First</span></div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">Review Platform Presence</div>
      <div class="ai-card-body">Brands with profiles on <strong>Trustpilot, Google Business, Sitejabber</strong> are 3x more likely to be recommended by ChatGPT than brands without. And brands with mentions on <strong>Reddit and Quora</strong> have 4x higher citation rates. Get listed and get reviewed off-site.<span class="ai-tag">3x Citation Boost</span></div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">Conversational Product Descriptions</div>
      <div class="ai-card-body">AI pulls from content written in <strong>question-answering, conversational style</strong> — not spec sheets. Rewrite descriptions to answer: "Who is this for? What problem does it solve? Why is it better than alternatives?" Front-load important info — <strong>44% of AI citations come from the first 30% of page text.</strong><span class="ai-tag">GEO</span></div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">Schema Markup</div>
      <div class="ai-card-body">Product schema (name, description, price, availability, reviews, brand) makes it easy for AI tools to read and cite your pages. Shopify adds basic schema but it's minimal. Use <strong>TinyIMG or SEO King</strong> to enhance. This is how AI knows your Oasis Crew exists, costs $80, and has reviews.<span class="ai-tag">Technical SEO</span></div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">Blog Content for AI Queries</div>
      <div class="ai-card-body">When someone asks AI "best heavyweight crewneck under $100" — AI needs a page to cite. Write:<br>• "Best heavyweight crewnecks 2026"<br>• "What makes 400gsm cotton worth it"<br>• "How to style an oversized crew for spring"<br><strong>These are the pages AI pulls from.</strong> Without them, you can't be recommended.<span class="ai-tag">AEO</span></div>
    </div>
    <div class="ai-card">
      <div class="ai-card-title">Domain & Backlink Authority</div>
      <div class="ai-card-body">Sites with <strong>32K+ referring domains are 3.5x more likely to be cited</strong> by ChatGPT. You won't hit that fast, but start building. Get featured in streetwear blog roundups, fashion newsletters, influencer posts that link back. Every backlink trains AI models to associate Kozi Desert with the fashion category.<span class="ai-tag">Long Game</span></div>
    </div>
  </div>
</div>

<!-- RESOURCES -->
<div class="section fade-s" id="resources">
  <div class="sec-label">Keep Learning</div>
  <div class="sec-title">LEARNING RESOURCES</div>
  <p style="font-size:14px;color:var(--muted2);margin-bottom:28px;font-weight:300">Everything you need to go deeper on each strategy covered in this playbook.</p>
  <div class="res-grid">
    <div class="res-card" onclick="window.open('https://www.youtube.com/@benheath','_blank')">
      <div class="res-cat">Meta Ads</div>
      <div class="res-title">Ben Heath — Facebook & Instagram Ads</div>
      <div class="res-desc">Best channel for Meta ads fundamentals, campaign structure, and scaling strategies. Clear, no-fluff explanations that match what actually works for ecommerce.</div>
      <span class="res-link">youtube.com/@benheath ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://www.youtube.com/@AmbassadorAds','_blank')">
      <div class="res-cat">Meta Ads</div>
      <div class="res-title">Nick Theriot — Meta Ads Scaling</div>
      <div class="res-desc">Focuses on scaling ecommerce brands with Meta ads. Real campaign walkthroughs, budget compounding strategies, and ROAS optimization — very relevant to your situation.</div>
      <span class="res-link">youtube.com/@AmbassadorAds ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://www.youtube.com/@thecjwitmer','_blank')">
      <div class="res-cat">Ecommerce Strategy</div>
      <div class="res-title">CJ Witmer — Shopify & DTC Growth</div>
      <div class="res-desc">Ecommerce brand building, Shopify optimization, and paid social strategy for fashion and apparel brands. Practical, actionable, covers exactly the stage you're at.</div>
      <span class="res-link">youtube.com/@thecjwitmer ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://klaviyo.com/academy','_blank')">
      <div class="res-cat">Email Marketing</div>
      <div class="res-title">Klaviyo Academy</div>
      <div class="res-desc">Free courses on setting up Welcome, Abandoned Cart, and Post-Purchase flows. The exact email automations we mapped in this playbook — all explained step by step.</div>
      <span class="res-link">klaviyo.com/academy ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview','_blank')">
      <div class="res-cat">AI Optimization</div>
      <div class="res-title">GEO (Generative Engine Optimization) Guide</div>
      <div class="res-desc">Search "GEO optimization ecommerce 2025" on Google for the latest research. Key papers from Princeton and Columbia track what makes AI tools recommend brands — this field is evolving fast.</div>
      <span class="res-link">Search: "GEO optimization 2025" ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://chatgpt.com/merchants','_blank')">
      <div class="res-cat">AI Optimization</div>
      <div class="res-title">ChatGPT Merchant Portal</div>
      <div class="res-desc">Submit your Kozi Desert product feed directly to OpenAI's shopping system. When people ask ChatGPT for streetwear recommendations, this is how you get in the conversation.</div>
      <span class="res-link">chatgpt.com/merchants ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://www.youtube.com/@klaviyo','_blank')">
      <div class="res-cat">Email Marketing</div>
      <div class="res-title">Klaviyo YouTube Channel</div>
      <div class="res-desc">Tutorials, case studies, and strategy content from the platform you'll be using for all your email flows. Especially useful for understanding segmentation as your list grows.</div>
      <span class="res-link">youtube.com/@klaviyo ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://www.shopify.com/blog/topics/marketing','_blank')">
      <div class="res-cat">Shopify & Store</div>
      <div class="res-title">Shopify Blog — Marketing & Growth</div>
      <div class="res-desc">Shopify's own blog covers conversion rate optimization, product page best practices, and ecommerce marketing. Directly relevant to fixing the store issues we identified in the checklist.</div>
      <span class="res-link">shopify.com/blog ↗</span>
    </div>
    <div class="res-card" onclick="window.open('https://www.reddit.com/r/streetwear/','_blank')">
      <div class="res-cat">Brand Research</div>
      <div class="res-title">r/streetwear — Know Your Buyer</div>
      <div class="res-desc">Your target customer is here. Read what they talk about, what they rate, what they dismiss. Spend 30 minutes a week here and your ad copy and product positioning will improve dramatically.</div>
      <span class="res-link">reddit.com/r/streetwear ↗</span>
    </div>
  </div>
</div>

<footer>
  <div class="foot-brand">KOZIDESERT.COM</div>
  <div class="foot-note">Master Growth Playbook 2026 · Built from scratch in one session</div>
  <div class="foot-note">Meta Ads · Email · Organic · AI Optimization · Scaling · Revenue Projections</div>
</footer>

<script>
// ── THEME ──
const themes = {
  blue:{
    '--bg':'#080C12','--bg2':'#0C1018','--bg3':'#10161E','--bg4':'#141C26','--bg5':'#18222E',
    '--accent':'#5B9BD5','--accent2':'#7BB8F0','--accent-dim':'#0F2035',
    '--cream':'#E8F0F8','--muted':'#4A6080','--muted2':'#6A84A8','--border':'#1A2638','--border2':'#243450',
    '--phase1':'#3A6EA8','--phase2':'#5B9BD5','--phase3':'#7BB8F0','--phase4':'#A8D4FF',
    '--safety':'#4A9E78','--balanced':'#C9A96E','--aggressive':'#C4604A'
  },
  sand:{
    '--bg':'#0A0908','--bg2':'#111009','--bg3':'#181613','--bg4':'#201E1A','--bg5':'#282420',
    '--accent':'#C9A96E','--accent2':'#E8D5B0','--accent-dim':'#3D3020',
    '--cream':'#F0EBE0','--muted':'#6A6050','--muted2':'#8A7E6A','--border':'#282420','--border2':'#302C26',
    '--phase1':'#8B7355','--phase2':'#C9A96E','--phase3':'#D4A847','--phase4':'#E8C87A',
    '--safety':'#6B9E78','--balanced':'#C9A96E','--aggressive':'#C4604A'
  },
  slate:{
    '--bg':'#0D0F14','--bg2':'#121418','--bg3':'#17191F','--bg4':'#1C1E26','--bg5':'#21242E',
    '--accent':'#9B8ED4','--accent2':'#C0B4F0','--accent-dim':'#1A1535',
    '--cream':'#EAE8F4','--muted':'#5A5470','--muted2':'#7A74A0','--border':'#222030','--border2':'#2E2A40',
    '--phase1':'#6A5AA8','--phase2':'#9B8ED4','--phase3':'#C0B4F0','--phase4':'#DDD8FF',
    '--safety':'#5A9E78','--balanced':'#C9A96E','--aggressive':'#C4604A'
  }
};
function setTheme(name){
  const r=document.documentElement;
  Object.entries(themes[name]).forEach(([k,v])=>r.style.setProperty(k,v));
  document.querySelectorAll('.theme-dot').forEach(d=>d.classList.remove('on'));
  document.querySelector('.td-'+name).classList.add('on');
  // Redraw chart
  buildChart();
}

// ── PHASE TOGGLE ──
function tp(bid,aid){
  const b=document.getElementById(bid),a=document.getElementById(aid);
  const open=b.classList.contains('open');
  b.classList.toggle('open',!open);
  a.classList.toggle('open',!open);
  if(!open) setTimeout(()=>b.querySelectorAll('.bbf').forEach(e=>e.classList.add('go')),100);
}

// ── SCROLL ANIMATIONS ──
const obs=new IntersectionObserver(entries=>entries.forEach(e=>{
  if(e.isIntersecting){e.target.classList.add('vis')}
}),{threshold:0.08});
document.querySelectorAll('.fade-s,.phase').forEach(el=>obs.observe(el));
setTimeout(()=>tp('pb1','a1'),500);

// ── CHECKLIST ──
function toggleChk(el){el.classList.toggle('done')}

// ── REVENUE CHART ──
const mos=['Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec','Jan'];
const fullMos=['Feb 2026','Mar 2026','Apr 2026','May 2026','Jun 2026','Jul 2026','Aug 2026','Sep 2026','Oct 2026','Nov 2026','Dec 2026','Jan 2027'];
const cvr=[0.009,0.012,0.016,0.019,0.021,0.023,0.025,0.026,0.027,0.030,0.032,0.028];
const aov=[95,98,100,102,105,107,108,110,112,115,118,112];
const email=[0,0,80,140,200,260,320,380,440,600,720,500];

function calcS(rate){
  let spend=500;const spends=[],revs=[],profits=[];
  for(let i=0;i<12;i++){
    const clicks=(spend/100)*70;
    const sales=Math.floor(clicks*cvr[i]);
    const rev=Math.round(sales*aov[i]+email[i]);
    const profit=rev-spend;
    const reinvest=profit>0?Math.round(profit*rate):0;
    spends.push(Math.round(spend));revs.push(rev);profits.push(profit);
    spend=Math.round(Math.min(spend+reinvest,8000));
  }
  return{spends,revs,profits};
}
const S=calcS(0.20),B=calcS(0.50),A=calcS(0.80);
const sum=a=>a.reduce((x,y)=>x+y,0);
const fmt=n=>'$'+n.toLocaleString();

// Update cards
document.getElementById('sv').textContent=fmt(sum(S.revs));
document.getElementById('bv').textContent=fmt(sum(B.revs));
document.getElementById('av').textContent=fmt(sum(A.revs));
document.getElementById('ss').textContent=fmt(sum(S.spends));
document.getElementById('bs').textContent=fmt(sum(B.spends));
document.getElementById('as').textContent=fmt(sum(A.spends));
document.getElementById('sf').textContent=fmt(S.spends[11])+'/mo';
document.getElementById('bf').textContent=fmt(B.spends[11])+'/mo';
document.getElementById('af').textContent=fmt(A.spends[11])+'/mo';

// Chart
let currentFilter='all';
function buildChart(){
  const svg=document.getElementById('chartSvg');
  svg.innerHTML='';
  const grid=document.getElementById('chartGrid');
  grid.innerHTML='';
  const xlbls=document.getElementById('xLbls');
  xlbls.innerHTML='';
  const maxV=Math.max(...S.revs,...B.revs,...A.revs);
  const gmax=Math.ceil(maxV/1000)*1000;
  const steps=5;
  for(let i=0;i<=steps;i++){
    const val=(gmax/steps)*(steps-i);
    const line=document.createElement('div');line.className='cg-line';
    const lbl=document.createElement('div');lbl.className='cg-line-lbl';
    lbl.textContent=val>=1000?'$'+(val/1000).toFixed(0)+'K':'$'+val;
    line.appendChild(lbl);grid.appendChild(line);
  }
  mos.forEach(m=>{const el=document.createElement('div');el.className='xl';el.textContent=m;xlbls.appendChild(el);});
  const cs=[
    {key:'safety',revs:S.revs,color:'var(--safety)',dim:'rgba(74,158,120,0.08)',spends:S.spends,delay:0},
    {key:'balanced',revs:B.revs,color:'var(--balanced)',dim:'rgba(201,169,110,0.08)',spends:B.spends,delay:0.2},
    {key:'aggressive',revs:A.revs,color:'var(--aggressive)',dim:'rgba(196,96,74,0.1)',spends:A.spends,delay:0.4},
  ];
  cs.forEach(({key,revs,color,dim,spends,delay})=>{
    const pts=revs.map((r,i)=>[(i/11)*100,100-(r/gmax)*100]);
    const pathD=pts.reduce((d,[x,y],i)=>{
      if(i===0)return`M ${x} ${y}`;
      const cp1x=pts[i-1][0]+(pts[i][0]-pts[i-1][0])/3;
      const cp2x=pts[i][0]-(pts[i][0]-pts[i-1][0])/3;
      return d+` C ${cp1x} ${pts[i-1][1]} ${cp2x} ${y} ${x} ${y}`;
    },'');
    const show=currentFilter==='all'||currentFilter===key;
    const area=document.createElementNS('http://www.w3.org/2000/svg','path');
    area.setAttribute('d',pathD+` L 100 100 L 0 100 Z`);
    area.setAttribute('fill',dim);
    area.style.opacity=show?'1':'0.04';
    area.className='area-'+key;
    svg.appendChild(area);
    const path=document.createElementNS('http://www.w3.org/2000/svg','path');
    path.setAttribute('d',pathD);
    path.setAttribute('fill','none');
    path.setAttribute('stroke',color);
    path.setAttribute('stroke-width','2');
    path.setAttribute('stroke-linecap','round');
    path.setAttribute('stroke-linejoin','round');
    path.style.opacity=show?'1':'0.04';
    path.style.strokeDasharray='3000';
    path.style.strokeDashoffset='3000';
    path.style.animation=`draw 2s ease ${delay}s forwards`;
    path.className='line-'+key;
    svg.appendChild(path);
    pts.forEach(([x,y],i)=>{
      const c=document.createElementNS('http://www.w3.org/2000/svg','circle');
      c.setAttribute('cx',x);c.setAttribute('cy',y);c.setAttribute('r','1.2');
      c.setAttribute('fill',color);c.style.opacity=show?'1':'0.04';
      c.className='dot-'+key;
      svg.appendChild(c);
    });
  });
  // Hover
  const inner=document.getElementById('chartInner');
  const tip=document.getElementById('tip');
  inner.onmousemove=e=>{
    const rect=inner.getBoundingClientRect();
    const xr=(e.clientX-rect.left-48)/(rect.width-48);
    const mi=Math.round(xr*11);
    if(mi<0||mi>11){tip.classList.remove('show');return;}
    tip.innerHTML=`<div class="tip-mo">${fullMos[mi]}</div>
      <div class="tip-row"><span class="ts">Safety</span><span class="ts">${fmt(S.revs[mi])} <span style="opacity:0.5;font-size:9px">(${fmt(S.spends[mi])} spend)</span></span></div>
      <div class="tip-row"><span class="tb">Balanced</span><span class="tb">${fmt(B.revs[mi])} <span style="opacity:0.5;font-size:9px">(${fmt(B.spends[mi])} spend)</span></span></div>
      <div class="tip-row"><span class="ta">Aggressive</span><span class="ta">${fmt(A.revs[mi])} <span style="opacity:0.5;font-size:9px">(${fmt(A.spends[mi])} spend)</span></span></div>`;
    let tx=e.clientX-rect.left+12,ty=e.clientY-rect.top-70;
    if(tx+190>rect.width)tx=e.clientX-rect.left-200;
    tip.style.left=tx+'px';tip.style.top=ty+'px';tip.classList.add('show');
  };
  inner.onmouseleave=()=>tip.classList.remove('show');
}

// Build table
const tbody=document.getElementById('revTbody');
mos.forEach((m,i)=>{
  const tr=document.createElement('tr');
  tr.innerHTML=`<td class="mo">${fullMos[i]}</td>
    <td class="ts2">${fmt(S.spends[i])}</td><td class="ts2">${fmt(S.revs[i])}</td>
    <td class="tb2">${fmt(B.spends[i])}</td><td class="tb2">${fmt(B.revs[i])}</td>
    <td class="ta2">${fmt(A.spends[i])}</td><td class="ta2">${fmt(A.revs[i])}</td>`;
  tbody.appendChild(tr);
});
const tot=document.createElement('tr');tot.className='tot-row';
tot.innerHTML=`<td class="mo" style="color:var(--accent)">TOTAL</td>
  <td class="ts2">${fmt(sum(S.spends))}</td><td class="ts2" style="font-size:13px">${fmt(sum(S.revs))}</td>
  <td class="tb2">${fmt(sum(B.spends))}</td><td class="tb2" style="font-size:13px">${fmt(sum(B.revs))}</td>
  <td class="ta2">${fmt(sum(A.spends))}</td><td class="ta2" style="font-size:13px">${fmt(sum(A.revs))}</td>`;
tbody.appendChild(tot);

// Filter chart
function filterChart(type,btn){
  currentFilter=type;
  document.querySelectorAll('.rtab').forEach(b=>b.classList.remove('on'));
  btn.classList.add('on');
  const keys=['safety','balanced','aggressive'];
  keys.forEach(k=>{
    const show=type==='all'||type===k;
    document.querySelectorAll('.line-'+k+',.dot-'+k+',.area-'+k).forEach(el=>el.style.opacity=show?'1':'0.04');
    const card=document.querySelector('.rsc.'+k);if(card)card.style.opacity=show?'1':'0.35';
  });
}

buildChart();
</script>
</body>
</html>
