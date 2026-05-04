[programim_faruk.html](https://github.com/user-attachments/files/27362652/programim_faruk.html)
# farukprogram<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="theme-color" content="#0A1428">
<title>الْفَارُوق · Programım</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
:root{
--bg:#0A1428;--bg-deep:#060D1C;--bg-grad:radial-gradient(circle at 20% 10%,rgba(6,214,255,.06) 0%,transparent 40%),radial-gradient(circle at 85% 95%,rgba(251,176,64,.05) 0%,transparent 40%);
--surface:#142342;--surface-soft:#1B2D52;--surface-elevated:#243A66;
--primary:#06D6FF;--primary-light:#38E1FF;--primary-dark:#0095B3;--primary-soft:rgba(6,214,255,.12);
--gold:#FBB040;--gold-light:#FDC971;--gold-soft:rgba(251,176,64,.14);
--accent:#10B981;--accent-soft:rgba(16,185,129,.12);
--rose:#F472B6;--rose-soft:rgba(244,114,182,.12);
--text:#F1F5F9;--text-soft:#94A3B8;--text-muted:#64748B;--text-dim:#475569;
--border:rgba(251,176,64,.18);--border-soft:rgba(251,176,64,.08);--border-tech:rgba(6,214,255,.25);
--shadow:0 1px 3px rgba(0,0,0,.5),0 6px 20px rgba(0,0,0,.4);
--shadow-card:0 2px 12px rgba(0,0,0,.35);
--shadow-glow-tech:0 0 24px rgba(6,214,255,.30);
--shadow-glow-gold:0 0 22px rgba(251,176,64,.25)
}
body{font-family:-apple-system,BlinkMacSystemFont,"SF Pro Display","Segoe UI",system-ui,sans-serif;background:var(--bg);color:var(--text);line-height:1.5;min-height:100vh;padding-bottom:100px;background-image:var(--bg-grad)}
.app{max-width:720px;margin:0 auto;padding:16px 14px}
.setup-screen{display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:90vh;text-align:center;padding:24px}
.setup-screen .arabic-title{font-size:46px;color:var(--gold);margin-bottom:6px;font-family:"Scheherazade New","Amiri",serif;direction:rtl;letter-spacing:2px;text-shadow:0 0 30px rgba(251,176,64,.3)}
.setup-screen .ornament{font-size:64px;margin-bottom:14px;color:var(--primary);font-family:serif;line-height:1;text-shadow:0 0 30px rgba(6,214,255,.4)}
.setup-screen h1{font-size:22px;font-weight:600;color:var(--primary-light);margin-bottom:12px;letter-spacing:.5px}
.setup-screen p{color:var(--text-soft);margin-bottom:14px;max-width:340px;font-size:14px;line-height:1.7}
.setup-screen p .highlight{color:var(--gold);font-weight:600}
.setup-screen p .tech{color:var(--primary);font-weight:600}
.setup-screen .dede-note{background:linear-gradient(135deg,var(--gold-soft) 0%,transparent 100%);border:1px solid var(--gold-soft);border-left:3px solid var(--gold);border-radius:10px;padding:12px 14px;margin:14px 0 24px;font-size:12px;color:var(--gold-light);max-width:340px;line-height:1.6;text-align:left}
.setup-screen input{width:100%;max-width:280px;padding:14px 18px;border:1px solid var(--border);border-radius:12px;font-size:16px;background:var(--surface);color:var(--text);margin-bottom:14px;text-align:center;font-family:inherit;outline:none;transition:all .2s}
.setup-screen input:focus{border-color:var(--primary);box-shadow:0 0 0 3px var(--primary-soft)}
.setup-screen button{background:linear-gradient(135deg,var(--primary-dark) 0%,var(--primary) 100%);color:var(--bg);border:none;border-radius:12px;padding:14px 38px;font-size:15px;font-weight:700;cursor:pointer;font-family:inherit;letter-spacing:.3px;box-shadow:var(--shadow-glow-tech)}
.setup-screen button:active{transform:scale(.97)}
.header{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:16px;padding:4px 4px 0}
.greeting .salam{font-size:11px;color:var(--text-muted);letter-spacing:.5px;text-transform:uppercase}
.greeting .arabic-name{font-size:28px;color:var(--gold);font-family:"Scheherazade New","Amiri",serif;direction:rtl;line-height:1.2;margin-top:2px;letter-spacing:1px;text-shadow:0 0 16px rgba(251,176,64,.25)}
.greeting .name{font-size:18px;font-weight:600;color:var(--primary-light);margin-top:2px}
.date-pill{background:var(--surface);border:1px solid var(--border-tech);border-radius:10px;padding:8px 12px;text-align:right;box-shadow:var(--shadow-card)}
.date-pill .day{font-size:12px;font-weight:700;color:var(--primary)}
.date-pill .date{font-size:10px;color:var(--text-soft);margin-top:2px}
.tabs{display:flex;background:var(--surface);border-radius:12px;padding:4px;margin-bottom:16px;box-shadow:var(--shadow-card);border:1px solid var(--border-soft);overflow-x:auto;-webkit-overflow-scrolling:touch}
.tabs::-webkit-scrollbar{display:none}
.tab{flex-shrink:0;min-width:60px;padding:9px 12px;border:none;background:transparent;color:var(--text-soft);font-size:11px;font-weight:600;cursor:pointer;border-radius:8px;font-family:inherit;transition:all .2s;white-space:nowrap;letter-spacing:.3px}
.tab.active{background:linear-gradient(135deg,var(--primary-dark) 0%,var(--primary) 100%);color:var(--bg);box-shadow:0 0 12px rgba(6,214,255,.3)}
.view{display:none}
.view.active{display:block;animation:fadeIn .3s}
@keyframes fadeIn{from{opacity:0;transform:translateY(4px)}to{opacity:1;transform:translateY(0)}}
@keyframes glowPulse{0%,100%{box-shadow:0 0 12px rgba(6,214,255,.3)}50%{box-shadow:0 0 22px rgba(6,214,255,.5)}}
.stats{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:14px}
.stat-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:12px 14px;box-shadow:var(--shadow-card)}
.stat-card .label{font-size:9px;color:var(--text-muted);text-transform:uppercase;letter-spacing:.8px;margin-bottom:6px}
.stat-card .number{font-size:24px;font-weight:700;letter-spacing:-.5px}
.stat-card .unit{font-size:11px;color:var(--text-soft);margin-left:4px;font-weight:400}
.stat-card.streak .number{color:var(--gold)}
.stat-card.progress .number{color:var(--primary)}
.stat-card.sport .number{color:var(--accent)}
.stat-card.kuran .number{color:var(--gold-light)}
.chain{display:flex;gap:3px;margin-top:6px}
.chain .link{flex:1;height:4px;background:rgba(251,176,64,.15);border-radius:2px;transition:background .3s}
.chain .link.filled{background:var(--gold);box-shadow:0 0 6px rgba(251,176,64,.5)}
.progress-bar{height:5px;background:var(--primary-soft);border-radius:3px;margin-top:6px;overflow:hidden}
.progress-fill{height:100%;background:linear-gradient(90deg,var(--primary-dark) 0%,var(--primary) 100%);border-radius:3px;transition:width .4s ease}
.banner{background:linear-gradient(135deg,var(--primary-soft) 0%,var(--gold-soft) 100%);border-radius:12px;padding:12px 16px;margin-bottom:16px;font-size:13px;color:var(--gold-light);text-align:center;line-height:1.5;border:1px solid var(--border-soft)}
.section-title{font-size:11px;font-weight:700;color:var(--text-soft);text-transform:uppercase;letter-spacing:1.2px;margin:18px 4px 10px;display:flex;align-items:center;gap:8px}
.section-title::before{content:'';width:4px;height:4px;background:var(--primary);border-radius:50%;box-shadow:0 0 6px var(--primary)}
.section-title.gold::before{background:var(--gold);box-shadow:0 0 6px var(--gold)}
.kuzey-yildizi{background:linear-gradient(135deg,var(--surface) 0%,var(--surface-elevated) 100%);border:1px solid var(--border-tech);border-radius:14px;padding:14px 16px;margin-bottom:14px;display:flex;align-items:center;gap:12px;box-shadow:var(--shadow-card)}
.kuzey-yildizi .icon{font-size:32px;flex-shrink:0}
.kuzey-yildizi .label{font-size:10px;color:var(--primary);text-transform:uppercase;letter-spacing:1px;font-weight:700}
.kuzey-yildizi .text{font-size:13px;color:var(--text);font-weight:600;margin-top:2px;line-height:1.4}
.goal-hero{background:linear-gradient(135deg,var(--surface) 0%,var(--surface-elevated) 100%);border:1px solid var(--border-tech);border-radius:16px;padding:20px 18px;margin-bottom:16px;box-shadow:var(--shadow);position:relative;overflow:hidden}
.goal-hero::before{content:'';position:absolute;top:-50px;right:-50px;width:140px;height:140px;background:radial-gradient(circle,var(--primary-soft) 0%,transparent 70%)}
.goal-hero .arabic-quote{font-size:22px;color:var(--gold);font-family:"Scheherazade New",serif;direction:rtl;text-align:center;margin-bottom:8px;line-height:1.5;position:relative}
.goal-hero .quote-meaning{font-size:12px;color:var(--text-soft);text-align:center;font-style:italic;margin-bottom:16px;line-height:1.5}
.destinations{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:12px}
.dest{padding:14px 12px;background:var(--bg-deep);border-radius:10px;border:1px solid var(--border-soft);text-align:center}
.dest .icon{font-size:32px;margin-bottom:6px}
.dest .label{font-size:9px;color:var(--text-muted);text-transform:uppercase;letter-spacing:.8px;margin-bottom:4px}
.dest .place{font-size:13px;color:var(--gold-light);font-weight:700;line-height:1.3}
.checklist-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:14px;margin-bottom:10px;box-shadow:var(--shadow-card)}
.checklist-card .ch-year{font-size:10px;color:var(--primary);text-transform:uppercase;letter-spacing:1px;font-weight:700}
.checklist-card .ch-title{font-size:14px;color:var(--text);font-weight:700;margin-top:2px;margin-bottom:10px}
.checklist-item{display:flex;gap:10px;align-items:flex-start;padding:6px 0;font-size:13px;color:var(--text-soft);line-height:1.5}
.checklist-item .ck{flex-shrink:0;width:18px;height:18px;border-radius:5px;border:2px solid var(--border);display:flex;align-items:center;justify-content:center;cursor:pointer;margin-top:1px}
.checklist-item.done .ck{background:var(--accent);border-color:var(--accent)}
.checklist-item.done .ck::after{content:'✓';color:white;font-size:11px;font-weight:bold}
.checklist-item.done{color:var(--text-muted);text-decoration:line-through}
.countdown-card{background:linear-gradient(135deg,#0E2A3F 0%,var(--surface) 100%);border:1px solid var(--primary-dark);border-radius:14px;padding:16px;margin-bottom:14px;text-align:center;box-shadow:var(--shadow-glow-tech)}
.countdown-card .label{font-size:11px;color:var(--text-soft);text-transform:uppercase;letter-spacing:1px;margin-bottom:8px}
.countdown-card .big-num{font-size:38px;font-weight:800;color:var(--primary);letter-spacing:-1px;line-height:1}
.countdown-card .small{font-size:12px;color:var(--text-soft);margin-top:6px}
.word-card{background:var(--surface);border-radius:14px;padding:14px 16px;margin-bottom:10px;border:1px solid var(--border-soft);position:relative;overflow:hidden}
.word-card.ar{border-left:3px solid var(--gold);background:linear-gradient(90deg,var(--gold-soft) 0%,var(--surface) 60%)}
.word-card.jp{border-left:3px solid var(--primary);background:linear-gradient(90deg,var(--primary-soft) 0%,var(--surface) 60%)}
.word-card.tech{border-left:3px solid var(--accent);background:linear-gradient(90deg,var(--accent-soft) 0%,var(--surface) 60%)}
.word-card .lang-badge{display:inline-block;font-size:9px;font-weight:700;padding:3px 8px;border-radius:8px;text-transform:uppercase;letter-spacing:.8px;margin-bottom:8px}
.word-card.ar .lang-badge{background:var(--gold-soft);color:var(--gold-light)}
.word-card.jp .lang-badge{background:var(--primary-soft);color:var(--primary-light)}
.word-card.tech .lang-badge{background:var(--accent-soft);color:var(--accent)}
.word-card .word-row{display:flex;align-items:center;gap:10px;margin-bottom:6px;flex-wrap:wrap}
.word-card .word-arabic{font-size:24px;font-weight:500;color:var(--gold-light);direction:rtl;font-family:"Scheherazade New","Amiri",serif}
.word-card .word-jp{font-size:22px;font-weight:500;color:var(--text)}
.word-card .pronounce{background:var(--surface-elevated);border:1px solid var(--border-soft);border-radius:50%;width:32px;height:32px;display:flex;align-items:center;justify-content:center;cursor:pointer;font-size:14px;flex-shrink:0;color:var(--text-soft)}
.word-card .meaning{font-size:14px;color:var(--text);margin-bottom:4px}
.word-card .latin{font-size:12px;color:var(--text-soft);font-style:italic;margin-bottom:8px}
.word-card .example{font-size:12px;color:var(--text-soft);padding:8px 10px;background:var(--bg-deep);border-radius:8px;line-height:1.5;border:1px solid var(--border-soft)}
.dua-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:14px 16px;margin-bottom:8px;box-shadow:var(--shadow-card);border-left:3px solid var(--primary)}
.dua-card .header-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:10px}
.dua-card .prayer-name{font-size:14px;font-weight:700;color:var(--gold-light)}
.dua-card .prayer-time{font-size:11px;color:var(--text-muted);font-family:SF Mono,Menlo,monospace}
.dua-card .arabic{font-size:19px;color:var(--gold);direction:rtl;text-align:right;line-height:1.9;margin-bottom:8px;font-family:"Scheherazade New","Amiri",serif}
.dua-card .latin{font-size:12px;color:var(--text-soft);font-style:italic;margin-bottom:6px;line-height:1.6}
.dua-card .meaning{font-size:13px;color:var(--text);line-height:1.5}
.dua-source{background:var(--gold-soft);border:1px solid var(--border);border-radius:10px;padding:12px 14px;margin-bottom:14px;font-size:12px;color:var(--gold-light);line-height:1.6}
.dua-source .src-title{font-size:10px;color:var(--gold);text-transform:uppercase;letter-spacing:1px;font-weight:700;margin-bottom:4px}
.dede-card{background:linear-gradient(135deg,var(--gold-soft) 0%,var(--surface) 80%);border:1px solid var(--gold);border-radius:14px;padding:18px;margin-bottom:14px;box-shadow:var(--shadow-glow-gold);position:relative;overflow:hidden}
.dede-card::before{content:'☩';position:absolute;top:14px;right:18px;font-size:32px;color:var(--gold);opacity:.3}
.dede-card .label{font-size:10px;color:var(--gold);text-transform:uppercase;letter-spacing:1.2px;font-weight:700;margin-bottom:6px}
.dede-card .title{font-size:16px;color:var(--gold-light);font-weight:700;margin-bottom:10px}
.dede-card .text{font-size:13px;color:var(--text);line-height:1.7}
.dede-card .text b{color:var(--gold-light)}
.sahabe-card{background:linear-gradient(135deg,var(--surface) 0%,var(--surface-elevated) 100%);border:1px solid var(--border);border-radius:14px;padding:16px;margin-bottom:12px;box-shadow:var(--shadow-card)}
.sahabe-card .name{font-size:16px;font-weight:700;color:var(--gold-light);margin-bottom:4px}
.sahabe-card .title{font-size:11px;color:var(--gold);margin-bottom:12px;font-style:italic}
.sahabe-card .story{font-size:13px;color:var(--text);line-height:1.7;margin-bottom:12px}
.sahabe-card .lesson{background:var(--bg-deep);border-left:3px solid var(--primary);padding:10px 12px;border-radius:8px;font-size:12px;color:var(--text-soft);line-height:1.6;font-style:italic}
.sahabe-card .lesson::before{content:'☩  ';color:var(--gold);font-weight:bold}
.sahabe-week-tag{display:inline-block;font-size:10px;padding:3px 10px;background:var(--primary-soft);color:var(--primary-light);border-radius:8px;margin-bottom:10px;text-transform:uppercase;letter-spacing:.8px;font-weight:700}
.blocks{display:flex;flex-direction:column;gap:6px}
.block{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:12px 14px;display:flex;gap:10px;align-items:flex-start;cursor:pointer;transition:all .2s;position:relative}
.block:hover{border-color:var(--primary)}
.block.done{background:var(--bg-deep);opacity:.55}
.block.done .title{text-decoration:line-through;color:var(--text-muted)}
.block-time{flex-shrink:0;font-size:11px;font-weight:600;color:var(--gold);min-width:48px;padding-top:3px;font-family:SF Mono,Menlo,monospace}
.block-icon{flex-shrink:0;width:32px;height:32px;border-radius:8px;background:var(--surface-elevated);display:flex;align-items:center;justify-content:center;font-size:16px;color:var(--gold)}
.block.cat-prayer .block-icon{background:var(--primary-soft);color:var(--primary)}
.block.cat-kuran .block-icon{background:var(--gold-soft);color:var(--gold)}
.block.cat-skill .block-icon{background:var(--primary-soft);color:var(--primary)}
.block.cat-arabic .block-icon{background:var(--gold-soft);color:var(--gold)}
.block-content{flex:1;min-width:0}
.block .title{font-size:14px;font-weight:600;color:var(--text);margin-bottom:2px}
.block .desc{font-size:12px;color:var(--text-soft);line-height:1.4}
.block .steps{font-size:12px;color:var(--text-soft);margin-top:8px;padding-top:8px;border-top:1px dashed var(--border-soft);display:none}
.block.expanded .steps{display:block}
.block .steps ol{padding-left:18px;line-height:1.7}
.block .note{font-size:11px;color:var(--gold);margin-top:8px;padding:6px 8px;background:var(--gold-soft);border-radius:6px;line-height:1.5;display:none}
.block.expanded .note{display:block}
.block-check{width:22px;height:22px;border-radius:6px;border:2px solid var(--border);flex-shrink:0;display:flex;align-items:center;justify-content:center;transition:all .2s;cursor:pointer}
.block-check.checked{background:var(--accent);border-color:var(--accent)}
.block-check.checked::after{content:'✓';color:white;font-weight:bold;font-size:14px}
.kuran-tracker{background:var(--surface);border:1px solid var(--gold-soft);border-radius:14px;padding:14px;margin-bottom:8px;box-shadow:var(--shadow-card)}
.kuran-tracker .row{display:flex;gap:10px;align-items:center;flex-wrap:wrap}
.kuran-tracker label{font-size:12px;color:var(--text-soft)}
.kuran-tracker .pages-input{width:60px;padding:8px 10px;border:1px solid var(--border);border-radius:8px;background:var(--bg-deep);color:var(--gold-light);font-family:inherit;font-size:14px;text-align:center;font-weight:700}
.kuran-tracker .upload-btn{background:var(--primary-soft);border:1px solid var(--primary);padding:8px 12px;border-radius:8px;font-size:12px;color:var(--primary-light);cursor:pointer;font-family:inherit;font-weight:600}
.kuran-tracker input[type="file"]{display:none}
.kuran-tracker .photo-preview{width:50px;height:50px;border-radius:8px;object-fit:cover;border:1px solid var(--border);display:none}
.kuran-tracker .photo-preview.show{display:block}
.week-info{background:linear-gradient(135deg,#0E2A3F 0%,var(--surface) 100%);border:1px solid var(--accent);border-radius:14px;padding:14px 16px;margin-bottom:12px;box-shadow:0 0 20px rgba(16,185,129,.2)}
.week-info .week-num{font-size:11px;color:var(--accent);text-transform:uppercase;letter-spacing:1px;font-weight:700}
.week-info .week-name{font-size:16px;font-weight:700;color:var(--gold);margin-top:4px}
.week-info .week-desc{font-size:13px;color:var(--text);margin-top:6px;line-height:1.5}
.exercise-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:12px 14px;margin-bottom:8px;display:flex;align-items:center;gap:12px;cursor:pointer;transition:all .2s}
.exercise-card.done{background:var(--bg-deep);opacity:.6}
.exercise-card.done .ex-name{text-decoration:line-through;color:var(--text-muted)}
.ex-check{width:22px;height:22px;border-radius:6px;border:2px solid var(--border);flex-shrink:0;display:flex;align-items:center;justify-content:center}
.exercise-card.done .ex-check{background:var(--accent);border-color:var(--accent)}
.exercise-card.done .ex-check::after{content:'✓';color:white;font-weight:bold}
.ex-name{font-size:14px;font-weight:600;color:var(--text)}
.ex-detail{font-size:12px;color:var(--text-soft);margin-top:2px}
.code-card{background:var(--surface);border:1px solid var(--border-tech);border-radius:12px;padding:14px;margin-bottom:10px;box-shadow:var(--shadow-card);position:relative;overflow:hidden}
.code-card .level-badge{display:inline-block;font-size:9px;padding:3px 8px;background:var(--primary-soft);color:var(--primary);border-radius:6px;text-transform:uppercase;letter-spacing:.8px;font-weight:700;margin-bottom:8px}
.code-card .level-badge.ileri{background:var(--rose-soft);color:var(--rose)}
.code-card .proj-name{font-size:15px;font-weight:700;color:var(--text);margin-bottom:4px;font-family:SF Mono,Menlo,monospace}
.code-card .proj-desc{font-size:12px;color:var(--text-soft);line-height:1.6;margin-bottom:8px}
.code-card .tech-stack{display:flex;flex-wrap:wrap;gap:5px}
.code-card .tech-tag{font-size:10px;padding:2px 8px;background:var(--bg-deep);color:var(--primary);border-radius:6px;border:1px solid var(--border-soft);font-family:SF Mono,Menlo,monospace}
.entrepreneur-card{background:linear-gradient(135deg,var(--surface) 0%,var(--surface-elevated) 100%);border:1px solid var(--border-soft);border-radius:14px;padding:16px;margin-bottom:10px;box-shadow:var(--shadow-card)}
.entrepreneur-card .country{display:inline-block;font-size:18px;margin-right:6px}
.entrepreneur-card .name{font-size:16px;font-weight:700;color:var(--gold-light);margin-bottom:2px;display:inline-block}
.entrepreneur-card .role{font-size:11px;color:var(--primary);margin-bottom:10px;font-style:italic}
.entrepreneur-card .story{font-size:12px;color:var(--text);line-height:1.6;margin-bottom:10px}
.entrepreneur-card .lesson{background:var(--bg-deep);border-left:3px solid var(--accent);padding:8px 12px;border-radius:6px;font-size:11px;color:var(--text-soft);line-height:1.6}
.entrepreneur-card .lesson::before{content:'➤  ';color:var(--accent);font-weight:bold}
.book-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:14px;margin-bottom:10px;box-shadow:var(--shadow-card);border-left:3px solid var(--gold)}
.book-card .b-cat{font-size:9px;padding:2px 8px;background:var(--gold-soft);color:var(--gold);border-radius:5px;text-transform:uppercase;letter-spacing:.8px;font-weight:700;display:inline-block;margin-bottom:8px}
.book-card .b-cat.tech{background:var(--primary-soft);color:var(--primary)}
.book-card .b-cat.bio{background:var(--accent-soft);color:var(--accent)}
.book-card .b-cat.fels{background:var(--rose-soft);color:var(--rose)}
.book-card .b-name{font-size:14px;font-weight:700;color:var(--text);margin-bottom:2px}
.book-card .b-author{font-size:12px;color:var(--text-soft);margin-bottom:8px;font-style:italic}
.book-card .b-why{font-size:12px;color:var(--text);line-height:1.6}
.book-tracker{background:linear-gradient(135deg,var(--gold-soft) 0%,var(--surface) 100%);border:1px solid var(--gold);border-radius:14px;padding:16px;margin-bottom:14px;box-shadow:var(--shadow-glow-gold)}
.book-tracker .label{font-size:10px;color:var(--gold);text-transform:uppercase;letter-spacing:1px;margin-bottom:6px;font-weight:700}
.book-tracker input{width:100%;padding:10px 12px;border:1px solid var(--border);border-radius:8px;background:var(--bg-deep);color:var(--text);font-family:inherit;font-size:14px;outline:none;margin-bottom:10px}
.book-tracker input:focus{border-color:var(--gold)}
.book-tracker .stats-row{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:8px}
.book-tracker .mini-stat{background:var(--bg-deep);border-radius:8px;padding:8px 10px;text-align:center}
.book-tracker .mini-stat .num{font-size:20px;font-weight:700;color:var(--gold)}
.book-tracker .mini-stat .lbl{font-size:9px;color:var(--text-muted);text-transform:uppercase;letter-spacing:.8px}
.kutuphane-link{background:var(--primary-soft);border:1px solid var(--primary);border-radius:10px;padding:12px 14px;font-size:12px;color:var(--primary-light);line-height:1.5;margin-bottom:12px}
.kutuphane-link a{color:var(--primary);text-decoration:underline;font-weight:600}
.journal-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:14px;box-shadow:var(--shadow-card)}
.journal-line{display:flex;gap:10px;margin-bottom:8px;align-items:center}
.journal-num{width:22px;height:22px;border-radius:50%;background:var(--gold-soft);color:var(--gold);display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:700;flex-shrink:0}
.journal-input{flex:1;padding:8px 10px;border:1px solid var(--border-soft);border-radius:8px;background:var(--bg-deep);color:var(--text);font-family:inherit;font-size:13px;outline:none;transition:border .2s}
.journal-input:focus{border-color:var(--gold)}
.prompt-card{background:linear-gradient(135deg,var(--primary-soft) 0%,var(--surface) 100%);border:1px solid var(--border-tech);border-radius:12px;padding:14px 16px;margin-bottom:12px}
.prompt-card .prompt-label{font-size:10px;color:var(--primary);text-transform:uppercase;letter-spacing:1px;font-weight:700;margin-bottom:6px}
.prompt-card .prompt-text{font-size:14px;color:var(--text);line-height:1.6}
.creative-textarea{width:100%;min-height:140px;padding:12px;border:1px solid var(--border-soft);border-radius:10px;background:var(--bg-deep);color:var(--text);font-family:inherit;font-size:14px;resize:vertical;line-height:1.6;outline:none}
.creative-textarea:focus{border-color:var(--primary)}
.email-btn{background:linear-gradient(135deg,var(--accent) 0%,#059669 100%);color:white;border:none;border-radius:12px;padding:14px 20px;font-size:14px;font-weight:700;cursor:pointer;font-family:inherit;width:100%;margin:14px 0;box-shadow:0 0 18px rgba(16,185,129,.3);display:flex;align-items:center;justify-content:center;gap:8px}
.email-btn:active{transform:scale(.98)}
.settings-card{background:var(--surface);border:1px solid var(--border-soft);border-radius:12px;padding:14px;margin-bottom:10px}
.settings-card .label{font-size:11px;color:var(--text-muted);text-transform:uppercase;letter-spacing:.8px;margin-bottom:6px}
.settings-card .value{font-size:14px;color:var(--text);margin-bottom:10px}
.settings-card input{width:100%;padding:8px 10px;border:1px solid var(--border-soft);border-radius:8px;background:var(--bg-deep);color:var(--text);font-family:inherit;font-size:13px;outline:none;margin-bottom:8px}
.settings-card button{background:var(--surface-elevated);border:1px solid var(--border);padding:8px 14px;border-radius:8px;font-size:12px;color:var(--text);cursor:pointer;font-family:inherit;font-weight:600;margin-right:6px}
.settings-card button.danger{color:#F87171;border-color:rgba(248,113,113,.3)}
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.85);z-index:100;align-items:center;justify-content:center;padding:24px}
.modal-overlay.show{display:flex;animation:fadeIn .3s}
.modal{background:linear-gradient(135deg,var(--surface) 0%,var(--surface-elevated) 100%);border:1px solid var(--gold);border-radius:16px;padding:24px;max-width:380px;width:100%;text-align:center;box-shadow:var(--shadow-glow-gold)}
.modal .gift{font-size:56px;margin-bottom:14px}
.modal .ornament{font-size:18px;font-weight:700;color:var(--gold);margin-bottom:8px}
.modal .modal-msg{font-size:13px;color:var(--text);line-height:1.6;margin-bottom:18px}
.modal .modal-close{background:linear-gradient(135deg,var(--primary-dark) 0%,var(--primary) 100%);color:var(--bg);border:none;border-radius:10px;padding:12px 28px;font-size:14px;font-weight:700;cursor:pointer;font-family:inherit}
</style>
</head>
<body>
<div class="app">
<div class="setup-screen" id="setup">
  <div class="arabic-title" style="font-size:32px;line-height:1.5;margin-bottom:32px">بِسْمِ ٱللَّٰهِ ٱلرَّحْمَٰنِ ٱلرَّحِيمِ</div>
  <input type="text" id="nameInput" placeholder="İsmini yaz" />
  <button onclick="completeSetup()">Başla</button>
</div>
<div id="app" style="display:none">
  <div class="header">
    <div class="greeting">
      <div class="salam">ٱلسَّلَامُ عَلَيْكُم</div>
      <div class="arabic-name">ٱلْفَارُوق</div>
      <div class="name" id="userName"></div>
    </div>
    <div class="date-pill"><div class="day" id="dayName"></div><div class="date" id="dateStr"></div></div>
  </div>
  <div class="tabs">
    <button class="tab active" onclick="showView('today',this)">Bugün</button>
    <button class="tab" onclick="showView('goal',this)">Hedef</button>
    <button class="tab" onclick="showView('learn',this)">Öğren</button>
    <button class="tab" onclick="showView('sahabe',this)">Sahâbe</button>
    <button class="tab" onclick="showView('sport',this)">Spor</button>
    <button class="tab" onclick="showView('code',this)">Kod</button>
    <button class="tab" onclick="showView('book',this)">Kitap</button>
    <button class="tab" onclick="showView('write',this)">Yaz</button>
    <button class="tab" onclick="showView('settings',this)">⚙</button>
  </div>
  <div id="view-today" class="view active">
    <div class="banner" id="banner"></div>
    <div class="kuzey-yildizi">
      <div class="icon">🧭</div>
      <div><div class="label">Kuzey Yıldızı</div><div class="text">Medine → Tokyo. Bugünkü her küçük adım, oraya bir tuğla.</div></div>
    </div>
    <div class="stats">
      <div class="stat-card streak"><div class="label">Zincirim</div><div class="number"><span id="streakNum">0</span><span class="unit">gün</span></div><div class="chain" id="streakChain"></div></div>
      <div class="stat-card progress"><div class="label">Bugün</div><div class="number"><span id="todayPct">0</span><span class="unit">%</span></div><div class="progress-bar"><div class="progress-fill" id="progressFill" style="width:0%"></div></div></div>
      <div class="stat-card sport"><div class="label">Spor seviyesi</div><div class="number">Hf <span id="sportWeek">1</span></div></div>
      <div class="stat-card kuran"><div class="label">Kuran sayfası</div><div class="number"><span id="totalPages">0</span></div></div>
    </div>
    <div class="section-title">Bugünün programı</div>
    <div class="blocks" id="blocksList"></div>
    <div class="section-title gold">Bugünün Kuran takibi</div>
    <div class="kuran-tracker"><div class="row">
      <label>Bugün okuduğum sayfa:</label>
      <input type="number" class="pages-input" id="kuranPages" min="0" max="100" onchange="saveKuran()" />
      <label for="kuranPhoto" class="upload-btn">📷 Foto yükle</label>
      <input type="file" id="kuranPhoto" accept="image/*" onchange="uploadKuranPhoto(event)" />
      <img class="photo-preview" id="kuranPreview" />
    </div></div>
    <div class="section-title">Bugünün sporu</div>
    <div id="todaySport"></div>
    <div class="section-title gold">Akşam defteri — bugün başardığım</div>
    <div class="journal-card">
      <div class="journal-line"><div class="journal-num">1</div><input type="text" class="journal-input" id="j1" placeholder="Bugün başardığım birinci şey..." onchange="saveJournal()" /></div>
      <div class="journal-line"><div class="journal-num">2</div><input type="text" class="journal-input" id="j2" placeholder="İkinci..." onchange="saveJournal()" /></div>
      <div class="journal-line"><div class="journal-num">3</div><input type="text" class="journal-input" id="j3" placeholder="Üçüncü..." onchange="saveJournal()" /></div>
    </div>
    <button class="email-btn" onclick="sendDailyReport()">📧 Gün Sonu — Anne &amp; Babaya Gönder</button>
  </div>
  <div id="view-goal" class="view">
    <div class="goal-hero">
      <div class="arabic-quote">وَأَن لَّيْسَ لِلْإِنسَانِ إِلَّا مَا سَعَىٰ</div>
      <div class="quote-meaning">"İnsan için ancak çalıştığı vardır." — Necm 39</div>
      <div class="destinations">
        <div class="dest"><div class="icon">🕋</div><div class="label">İlk Durak</div><div class="place">Medine<br>İslam Üniversitesi</div></div>
        <div class="dest"><div class="icon">🌸</div><div class="label">Sonra</div><div class="place">Tokyo / Singapore<br>AI &amp; Robotik</div></div>
      </div>
    </div>
    <div class="countdown-card"><div class="label">Bu yola adım atalı</div><div class="big-num" id="totalDays">0</div><div class="small">gün geçti</div></div>
    <div class="section-title">Bu yıl yapacaklarım (16 yaş)</div>
    <div class="checklist-card">
      <div class="ch-year">2026 — Lise yılı</div>
      <div class="ch-title">Tıkla, başardığında işaretle</div>
      <div id="checklist16"></div>
    </div>
    <div class="section-title">Sonraki aşamalar</div>
    <div id="roadmapList"></div>
  </div>
  <div id="view-learn" class="view">
    <div class="section-title gold">Bugünün Arapça kelimeleri (3)</div>
    <div id="arabicWords"></div>
    <div class="section-title">Bugünün Japonca kelimeleri (3)</div>
    <div id="japaneseWords"></div>
    <div class="section-title">Tech Arapçası — yazılım dünyası</div>
    <div id="techArabicWords"></div>
    <div class="section-title gold">5 vakit namaz duaları</div>
    <div class="dua-source">
      <div class="src-title">Kaynak</div>
      Dualar <a href="https://eraykitap.com/" target="_blank" style="color:var(--gold);text-decoration:underline">eraykitap.com</a> sitesinden alınmıştır.
    </div>
    <div id="prayersList"></div>
    <div class="section-title">Bu haftanın sîreti</div>
    <div id="siretWeek"></div>
  </div>
  <div id="view-sahabe" class="view">
    <div class="section-title gold">Bu haftanın sahâbesi</div>
    <div id="weekSahabe"></div>
    <div class="section-title">Tüm sahâbeler — keşfet</div>
    <div id="allSahabe"></div>
  </div>
  <div id="view-sport" class="view">
    <div class="section-title">Bu haftanın seviyesi</div>
    <div id="sportWeekInfo"></div>
    <div class="section-title">Bugünün antrenmanı</div>
    <div id="sportList"></div>
  </div>
  <div id="view-code" class="view">
    <div class="banner" style="background:linear-gradient(135deg,var(--primary-soft) 0%,var(--surface) 100%);color:var(--primary);border-color:var(--border-tech)">// Yenilikçi ol. "Yapılmış" diye bir şey yok — sadece "henüz senin yapmadığın" var.</div>
    <div class="section-title">Önerilen projeler — kendin yap</div>
    <div id="codeProjects"></div>
    <div class="section-title gold">Son 100 yılın ilham verici girişimcileri</div>
    <div id="entrepreneurs"></div>
  </div>
  <div id="view-book" class="view">
    <div class="banner" style="background:linear-gradient(135deg,var(--gold-soft) 0%,var(--surface) 100%);color:var(--gold-light);border-color:var(--border)">📚 Mühendis çok okur. Hayalin büyükse, kütüphanen büyük olmalı.</div>
    <div class="kutuphane-link">🏛️ <b>Qatar National Library</b> kart sahibi olduğunda binlerce kitap bedava: <a href="https://www.qnl.qa/" target="_blank">qnl.qa</a> — Faruk, Doha'da yaşıyorsan bu kütüphane senin sermayen.</div>
    <div class="section-title gold">Şu an okuduğum kitap</div>
    <div class="book-tracker">
      <div class="label">Kitap adı</div>
      <input type="text" id="currentBook" placeholder="Kitap adı, yazar..." onchange="saveBook()" />
      <div class="label">Bugün etkilendiğim bir cümle</div>
      <input type="text" id="bookQuote" placeholder="Beni etkileyen bir cümle..." onchange="saveBookQuote()" />
      <div class="stats-row">
        <div class="mini-stat"><div class="num" id="bookPagesNum">0</div><div class="lbl">Bugün okudum (sayfa)</div></div>
        <div class="mini-stat"><div class="num" id="totalBooks">0</div><div class="lbl">Bitirdiğim kitap</div></div>
      </div>
      <div class="label" style="margin-top:10px">Bugün okuduğum sayfa</div>
      <input type="number" id="bookPages" min="0" max="500" placeholder="0" onchange="saveBookPages()" />
      <button onclick="finishBook()" style="background:var(--gold);color:var(--bg);border:none;border-radius:8px;padding:8px 14px;font-size:12px;font-weight:700;cursor:pointer;font-family:inherit;margin-top:8px">✓ Bu kitabı bitirdim</button>
    </div>
    <div class="section-title">Önerilen kitaplar — Faruk için seçildi</div>
    <div id="bookList"></div>
    <div class="section-title gold">Hadis &amp; Ayet — bugünün sözü</div>
    <div id="dailyWisdom"></div>
  </div>
  <div id="view-write" class="view">
    <div class="banner" style="background:linear-gradient(135deg,var(--rose-soft) 0%,var(--surface) 100%);color:var(--rose);border-color:rgba(244,114,182,.2)">✎ Anlatmayı, araştırmayı seven bir Faruk var. Buraya dök. Kimse okumayacak — sadece sen.</div>
    <div class="section-title">Bugünün yazı konusu</div>
    <div class="prompt-card"><div class="prompt-label">Bugün düşün, yaz</div><div class="prompt-text" id="todayPrompt"></div></div>
    <textarea class="creative-textarea" id="creativeText" placeholder="Yazmaya başla. Hata yok. Düşünce akışı." onchange="saveCreative()"></textarea>
    <div class="section-title gold">İlham — proactive sorular</div>
    <div id="proactivePrompts"></div>
  </div>
  <div id="view-settings" class="view">
    <div class="section-title">Ayarlar</div>
    <div class="settings-card"><div class="label">İsim</div><div class="value" id="currentName"></div><button onclick="changeName()">İsmi değiştir</button></div>
    <div class="settings-card">
      <div class="label">Anne &amp; Baba E-posta (gün sonu raporu için)</div>
      <input type="email" id="babaEmail" placeholder="Baba e-posta" onchange="saveEmails()" />
      <input type="email" id="anneEmail" placeholder="Anne e-posta" onchange="saveEmails()" />
      <div style="font-size:11px;color:var(--text-muted);line-height:1.5;margin-top:6px">"Gün Sonu — Anne &amp; Babaya Gönder" butonuna basınca bu adreslere otomatik özet gider.</div>
    </div>
    <div class="settings-card"><div class="label">Veri</div><div class="value">Tüm verilerin telefonunda saklı.</div><button onclick="exportData()">Yedek al</button></div>
    <div class="settings-card"><div class="label">Sıfırla</div><div class="value">Tüm verilerini siler. Geri alınamaz.</div><button class="danger" onclick="resetAll()">Sıfırla</button></div>
    <div class="settings-card"><div class="label">Hakkında</div><div class="value">Babanın sana özel hazırladığı uygulama.<br>Dualar: eraykitap.com<br>v3.0</div></div>
  </div>
</div>
<div class="modal-overlay" id="modalOverlay"><div class="modal"><div class="gift" id="modalIcon">🎁</div><div class="ornament" id="modalOrnament">Tebrikler</div><div class="modal-msg" id="modalMsg"></div><button class="modal-close" onclick="closeModal()">Devam et</button></div></div>
</div>
<script>
const STORAGE_KEY='programim_faruk_v3';
const DAY_NAMES=['Pazar','Pazartesi','Salı','Çarşamba','Perşembe','Cuma','Cumartesi'];
const SAT_DATE='2026-06-06';
const SAT_LAST_STUDY='2026-06-05';
const SCHOOL_END='2026-06-28';
const ARABIC_WORDS=[
{word:'مَال',latin:'mâl',meaning:'mal, servet',example:'الْمَال أَمَانَة — Mâl emanettir'},
{word:'تِجَارَة',latin:'ticârah',meaning:'ticaret',example:'التِّجَارَة بَرَكَة — Ticaret berekettir'},
{word:'عَمَل',latin:'amel',meaning:'iş, çalışma',example:'الْعَمَلُ عِبَادَة — Çalışma ibadettir'},
{word:'نَجَاح',latin:'necâh',meaning:'başarı',example:'النَّجَاحُ بِالصَّبْر — Başarı sabırla'},
{word:'هَدَف',latin:'hedef',meaning:'hedef',example:'هَدَفِي وَاضِح — Hedefim net'},
{word:'حِكْمَة',latin:'hikme',meaning:'hikmet',example:'كَلِمَةٌ فِيهَا حِكْمَة — Hikmetli söz'},
{word:'عِلْم',latin:'ilm',meaning:'ilim',example:'الْعِلْمُ نُور — İlim nurdur'},
{word:'صَبْر',latin:'sabr',meaning:'sabır',example:'الصَّبْرُ مِفْتَاحُ الْفَرَج — Sabır kurtuluş anahtarı'},
{word:'كِتَاب',latin:'kitâb',meaning:'kitap',example:'الْكِتَابُ خَيْرُ صَدِيق — Kitap en iyi dost'},
{word:'قَلَم',latin:'kalem',meaning:'kalem',example:'بِالْقَلَمِ يُكْتَبُ التَّارِيخ — Kalemle yazılır tarih'},
{word:'مَدْرَسَة',latin:'medrese',meaning:'okul',example:'الْمَدْرَسَةُ بَيْتٌ ثَانٍ — Okul ikinci ev'},
{word:'جَامِعَة',latin:'câmiah',meaning:'üniversite',example:'سَأَدْرُسُ فِي الْجَامِعَة — Üniversitede okuyacağım'},
{word:'الْمَدِينَة',latin:'el-medîne',meaning:'Medine, şehir',example:'الْمَدِينَةُ الْمُنَوَّرَة — Münevver Medine'},
{word:'مَكَّة',latin:'mekke',meaning:'Mekke',example:'مَكَّةُ الْمُكَرَّمَة — Mükerrem Mekke'},
{word:'مَسْجِد',latin:'mescid',meaning:'mescid',example:'الْمَسْجِدُ بَيْتُ الله — Mescid Allah\'ın evi'},
{word:'صَلَاة',latin:'salât',meaning:'namaz',example:'الصَّلَاةُ عَمُودُ الدِّين — Namaz dinin direği'},
{word:'قُرْآن',latin:'kur\'ân',meaning:'Kur\'an',example:'الْقُرْآنُ نُور — Kur\'an nurdur'},
{word:'حَدِيث',latin:'hadîs',meaning:'hadis',example:'حَدِيثُ النَّبِيِّ شِفَاء — Peygamberin hadisi şifa'},
{word:'سُنَّة',latin:'sünne',meaning:'sünnet, yol',example:'سُنَّةُ الْمُصْطَفَى — Mustafa\'nın yolu'},
{word:'إِيمَان',latin:'îmân',meaning:'iman',example:'الْإِيمَانُ قُوَّة — İman güçtür'},
{word:'أَخْلَاق',latin:'ahlâk',meaning:'ahlâk',example:'الْأَخْلَاقُ تَاج — Ahlâk taçtır'},
{word:'أَدَب',latin:'edeb',meaning:'edeb, terbiye',example:'الْأَدَبُ خَيْرٌ مِنَ الْعِلْم — Edeb ilimden hayırlı'},
{word:'صَدِيق',latin:'sadîk',meaning:'dost, arkadaş',example:'الصَّدِيقُ وَقْتَ الضِّيق — Dost dar günde'},
{word:'أَخ',latin:'eh',meaning:'kardeş',example:'الْمُؤْمِنُ أَخُ الْمُؤْمِن — Mümin müminin kardeşi'},
{word:'أَب',latin:'eb',meaning:'baba',example:'أَبِي قُدْوَتِي — Babam örneğim'},
{word:'أُمّ',latin:'ümm',meaning:'anne',example:'الْجَنَّةُ تَحْتَ أَقْدَامِ الْأُمَّهَات — Cennet annelerin ayağı altında'},
{word:'ابْن',latin:'ibn',meaning:'oğul',example:'ابْنِي ذَكِيّ — Oğlum zeki'},
{word:'أُسْرَة',latin:'üsra',meaning:'aile',example:'الْأُسْرَةُ نَواةُ الْمُجْتَمَع — Aile toplum çekirdeği'},
{word:'بَيْت',latin:'beyt',meaning:'ev',example:'بَيْتِي جَنَّتِي — Evim cennetim'},
{word:'وَطَن',latin:'vatan',meaning:'vatan',example:'حُبُّ الْوَطَنِ مِنَ الْإِيمَان — Vatan sevgisi imandan'},
{word:'سَفَر',latin:'sefer',meaning:'yolculuk',example:'فِي السَّفَرِ فَوَائِد — Yolculukta faydalar var'},
{word:'طَرِيق',latin:'tarîk',meaning:'yol',example:'طَرِيقُ النَّجَاحِ مُمْتَلِئٌ بِالصَّبْر — Başarı yolu sabırla'},
{word:'رِزْق',latin:'rızk',meaning:'rızık',example:'الرِّزْقُ مِنَ الله — Rızık Allah\'tan'},
{word:'بَرَكَة',latin:'bereket',meaning:'bereket',example:'الْبَرَكَةُ فِي الْجَمَاعَة — Bereket cemaatte'},
{word:'شُكْر',latin:'şükr',meaning:'şükür',example:'الشُّكْرُ نِصْفُ الْإِيمَان — Şükür imanın yarısı'},
{word:'تَوَكُّل',latin:'tevekkül',meaning:'tevekkül',example:'تَوَكَّلْ عَلَى الله — Allah\'a tevekkül et'},
{word:'صِدْق',latin:'sıdk',meaning:'doğruluk',example:'الصِّدْقُ يَنْجُو — Doğruluk kurtarır'},
{word:'أَمَانَة',latin:'emâne',meaning:'emanet',example:'الْأَمَانَةُ شَرَف — Emanet şereftir'},
{word:'عَدَالَة',latin:'adâle',meaning:'adalet',example:'الْعَدْلُ أَسَاسُ الْمُلْك — Adalet mülkün temeli'},
{word:'عَزْم',latin:'azm',meaning:'azim',example:'بِالْعَزْمِ تُفْتَحُ الْأَبْوَاب — Azimle kapılar açılır'},
{word:'هِمَّة',latin:'himmet',meaning:'gayret',example:'الْهِمَّةُ تَصْنَعُ الْمُعْجِزَات — Himmet mucizeler yaratır'},
{word:'مُسْتَقْبَل',latin:'müstakbel',meaning:'gelecek',example:'مُسْتَقْبَلِي بِيَدَيَّ — Geleceğim ellerimde'},
{word:'تَطَوُّر',latin:'tatavvur',meaning:'gelişme',example:'التَّطَوُّرُ ضَرُورِيّ — Gelişme zorunlu'},
{word:'ذَهَب',latin:'zeheb',meaning:'altın',example:'الْوَقْتُ كَالذَّهَب — Vakit altın gibi'},
{word:'سُوق',latin:'sûk',meaning:'çarşı, pazar',example:'سُوقُ الْمَدِينَة — Medine pazarı'},
{word:'حَلَال',latin:'helâl',meaning:'helâl',example:'الْكَسْبُ الْحَلَال — Helâl kazanç'},
{word:'وَقْت',latin:'vakt',meaning:'vakit, zaman',example:'الْوَقْتُ كَالسَّيْف — Vakit kılıç gibi'},
{word:'قُوَّة',latin:'kuvve',meaning:'güç',example:'لَا قُوَّةَ إِلَّا بِالله — Güç ancak Allah\'tan'},
{word:'شَجَاعَة',latin:'şecâa',meaning:'cesaret',example:'الشَّجَاعَةُ صَبْرٌ مُسَاعَة — Cesaret bir saatlik sabırdır'},
{word:'كَرَم',latin:'kerem',meaning:'cömertlik',example:'الْكَرَمُ مِنَ الْإِيمَان — Cömertlik imandan'}
];
const TECH_ARABIC=[
{word:'بَرْمَجَة',latin:'bermece',meaning:'programlama, kodlama',example:'أَتَعَلَّمُ الْبَرْمَجَة — Eteallemu\'l-bermece — Programlama öğreniyorum'},
{word:'شِيفْرَة',latin:'şifrah',meaning:'kod',example:'كَتَبْتُ شِيفْرَة جَدِيدَة — Yeni kod yazdım'},
{word:'خَوَارِزْمِيَّة',latin:'hârizmiyyah',meaning:'algoritma',example:'الْخَوَارِزْمِيَّة قَلْبُ الْحَاسُوب — Algoritma bilgisayarın kalbi (İsim Harizmî matematikçiden geliyor)'},
{word:'بَيَانَات',latin:'beyânât',meaning:'data, veri',example:'الْبَيَانَاتُ ذَهَبُ الْعَصْر — Veri çağın altını'},
{word:'حَاسُوب',latin:'hâsûb',meaning:'bilgisayar',example:'حَاسُوبِي قَوِيّ — Bilgisayarım güçlü'},
{word:'ذَكَاء اِصْطِنَاعِيّ',latin:'zekâ\' istinâî',meaning:'yapay zeka',example:'الذَّكَاءُ الاصْطِنَاعِيّ مُسْتَقْبَل — AI gelecektir'},
{word:'تَطْبِيق',latin:'tatbîk',meaning:'uygulama, app',example:'بَنَيْتُ تَطْبِيقًا — Bir uygulama yaptım'},
{word:'مَوْقِع',latin:'mevkı',meaning:'website',example:'مَوْقِعِي عَلَى الإِنْتَرْنِت — Sitem internette'},
{word:'شَبَكَة',latin:'şebeke',meaning:'network',example:'شَبَكَةُ الإِنْتَرْنِت — İnternet ağı'},
{word:'نِظَام',latin:'nizâm',meaning:'sistem',example:'نِظَامُ التَّشْغِيل — İşletim sistemi'},
{word:'مُتَغَيِّر',latin:'mütegayyir',meaning:'değişken (variable)',example:'الْمُتَغَيِّر يَحْفَظُ الْقِيَم — Değişken değer saklar'},
{word:'دَالَّة',latin:'dâlle',meaning:'fonksiyon',example:'كَتَبْتُ دَالَّة جَدِيدَة — Yeni fonksiyon yazdım'},
{word:'قَاعِدَة بَيَانَات',latin:'kâidetü beyânât',meaning:'database',example:'قَاعِدَةُ الْبَيَانَات تَنْمُو — Veritabanı büyüyor'},
{word:'خَادِم',latin:'hâdim',meaning:'server',example:'الْخَادِم يُشَغِّلُ الْمَوْقِع — Server siteyi çalıştırır'},
{word:'رُوبُوت',latin:'robot',meaning:'robot',example:'سَأَصْنَعُ رُوبُوتًا — Bir robot yapacağım'},
{word:'هَنْدَسَة بَرْمَجِيَّة',latin:'hendese bermeciyye',meaning:'yazılım mühendisliği',example:'دَرَسْتُ هَنْدَسَة بَرْمَجِيَّة — Yazılım mühendisliği okudum'},
{word:'ذَاكِرَة',latin:'zâkire',meaning:'memory, hafıza',example:'الذَّاكِرَة مَهَمَّة — Hafıza önemli'},
{word:'مُعَالِج',latin:'muâlic',meaning:'işlemci (CPU)',example:'مُعَالِج سَرِيع — Hızlı işlemci'}
];
const JAPANESE_WORDS=[
{word:'こんにちは',latin:'konnichiwa',meaning:'merhaba',example:'こんにちは、ファルク です — Merhaba, ben Faruk'},
{word:'ありがとう',latin:'arigatō',meaning:'teşekkür',example:'ありがとう ございます — Teşekkür ederim'},
{word:'すみません',latin:'sumimasen',meaning:'pardon, özür',example:'すみません、わかりません — Pardon, anlamıyorum'},
{word:'はい',latin:'hai',meaning:'evet',example:'はい、わかりました — Evet, anladım'},
{word:'いいえ',latin:'iie',meaning:'hayır',example:'いいえ、ちがいます — Hayır, yanlış'},
{word:'お願いします',latin:'onegaishimasu',meaning:'lütfen',example:'みず を おねがいします — Su lütfen'},
{word:'学校',latin:'gakkō',meaning:'okul',example:'がっこう に いきます — Okula gidiyorum'},
{word:'大学',latin:'daigaku',meaning:'üniversite',example:'とうきょう だいがく — Tokyo Üniversitesi'},
{word:'学生',latin:'gakusei',meaning:'öğrenci',example:'わたし は がくせい です — Ben öğrenciyim'},
{word:'先生',latin:'sensei',meaning:'öğretmen, hoca',example:'せんせい、しつもん が あります — Hocam, sorum var'},
{word:'勉強',latin:'benkyō',meaning:'çalışma',example:'べんきょう が だいすき — Çalışmayı seviyorum'},
{word:'本',latin:'hon',meaning:'kitap',example:'ほん を よみます — Kitap okuyorum'},
{word:'友達',latin:'tomodachi',meaning:'arkadaş',example:'いい ともだち — İyi arkadaş'},
{word:'家族',latin:'kazoku',meaning:'aile',example:'かぞく が だいじ — Aile önemli'},
{word:'父',latin:'chichi',meaning:'baba (kendi)',example:'ちち は シェフ です — Babam şef'},
{word:'母',latin:'haha',meaning:'anne (kendi)',example:'はは は やさしい — Annem nazik'},
{word:'兄弟',latin:'kyōdai',meaning:'kardeşler',example:'きょうだい が います — Kardeşim var'},
{word:'家',latin:'ie',meaning:'ev',example:'いえ に かえります — Eve dönüyorum'},
{word:'国',latin:'kuni',meaning:'ülke',example:'わたし の くに は トルコ — Ülkem Türkiye'},
{word:'日本',latin:'nihon',meaning:'Japonya',example:'にほん に いきたい — Japonya\'ya gitmek istiyorum'},
{word:'言葉',latin:'kotoba',meaning:'kelime, dil',example:'あたらしい ことば — Yeni kelime'},
{word:'日本語',latin:'nihongo',meaning:'Japonca',example:'にほんご を べんきょう します — Japonca çalışıyorum'},
{word:'アラビア語',latin:'arabiago',meaning:'Arapça',example:'アラビアご が じょうず — Arapçam iyi'},
{word:'英語',latin:'eigo',meaning:'İngilizce',example:'えいご も はなします — İngilizce de konuşuyorum'},
{word:'トルコ語',latin:'torukogo',meaning:'Türkçe',example:'トルコご は ぼご — Türkçe ana dilim'},
{word:'ロボット',latin:'robotto',meaning:'robot',example:'ロボット を つくりたい — Robot yapmak istiyorum'},
{word:'コンピューター',latin:'konpyūtā',meaning:'bilgisayar',example:'コンピューター が すき — Bilgisayarı seviyorum'},
{word:'プログラム',latin:'puroguramu',meaning:'program',example:'プログラム を かきます — Program yazıyorum'},
{word:'プログラマー',latin:'puroguramā',meaning:'programcı',example:'いい プログラマー に なりたい — İyi programcı olmak istiyorum'},
{word:'人工知能',latin:'jinkō chinō',meaning:'yapay zeka',example:'じんこうちのう の みらい — AI\'nın geleceği'},
{word:'科学',latin:'kagaku',meaning:'bilim',example:'かがく は おもしろい — Bilim ilginç'},
{word:'数学',latin:'sūgaku',meaning:'matematik',example:'すうがく が とくい — Matematikte iyiyim'},
{word:'工学',latin:'kōgaku',meaning:'mühendislik',example:'こうがく を まなびます — Mühendislik öğreniyorum'},
{word:'技術',latin:'gijutsu',meaning:'teknoloji',example:'あたらしい ぎじゅつ — Yeni teknoloji'},
{word:'仕事',latin:'shigoto',meaning:'iş',example:'しごと は たのしい — İş eğlenceli'},
{word:'会社',latin:'kaisha',meaning:'şirket',example:'じぶん の かいしゃ — Kendi şirketim'},
{word:'お金',latin:'okane',meaning:'para',example:'おかね を ためる — Para biriktirmek'},
{word:'時間',latin:'jikan',meaning:'zaman',example:'じかん が たいせつ — Zaman önemli'},
{word:'今日',latin:'kyō',meaning:'bugün',example:'きょう は いい ひ — Bugün iyi gün'},
{word:'明日',latin:'ashita',meaning:'yarın',example:'あした がんばる — Yarın çabalayacağım'},
{word:'朝',latin:'asa',meaning:'sabah',example:'あさ の いのり — Sabah duası'},
{word:'夜',latin:'yoru',meaning:'gece',example:'よる は しずか — Gece sessiz'},
{word:'食べ物',latin:'tabemono',meaning:'yemek',example:'おいしい たべもの — Lezzetli yemek'},
{word:'水',latin:'mizu',meaning:'su',example:'みず を のみます — Su içiyorum'},
{word:'健康',latin:'kenkō',meaning:'sağlık',example:'けんこう が だいいち — Sağlık birinci'},
{word:'スポーツ',latin:'supōtsu',meaning:'spor',example:'スポーツ を します — Spor yapıyorum'},
{word:'走る',latin:'hashiru',meaning:'koşmak',example:'まいにち はしります — Her gün koşuyorum'},
{word:'力',latin:'chikara',meaning:'güç',example:'ちから が ある — Gücüm var'},
{word:'強い',latin:'tsuyoi',meaning:'güçlü',example:'こころ が つよい — Kalbim güçlü'},
{word:'心',latin:'kokoro',meaning:'kalp, gönül',example:'こころ から ありがとう — Kalpten teşekkür'},
{word:'夢',latin:'yume',meaning:'rüya, hayal',example:'ゆめ を おう — Hayalin peşinden'},
{word:'目標',latin:'mokuhyō',meaning:'hedef',example:'もくひょう が ある — Hedefim var'},
{word:'希望',latin:'kibō',meaning:'umut',example:'きぼう を もつ — Umut beslemek'},
{word:'努力',latin:'doryoku',meaning:'gayret, çaba',example:'どりょく は うらぎらない — Gayret seni bırakmaz'},
{word:'成功',latin:'seikō',meaning:'başarı',example:'せいこう の かぎ は どりょく — Başarının anahtarı çaba'},
{word:'勝利',latin:'shōri',meaning:'zafer',example:'しょうり を つかむ — Zaferi yakalamak'},
{word:'勇気',latin:'yūki',meaning:'cesaret',example:'ゆうき を だす — Cesaretini topla'},
{word:'真実',latin:'shinjitsu',meaning:'gerçek, doğruluk',example:'しんじつ は ひとつ — Gerçek tek'},
{word:'道',latin:'michi',meaning:'yol',example:'じぶん の みち — Kendi yolum'},
{word:'頑張って',latin:'ganbatte',meaning:'dayan! / elinden geleni yap!',example:'がんばって ファルク — Devam et Faruk!'}
];
const SAHABE=[
{name:'Hz. Ömer (RA) — el-Fârûq',title:'Adaletin sembolü, Faruk\'un adının kaynağı',story:'Ömer iman etmeden önce İslam\'ın en büyük düşmanlarındandı. Bir gün kız kardeşinin evinde Kuran okunduğunu duydu, içeri girip kız kardeşini dövdü. Sonra utandı, sayfayı eline aldı, "Tâhâ" suresini okudu — kalbi yumuşadı, doğruca Peygamberimize gidip iman etti. Halifelik döneminde devasa bir İmparatorluk yönetti ama tek elbise giyer, Medine sokaklarında yamalı cübbesiyle gezerdi. Peygamberimiz ona "Hak ile bâtılı ayıran" anlamında <b>Fârûq</b> lakabını verdi.',lesson:'Senin adın boş seçilmedi Faruk. el-Fârûq, hak ile bâtılı ayıran demektir. Sen büyürken hayatta hep bir tarafa dur — doğrunun tarafına. Adaletini önce kendine, sonra etrafına uygula.'},
{name:'Abdurrahman b. Avf (RA)',title:'İslam\'ın efsane tüccarı',story:'Mekke\'de zengindi. Hicret ettiğinde tüm malını bıraktı, Medine\'ye boş geldi. Sa\'d ibn Rabî "evimin yarısını sana veriyorum" dedi. Abdurrahman cevabı tarihe geçti: <i>"Allah malını sana mübarek etsin. Bana sadece pazarın yolunu göster."</i> Pazara gitti, peynir ve yağ alıp sattı. Yıllar sonra Medine\'nin en zenginlerindendi — ama tek bir gümüş bile haram kazanmadı.',lesson:'Para da, başarı da haram olarak kazanılırsa zehirdir; helal olarak kazanılırsa berekettir. "Pazarın yolunu göster" diyebilen adam, kimseye yük olmayan adamdır. Sen de yapay zekayı, kodu, sermayeni helâl alın teri ile kazanırsan bereket olur.'},
{name:'Hz. Osman (RA)',title:'Cömertliğin abidesi',story:'Mekke\'nin en zengin gençlerindendi. Tebük seferi öncesi ordu fakirdi. Osman 300 deve, 50 at, 1000 dinar bağışladı — ordunun üçte birini tek başına donattı. Peygamberimiz "Bugünden sonra Osman ne yaparsa yapsın, ona zarar vermez" buyurdu. Medine\'de su sıkıntısında Yahudi sahibinden Rûme kuyusunu satın aldı, bütün Müslümanlara vakfetti — bugün hâlâ o topraklarda Osman\'ın bağışı suluyor.',lesson:'Para biriktirmenin amacı sadece daha çok para değildir. Cömertlik bir karakterdir — küçük yaşta sadaka vermeyi öğrenen büyüdüğünde de paylaşmayı bilir.'},
{name:'Hz. Ebû Bekir es-Sıddîk (RA)',title:'Sıddîk — doğrulayan, ilk halife',story:'Peygamberimizin en yakın dostu. Mirac olayı anlatıldığında müşrikler güldü, Ebu Bekir tek soru sormadan "O söylüyorsa doğrudur" dedi — bu yüzden ona <b>es-Sıddîk</b> lakabı verildi. Hicrette Sevr mağarasında 3 gün saklandılar; müşrikler mağaranın ağzına geldiğinde Peygamberimiz "Korkma, Allah bizimle" dedi. Halifeliğinde tüm servetini İslam\'a vermişti.',lesson:'Sadakat, dostluğun en yüksek mertebesidir. Bir insanın sözüne tereddütsüz inanabilmek için o kişinin yıllarca o güveni kazanması gerekir. Sözün senet olsun.'},
{name:'Hz. Ali (RA)',title:'İlim şehri, cesaret aslanı',story:'Çocuk yaşta iman edenlerin ilki. Hicret gecesi Peygamberimizin yatağına yattı — müşrikler Peygamberimizi öldürmek için evi sardığında, perde kaldırılınca yatakta Ali\'yi gördüler. Aynı zamanda derin bir alimdi: "Ben ilim şehrinin kapısıyım" diye anılırdı. Hutbeleri bugün hâlâ Nehcü\'l-Belâğa diye okutuluyor.',lesson:'Cesaret + ilim — ikisi bir arada olmazsa eksik kalır. Sadece bilen biri korkak olabilir; sadece cesur biri akılsız olabilir. Sen ikisini de geliştir.'},
{name:'Talha b. Ubeydullah (RA)',title:'Talha el-Hayr — Hayrın Talhası',story:'Cömertliğiyle ünlüydü. Bir kervan geldiğinde 700.000 dirhem kazandı, gece uyuyamadı, sabah hepsini fakirlere dağıttı. Uhud\'da Peygamberimizi korumak için kollarını kalkan yaptı — bir oku Peygamberimize gelmesin diye eliyle tuttu, parmakları kırıldı. Peygamberimiz "Cennette yürüyen birini görmek isteyen Talha\'ya baksın" dedi.',lesson:'Yüzyüze geldiğin zorluk anında ne yapacağın seni belirler. Sevdiğin biri, bir hak için ayağa kalkacaksın bir gün. O an pişman olmamak için bugünden cesaretini eğit.'},
{name:'Zubeyr b. Avvâm (RA)',title:'Cennetle müjdelenen, Peygamberimizin havarisi',story:'16 yaşında iman etti. Genç yaşta sahabenin saygısını kazanmıştı. Bedir, Uhud, Hendek, Hayber — her savaşta önde. Yermuk\'ta Bizans ordusunu tek başına yarıp geçtiği anlatılır. Aynı zamanda iyi bir tüccardı. Peygamberimiz "Her peygamberin bir havarisi vardır, benim havarim Zubeyr\'dir" buyurdu.',lesson:'Erken yaşta iman, erken yaşta karakter — bunlar bir insanın kaderini değiştirir. 16 yaşında bir karar, 60 yaşına kadar seni yönlendirir.'},
{name:'Sa\'d b. Ebî Vakkâs (RA)',title:'İslam için ilk ok atan',story:'17 yaşında iman etti. İslam yolunda ilk ok atan O\'dur. Annesi onu iman ettiği için yemekten vazgeçti, ölecek kadar zayıfladı. "Eğer bin canım olsa Allah\'ın dininden dönmem" dedi. Sonunda annesi vazgeçti. Sa\'d Kadisiye\'de Sasani İmparatorluğu\'nu yenip Pers topraklarını fethetti.',lesson:'Sevdiklerin senden sevmediğin bir şey isterse — özellikle iman, ahlâk, namaz konularında — yumuşak ama net "hayır" demeyi öğren. Sevgiyle ama dimdik.'},
{name:'Hâlid b. Velîd (RA) — Seyfullâh',title:'Allah\'ın Kılıcı',story:'Önce Müslümanlara karşı savaşan bir komutandı — Uhud\'da Müslümanları arkadan vurmasıyla ünlüydü. Ama gerçeği gördüğünde inkâr etmedi, hicretle Medine\'ye gelip iman etti. Peygamberimiz ona <b>Seyfullâh</b> lakabını verdi. 100\'den fazla savaşa girdi, hiçbirini kaybetmedi. Yermuk\'ta 40.000 Müslümanla 200.000 Bizans askerine karşı zafer kazandı.',lesson:'Geçmişin önemli değil, bugünün önemli. Daha önce yanlış yapmış olabilirsin — bunlar seni tanımlamaz. Senin gerçek kimliğin bugünkü kararlarındadır. Hâlid yıllarca İslam\'a karşıydı; sonra dünya tarihinin en büyük komutanı oldu.'},
{name:'Bilâl-i Habeşî (RA)',title:'İlk müezzin, sebat sembolü',story:'Mekke\'de Ümeyye ibn Halef\'in kölesiydi. İman ettiğinde efendisi onu kızgın çöl kumlarına yatırdı, göğsüne büyük taşlar koydu. Bilâl tek bir kelime tekrar etti: <b>"Ehad, Ehad"</b> (Allah birdir). Ebu Bekir onu satın aldı ve hür kıldı. Mekke\'nin fethinde Peygamberimiz Bilâl\'e Kâbe\'nin damına çıkıp ezan okumasını söyledi.',lesson:'Senin imanın, kimliğin, sözlerin — kimse karşı çıksa da, sen değişmiyorsan güçlüsün. Bilâl çöl kumunda yandı ama "Ehad" demeyi bırakmadı. Sen de hayatta zorluklar göreceksin — onları seni değiştirmesin, sen onları aş.'},
{name:'Mus\'ab b. Umeyr (RA)',title:'Mekke\'nin gülü, Uhud şehidi',story:'Mekke\'nin en zengin gençlerindendi. Annesi onu ipek kumaşlar içinde, en güzel parfümlerle büyüttü. İslam\'a girdiğinde annesi onu hapsetti, yemek vermedi. Mus\'ab kaçtı. Peygamberimiz onu Medine\'ye ilk muallim olarak gönderdi — yamalı abasıyla. Uhud\'da sancağı taşıdı; bir kolu kesildi, diğer eline aldı; o da kesildi, sancağı göğsüne bastı; şehit edildi.',lesson:'Lüks içinde büyümek seni güçsüz yapmaz; ama lükse bağlı kalmak yapar. Mus\'ab her şeyi bıraktı çünkü ondan büyük bir şey vardı. Sen de — Doha\'da rahat bir hayat yaşıyor olabilirsin, ama bu rahatlık seni esir etmesin.'},
{name:'Selmân-ı Fârisî (RA)',title:'Hakikat avcısı, Hendek\'in stratejisti',story:'İran\'da bir Mecusi ailenin çocuğuydu. Bir kiliseye girdi, Hristiyanlığı öğrendi. "Daha doğru bir din var mı?" diye Suriye\'ye, Musul\'a gitti — yıllarca rahiplerin yanında çalıştı, son rahip ona "son peygamber gelecek" dedi. Selman Arabistan\'a geldi, satıldı, köleleştirildi. Medine\'ye geldiğinde Peygamberimizi gördü, mührü gördü ve hıçkırarak iman etti. Hendek savaşında Pers usulü hendek kazma stratejisini önerdi.',lesson:'Hakikat aramak yıllar alabilir. Selman ülkesinden, ailesinden, hatta kölelikten geçti — ama hakikat onu hür yaptı. Sen de hayatta sıkıştığında, "ben ne yapıyorum?" diye sorduğunda — cevabı içinde ara.'},
{name:'Mu\'âz b. Cebel (RA)',title:'Helâl-haramı en iyi bilen',story:'Genç yaşta iman etti, çok zekiydi. Peygamberimiz onu Yemen\'e vali olarak gönderirken "İçtihat ederim" cevabıyla onu uğurlamıştı — yani önce Kuran\'a, sonra sünnete, sonra kendi aklına başvuracaktı. Bu hadis İslam fıkhının temellerinden biri oldu. Peygamberimiz "Ümmetimin helâl ve haramı en iyi bilen Mu\'âz\'dır" buyurdu.',lesson:'Gençken çok şey öğrenmek mümkündür — beyin sünger gibi. Ama her bilgi seni alim yapmaz; bilgiyi kullanmasını bilmek yapar.'},
{name:'Üsâme b. Zeyd (RA)',title:'17 yaşında ordu komutanı',story:'Peygamberimizin azadlı kölesi Zeyd\'in oğluydu. 17 yaşına geldiğinde Peygamberimiz onu Şam üzerine giden büyük bir ordunun komutanı yaptı — orduda Ebû Bekir, Ömer gibi yaşlı sahabe de vardı. Bazıları "bu kadar genç bir komutan olur mu?" diye itiraz etti, Peygamberimiz "Babası da hak ediyordu, oğlu da hak ediyor" dedi.',lesson:'Yaş, cesarete engel değildir. Yetenekli, dürüst, hazırlıklı bir genç — yaşlı bir tecrübesizden daha değerlidir. Bekleme: küçük başlangıçlar yap. Hazır hissetmeden başlanır — başlayınca hazır olunur.'},
{name:'Ammâr b. Yâsir (RA)',title:'İşkenceye dayanan',story:'Mekke\'de işkenceye uğrayan ilk Müslümanlardan. Çöl güneşinde sıcak kumlara yatırıldılar. Babası ve annesi şehit edildi. Ammâr o kadar büyük işkence gördü ki bir an dilini İslam\'a karşı kullandı, sonra pişman olup ağladı. Peygamberimiz "Eğer bir daha öyle yaparlarsa, sen de aynısını söyle — kalbin imanla doluysa zarar gelmez" dedi.',lesson:'Hayatta zayıf bir an yaşadığında, hata yaptığında, kendini affet ve Allah\'a dön. Tövbe ve geri dönüş kapısı her zaman açık. Mühim olan tekrar tekrar dönmektir.'},
{name:'Câbir b. Abdullâh (RA)',title:'Genç hadis nakili',story:'19 yaşında babasını Uhud\'da kaybetti — babası 9 kız kardeşine ve borçlara emanet bırakmıştı. Peygamberimiz Câbir\'in evine gitti, bahçesindeki verimsiz hurma ağaçlarına dua etti, o yıl ağaçlar bereketlendi, borçlar ödendi. Câbir genç yaşta sahâbenin önde gelen âlimlerinden biri oldu. 1540 hadis aktarmıştır.',lesson:'Genç yaşta bilgi biriktir, yaşlı yaşta paylaş. Bugün öğrendiğin her şey — bir kelime, bir kod, bir hadis — yarın başkasına öğreteceğin değerli bir şeydir.'}
];
const SIRET_WEEKS=[
{week:1,theme:'Yetimlik ve sabır',text:'Peygamberimiz daha doğmadan babasını kaybetti. 6 yaşında annesini, 8 yaşında dedesini. Amcası Ebû Tâlib\'in fakir evinde büyüdü. Bu yetimlik onu kalbi kırık değil, kalbi geniş bir adam yaptı.',lesson:'Hayat sana zor başlamış olabilir, ama bu seni yumuşak değil, derin yapar. Acı çeken biri başkasının acısını anlar.'},
{week:2,theme:'Ergenlik ve ticaret — el-Emin',text:'12 yaşında amcasıyla Şam\'a ticaret yolculuğuna çıktı. 20\'lerinde başkalarının malıyla ticaret yapıyordu — bir tek kuruşunu zayi etmedi, bir tek kişiyi aldatmadı. Mekkeliler ona <b>el-Emîn</b> lakabını taktılar.',lesson:'Genç yaşta dürüstlük insanın sermayesidir. Para gelir gider, ama "bu çocuk sözünün eridir" dedirten karakter ömür boyu kalır.'},
{week:3,theme:'Hatice ile evlilik — aile ortaklığı',text:'Hatice 40 yaşında dul bir iş kadınıydı. Kendi ticaretini Peygamberimize emanet etti, sonra evlenme teklifi etti. 25 yıl boyunca tek eşi olarak kaldı. İlk vahiyde onu sakinleştirdi, servetini İslam\'a verdi.',lesson:'İyi bir eş hayatın motorudur. İleride evleneceğin kadın senin işine, hayaline destek olmalı; sen de onun.'},
{week:4,theme:'Hira mağarası — inziva',text:'35 yaşından itibaren Hira Mağarası\'na çekilirdi. Aylarca yalnız, sessizce — düşünür, dua ederdi. 40 yaşında, bir Ramazan gecesinde Cebrail orada ona ilk vahyi getirdi: "Oku!"',lesson:'Sessizlik bir lükstür modern dünyada. Telefonu bir kenara koy, bir saat tek başına kal. Büyük fikirler gürültüde değil, sessizlikte gelir.'},
{week:5,theme:'İlk vahiy — sorumluluk',text:'"Oku!" emriyle Peygamberlik başladı. Müddessir suresi indi: "Ey örtüsüne bürünmüş! Kalk ve uyar!" 23 yıllık bir mücadele başladı.',lesson:'Bir gün sen de bir "kalk!" çağrısı duyacaksın — bir hedef, bir mesele. O zaman ertelemek yerine, kalkıp yola çıkmaya hazır ol.'},
{week:6,theme:'Mekke yılları — sabır',text:'13 yıl boyunca Mekke\'de tebliğ etti. Müşrikler işkence yaptı, ailesini boykot etti — 3 yıl açlık. Peygamberimiz tek kelime intikam, tek kelime şikayet etmedi.',lesson:'En değerli iş, en uzun zaman ister. Hızlı sonuç bekleme, kalıcı eserin uzun zaman aldığını bil.'},
{week:7,theme:'Tâif — red ve dua',text:'Tâifliler onu dinlemediler, çocukları arkasına salıp taşladılar. Kanlar içinde dönen Peygamberimiz "bu insanları yok edeyim mi?" teklifini reddetti, dua etti: "Ben onları affediyorum."',lesson:'En zorlu reddedilme anında bile insanı affetmek — sadece güçlü insanların yapabildiği bir şeydir.'},
{week:8,theme:'Hicret — planlama ve tevekkül',text:'Müşrikler Peygamberimizi öldürmek için ev sardığında detaylı bir plan vardı: gizlice gece çıkış, mağarada saklanma, alternatif yol. Plan + tevekkül = bir tek kıl bile zarar görmedi.',lesson:'Tevekkül "hiçbir şey yapmadan Allah\'a güvenmek" değildir. Önce sen plan yap, gücünün yettiğini yap, sonra "Allah\'a güveniyorum" de.'},
{week:9,theme:'Medine\'de pazar — ekonomik bağımsızlık',text:'Medine\'de Yahudiler tüm ticareti elinde tutuyordu. Peygamberimiz alan açtı, "Bu sizin pazarınızdır, vergi yok" dedi. Müslümanlar kendi ayakları üzerinde durmaya başladı.',lesson:'Bireyin gerçek özgürlüğü ekonomik bağımsızlıktan geçer. Çocuk yaşta para biriktirmeyi öğren, kendi gelir kapını aç.'},
{week:10,theme:'Hudeybiye — uzun vadeli zafer',text:'Antlaşma şartları görünüşte Müslümanların aleyhineydi. Sahâbe çok üzüldü. Sonra Allah Fetih suresini indirdi: "Biz sana apaçık bir fetih müjdeliyoruz." 2 yıl içinde Mekke fethedildi.',lesson:'Bugün kayıp gibi görünen şey, yarın zaferin tohumu olabilir. Uzun vadede düşün. Bir reddedilme, bir başarısızlık — kıyamet değil.'},
{week:11,theme:'Veda Haccı — vasiyet',text:'63 yaşında Arafat\'ta 100.000 sahâbeye Veda Hutbesini okudu: "Arap\'ın Arap olmayana, beyazın siyahın üzerine takvâ dışında üstünlüğü yoktur."',lesson:'Hayatın bir ödevi var — sen ne öğrendinse, başkasına aktarmadan gitme. Öğrendiğin her dili, kodu, sahâbe kıssasını paylaş.'}
];
const PRAYERS=[
{name:'Sabah (Fecr)',time:'~04:30',arabic:'اَللّٰهُمَّ اِيمَانًا بِكَ وَتَصْدِيقًا بِكِتَابِكَ وَوَفَاءً بِعَهْدِكَ وَاتِّبَاعًا لِسُنَّةِ نَبِيِّكَ',latin:'Allâhümme imânen bike ve tasdîkan bi-kitâbike ve vefâen bi-ahdike vettibâan li-sünneti nebiyyike.',meaning:'Allah\'ım! Sana inanarak, kitabını tasdik ederek, sana verdiğim sözü tutarak ve Peygamberinin sünnetine uyarak işte buradayım. (Diyanet İşleri Başkanlığı)'},
{name:'Öğle (Zuhr)',time:'~11:45',arabic:'اَللّٰهُمَّ مُصَرِّفَ الْقُلُوبِ صَرِّفْ قُلُوبَنَا عَلَى طَاعَتِكَ',latin:'Allâhümme musarrife\'l-kulûb! Sarrif kulûbenâ alâ tâatik.',meaning:'Ey kalpleri yönlendiren Allahım! Kalplerimizi sana itaate yönelt. (Müslim, Kader 17)'},
{name:'İkindi (Asr)',time:'~15:30',arabic:'يَا مُقَلِّبَ الْقُلُوبِ ثَبِّتْ قَلْبِي عَلَى دِينِكَ',latin:'Yâ mukallibe\'l-kulûb! Sebbit kalbî alâ dînike.',meaning:'Ey kalpleri hâlden hâle çeviren Allah\'ım, kalbimi dinin üzere sabit kıl. (Tirmizî, Deavât 124)'},
{name:'Akşam (Mağrib)',time:'~18:25',arabic:'اَللّٰهُمَّ اغْفِرْ لِي وَارْحَمْنِي وَأَلْحِقْنِي بِالرَّفِيقِ الْأَعْلَى',latin:'Allâhümme\'ğfirlî verhamnî ve elhıknî bi\'r-Refîki\'l-Aʿlâ.',meaning:'Allah\'ım! Beni bağışla, bana merhamet eyle ve beni Refîk-i Aʿlâ\'ya (en yüce dosta) kavuştur. (Hâkim, el-Müstedrek 1/676)'},
{name:'Yatsı (İşâ)',time:'~19:55',arabic:'اَللّٰهُمَّ حَاسِبْنِي حِسَابًا يَسِيرًا',latin:'Allâhümme hâsibnî hisâben yesîrâ.',meaning:'Allah\'ım! Hesabımı kolaylaştır. (Ahmed b. Hanbel; Hâkim, Sahih)'}
];
const SPORT_PROGRAM={
1:{name:'Hafta 1 — Temel',desc:'Form önemli, sayı değil.',daily:[{name:'5 push-up',detail:'Diz üstü olabilir, form önemli'},{name:'10 squat',detail:'Yavaş in, yavaş çık'},{name:'15 sn plank',detail:'Vücut düz çizgi'},{name:'5 dk koşu/yürüyüş',detail:'Akşam serinliğinde'}]},
2:{name:'Hafta 2 — Kas Uyanıyor',desc:'Vücut adapte oluyor.',daily:[{name:'8 push-up',detail:'Tam form'},{name:'15 squat',detail:'2 set: 8+7'},{name:'25 sn plank',detail:''},{name:'8 dk koşu',detail:'Dayanıklılık'}]},
3:{name:'Hafta 3 — İlk Eşik',desc:'15 günü geçtin.',daily:[{name:'12 push-up',detail:'2 set: 7+5'},{name:'20 squat',detail:'Derin'},{name:'35 sn plank',detail:''},{name:'10 dk koşu',detail:'Tempolu'},{name:'5 pull-up denemesi',detail:'Kapı çubuğu'}]},
4:{name:'Hafta 4 — Bir Ay! Milat',desc:'Aynaya bak — değişiyorsun.',daily:[{name:'15 push-up',detail:'2 set: 8+7'},{name:'25 squat',detail:'Set 1: 13, Set 2: 12'},{name:'45 sn plank',detail:''},{name:'12 dk koşu',detail:''},{name:'5 pull-up',detail:'Tam form'}]},
5:{name:'Hafta 5 — Yeni Seviye',desc:'Spor artık alışkanlık.',daily:[{name:'20 push-up',detail:'2 set: 10+10'},{name:'30 squat',detail:'+ 10 jump squat'},{name:'60 sn plank',detail:'1 dakika!'},{name:'15 dk koşu',detail:'Son 2 dk hızlı'},{name:'8 pull-up',detail:''}]},
6:{name:'Hafta 6 — Güçleniyor',desc:'Vücut görsel olarak değişiyor.',daily:[{name:'25 push-up',detail:''},{name:'35 squat',detail:'+ 15 lunges'},{name:'75 sn plank',detail:'+ yan plank'},{name:'18 dk koşu',detail:'Aralıklı'},{name:'10 pull-up',detail:''}]},
7:{name:'Hafta 7 — Atletik',desc:'Spor adamı bedeni.',daily:[{name:'30 push-up',detail:''},{name:'40 squat',detail:'+ 20 lunges + 10 burpee'},{name:'90 sn plank',detail:''},{name:'20 dk koşu',detail:''},{name:'12 pull-up',detail:''}]},
8:{name:'Hafta 8+ — Disiplin Modu',desc:'Bu seviyeyi koru.',daily:[{name:'30+ push-up',detail:'Çeşit ekle: diamond, wide'},{name:'40+ squat',detail:'Pistol squat'},{name:'90+ sn plank',detail:'Side plank'},{name:'20-30 dk kardio',detail:'Boks, yüzme'},{name:'12-15 pull-up',detail:''}]}
};
const DAILY_WISDOM=[
{type:'Ayet',source:'Necm 39-40',text:'وَأَن لَّيْسَ لِلْإِنسَانِ إِلَّا مَا سَعَىٰ ۝ وَأَنَّ سَعْيَهُ سَوْفَ يُرَىٰ',meaning:'"İnsan için ancak çalıştığı vardır. Ve onun çalışması ileride görülecektir."'},
{type:'Hadis',source:'Buhârî',text:'إِنَّ اللَّهَ يُحِبُّ إِذَا عَمِلَ أَحَدُكُمْ عَمَلًا أَنْ يُتْقِنَهُ',meaning:'"Allah, bir iş yapacaksanız onu sağlam yapmanızı sever." (yani: yarım iş yapma, kaliteli yap)'},
{type:'Hadis',source:'Tirmizî',text:'الْمُؤْمِنُ الْقَوِيُّ خَيْرٌ وَأَحَبُّ إِلَى اللَّهِ مِنَ الْمُؤْمِنِ الضَّعِيف',meaning:'"Güçlü mümin, zayıf müminden Allah\'a daha sevimlidir." (Hem ruhen hem bedenen güçlü ol)'},
{type:'Söz',source:'Hz. Ali (RA)',text:'مَنْ عَلَّمَنِي حَرْفًا صِرْتُ لَهُ عَبْدًا',meaning:'"Bana bir harf öğretenin kölesi olurum." — Hocaya, kitaba, öğretene saygının ne kadar derin olması gerektiğini gösterir.'},
{type:'Söz',source:'İmam Şâfiî',text:'مَنْ لَمْ يَتَعَلَّمْ فِي صِغَرِهِ، تَخَلَّفَ فِي كِبَرِهِ',meaning:'"Küçükken öğrenmeyen, büyükken geri kalır." — 16 yaşında her şey için doğru zaman.'},
{type:'Ayet',source:'Tâhâ 114',text:'وَقُل رَّبِّ زِدْنِي عِلْمًا',meaning:'"De ki: Rabbim ilmimi artır."'},
{type:'Söz',source:'Steve Jobs',text:'"Stay hungry, stay foolish."',meaning:'"Aç ve cesur kal." — Bilmediğini sanmak yenilik kapısını açar.'},
{type:'Söz',source:'İbn Haldun',text:'الْإِنْسَانُ ابْنُ بِيئَتِهِ',meaning:'"İnsan, çevresinin çocuğudur." — Etrafındaki insanlar, kitaplar, alışkanlıklar — seni şekillendirir.'},
{type:'Hadis',source:'Müslim',text:'يَدُ اللَّهِ مَعَ الْجَمَاعَة',meaning:'"Allah\'ın eli cemaat üzerinedir." — Tek başına değil, doğru insanlarla yola çık.'},
{type:'Söz',source:'Mevlânâ',text:'دیروز گذشت، فردا نیامده، فقط امروز هست',meaning:'"Dün geçti, yarın gelmedi, sadece bugün var." — Bugünün hakkını ver.'},
{type:'Hadis',source:'Buhârî',text:'اغْتَنِمْ خَمْسًا قَبْلَ خَمْسٍ',meaning:'"Beş şeyi beşten önce ganimet bil: gençliğini yaşlılıktan önce, sağlığını hastalıktan önce, varlığını yokluktan önce, boş vaktini meşguliyetten önce, hayatını ölümden önce." — Şu an 16 yaşındasın. Bu en kıymetli zaman.'},
{type:'Söz',source:'Albert Einstein',text:'"Compound interest is the eighth wonder of the world."',meaning:'"Bileşik faiz dünyanın sekizinci harikasıdır." — Para için söylendi ama bilgi, alışkanlık, kelimeler — hepsi öyle. Her gün +1 = bir yıl sonra dağ.'}
];
const CODE_PROJECTS=[
{name:'AI Chatbot — Quran Asistanı',desc:'Claude/OpenAI API ile Kuran/hadis sorularına cevap veren bot. Frontend HTML, backend Python.',stack:['Python','API','HTML'],level:'Başlangıç'},
{name:'Namaz Vakti Scraper',desc:'Doha namaz vakitlerini her gün otomatik çeken Python scripti.',stack:['Python','BeautifulSoup','cron'],level:'Başlangıç'},
{name:'Arapça-Japonca Kelime Kart Oyunu',desc:'Kendi öğrendiğin kelimelerle quiz oyunu. Skor ve doğruluk takibi.',stack:['JavaScript','HTML','CSS'],level:'Başlangıç'},
{name:'Kuran Ezber Takip Uygulaması',desc:'Bu uygulamanın kendisi gibi. Hangi sureyi ezberledin, ne kadar tekrar ettin.',stack:['HTML','JavaScript','LocalStorage'],level:'Orta'},
{name:'Dede Mirası Web Sitesi',desc:'Rahmetli deden Ebubekir Yasin\'in çalışmaları için modern bir site. Aile mirası dijital ortama.',stack:['Next.js','React','MDX'],level:'Orta'},
{name:'Sahâbe Bilgi Yarışması',desc:'Sahâbe hayatından sorular, çoktan seçmeli, leaderboard.',stack:['React','JavaScript'],level:'Orta'},
{name:'Spor Takip + Grafik',desc:'Push-up, squat, plank sayılarını gir, haftalık-aylık grafik (Chart.js).',stack:['JavaScript','Chart.js'],level:'Orta'},
{name:'Otomatik Hatim Programı',desc:'30/60 günlük hatim için günlük sayfa takibi + Telegram bildirim.',stack:['Python','Telegram API'],level:'Orta'},
{name:'Kişisel Web Sitesi',desc:'Kendi portfolio siten. Kim olduğun, projelerin, hedefin. GitHub Pages ücretsiz.',stack:['HTML','CSS','Git'],level:'Başlangıç'},
{name:'Faruk\'un Beslenme Asistanı',desc:'Babanın WCK\'da yaptığı işten ilham — gıda kalitesi, sağlıklı beslenme tracker.',stack:['React Native','Python'],level:'Orta'},
{name:'Arduino LED Kontrol',desc:'Arduino al, LED\'leri telefondan kontrol et. Bluetooth = robotik dünyasına ilk adım.',stack:['Arduino','C++','Bluetooth'],level:'İleri'},
{name:'Discord Bot — İslami Topluluk',desc:'Sunucuda namaz vakti, hadis, Kuran ayeti paylaşan bot.',stack:['Node.js','Discord.js'],level:'İleri'},
{name:'Görüntü İşleme — Hat Tanıma',desc:'Arapça hat görüntüsünden harfleri tanıyan AI. OpenCV + TensorFlow.',stack:['Python','OpenCV','TensorFlow'],level:'İleri'},
{name:'AI Yazı Tashîh Aracı',desc:'Türkçe veya Arapça metni okuyup yazım/dilbilgisi düzelten araç. LLM API.',stack:['Python','Claude API'],level:'İleri'},
{name:'Mini Robot — Fonksiyonlu',desc:'Arduino + sensörlerle çizgi takip eden veya engel algılayan basit robot.',stack:['Arduino','C++','Sensörler'],level:'İleri'}
];
const ENTREPRENEURS=[
{country:'🇺🇸',name:'Steve Jobs',role:'Apple kurucusu (1955-2011)',story:'Garajda başladı, üvey aile çocuğuydu. Kolejden ayrıldı, hat sanatı dersini takip etti — bu sonra Apple bilgisayarlarındaki güzel fontların temelini oluşturdu. Apple\'ı kurdu, kendi şirketinden kovuldu, NeXT ve Pixar ile döndü, geri çağrıldı, dünyayı iPhone ile değiştirdi.',lesson:'Bağlantısız görünen bir şey öğrenmek (hat sanatı gibi) gelecekte değer kazanabilir. Hiçbir öğrenme boşa değildir.'},
{country:'🇺🇸',name:'Bill Gates',role:'Microsoft kurucusu (1955-)',story:'13 yaşında ilk kodunu yazdı. Harvard\'tan ayrıldı, Microsoft\'u kurdu. Dünyayı kişisel bilgisayarla değiştirdi. Şimdi servetinin %99\'unu hayır işlerine adadı — Bill & Melinda Gates Foundation aracılığıyla milyonlarca çocuğa aşı, eğitim götürüyor.',lesson:'Para kazanmak başlangıç. Onu nasıl kullandığın seni belirler. Cömertlik en yüksek güçtür.'},
{country:'🇿🇦🇺🇸',name:'Elon Musk',role:'Tesla, SpaceX, X kurucusu (1971-)',story:'Güney Afrika\'da büyüdü, 12 yaşında ilk video oyununu kodladı ve 500$\'a sattı. Üç şirket kurdu, üçü de başarılı: Tesla (elektrikli araba), SpaceX (uzay), Neuralink (beyin-bilgisayar). Riskli işlere girer, çoğu insan "olmaz" der, o yine yapar.',lesson:'Çoğu insan "yapılmaz" dediğinde, gerçekten yapılamaz olduğu için değil — onlar yapamadığı içindir. Sen kendi yargını kullan.'},
{country:'🇺🇸',name:'Jeff Bezos',role:'Amazon kurucusu (1964-)',story:'Garajında 1994\'te bir kitap satış sitesi kurdu — Amazon. 30 yıl içinde dünyanın en büyük perakendecisi oldu. "Eğer kararından %30 emin olduğunda harekete geçersen, geç kalmazsın" der.',lesson:'Mükemmel bilgi gelmez. Yeterli bilgiyle başla, yolda öğren. Erteleme — bilgisizlik değil, beklemek seni yavaşlatır.'},
{country:'🇨🇳',name:'Jack Ma',role:'Alibaba kurucusu (1964-)',story:'Çin\'de İngilizce öğretmeniydi. 30 üniversite reddetti onu. KFC bile işe almadı. 35 yaşında Alibaba\'yı kurdu — dünyanın en büyük e-ticaret platformlarından biri. "Reddedilmeyi sevmeyi öğren — her hayır seni doğru evete yaklaştırır."',lesson:'Reddedilme bir şeyin sonu değil, başkasının başlangıcıdır. Hayatın ilk yarısı kapı çalmakla geçer; ikinci yarısı kapı açmakla.'},
{country:'🇹🇼🇺🇸',name:'Jensen Huang',role:'NVIDIA kurucusu (1963-)',story:'Tayvan\'da doğdu, ABD\'ye 9 yaşında göç etti. Denny\'s lokantasında bulaşıkçı olarak çalıştı. 30 yaşında NVIDIA\'yı kurdu — bugün yapay zekanın motorunu üreten şirket. Kendisi hâlâ deri ceket giyer, ofiste herkesle eşit.',lesson:'Göçmen olmak dezavantaj değil — ekstra disiplin verir. Tevazu seni eğer, kibir seni kırar.'},
{country:'🇺🇸',name:'Sam Altman',role:'OpenAI CEO (1985-)',story:'19 yaşında ilk şirketini kurdu. Y Combinator\'ı yönetti. 2015\'te Elon Musk ile OpenAI\'yi kurdu — 2022\'de ChatGPT ile dünyayı sarstı. Şimdi yapay zekanın en güçlü ismi, sadece 40 yaşında.',lesson:'Yaş bahane değildir. Doğru fikir + doğru zaman + iyi insanlarla çalışmak — büyük şeyler başarılır. 40 değil 20\'lerinde başarı normaldir.'},
{country:'🇬🇧🇸🇾',name:'Mustafa Suleyman',role:'DeepMind kurucu, Microsoft AI CEO (1984-)',story:'Suriyeli baba, İngiliz anne. Oxford\'tan ayrıldı, 19 yaşında bir telefon yardım hattı kurdu. 2010\'da DeepMind\'ı kurdu — Google satın aldı. Bugün Microsoft\'un AI bölümünü yönetiyor. <b>Müslüman, başarılı, etik AI savunucusu.</b>',lesson:'Müslüman ve başarılı bir tech adamı olmak mümkün — Mustafa kanıtı. İmanın seni teknolojiden uzaklaştırmaz, daha sağlam zemin verir.'},
{country:'🇮🇷',name:'Pierre Omidyar',role:'eBay kurucusu (1967-)',story:'İranlı bir aileden, Paris\'te doğdu, ABD\'ye geldi. 28 yaşında bir hafta sonu projesi olarak eBay\'i kurdu — sonra dünyanın en büyük açık artırma sitesi oldu. Servetini büyük ölçüde insani yardıma adadı.',lesson:'Büyük fikirler bazen "küçük bir hafta sonu projesi" diye başlar. Atmaktan korkma — çoğu büyük şey "deneyim" diye başladı.'},
{country:'🇹🇷',name:'Hamdi Ulukaya',role:'Chobani kurucusu (1972-)',story:'Erzincanlı Kürt-Türk göçmen. New York\'a 1994\'te 3000 dolarla geldi. 2005\'te kapanmış bir yoğurt fabrikasını satın aldı, Chobani\'yi kurdu. Bugün ABD\'nin en büyük yoğurt markası. Çalışanlarına şirketinin %10\'unu hisse olarak verdi.',lesson:'Türkiye\'den Amerika\'ya 3000 dolarla gitmek delilik gibi görünür — ama büyük başarılar sağlam bir aklın delilik gibi görünmesinden doğar. Cömertlik = sürdürülebilirlik.'},
{country:'🇮🇩',name:'Achmad Zaky',role:'Bukalapak kurucusu (1986-)',story:'Endonezyalı Müslüman. 2010\'da küçük tüccarlar için online platform kurdu — Bukalapak. Bugün milyonlarca KOBİ\'nin online satış yapmasını sağlıyor. "Köyümüzdeki insanlar bile online satış yapabilsin" diye başladı.',lesson:'Sorunu kendi etrafında ara. Senin ailen, mahallen, ülken — onlara hizmet eden teknoloji yap. Yerel sorun, küresel çözüm.'},
{country:'🇮🇳',name:'Sundar Pichai',role:'Google CEO (1972-)',story:'Hindistan\'da fakir bir evde büyüdü, evlerinde telefon yoktu. ABD\'ye burs ile gitti. Google\'da yıllarca Chrome\'u inşa etti, sonra CEO oldu. "Hiç hızlı değildim, ama hep merakliydim."',lesson:'Yetenek değil merak — uzun vadede kazanır. Yavaş ama tutkulu öğrenen, hızlı ama sıkılan birinden ileri geçer.'}
];
const RECOMMENDED_BOOKS=[
{cat:'islami',catLabel:'İslami',name:'Risale-i Nur Külliyatı',author:'Bediüzzaman Said Nursî',why:'Modern aklın sorularına klasik İslami cevap. Felsefe, bilim, iman dengesi. Yavaş okunur, derin anlaşılır.'},
{cat:'islami',catLabel:'İslami',name:'Hayatü\'s-Sahâbe',author:'Muhammed Yûsuf Kandehlevî',why:'Sahâbenin hayatından kıssalar. Bu uygulamadaki hikayelerin kaynağı. Faruk için altın bir kütüphane.'},
{cat:'islami',catLabel:'İslami',name:'İhyâu Ulûmi\'d-Dîn',author:'İmam Gazâlî',why:'İslam\'ın derin felsefesi, ahlâk, manevî hayat. Bir ömür okunur, bir ömre yetmez.'},
{cat:'tech',catLabel:'Tech',name:'Atomic Habits',author:'James Clear',why:'Küçük alışkanlıkların büyük değişimleri. Disiplinin bilimsel açıklaması. Bu uygulamanın felsefesi.'},
{cat:'tech',catLabel:'Tech',name:'The Pragmatic Programmer',author:'Hunt & Thomas',why:'Yazılımcı olmak isteyenin temel kitabı. Kodun yanı sıra "iyi mühendis nasıl olunur" — düşünce yapısı kuran.'},
{cat:'tech',catLabel:'Tech',name:'Clean Code',author:'Robert C. Martin',why:'Çalışan kod yetmez — temiz kod yaz. Mühendislik sanatının temelleri. Bir ömür referans.'},
{cat:'tech',catLabel:'Tech',name:'Sapiens',author:'Yuval Noah Harari',why:'İnsan türünün hikayesi. Tarih, biyoloji, ekonomi — hepsi bir arada. Eleştirel bak, ama oku.'},
{cat:'tech',catLabel:'Tech',name:'Life 3.0',author:'Max Tegmark',why:'Yapay zeka geleceği. Faruk\'un girdiği alanın felsefi temeli. Hem heyecanlı hem ürkütücü.'},
{cat:'bio',catLabel:'Biyografi',name:'Steve Jobs',author:'Walter Isaacson',why:'En etkili biyografilerden. Bir adamın kafa yapısı, ekip kurma, vizyon — kelime kelime ders.'},
{cat:'bio',catLabel:'Biyografi',name:'Elon Musk',author:'Walter Isaacson',why:'Çağımızın en tartışmalı tech adamı. Riskli karar verme, sıkıntı toleransı, hız.'},
{cat:'bio',catLabel:'Biyografi',name:'Şu Çılgın Türkler',author:'Turgut Özakman',why:'Türk kimliği, milli mücadele, bir milletin yeniden ayağa kalkışı. Vatan duygusunu derinleştirir.'},
{cat:'bio',catLabel:'Biyografi',name:'Hindistan\'a Yolculuk',author:'Cemil Meriç',why:'Türk düşünce dünyasının dev isimlerinden. Doğu-Batı dengesi, kendi dilini bulma.'},
{cat:'fels',catLabel:'Felsefe',name:'Meditasyonlar',author:'Marcus Aurelius',why:'Romalı imparator, savaş alanında not tuttu. Stoacılık + ahlâk. Modern erkeğin hâlâ okuması gereken kitap.'},
{cat:'fels',catLabel:'Felsefe',name:'İnsan Anlamını Arıyor',author:'Viktor Frankl',why:'Auschwitz\'ten sağ çıkan psikiyatrist. Hayatın anlamı, acıdan üretkenlik. Hayatta zor an gelirse — bu kitap rehberin.'},
{cat:'fels',catLabel:'Felsefe',name:'Mesnevî',author:'Mevlânâ Celâleddîn-i Rûmî',why:'Doğu\'nun manevî hazinesi. Hikâyeler aracılığıyla derin bilgelik. Yavaş, sürekli okunur.'}
];
const WRITING_PROMPTS=[
'30 yaşındaki Faruk\'a bir mektup yaz. Bugünden 14 yıl sonra. Ona hangi yanlışlardan kaçınmasını söylersin?',
'Yapay zeka 10 yıl sonra dünyayı nasıl değiştirecek? Senin görüşün — araştır, düşün, yaz.',
'Babamın WCK\'daki işi hakkında ne biliyorum, ne öğrenmek isterim? Onun gözünden bir gün anlat.',
'Dedem Ebubekir Yasin\'in çalışmaları... O\'nu hiç tanımadım ama mirası bana kaldı. Ona ne demek isterim?',
'Hatice 5 yıl sonra 18 yaşında olacak. Ben 21 olacağım. Ona o gün ne demek istiyorum?',
'Annem hakkında 3 sahne — onu en iyi anlatan. Yaz, detayla.',
'Seyyahchef olarak baba: bana bu seyahat hayatından ne öğretti?',
'Türk olmak, Müslüman olmak, Asya\'ya gitmek istemek — bu üç kimlik nasıl bir araya geliyor bende?',
'Doha\'da büyümek bana ne öğretti? İyi ve zor yanları.',
'İlk yapay zeka deneyimim — ne hissettim? Korku mu, heyecan mı?',
'Eğer bir AI girişimcisi olsaydım, hangi problemi çözerdim? Detaylıca düşün.',
'Bir robot tasarlasaydım, neyi otomatize ederdi? Ailem için neyi yapardı?',
'Korktuğum bir şey — yaz, sonra "bunu nasıl aşacağım" diye 5 satır yaz.',
'Şu anki en büyük zorluğum. Dürüst yaz — sadece sen okuyacaksın.',
'Hangi sahâbeye benzemek isterdim? Neden? O\'nun bende olmayan ne özelliği var?',
'5 yıl sonra hangi şehirde, ne yapıyorum? Bir günümü detaylıca anlat — sabahtan akşama.',
'Allah\'a kısa bir mektup yaz. Tek başına okuyacaksın. Dürüst ol.',
'Bir startup kursam adı ne olur? Ne yapar? Hangi insana hizmet eder?',
'Sosyal medya — hayatıma ne katıyor, ne götürüyor? Dürüst hesap.',
'Para kazanmak ve helâl olması — ne anlama geliyor? Bir tüccar (sahâbe Abdurrahman b. Avf gibi) olmak ne demek?',
'Ergenlik beni nasıl değiştirdi? 13 yaşımdaki Faruk ile bugünkü ben — fark ne?',
'Bir hafta tek başına yaşasam — Tokyo\'da, Medine\'de, Türkiye\'de. Hangisi? Nasıl bir hafta?',
'Kuran\'dan en sevdiğim ayet ya da sure. Neden? Bana ne anlatıyor?',
'Bir hata yaptığım bir an. Yaz. Ne öğrendim? Nasıl düzelttim?',
'Babamla bir konuşmamızı yaz — gerçek olmuş veya hayal ettiğin. Açık konuş.',
'Türkçe — Arapça — İngilizce — Japonca: dört dil. Hangisi en sevdiğim, neden?',
'Şu an okuduğum kitap bana ne anlatıyor? Bir paragraf yaz — başkasına anlatır gibi.',
'Eğer bir öğrenci olarak kendi okulumu kursam — nasıl bir yer olurdu?',
'Hayatımda en ilham aldığım bir kişi. Onun bende kalan bir cümlesi.',
'Dünyaya bırakmak istediğim tek miras — ne olurdu? Bir buluş, bir yazı, bir aile, bir kuruluş?',
'Bugün araştırdığım yeni bir konu. Bir paragraf özet yaz, sonra "neden ilgimi çekti" diye iki cümle ekle.',
'Bir hafta sonra ne yazmak isterim — buraya bir mektup. Geleceğe not.'
];
const GOAL_CHECKLIST_16=[
{id:'sat',text:'SAT sınavına girmek (6 Haziran 2026)'},
{id:'kuran',text:'Yaz tatilinde Kuran\'dan en az 5 sure ezberlemek'},
{id:'arabic',text:'500 Arapça kelime hafızada (yıl sonuna kadar)'},
{id:'japanese',text:'200 Japonca kelime hafızada'},
{id:'pushup',text:'Ardışık 30 push-up — kesintisiz'},
{id:'pullup',text:'Ardışık 10 pull-up'},
{id:'kitap',text:'Bu yıl 12 kitap bitirmek (ayda 1)'},
{id:'project',text:'1 yapay zeka projesi tamamlamak'},
{id:'github',text:'GitHub profilini doldurmak — 5+ proje'},
{id:'deutsche',text:'Türkçe yazma — 1 hikaye veya makale yayınlamak'},
{id:'medina',text:'Medine\'de okumak için en az 1 başvuru hazırlığı'},
{id:'umre',text:'Aile ile Umre — niyet et, planla'}
];
const ROADMAP=[
{age:'17-18 yaş',title:'Lise bitirme + Üniversite hazırlık',desc:'Üniversite başvuruları. Dil seviyesi B2-C1. Portfolio.'},
{age:'18-19 yaş',title:'Medine İslam Üniversitesi · Başlangıç',desc:'Şeriat veya İslami İlimler. Arapça mükemmelleşme.'},
{age:'19-21 yaş',title:'Medine\'de 2 yıl',desc:'Arapça akıcı. Hıfz tamamı. İslami formasyon sağlam.'},
{age:'21-22 yaş',title:'KARAR ANI',desc:'Medine\'yi bitirmek mi, dondurup Asya\'ya geçmek mi?'},
{age:'22-26 yaş',title:'Tokyo / Singapore · Yazılım & AI',desc:'NUS, NTU, Tokyo Üniversitesi. Yazılım, robotik, yapay zeka.'},
{age:'26+ yaş',title:'Kendi yolun',desc:'Türkiye, Qatar, Asya — kendi şirketin, kendi araştırman.'}
];
const PROACTIVE_PROMPTS=[
'Bu hafta öğrendiğin en şaşırtıcı bilgi — yaz.',
'Bugün araştırmak istediğin 3 konu — listele, neden seçtiğini söyle.',
'Eğer bir TED konuşması yapsan — konun ne olur?',
'Bir öğretmen olsaydın — bugün hangi konuyu, kime, nasıl öğretirdin?',
'Dünyada şu anda olan 1 olay — hakkında ne düşünüyorsun? (Politik değil, bilimsel/insani)',
'Bir röportaj yapsan kiminle yapardın? Hangi 3 soru sorardın?',
'Bir ürün eleştirisi yaz — kullandığın bir uygulama, oyun, alet — iyi/kötü.',
'Bir konuyu kendine anlat (kameraya gibi) — bu hafta öğrendiğin bir şey, 3-5 dakika sözlü anlatım. Sonra metni yaz.'
];
const SURPRISES={
3:{title:'3 gün üst üste!',message:'Zincir başladı. Bir karakteri inşa eden ilk taşlar. Devam et.'},
7:{title:'1 hafta!',message:'Yedi gün. Sıradan değil. Babanın bir sürprizi yolda — belki o mekanik klavye, belki o kulaklık.'},
14:{title:'2 hafta!',message:'İki hafta — alışkanlık şekilleniyor. Çoğu insan bu noktaya gelmez. Sen geldin.'},
21:{title:'21 gün — Yeni alışkanlık',message:'Bilim diyor ki 21 gün = yeni bir alışkanlık beyne kazınır. Sen artık başka bir Faruk\'sun.'},
30:{title:'1 ay! Milat',message:'Otuz gün. Bunu çoğu insan başaramaz. Babandan büyük bir sürpriz — Raspberry Pi, Arduino, ya da seni şaşırtacak bir şey.'},
60:{title:'2 ay!',message:'60 gün. Asya seyahati hazırlığı için büyük bir hediye yolda.'},
100:{title:'100 GÜN!',message:'Yüz. Çoğu insan 7 gün dayanamaz. Babandan en büyük sürpriz: belki bir Umre, belki Medine ziyareti.'}
};
const WEEKDAY_BLOCKS_FULL=[
{id:'fajr',time:'04:30',icon:'☾',cat:'prayer',title:'Sabah Namazı',desc:'Allah\'a günün ilk sözünü ver',steps:['Abdest al','2 sünnet + 2 farz','Tesbihat: 33-33-33 + Ayet\'el-Kürsi','Sabah duasını oku'],note:'"Sabah namazı, dünya ve içindekilerden hayırlıdır" — Buhârî'},
{id:'sleep_back',time:'04:45',icon:'☽',cat:'rest',title:'Tekrar uyku',desc:'Vücut hâlâ dinlenmek istiyor',steps:['Yatağa dön','06:00 alarmı kur','Telefonu uzaklaştır'],note:''},
{id:'morning',time:'06:00',icon:'✦',cat:'health',title:'Sabah Rutini',desc:'Diş, deodorant, güneş kremi, beslenme',steps:['Diş fırçala','Deodorant','Güneş kremi (Doha güneşi sert)','Beslenme/öğle yemeği al','Çantayı kontrol et','06:30 evden çık'],note:'1 bardak suyla başla, çantanda mutlaka su olsun.'},
{id:'school',time:'06:30',icon:'✧',cat:'school',title:'Okul + Yol',desc:'06:30 çıkış → 15:30 evde',steps:['Telefonu sessize al','Defter ve kalem hazır','Derste aktif ol','Sorularını çekinmeden sor','Kahvaltını okulda yap'],note:'Tüm dersler 100 — bu seviyeyi koru. Disiplin senin sermayen.'},
{id:'home',time:'15:30',icon:'◔',cat:'health',title:'Eve Dönüş + Su',desc:'Bol su iç, üstünü değiştir',steps:['Kapıdan girer girmez 1 büyük bardak su','Üstünü değiştir, rahat kıyafet','Hafif bir şeyler atıştır','İkindi namazını kıl'],note:'Sıcaktan susuz kalmak performansı düşürür.'},
{id:'asr',time:'15:30',icon:'◑',cat:'prayer',title:'İkindi Namazı',desc:'Eve gelir gelmez kıl',steps:['Abdest al','4 sünnet + 4 farz','Tesbihat','İkindi duasını oku'],note:'İkindi vakti dua kabul vakitlerindendir.'},
{id:'sat',time:'16:30',icon:'✎',cat:'skill',title:'SAT Çalışması',desc:'Faruk\'un kendi planı — dokunulmuyor',steps:['Konu seç','Pratik test çöz','Hatalı soruları analiz et'],note:'6 Haziran sınava 1 ay kaldı — odaklan.'},
{id:'rest1',time:'17:30',icon:'◌',cat:'rest',title:'Dinlenme',desc:'Su, hafif sohbet',steps:[],note:''},
{id:'maghrib',time:'18:25',icon:'◐',cat:'prayer',title:'Akşam Namazı',desc:'Mağrib vakti',steps:['Abdest al','3 farz + 2 sünnet','Tesbihat','Akşam duasını oku','1 dakika kişisel dua'],note:'Akşam vakti dua kabul vakitlerinden.'},
{id:'lang',time:'18:30',icon:'ع',cat:'arabic',title:'Dil Çalışması',desc:'Arapça + Japonca + Tech Arapçası',steps:['Öğren sekmesini aç','3 Arapça + 3 Japonca kelime + 1 tech Arapça','Sesli oku, defterine yaz','Akşam yatmadan zihinde tekrar et'],note:'Her gün 7 kelime × 365 gün = 2555 kelime/yıl. Akıcı konuşan Faruk.'},
{id:'rest2',time:'19:30',icon:'◌',cat:'rest',title:'Dinlenme + Yemek',desc:'',steps:[],note:''},
{id:'isha',time:'19:55',icon:'☽',cat:'prayer',title:'Yatsı Namazı',desc:'Günü kapat',steps:['Abdest al','4 sünnet + 4 farz + 2 son sünnet + 3 vitir','Tesbihat','Yatsı duasını oku'],note:'Yatsıdan sonra "Bismike emûtü ve ahyâ" — bu dua ile uyu.'},
{id:'kuran_daily',time:'20:30',icon:'۞',cat:'kuran',title:'Günlük Kuran 30 dk',desc:'Kesinlikle hergün',steps:['Kaldığın sayfadan oku','Sesli okuyarak (kıraat alıştırması)','Anlamına da bak','Sayfanın fotoğrafını uygulamaya yükle'],note:'Salı/Perşembe/Cumartesi: Önce sure tekrarı + yeni sure (15+15 dk).'},
{id:'kitap',time:'21:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 30 dk',desc:'Mühendis çok okur',steps:['Şu an okuduğun kitabı aç','En az 15-20 sayfa','Etkileyen bir cümleyi Kitap sekmesine yaz'],note:'Okuma alışkanlığı — bu yaşta kazanılır, yoksa kaybedilir.'},
{id:'journal',time:'21:30',icon:'✎',cat:'reflect',title:'Akşam Defteri + Email',desc:'3 başarı yaz, gün sonu raporu gönder',steps:['Bugün sekmesinde 3 satırı doldur','Yarın için 1 niyet yaz','📧 Anne & Babaya gün sonu raporu gönder','Telefonu yatak odasından çıkar'],note:'Her gece 3 başarı = 1 yıl sonra 1095 başarın.'},
{id:'sleep',time:'22:00',icon:'☾',cat:'rest',title:'Uyku — 22:00 SHARP',desc:'6.5 saat (04:30 Fajr için)',steps:['Telefonu uzakta bırak','Bugünün kelimelerini zihinde tekrar et','"Bismike emûtü ve ahyâ" — Allahım senin isminle uyur, senin isminle uyanırım','Ayet\'el-Kürsi okuyarak uyu'],note:'Düzenli uyku = sabit beyin = sabit performans. 22:00 SHARP — pazarlık yok.'}
];
const WEEKDAY_BLOCKS_NOSAT=[
{id:'fajr',time:'04:30',icon:'☾',cat:'prayer',title:'Sabah Namazı',desc:'Günün ilk sözü',steps:['Abdest','2 sünnet + 2 farz','Tesbihat','Sabah duası'],note:''},
{id:'sleep_back',time:'04:45',icon:'☽',cat:'rest',title:'Tekrar uyku',desc:'',steps:[],note:''},
{id:'morning',time:'06:00',icon:'✦',cat:'health',title:'Sabah Rutini',desc:'Diş, deodorant, güneş kremi',steps:['Diş','Deodorant','Güneş kremi','Su iç'],note:''},
{id:'school',time:'06:30',icon:'✧',cat:'school',title:'Okul + Yol',desc:'15:30\'a kadar',steps:[],note:'SAT bitti — okul yine birinci öncelik. Tüm dersler 100.'},
{id:'home',time:'15:30',icon:'◔',cat:'health',title:'Eve Dönüş + Su',desc:'',steps:[],note:''},
{id:'asr',time:'15:30',icon:'◑',cat:'prayer',title:'İkindi Namazı',desc:'',steps:[],note:''},
{id:'kod',time:'16:30',icon:'⌨',cat:'skill',title:'Kod / Yazılım Atölyesi',desc:'SAT yerine: kod projeleri',steps:['Kod sekmesinden bir proje seç','En az 1 saat üzerinde çalış','GitHub\'a commit at'],note:'SAT bitti — şimdi sıra kendi yapay zeka projende.'},
{id:'rest1',time:'17:30',icon:'◌',cat:'rest',title:'Dinlenme',desc:'',steps:[],note:''},
{id:'maghrib',time:'18:25',icon:'◐',cat:'prayer',title:'Akşam Namazı',desc:'',steps:[],note:''},
{id:'lang',time:'18:30',icon:'ع',cat:'arabic',title:'Dil Çalışması',desc:'Arapça + Japonca + Tech',steps:[],note:''},
{id:'rest2',time:'19:30',icon:'◌',cat:'rest',title:'Yemek + Dinlenme',desc:'',steps:[],note:''},
{id:'isha',time:'19:55',icon:'☽',cat:'prayer',title:'Yatsı Namazı',desc:'',steps:[],note:''},
{id:'kuran_daily',time:'20:30',icon:'۞',cat:'kuran',title:'Günlük Kuran 30 dk',desc:'',steps:[],note:''},
{id:'kitap',time:'21:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 30 dk',desc:'',steps:[],note:''},
{id:'journal',time:'21:30',icon:'✎',cat:'reflect',title:'Akşam Defteri + Email',desc:'',steps:[],note:''},
{id:'sleep',time:'22:00',icon:'☾',cat:'rest',title:'Uyku — 22:00 SHARP',desc:'',steps:[],note:''}
];
const SUMMER_BLOCKS=[
{id:'fajr',time:'04:30',icon:'☾',cat:'prayer',title:'Sabah Namazı',desc:'Yaz tatili — disiplin yine aynı',steps:['Abdest','2 sünnet + 2 farz','Tesbihat','Sabah duası'],note:'Yaz farklı tempo — ama Fajr aynı.'},
{id:'sleep_back',time:'04:45',icon:'☽',cat:'rest',title:'Tekrar uyku',desc:'09:00\'a kadar',steps:[],note:''},
{id:'wake',time:'09:00',icon:'◷',cat:'health',title:'Uyanma + Kahvaltı',desc:'Aile ile',steps:['Yüzünü yıka','Bol su iç','Aileyle kahvaltı et — telefon yok'],note:'Yaz sabahları aile zamanı.'},
{id:'kod',time:'10:00',icon:'⌨',cat:'skill',title:'Kod / Atölye 2 saat',desc:'Yaz = projelerin zamanı',steps:['Bir AI projesi seç','En az 2 saat odaklı çalış','GitHub\'a commit'],note:'Yaz boyunca 1 büyük proje bitirme hedefi.'},
{id:'lang',time:'12:00',icon:'ع',cat:'arabic',title:'Dil Çalışması',desc:'Arapça + Japonca + Tech',steps:[],note:''},
{id:'lunch',time:'13:00',icon:'◌',cat:'rest',title:'Öğle yemeği + Dinlenme',desc:'',steps:[],note:''},
{id:'kitap_summer',time:'14:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 1 saat',desc:'Yaz tatili — daha çok oku',steps:['Şu an okuduğun kitap','En az 30-50 sayfa','Etkileyen cümleyi yaz'],note:'Yaz hedefi: 3-4 kitap bitir.'},
{id:'asr',time:'15:30',icon:'◑',cat:'prayer',title:'İkindi Namazı',desc:'',steps:[],note:''},
{id:'spor_summer',time:'16:00',icon:'💪',cat:'sport',title:'Spor + Yüzme/Yürüyüş',desc:'Yaz aktif',steps:['Spor sekmesinden günlük plan','Akşam serinde yürüyüş','Yüzme havuza git'],note:''},
{id:'maghrib',time:'18:25',icon:'◐',cat:'prayer',title:'Akşam Namazı',desc:'',steps:[],note:''},
{id:'family',time:'19:00',icon:'♡',cat:'family',title:'Aile Zamanı',desc:'Sohbet, çay, oyun',steps:['Telefon yok','Anne baba ile sohbet','Hatice ile bir şey yap'],note:'Yaz aile için en bereketli vakit.'},
{id:'isha',time:'19:55',icon:'☽',cat:'prayer',title:'Yatsı Namazı',desc:'',steps:[],note:''},
{id:'kuran_daily',time:'20:30',icon:'۞',cat:'kuran',title:'Günlük Kuran 30 dk',desc:'',steps:[],note:'Yaz hedefi: 5 sure ezberle.'},
{id:'kitap_evening',time:'21:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 30 dk',desc:'',steps:[],note:''},
{id:'journal',time:'21:30',icon:'✎',cat:'reflect',title:'Akşam Defteri + Email',desc:'',steps:[],note:''},
{id:'sleep',time:'22:00',icon:'☾',cat:'rest',title:'Uyku — 22:00 SHARP',desc:'',steps:[],note:''}
];
const WEEKEND_BLOCKS=[
{id:'fajr_w',time:'04:30',icon:'☾',cat:'prayer',title:'Sabah Namazı',desc:'Hafta sonu da disiplin',steps:['Abdest','Namaz','Tesbihat','Cuma günü Kehf suresi'],note:'Cuma: "İki Cuma arası nur olur"'},
{id:'sleep_back_w',time:'04:45',icon:'☽',cat:'rest',title:'Tekrar uyku',desc:'09:30\'a kadar',steps:[],note:''},
{id:'wake_w',time:'09:30',icon:'◷',cat:'health',title:'Uyanma + Kahvaltı',desc:'Aile sofrası — telefonsuz',steps:[],note:'Hafta sonu kahvaltısı — ailenin enerjisi haftaya yansır.'},
{id:'sat_w1',time:'11:00',icon:'✎',cat:'skill',title:'SAT Çalışması',desc:'Faruk\'un planı',steps:[],note:''},
{id:'rest_w1',time:'12:30',icon:'◌',cat:'rest',title:'Dinlenme',desc:'',steps:[],note:''},
{id:'lang_w',time:'14:00',icon:'ع',cat:'arabic',title:'Dil + Sahâbe',desc:'Hafta sonu derinleş',steps:['3 Arapça + 3 Japonca + 1 tech','Bu haftanın sahâbe hikayesi','Defterine notunu al'],note:''},
{id:'kitap_w',time:'15:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 1 saat',desc:'Hafta sonu ekstra okuma',steps:[],note:''},
{id:'asr_w',time:'16:00',icon:'◑',cat:'prayer',title:'İkindi Namazı',desc:'',steps:[],note:''},
{id:'sat_w2',time:'16:30',icon:'✎',cat:'skill',title:'SAT / Ek Çalışma',desc:'',steps:[],note:''},
{id:'rest_w3',time:'18:00',icon:'◌',cat:'rest',title:'Dinlenme',desc:'',steps:[],note:''},
{id:'maghrib_w',time:'18:25',icon:'◐',cat:'prayer',title:'Akşam Namazı',desc:'',steps:[],note:''},
{id:'kuran_w',time:'19:30',icon:'۞',cat:'kuran',title:'Günlük Kuran 30 dk',desc:'',steps:[],note:''},
{id:'family_w',time:'20:00',icon:'♡',cat:'family',title:'Aile + Çay',desc:'Telefonsuz',steps:[],note:'Hafta sonu en bereketli vakit.'},
{id:'isha_w',time:'20:30',icon:'☽',cat:'prayer',title:'Yatsı Namazı',desc:'',steps:[],note:''},
{id:'kitap_w_eve',time:'21:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 30 dk',desc:'',steps:[],note:'Hafta sonu daha fazla oku.'},
{id:'journal_w',time:'21:30',icon:'✎',cat:'reflect',title:'Akşam Defteri + Email',desc:'Cumartesi gecesi babanla 15 dk değerlendirme',steps:[],note:''},
{id:'sleep_w',time:'22:00',icon:'☾',cat:'rest',title:'Uyku — 22:00 SHARP',desc:'',steps:[],note:''}
];
const WEEKEND_BLOCKS_NOSAT=[
{id:'fajr_w',time:'04:30',icon:'☾',cat:'prayer',title:'Sabah Namazı',desc:'Hafta sonu da disiplin',steps:[],note:''},
{id:'sleep_back_w',time:'04:45',icon:'☽',cat:'rest',title:'Tekrar uyku',desc:'09:30\'a kadar',steps:[],note:''},
{id:'wake_w',time:'09:30',icon:'◷',cat:'health',title:'Uyanma + Kahvaltı',desc:'Aile sofrası',steps:[],note:''},
{id:'kod_w',time:'11:00',icon:'⌨',cat:'skill',title:'Kod / Atölye 2 saat',desc:'SAT bitti — yapay zeka projeleri',steps:['Bir AI projesi seç','GitHub\'a commit at'],note:'Hafta sonu = derin odaklanma günü.'},
{id:'rest_w1',time:'13:00',icon:'◌',cat:'rest',title:'Öğle yemeği + Dinlenme',desc:'',steps:[],note:''},
{id:'lang_w',time:'14:00',icon:'ع',cat:'arabic',title:'Dil + Sahâbe',desc:'',steps:[],note:''},
{id:'kitap_w',time:'15:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 1 saat',desc:'Hafta sonu ekstra okuma',steps:[],note:''},
{id:'asr_w',time:'16:00',icon:'◑',cat:'prayer',title:'İkindi Namazı',desc:'',steps:[],note:''},
{id:'kod_w2',time:'16:30',icon:'⌨',cat:'skill',title:'Kod / Yaratıcı Proje',desc:'',steps:[],note:''},
{id:'rest_w3',time:'18:00',icon:'◌',cat:'rest',title:'Dinlenme',desc:'',steps:[],note:''},
{id:'maghrib_w',time:'18:25',icon:'◐',cat:'prayer',title:'Akşam Namazı',desc:'',steps:[],note:''},
{id:'kuran_w',time:'19:30',icon:'۞',cat:'kuran',title:'Günlük Kuran 30 dk',desc:'',steps:[],note:''},
{id:'family_w',time:'20:00',icon:'♡',cat:'family',title:'Aile + Çay',desc:'Telefonsuz',steps:[],note:''},
{id:'isha_w',time:'20:30',icon:'☽',cat:'prayer',title:'Yatsı Namazı',desc:'',steps:[],note:''},
{id:'kitap_w_eve',time:'21:00',icon:'📚',cat:'kitap',title:'Kitap Okuma 30 dk',desc:'',steps:[],note:''},
{id:'journal_w',time:'21:30',icon:'✎',cat:'reflect',title:'Akşam Defteri + Email',desc:'',steps:[],note:''},
{id:'sleep_w',time:'22:00',icon:'☾',cat:'rest',title:'Uyku — 22:00 SHARP',desc:'',steps:[],note:''}
];
let state={name:'',setupDone:false,completed:{},exerciseDone:{},journal:{},creative:{},streak:{current:0,longest:0,lastDate:null},shownSurprises:[],kuranData:{},startDate:null,checklistDone:[],bookData:{currentBook:'',bookQuote:'',totalBooks:0,bookPagesByDay:{}},babaEmail:'oaydemir@worldcentralkitchen.org',anneEmail:''};
function loadState(){try{const s=localStorage.getItem(STORAGE_KEY);if(s){const parsed=JSON.parse(s);state={...state,...parsed};if(!state.bookData)state.bookData={currentBook:'',bookQuote:'',totalBooks:0,bookPagesByDay:{}};if(!state.checklistDone)state.checklistDone=[];}}catch(e){console.error(e);}}
function saveState(){try{const c=JSON.parse(JSON.stringify(state));if(c.kuranData){const d=Object.keys(c.kuranData).sort();if(d.length>7){d.slice(0,d.length-7).forEach(x=>{if(c.kuranData[x])c.kuranData[x].photo=null;});}}localStorage.setItem(STORAGE_KEY,JSON.stringify(c));}catch(e){console.error(e);if(e.name==='QuotaExceededError')alert('Depolama dolu — eski Kuran fotoğrafları temizleniyor.');}}
function todayKey(){return new Date().toISOString().split('T')[0];}
function daysSinceStart(){if(!state.startDate)return 0;return Math.floor((new Date()-new Date(state.startDate))/(1000*60*60*24));}
function speak(text,lang){if(!('speechSynthesis' in window))return;speechSynthesis.cancel();const u=new SpeechSynthesisUtterance(text);u.lang=lang||'tr-TR';u.rate=0.85;speechSynthesis.speak(u);}
function getTodayWords(){const d=daysSinceStart();return{ar:[0,1,2].map(i=>({...ARABIC_WORDS[(d*3+i)%ARABIC_WORDS.length],idx:(d*3+i)%ARABIC_WORDS.length})),jp:[0,1,2].map(i=>({...JAPANESE_WORDS[(d*3+i)%JAPANESE_WORDS.length],idx:(d*3+i)%JAPANESE_WORDS.length})),tech:[TECH_ARABIC[d%TECH_ARABIC.length]]};}
function getCurrentSahabe(){return SAHABE[Math.floor(daysSinceStart()/7)%SAHABE.length];}
function getCurrentSiret(){return SIRET_WEEKS[Math.floor(daysSinceStart()/7)%SIRET_WEEKS.length];}
function getSportWeek(){return Math.min(Math.floor(daysSinceStart()/7)+1,8);}
function getTodayPrompt(){return WRITING_PROMPTS[daysSinceStart()%WRITING_PROMPTS.length];}
function getTodayWisdom(){return DAILY_WISDOM[daysSinceStart()%DAILY_WISDOM.length];}
function getTodayBlocks(){const t=todayKey();const day=new Date().getDay();if(t>=SCHOOL_END)return SUMMER_BLOCKS;if(day===5||day===6){if(t>SAT_LAST_STUDY)return WEEKEND_BLOCKS_NOSAT;return WEEKEND_BLOCKS;}if(t>SAT_LAST_STUDY)return WEEKDAY_BLOCKS_NOSAT;return WEEKDAY_BLOCKS_FULL;}
function isAfterSat(){return todayKey()>SAT_DATE;}
function isSummer(){return todayKey()>=SCHOOL_END;}
function completeSetup(){const n=document.getElementById('nameInput').value.trim();if(!n)return;state.name=n;state.setupDone=true;state.startDate=todayKey();saveState();initApp();}
function initApp(){document.getElementById('setup').style.display='none';document.getElementById('app').style.display='block';document.getElementById('userName').textContent=state.name;document.getElementById('currentName').textContent=state.name;const n=new Date();document.getElementById('dayName').textContent=DAY_NAMES[n.getDay()];document.getElementById('dateStr').textContent=n.toLocaleDateString('tr-TR',{day:'numeric',month:'long'});if(state.babaEmail)document.getElementById('babaEmail').value=state.babaEmail;if(state.anneEmail)document.getElementById('anneEmail').value=state.anneEmail;updateStreak();renderAll();loadJournal();loadBookData();updateAllStats();}
function updateAllStats(){document.getElementById('streakNum').textContent=state.streak.current;document.getElementById('sportWeek').textContent=getSportWeek();document.getElementById('totalPages').textContent=Object.values(state.kuranData).filter(d=>d&&d.read).length;document.getElementById('totalDays').textContent=daysSinceStart();document.getElementById('totalBooks').textContent=state.bookData.totalBooks||0;const t=todayKey();document.getElementById('bookPagesNum').textContent=(state.bookData.bookPagesByDay&&state.bookData.bookPagesByDay[t])||0;renderStreakDisplay();}
function updateStreak(){const t=todayKey();if(state.streak.lastDate&&state.streak.lastDate!==t){const diff=Math.floor((new Date(t)-new Date(state.streak.lastDate))/(1000*60*60*24));if(diff>1)state.streak.current=0;}saveState();}
function renderStreakDisplay(){const c=document.getElementById('streakChain');c.innerHTML='';const f=Math.min(state.streak.current%7||(state.streak.current>0?7:0),7);for(let i=0;i<7;i++){const l=document.createElement('div');l.className='link'+(i<f?' filled':'');c.appendChild(l);}}
function renderBanner(){const t=todayKey();let msg;if(t===SAT_DATE){msg='📝 BUGÜN SAT GÜNÜ! Bismillah. Bildiklerini güvenle yaz, sakin gir, sakin çık. Sen hazırsın.';}else if(t===SCHOOL_END){msg='🌴 BUGÜN OKUL KAPANIŞ! Tüm dersler 100 — gurur duy. Yaz programı başlıyor.';}else if(isSummer()){msg='🌴 Yaz tatili — farklı tempo, aynı disiplin. Daha çok kitap, daha çok kod, daha çok aile.';}else if(isAfterSat()){const d=Math.ceil((new Date(SCHOOL_END)-new Date(t))/(1000*60*60*24));msg='✓ SAT bitti. Okul kapanışına '+d+' gün. SAT yerine artık kod ve projeler.';}else{const d=Math.ceil((new Date(SAT_DATE)-new Date(t))/(1000*60*60*24));const day=new Date().getDay();const m={0:'Pazar — yeni hafta. Bismillah.',1:'Pazartesi — haftanın motoru.',2:'Salı — derinleşme günü.',3:'Çarşamba — orta nokta.',4:'Perşembe — Cuma\'ya hazırlık.',5:'Cuma — bereketli gün. Kehf, atölye, aile.',6:'Cumartesi — yenilenme.'};msg=m[day]+' SAT\'a '+d+' gün.';}document.getElementById('banner').textContent=msg;}
function renderAll(){renderBanner();renderToday();renderGoal();renderLearn();renderSahabe();renderSport();renderCode();renderBook();renderWrite();}
function renderToday(){const blocks=getTodayBlocks();const t=todayKey();const done=state.completed[t]||[];const list=document.getElementById('blocksList');list.innerHTML='';blocks.forEach(b=>{const isDone=done.includes(b.id);const div=document.createElement('div');div.className='block cat-'+b.cat+(isDone?' done':'');let stepsHtml='';if(b.steps&&b.steps.length>0)stepsHtml='<div class="steps"><ol>'+b.steps.map(s=>'<li>'+s+'</li>').join('')+'</ol></div>';let noteHtml=b.note?'<div class="note">'+b.note+'</div>':'';div.innerHTML='<div class="block-time">'+b.time+'</div><div class="block-icon">'+b.icon+'</div><div class="block-content"><div class="title">'+b.title+'</div><div class="desc">'+b.desc+'</div>'+stepsHtml+noteHtml+'</div><div class="block-check'+(isDone?' checked':'')+'" onclick="event.stopPropagation();toggleBlock(\''+b.id+'\')"></div>';div.onclick=()=>div.classList.toggle('expanded');list.appendChild(div);});updateProgress();renderTodaySport();}
function toggleBlock(id){const t=todayKey();if(!state.completed[t])state.completed[t]=[];const idx=state.completed[t].indexOf(id);if(idx===-1){state.completed[t].push(id);}else{state.completed[t].splice(idx,1);}checkStreak();saveState();renderToday();updateAllStats();updateProgress();}
function updateProgress(){const blocks=getTodayBlocks();const t=todayKey();const done=(state.completed[t]||[]).length;const pct=Math.round((done/blocks.length)*100);document.getElementById('todayPct').textContent=pct;document.getElementById('progressFill').style.width=pct+'%';}
function checkStreak(){const t=todayKey();const blocks=getTodayBlocks();const done=(state.completed[t]||[]).length;if(done>=Math.ceil(blocks.length*0.7)){if(state.streak.lastDate!==t){state.streak.current=(state.streak.lastDate===yesterdayKey())?state.streak.current+1:1;state.streak.lastDate=t;if(state.streak.current>state.streak.longest)state.streak.longest=state.streak.current;checkSurprise();saveState();updateAllStats();}}}
function yesterdayKey(){const d=new Date();d.setDate(d.getDate()-1);return d.toISOString().split('T')[0];}
function checkSurprise(){const days=[3,7,14,21,30,60,100];const cur=state.streak.current;if(days.includes(cur)&&!state.shownSurprises.includes(cur)){state.shownSurprises.push(cur);saveState();showModal(SURPRISES[cur]);}}
function showModal(s){document.getElementById('modalIcon').textContent=s.title.includes('100')?'🕋':s.title.includes('30')||s.title.includes('60')?'🎁':'✨';document.getElementById('modalOrnament').textContent=s.title;document.getElementById('modalMsg').textContent=s.message;document.getElementById('modalOverlay').classList.add('show');}
function closeModal(){document.getElementById('modalOverlay').classList.remove('show');}
function renderGoal(){const c=document.getElementById('checklist16');c.innerHTML='';GOAL_CHECKLIST_16.forEach(item=>{const isDone=state.checklistDone.includes(item.id);const div=document.createElement('div');div.className='checklist-item'+(isDone?' done':'');div.innerHTML='<div class="ck"></div><div>'+item.text+'</div>';div.onclick=()=>toggleChecklistItem(item.id);c.appendChild(div);});const r=document.getElementById('roadmapList');r.innerHTML='';ROADMAP.forEach((m,i)=>{const div=document.createElement('div');div.className='checklist-card';div.innerHTML='<div class="ch-year">'+m.age+'</div><div class="ch-title">'+m.title+'</div><div style="font-size:12px;color:var(--text-soft);line-height:1.6">'+m.desc+'</div>';r.appendChild(div);});}
function toggleChecklistItem(id){const idx=state.checklistDone.indexOf(id);if(idx===-1)state.checklistDone.push(id);else state.checklistDone.splice(idx,1);saveState();renderGoal();}
function renderLearn(){const w=getTodayWords();const ar=document.getElementById('arabicWords');ar.innerHTML='';w.ar.forEach(word=>{const div=document.createElement('div');div.className='word-card ar';div.innerHTML='<span class="lang-badge">عربي · Arapça</span><div class="word-row"><div class="word-arabic">'+word.word+'</div><button class="pronounce" onclick="speak(\''+word.word.replace(/'/g,"\\'")+'\',\'ar-SA\')">🔊</button></div><div class="meaning">'+word.meaning+'</div><div class="latin">'+word.latin+'</div><div class="example">'+word.example+'</div>';ar.appendChild(div);});const jp=document.getElementById('japaneseWords');jp.innerHTML='';w.jp.forEach(word=>{const div=document.createElement('div');div.className='word-card jp';div.innerHTML='<span class="lang-badge">日本語 · Japonca</span><div class="word-row"><div class="word-jp">'+word.word+'</div><button class="pronounce" onclick="speak(\''+word.word.replace(/'/g,"\\'")+'\',\'ja-JP\')">🔊</button></div><div class="meaning">'+word.meaning+'</div><div class="latin">'+word.latin+'</div><div class="example">'+word.example+'</div>';jp.appendChild(div);});const tech=document.getElementById('techArabicWords');tech.innerHTML='';w.tech.forEach(word=>{const div=document.createElement('div');div.className='word-card tech';div.innerHTML='<span class="lang-badge">⌨ Tech Arapçası</span><div class="word-row"><div class="word-arabic">'+word.word+'</div><button class="pronounce" onclick="speak(\''+word.word.replace(/'/g,"\\'")+'\',\'ar-SA\')">🔊</button></div><div class="meaning">'+word.meaning+'</div><div class="latin">'+word.latin+'</div><div class="example">'+word.example+'</div>';tech.appendChild(div);});const pl=document.getElementById('prayersList');pl.innerHTML='';PRAYERS.forEach(p=>{const div=document.createElement('div');div.className='dua-card';div.innerHTML='<div class="header-row"><div class="prayer-name">'+p.name+'</div><div class="prayer-time">'+p.time+'</div></div><div class="arabic">'+p.arabic+'</div><div class="latin">'+p.latin+'</div><div class="meaning">'+p.meaning+'</div>';pl.appendChild(div);});const sw=getCurrentSiret();document.getElementById('siretWeek').innerHTML='<div class="sahabe-card"><span class="sahabe-week-tag">Hafta '+sw.week+'</span><div class="name">'+sw.theme+'</div><div class="story">'+sw.text+'</div><div class="lesson">'+sw.lesson+'</div></div>';}
function renderSahabe(){const cur=getCurrentSahabe();const ws=document.getElementById('weekSahabe');ws.innerHTML='<div class="sahabe-card"><span class="sahabe-week-tag">Bu hafta</span><div class="name">'+cur.name+'</div><div class="title">'+cur.title+'</div><div class="story">'+cur.story+'</div><div class="lesson">'+cur.lesson+'</div></div>';const all=document.getElementById('allSahabe');all.innerHTML='';SAHABE.forEach(s=>{const div=document.createElement('div');div.className='sahabe-card';div.innerHTML='<div class="name">'+s.name+'</div><div class="title">'+s.title+'</div><div class="story">'+s.story+'</div><div class="lesson">'+s.lesson+'</div>';all.appendChild(div);});}
function renderSport(){const w=getSportWeek();const p=SPORT_PROGRAM[w];document.getElementById('sportWeekInfo').innerHTML='<div class="week-info"><div class="week-num">Hafta '+w+' / 8</div><div class="week-name">'+p.name+'</div><div class="week-desc">'+p.desc+'</div></div>';renderSportList();}
function renderSportList(){const w=getSportWeek();const p=SPORT_PROGRAM[w];const t=todayKey();const done=state.exerciseDone[t]||[];const list=document.getElementById('sportList');list.innerHTML='';p.daily.forEach((ex,i)=>{const isDone=done.includes(i);const div=document.createElement('div');div.className='exercise-card'+(isDone?' done':'');div.innerHTML='<div class="ex-check"></div><div class="ex-content"><div class="ex-name">'+ex.name+'</div><div class="ex-detail">'+ex.detail+'</div></div>';div.onclick=()=>toggleExercise(i);list.appendChild(div);});}
function renderTodaySport(){const w=getSportWeek();const p=SPORT_PROGRAM[w];const t=todayKey();const done=state.exerciseDone[t]||[];const list=document.getElementById('todaySport');list.innerHTML='';p.daily.forEach((ex,i)=>{const isDone=done.includes(i);const div=document.createElement('div');div.className='exercise-card'+(isDone?' done':'');div.innerHTML='<div class="ex-check"></div><div class="ex-content"><div class="ex-name">'+ex.name+'</div><div class="ex-detail">'+ex.detail+'</div></div>';div.onclick=()=>toggleExercise(i);list.appendChild(div);});}
function toggleExercise(i){const t=todayKey();if(!state.exerciseDone[t])state.exerciseDone[t]=[];const idx=state.exerciseDone[t].indexOf(i);if(idx===-1){state.exerciseDone[t].push(i);}else{state.exerciseDone[t].splice(idx,1);}saveState();renderSportList();renderTodaySport();}
function renderCode(){const list=document.getElementById('codeProjects');list.innerHTML='';CODE_PROJECTS.forEach(p=>{const div=document.createElement('div');div.className='code-card';const lvl=p.level==='İleri'?'ileri':'';div.innerHTML='<span class="level-badge '+lvl+'">'+p.level+'</span><div class="proj-name">'+p.name+'</div><div class="proj-desc">'+p.desc+'</div><div class="tech-stack">'+p.stack.map(s=>'<span class="tech-tag">'+s+'</span>').join('')+'</div>';list.appendChild(div);});const e=document.getElementById('entrepreneurs');e.innerHTML='';ENTREPRENEURS.forEach(en=>{const div=document.createElement('div');div.className='entrepreneur-card';div.innerHTML='<div><span class="country">'+en.country+'</span><span class="name">'+en.name+'</span></div><div class="role">'+en.role+'</div><div class="story">'+en.story+'</div><div class="lesson">'+en.lesson+'</div>';e.appendChild(div);});}
function renderBook(){const list=document.getElementById('bookList');list.innerHTML='';RECOMMENDED_BOOKS.forEach(b=>{const div=document.createElement('div');div.className='book-card';div.innerHTML='<span class="b-cat '+b.cat+'">'+b.catLabel+'</span><div class="b-name">'+b.name+'</div><div class="b-author">'+b.author+'</div><div class="b-why">'+b.why+'</div>';list.appendChild(div);});const w=getTodayWisdom();document.getElementById('dailyWisdom').innerHTML='<div class="dua-card"><div class="header-row"><div class="prayer-name">'+w.type+'</div><div class="prayer-time">'+w.source+'</div></div>'+(w.text.match(/[\u0600-\u06FF]/)?'<div class="arabic">'+w.text+'</div>':'<div style="font-size:15px;color:var(--gold-light);font-style:italic;margin-bottom:8px;line-height:1.6">'+w.text+'</div>')+'<div class="meaning">'+w.meaning+'</div></div>';}
function loadBookData(){if(state.bookData.currentBook)document.getElementById('currentBook').value=state.bookData.currentBook;if(state.bookData.bookQuote)document.getElementById('bookQuote').value=state.bookData.bookQuote;const t=todayKey();const todayPages=(state.bookData.bookPagesByDay&&state.bookData.bookPagesByDay[t])||0;document.getElementById('bookPages').value=todayPages||'';}
function saveBook(){state.bookData.currentBook=document.getElementById('currentBook').value;saveState();}
function saveBookQuote(){state.bookData.bookQuote=document.getElementById('bookQuote').value;saveState();}
function saveBookPages(){const t=todayKey();const p=parseInt(document.getElementById('bookPages').value)||0;if(!state.bookData.bookPagesByDay)state.bookData.bookPagesByDay={};state.bookData.bookPagesByDay[t]=p;saveState();updateAllStats();}
function finishBook(){if(!state.bookData.currentBook){alert('Önce kitap adını yaz.');return;}if(confirm('"'+state.bookData.currentBook+'" kitabını bitirdin mi? Tebrikler!')){state.bookData.totalBooks=(state.bookData.totalBooks||0)+1;state.bookData.currentBook='';state.bookData.bookQuote='';document.getElementById('currentBook').value='';document.getElementById('bookQuote').value='';saveState();updateAllStats();alert('🎉 '+state.bookData.totalBooks+' kitap bitirdin! Bir sonrakine bismillah.');}}
function renderWrite(){document.getElementById('todayPrompt').textContent=getTodayPrompt();const t=todayKey();if(state.creative[t])document.getElementById('creativeText').value=state.creative[t];const p=document.getElementById('proactivePrompts');p.innerHTML='';PROACTIVE_PROMPTS.forEach(text=>{const div=document.createElement('div');div.className='prompt-card';div.style.background='linear-gradient(135deg,var(--rose-soft) 0%,var(--surface) 100%)';div.style.borderColor='rgba(244,114,182,.2)';div.innerHTML='<div class="prompt-label" style="color:var(--rose)">İlham</div><div class="prompt-text">'+text+'</div>';p.appendChild(div);});}
function loadJournal(){const t=todayKey();const j=state.journal[t]||{};document.getElementById('j1').value=j[1]||'';document.getElementById('j2').value=j[2]||'';document.getElementById('j3').value=j[3]||'';if(state.kuranData[t]){document.getElementById('kuranPages').value=state.kuranData[t].pages||'';if(state.kuranData[t].photo){const p=document.getElementById('kuranPreview');p.src=state.kuranData[t].photo;p.classList.add('show');}}}
function saveJournal(){const t=todayKey();state.journal[t]={1:document.getElementById('j1').value,2:document.getElementById('j2').value,3:document.getElementById('j3').value};saveState();}
function saveCreative(){const t=todayKey();state.creative[t]=document.getElementById('creativeText').value;saveState();}
function saveKuran(){const t=todayKey();const p=parseInt(document.getElementById('kuranPages').value)||0;if(!state.kuranData[t])state.kuranData[t]={};state.kuranData[t].read=p>0;state.kuranData[t].pages=p;saveState();updateAllStats();}
function uploadKuranPhoto(e){const f=e.target.files[0];if(!f)return;const r=new FileReader();r.onload=ev=>{const t=todayKey();if(!state.kuranData[t])state.kuranData[t]={};state.kuranData[t].photo=ev.target.result;saveState();const p=document.getElementById('kuranPreview');p.src=ev.target.result;p.classList.add('show');};r.readAsDataURL(f);}
function saveEmails(){state.babaEmail=document.getElementById('babaEmail').value;state.anneEmail=document.getElementById('anneEmail').value;saveState();}
function sendDailyReport(){const t=todayKey();const blocks=getTodayBlocks();const done=state.completed[t]||[];const journal=state.journal[t]||{};const kuran=state.kuranData[t]||{};const exDone=(state.exerciseDone[t]||[]).length;const w=getSportWeek();const totalEx=SPORT_PROGRAM[w].daily.length;const todayPages=(state.bookData.bookPagesByDay&&state.bookData.bookPagesByDay[t])||0;const pct=Math.round((done.length/blocks.length)*100);const wordsToday=getTodayWords();let body='Selamün aleyküm anne, baba.\n\nBugünkü gün özetimi gönderiyorum:\n\n';body+='📅 Tarih: '+new Date().toLocaleDateString('tr-TR',{day:'numeric',month:'long',year:'numeric',weekday:'long'})+'\n';body+='✓ Tamamlanan bloklar: '+done.length+'/'+blocks.length+' (%'+pct+')\n';body+='🔥 Zincirim: '+state.streak.current+' gün\n\n';body+='— GÜNLÜK İBADET —\n';const prayerBlocks=blocks.filter(b=>b.cat==='prayer');const prayerDone=prayerBlocks.filter(b=>done.includes(b.id)).length;body+='Namaz: '+prayerDone+'/'+prayerBlocks.length+' vakit\n';body+='Kuran okuma: '+(kuran.pages||0)+' sayfa\n\n';body+='— DİL —\n';body+='Bugünkü Arapça: '+wordsToday.ar.map(w=>w.word+' ('+w.meaning+')').join(', ')+'\n';body+='Bugünkü Japonca: '+wordsToday.jp.map(w=>w.word+' ('+w.meaning+')').join(', ')+'\n';if(wordsToday.tech&&wordsToday.tech[0])body+='Tech Arapçası: '+wordsToday.tech[0].word+' ('+wordsToday.tech[0].meaning+')\n';body+='\n— SPOR —\n';body+='Hafta '+w+'/8 — yapılan: '+exDone+'/'+totalEx+' egzersiz\n\n';body+='— OKUMA —\n';if(state.bookData.currentBook){body+='Şu an okuduğum: '+state.bookData.currentBook+'\n';body+='Bugün: '+todayPages+' sayfa\n';if(state.bookData.bookQuote)body+='Bugün etkilendiğim cümle: "'+state.bookData.bookQuote+'"\n';}else{body+='Bugün okuma yok\n';}body+='Bitirdiğim toplam kitap: '+(state.bookData.totalBooks||0)+'\n\n';body+='— BUGÜN BAŞARDIĞIM 3 ŞEY —\n';body+='1. '+(journal[1]||'-')+'\n';body+='2. '+(journal[2]||'-')+'\n';body+='3. '+(journal[3]||'-')+'\n\n';if(state.creative[t]){body+='— BUGÜNÜN YAZISI —\n';body+=state.creative[t]+'\n\n';}body+='— ÖZEL NOT —\n';body+='Hatırlatma: bu uygulamadaki dualar rahmetli dedem Ebubekir Yasin\'in çalışmaları. Bugün de onu andım, kendisi için Fatiha okudum.\n\n';body+='Hayırlı geceler,\nFaruk';const subject='Faruk\'un Gün Sonu Raporu — '+t;const to=[state.babaEmail,state.anneEmail].filter(e=>e).join(',');if(!to){alert('Önce Ayarlar\'dan anne ve baba e-posta adreslerini gir.');showView('settings',document.querySelectorAll('.tab')[8]);return;}const url='mailto:'+to+'?subject='+encodeURIComponent(subject)+'&body='+encodeURIComponent(body);window.location.href=url;}
function showView(v,el){document.querySelectorAll('.view').forEach(x=>x.classList.remove('active'));document.querySelectorAll('.tab').forEach(x=>x.classList.remove('active'));document.getElementById('view-'+v).classList.add('active');if(el)el.classList.add('active');}
function changeName(){const n=prompt('Yeni isim:',state.name);if(n&&n.trim()){state.name=n.trim();saveState();document.getElementById('userName').textContent=state.name;document.getElementById('currentName').textContent=state.name;}}
function exportData(){const data=JSON.stringify(state,null,2);const b=new Blob([data],{type:'application/json'});const u=URL.createObjectURL(b);const a=document.createElement('a');a.href=u;a.download='programim_faruk_yedek_'+todayKey()+'.json';a.click();URL.revokeObjectURL(u);}
function resetAll(){if(confirm('Tüm veriler silinecek. Emin misin?')){localStorage.removeItem(STORAGE_KEY);location.reload();}}
loadState();
if(state.setupDone){initApp();}else{document.getElementById('setup').style.display='flex';document.getElementById('app').style.display='none';}
</script>
</body>
</html>
