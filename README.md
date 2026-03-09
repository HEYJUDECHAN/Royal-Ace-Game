[index.html](https://github.com/user-attachments/files/25842967/royal-ace-games.1.html)
<!DOCTYPE html>
<html lang="en" data-theme="gold">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Royal Ace Games</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;900&family=Cormorant+Garamond:ital,wght@0,300;0,600;1,300;1,400&family=Bebas+Neue&display=swap" rel="stylesheet">
<style>
[data-theme="gold"]{--a1:#c8a45a;--a2:#f0d080;--a3:#7a5e20;--a4:#3a2a08;--glow:rgba(200,164,90,.5);--glow2:rgba(200,164,90,.12);--accent-rgb:200,164,90;--t1:radial-gradient(ellipse at 30% 20%,#2a1060,#0a0520,#050210);--t2:radial-gradient(ellipse at 70% 30%,#0a3a1a,#041208,#020805);--t3:radial-gradient(ellipse at 50% 70%,#2a1a04,#0f0a02,#060402);--t4:radial-gradient(ellipse at 20% 80%,#1a0808,#0a0404,#050202);}
[data-theme="crimson"]{--a1:#c84a4a;--a2:#f08080;--a3:#7a2020;--a4:#3a0808;--glow:rgba(200,74,74,.5);--glow2:rgba(200,74,74,.12);--accent-rgb:200,74,74;--t1:radial-gradient(ellipse at 30% 20%,#3a0a0a,#180505,#0a0202);--t2:radial-gradient(ellipse at 70% 30%,#280808,#100303,#060202);--t3:radial-gradient(ellipse at 50% 70%,#200808,#0a0303,#040101);--t4:radial-gradient(ellipse at 20% 80%,#1a0808,#0c0404,#050202);}
[data-theme="sapphire"]{--a1:#4a7ac8;--a2:#80b0f0;--a3:#203a7a;--a4:#081a3a;--glow:rgba(74,122,200,.5);--glow2:rgba(74,122,200,.12);--accent-rgb:74,122,200;--t1:radial-gradient(ellipse at 30% 20%,#0a1a3a,#050a1a,#020408);--t2:radial-gradient(ellipse at 70% 30%,#0a1530,#040810,#020408);--t3:radial-gradient(ellipse at 50% 70%,#0a1228,#04080f,#020306);--t4:radial-gradient(ellipse at 20% 80%,#08102a,#040810,#020305);}
[data-theme="emerald"]{--a1:#4ac87a;--a2:#80f0a0;--a3:#207a3a;--a4:#083a18;--glow:rgba(74,200,122,.5);--glow2:rgba(74,200,122,.12);--accent-rgb:74,200,122;--t1:radial-gradient(ellipse at 30% 20%,#0a2a14,#050f08,#020603);--t2:radial-gradient(ellipse at 70% 30%,#081a10,#030a06,#020403);--t3:radial-gradient(ellipse at 50% 70%,#0a2010,#040c06,#020503);--t4:radial-gradient(ellipse at 20% 80%,#051508,#030a05,#020403);}
[data-theme="obsidian"]{--a1:#a0a0b8;--a2:#d0d0e8;--a3:#505068;--a4:#202030;--glow:rgba(160,160,184,.5);--glow2:rgba(160,160,184,.12);--accent-rgb:160,160,184;--t1:radial-gradient(ellipse at 30% 20%,#18182a,#0a0a18,#050508);--t2:radial-gradient(ellipse at 70% 30%,#141424,#080814,#040408);--t3:radial-gradient(ellipse at 50% 70%,#161622,#090910,#040406);--t4:radial-gradient(ellipse at 20% 80%,#10101e,#08080e,#040406);}

*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html,body{width:100%;height:100%;overflow:hidden;}
body{background:#060404;font-family:'Cormorant Garamond',Georgia,serif;color:#f5efe0;cursor:none;user-select:none;}

/* CURSOR */
#cur,#cur-ring{position:fixed;pointer-events:none;z-index:9999;border-radius:50%;transform:translate(-50%,-50%);}
#cur{width:10px;height:10px;background:var(--a1);mix-blend-mode:difference;transition:width .15s,height .15s;}
#cur-ring{width:32px;height:32px;border:1px solid rgba(var(--accent-rgb),.4);transition:width .22s,height .22s;}
body.hov #cur{width:20px;height:20px;}
body.hov #cur-ring{width:52px;height:52px;border-color:var(--glow);}

/* CANVASES */
#bgc,#blmc,#coinc{position:fixed;inset:0;pointer-events:none;}
#bgc{z-index:0;}
#blmc{z-index:1;mix-blend-mode:screen;opacity:.5;}
#coinc{z-index:350;}
body::after{content:'';position:fixed;inset:0;z-index:2;pointer-events:none;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.04'/%3E%3C/svg%3E");opacity:.32;animation:gs .5s steps(1) infinite;}
@keyframes gs{0%{transform:translate(0,0)}25%{transform:translate(-2%,-1%)}50%{transform:translate(1%,2%)}75%{transform:translate(-1%,1%)}100%{transform:translate(2%,-2%)}}

/* INTRO */
#intro{position:fixed;inset:0;z-index:500;display:flex;flex-direction:column;align-items:center;justify-content:center;background:radial-gradient(ellipse at 50% 40%,#110b04,#060404 70%);transition:opacity 1.4s,visibility 1.4s;}
#intro.gone{opacity:0;visibility:hidden;}
.ilv{width:1px;height:88px;background:linear-gradient(180deg,transparent,var(--a1),transparent);margin-bottom:34px;animation:lg 1.6s ease forwards;transform-origin:top;}
@keyframes lg{from{transform:scaleY(0)}to{transform:scaleY(1)}}
.iwm{font-family:'Cinzel',serif;font-size:clamp(50px,9vw,108px);font-weight:900;letter-spacing:22px;color:var(--a1);text-shadow:0 0 80px var(--glow),0 0 160px var(--glow2);opacity:0;animation:fu 1s .7s ease forwards;}
.iest{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:15px;letter-spacing:9px;color:rgba(var(--accent-rgb),.5);margin-top:10px;opacity:0;animation:fu 1s 1s ease forwards;}
.ihr{width:200px;height:1px;background:linear-gradient(90deg,transparent,var(--a1),transparent);margin:34px 0 0;opacity:0;animation:fu 1s 1.2s ease forwards;}
.ienter{margin-top:50px;font-family:'Cinzel',serif;font-size:10px;letter-spacing:7px;color:rgba(var(--accent-rgb),.5);border:1px solid rgba(var(--accent-rgb),.3);padding:14px 42px;background:transparent;cursor:none;transition:all .4s;opacity:0;animation:fu 1s 1.5s ease forwards;}
.ienter:hover{background:rgba(var(--accent-rgb),.07);color:var(--a1);border-color:var(--a1);box-shadow:0 0 40px rgba(var(--accent-rgb),.1),inset 0 0 30px rgba(var(--accent-rgb),.04);}
@keyframes fu{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}

/* SHELL */
#shell{position:fixed;inset:0;z-index:3;display:flex;flex-direction:column;opacity:0;transition:opacity 1.2s ease;}
#shell.on{opacity:1;}

/* HEADER */
#hdr{display:flex;align-items:center;justify-content:space-between;padding:0 42px;height:66px;flex-shrink:0;background:rgba(4,2,2,.8);backdrop-filter:blur(26px) saturate(1.3);border-bottom:1px solid rgba(var(--accent-rgb),.14);box-shadow:0 8px 40px rgba(0,0,0,.5);position:relative;z-index:10;}
.wm{font-family:'Cinzel',serif;font-size:19px;font-weight:900;letter-spacing:12px;color:var(--a1);text-shadow:0 0 28px rgba(var(--accent-rgb),.38);}
.nav{display:flex;}
.ntab{font-family:'Cinzel',serif;font-size:8px;letter-spacing:4px;color:rgba(var(--accent-rgb),.33);padding:7px 16px;border:none;background:none;cursor:none;transition:color .3s;position:relative;}
.ntab::after{content:'';position:absolute;bottom:0;left:50%;right:50%;height:1px;background:var(--a1);transition:left .3s,right .3s;}
.ntab:hover,.ntab.active{color:var(--a1);}
.ntab:hover::after,.ntab.active::after{left:8%;right:8%;}
.hr{display:flex;align-items:center;gap:14px;}
.chips{display:flex;}
.chip{width:22px;height:22px;border-radius:50%;border:2px solid rgba(255,255,255,.16);margin-left:-6px;box-shadow:0 2px 6px rgba(0,0,0,.6);}
.chip:first-child{margin-left:0;}
.cr{background:radial-gradient(circle at 35% 35%,#e05a4a,#a02020);}
.cb2{background:radial-gradient(circle at 35% 35%,#4a9ad4,#1a5a9a);}
.cg{background:radial-gradient(circle at 35% 35%,#4abf6a,#1a7a3a);}
.ca{background:radial-gradient(circle at 35% 35%,var(--a2),var(--a3));}
.bal{font-family:'Bebas Neue',sans-serif;font-size:25px;letter-spacing:2px;color:var(--a2);text-shadow:0 0 18px rgba(var(--accent-rgb),.28);transition:all .5s;}
.bal.fw{animation:bfw .8s ease;}
.bal.fl{animation:bfl .8s ease;}
@keyframes bfw{0%,100%{color:var(--a2)}40%{color:#80ff80;text-shadow:0 0 28px #0f0;}}
@keyframes bfl{0%,100%{color:var(--a2)}40%{color:#ff8080;text-shadow:0 0 28px #f00;}}
.tdots{display:flex;gap:5px;align-items:center;}
.td{width:13px;height:13px;border-radius:50%;cursor:none;border:2px solid transparent;transition:all .22s;flex-shrink:0;}
.td:hover,.td.on{border-color:white;transform:scale(1.35);}
.tg{background:linear-gradient(135deg,#c8a45a,#7a5e20);}
.tc{background:linear-gradient(135deg,#c84a4a,#7a2020);}
.ts{background:linear-gradient(135deg,#4a7ac8,#203a7a);}
.te{background:linear-gradient(135deg,#4ac87a,#207a3a);}
.to{background:linear-gradient(135deg,#a0a0b8,#505068);}

/* LOBBY */
#lobby{flex:1;overflow:hidden;display:grid;grid-template-columns:repeat(4,1fr);}
.gtile{position:relative;overflow:hidden;cursor:none;border-right:1px solid rgba(var(--accent-rgb),.07);transition:all .6s cubic-bezier(.23,1,.32,1);}
.gtile:last-child{border-right:none;}
.tbg{position:absolute;inset:0;transition:transform .8s cubic-bezier(.23,1,.32,1),filter .6s;will-change:transform;}
.t-slots .tbg{background:var(--t1);}
.t-bj .tbg{background:var(--t2);}
.t-pk .tbg{background:var(--t3);}
.t-rl .tbg{background:var(--t4);}
.gtile:hover .tbg{transform:scale(1.07);filter:brightness(1.35);}
.gtile::after{content:'';position:absolute;inset:0;opacity:0;box-shadow:inset 0 0 60px rgba(var(--accent-rgb),.1);transition:opacity .5s;pointer-events:none;z-index:3;}
.gtile:hover::after{opacity:1;}
.tscan{position:absolute;inset:0;pointer-events:none;background:repeating-linear-gradient(0deg,transparent,transparent 3px,rgba(0,0,0,.03) 3px,rgba(0,0,0,.03) 4px);}
.tvig{position:absolute;inset:0;background:linear-gradient(180deg,rgba(0,0,0,.12),rgba(0,0,0,.04) 40%,rgba(0,0,0,.88) 100%);}
.tglow{position:absolute;top:50%;left:50%;transform:translate(-50%,-65%);width:170px;height:170px;border-radius:50%;opacity:0;transition:opacity .6s,transform .6s;pointer-events:none;}
.t-slots .tglow{background:radial-gradient(circle,rgba(150,80,255,.28),transparent 70%);}
.t-bj .tglow{background:radial-gradient(circle,rgba(80,200,80,.22),transparent 70%);}
.t-pk .tglow{background:radial-gradient(circle,rgba(var(--accent-rgb),.26),transparent 70%);}
.t-rl .tglow{background:radial-gradient(circle,rgba(200,60,60,.26),transparent 70%);}
.gtile:hover .tglow{opacity:1;transform:translate(-50%,-65%) scale(1.6);}
.tico{position:absolute;top:50%;left:50%;transform:translate(-50%,-66%);font-size:74px;filter:drop-shadow(0 10px 38px rgba(0,0,0,.9));transition:transform .6s cubic-bezier(.23,1,.32,1);z-index:2;}
.gtile:hover .tico{transform:translate(-50%,-72%) scale(1.18);}
.tjp{position:absolute;top:14px;right:14px;z-index:4;font-family:'Bebas Neue',sans-serif;font-size:12px;letter-spacing:2px;color:var(--a2);background:rgba(0,0,0,.72);border:1px solid rgba(var(--accent-rgb),.28);padding:3px 9px;backdrop-filter:blur(8px);}
.tnpcs{position:absolute;bottom:0;left:0;right:0;height:42%;pointer-events:none;z-index:3;overflow:hidden;}
.npc{position:absolute;bottom:0;background:rgba(0,0,0,.65);filter:blur(2px);border-radius:50% 50% 0 0/30% 30% 0 0;animation:npcW linear infinite;opacity:.35;}
@keyframes npcW{from{transform:translateX(-60px)}to{transform:translateX(calc(100vw + 80px))}}
.tinfo{position:absolute;bottom:0;left:0;right:0;padding:26px 24px;z-index:4;transform:translateY(16px);transition:transform .5s cubic-bezier(.23,1,.32,1);}
.gtile:hover .tinfo{transform:translateY(0);}
.tname{font-family:'Cinzel',serif;font-size:22px;font-weight:900;letter-spacing:4px;color:var(--a1);text-shadow:0 2px 18px rgba(0,0,0,.8);line-height:1;}
.ttag{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:13px;color:rgba(245,239,224,.52);letter-spacing:2px;margin-top:5px;opacity:0;transition:opacity .4s .1s;}
.gtile:hover .ttag{opacity:1;}
.tcta{display:inline-block;margin-top:13px;font-family:'Cinzel',serif;font-size:9px;letter-spacing:6px;color:#060404;background:var(--a1);padding:9px 20px;border:none;cursor:none;transform:translateY(8px);opacity:0;transition:transform .4s .05s,opacity .4s .05s,background .25s;position:relative;overflow:hidden;}
.tcta::before{content:'';position:absolute;inset:0;background:linear-gradient(90deg,transparent,rgba(255,255,255,.2),transparent);transform:translateX(-100%);transition:transform .5s;}
.gtile:hover .tcta{transform:translateY(0);opacity:1;}
.tcta:hover{background:var(--a2);}
.tcta:hover::before{transform:translateX(100%);}

/* SECTIONS */
.sec{display:none;flex:1;padding:38px;overflow-y:auto;flex-direction:column;}
.sec.on{display:flex;}
.sec-title{font-family:'Cinzel',serif;font-size:13px;letter-spacing:7px;color:var(--a1);margin-bottom:6px;}
.sec-sub{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:14px;color:rgba(var(--accent-rgb),.4);margin-bottom:24px;}

/* STATS */
.sgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:28px;}
.scard{padding:18px;background:rgba(0,0,0,.4);border:1px solid rgba(var(--accent-rgb),.1);text-align:center;}
.sval{font-family:'Bebas Neue',sans-serif;font-size:30px;letter-spacing:2px;color:var(--a2);}
.slbl{font-family:'Cinzel',serif;font-size:8px;letter-spacing:3px;color:rgba(var(--accent-rgb),.4);margin-top:4px;}
.hlbl2{font-family:'Cinzel',serif;font-size:10px;letter-spacing:4px;color:var(--a3);margin-bottom:12px;}
.hrow{display:flex;justify-content:space-between;padding:8px 14px;background:rgba(0,0,0,.3);border:1px solid rgba(var(--accent-rgb),.07);font-family:'Bebas Neue',sans-serif;letter-spacing:1px;font-size:12px;margin-bottom:4px;}

/* ACHIEVEMENTS */
.apanel{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;}
.acard{padding:14px 15px;background:rgba(0,0,0,.4);border:1px solid rgba(var(--accent-rgb),.08);display:flex;gap:12px;align-items:flex-start;transition:all .3s;}
.acard.ul{border-color:rgba(var(--accent-rgb),.38);background:rgba(var(--accent-rgb),.06);}
.acard.lk{filter:grayscale(1);opacity:.3;}
.aico{font-size:26px;flex-shrink:0;}
.aname{font-family:'Cinzel',serif;font-size:10px;letter-spacing:2px;color:var(--a1);}
.adesc{font-size:11px;color:rgba(245,239,224,.42);margin-top:3px;line-height:1.4;}

/* LEADERBOARD */
.lbrow{display:flex;align-items:center;gap:14px;padding:11px 15px;border-bottom:1px solid rgba(var(--accent-rgb),.07);transition:background .25s;}
.lbrow:hover{background:rgba(var(--accent-rgb),.04);}
.lbrank{font-family:'Bebas Neue',sans-serif;font-size:18px;color:var(--a3);width:26px;text-align:center;}
.lbrank.top{color:var(--a2);text-shadow:0 0 10px rgba(var(--accent-rgb),.4);}
.lbname{font-family:'Cinzel',serif;font-size:11px;letter-spacing:2px;flex:1;}
.lbscore{font-family:'Bebas Neue',sans-serif;font-size:17px;color:var(--a1);letter-spacing:1px;}
.lbyou{background:rgba(var(--accent-rgb),.05)!important;border-left:2px solid var(--a1);}

/* TOAST */
#toast{position:fixed;bottom:44px;left:50%;transform:translateX(-50%) translateY(60px);z-index:400;pointer-events:none;opacity:0;transition:all .5s cubic-bezier(.34,1.56,.64,1);}
#toast.show{opacity:1;transform:translateX(-50%) translateY(0);}
.ti{font-family:'Cinzel',serif;font-size:13px;letter-spacing:3px;padding:14px 34px;border-left:3px solid;backdrop-filter:blur(22px);white-space:nowrap;}
.ti.win{background:rgba(5,28,10,.95);border-color:#4f4;color:#80ff80;box-shadow:0 20px 60px rgba(0,200,80,.18);}
.ti.lose{background:rgba(28,5,5,.95);border-color:#f44;color:#ff8080;box-shadow:0 20px 60px rgba(200,0,0,.18);}
.ti.push{background:rgba(26,20,5,.95);border-color:var(--a1);color:var(--a2);box-shadow:0 20px 50px rgba(var(--accent-rgb),.12);}
.ti.ach{background:rgba(8,5,28,.95);border-color:#80f;color:#c080ff;box-shadow:0 20px 50px rgba(128,0,255,.18);}

/* MODAL */
#mov{position:fixed;inset:0;z-index:100;display:none;align-items:center;justify-content:center;transition:background .4s,backdrop-filter .4s;}
#mov.open{display:flex;background:rgba(0,0,0,.88);backdrop-filter:blur(14px) saturate(.4);}
#mod{position:relative;width:min(780px,96vw);max-height:92vh;background:linear-gradient(155deg,#100c07,#080504);border:1px solid rgba(var(--accent-rgb),.2);box-shadow:0 0 0 1px rgba(var(--accent-rgb),.04),0 60px 120px rgba(0,0,0,.95),inset 0 1px 0 rgba(var(--accent-rgb),.09);display:flex;flex-direction:column;overflow:hidden;animation:mi .5s cubic-bezier(.34,1.56,.64,1);}
@keyframes mi{from{transform:scale(.88) translateY(-28px);opacity:0}to{transform:scale(1);opacity:1}}
#mod::before,#mod::after{content:'';position:absolute;width:42px;height:42px;border-color:rgba(var(--accent-rgb),.32);border-style:solid;pointer-events:none;z-index:2;}
#mod::before{top:9px;left:9px;border-width:1px 0 0 1px;}
#mod::after{bottom:9px;right:9px;border-width:0 1px 1px 0;}
.mhdr{display:flex;align-items:center;justify-content:space-between;padding:19px 28px;border-bottom:1px solid rgba(var(--accent-rgb),.11);flex-shrink:0;}
.mtitle{font-family:'Cinzel',serif;font-size:15px;font-weight:900;letter-spacing:7px;color:var(--a1);}
.mcls{width:34px;height:34px;background:rgba(var(--accent-rgb),.05);border:1px solid rgba(var(--accent-rgb),.18);color:rgba(var(--accent-rgb),.48);font-size:12px;cursor:none;display:flex;align-items:center;justify-content:center;transition:all .22s;}
.mcls:hover{background:rgba(var(--accent-rgb),.1);color:var(--a1);}
.mbody{padding:24px 28px;overflow-y:auto;flex:1;}
.mbody::-webkit-scrollbar{width:2px;}
.mbody::-webkit-scrollbar-thumb{background:var(--a3);}

/* BET BAR */
.bbar{display:flex;align-items:center;gap:7px;padding:11px 14px;background:rgba(0,0,0,.45);border:1px solid rgba(var(--accent-rgb),.1);margin-bottom:18px;flex-wrap:wrap;}
.bbarlbl{font-family:'Cinzel',serif;font-size:7px;letter-spacing:5px;color:var(--a3);margin-right:2px;}
.bc{font-family:'Bebas Neue',sans-serif;font-size:12px;letter-spacing:2px;padding:5px 11px;border:1px solid rgba(var(--accent-rgb),.18);background:rgba(var(--accent-rgb),.04);color:rgba(var(--accent-rgb),.52);cursor:none;transition:all .2s;}
.bc:hover,.bc.on{background:var(--a1);color:#060404;border-color:var(--a1);}
.bc.on{box-shadow:0 0 14px rgba(var(--accent-rgb),.35);}
.bcur{font-family:'Bebas Neue',sans-serif;font-size:18px;letter-spacing:2px;color:var(--a2);margin-left:auto;}

/* BUTTONS */
.arow{display:flex;gap:9px;margin-top:16px;flex-wrap:wrap;}
.bgold{flex:1;min-width:90px;font-family:'Cinzel',serif;font-size:9px;letter-spacing:4px;padding:12px 16px;background:linear-gradient(135deg,var(--a1) 0%,var(--a3) 50%,var(--a1) 100%);background-size:200% 100%;border:none;color:#060404;cursor:none;transition:background-position .4s,transform .2s,box-shadow .3s;box-shadow:0 4px 18px rgba(var(--accent-rgb),.22);position:relative;overflow:hidden;}
.bgold::after{content:'';position:absolute;inset:0;background:linear-gradient(90deg,transparent,rgba(255,255,255,.14),transparent);transform:translateX(-100%);transition:transform .4s;}
.bgold:hover{background-position:100% 0;box-shadow:0 8px 28px rgba(var(--accent-rgb),.42);transform:translateY(-2px);}
.bgold:hover::after{transform:translateX(100%);}
.bgold:active{transform:translateY(1px);}
.bgold:disabled{opacity:.3;transform:none;cursor:not-allowed;}
.bgh{flex:1;min-width:75px;font-family:'Cinzel',serif;font-size:9px;letter-spacing:4px;padding:12px 16px;background:transparent;border:1px solid rgba(245,239,224,.13);color:rgba(245,239,224,.52);cursor:none;transition:all .22s;}
.bgh:hover{border-color:rgba(245,239,224,.35);color:#f5efe0;background:rgba(255,255,255,.04);}
.bgh:disabled{opacity:.3;}

/* CARDS */
.csc{perspective:700px;display:inline-block;}
.c3{width:60px;height:88px;position:relative;transform-style:preserve-3d;animation:cf .45s cubic-bezier(.23,1,.32,1) forwards;}
.c3:hover{transform:translateY(-7px) rotateY(8deg)!important;transition:transform .25s;}
@keyframes cf{from{transform:rotateY(90deg) scale(.84)}to{transform:rotateY(0) scale(1)}}
.cf2,.cbk{position:absolute;inset:0;backface-visibility:hidden;border-radius:7px;display:flex;flex-direction:column;align-items:center;justify-content:center;box-shadow:2px 6px 20px rgba(0,0,0,.7),inset 0 1px 0 rgba(255,255,255,.28);}
.cf2{background:linear-gradient(155deg,#fefcf5,#f5f0e0);}
.cf2.r{color:#c0392b;}
.cf2.b2{color:#1a1a2a;}
.cbk{background:linear-gradient(135deg,#1a3060,#0f1f40);transform:rotateY(180deg);background-image:repeating-linear-gradient(45deg,rgba(200,164,90,.07) 0px,rgba(200,164,90,.07) 1px,transparent 1px,transparent 8px);}
.crk{font-size:21px;line-height:1;font-family:'Cormorant Garamond',serif;font-weight:700;}
.cst{font-size:15px;margin-top:2px;}
.hwrap{display:flex;gap:7px;flex-wrap:wrap;min-height:96px;}

/* FELT */
.felt{background:radial-gradient(ellipse at 50% 0%,rgba(30,100,60,.32) 0%,transparent 70%),#0b2318;border:1px solid rgba(255,255,255,.05);border-radius:4px;padding:20px;position:relative;overflow:hidden;}
.felt::before{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,transparent,transparent 44px,rgba(255,255,255,.007) 44px,rgba(255,255,255,.007) 45px);}
.felt2{background:radial-gradient(ellipse at 50% 100%,rgba(60,40,0,.18) 0%,transparent 70%),#071a10;border:1px solid rgba(255,255,255,.04);border-radius:4px;padding:20px;}
.hlbl{font-family:'Cinzel',serif;font-size:8px;letter-spacing:5px;color:rgba(var(--accent-rgb),.36);margin-bottom:8px;display:flex;align-items:center;gap:9px;}
.hval{font-family:'Bebas Neue',sans-serif;font-size:14px;color:var(--a2);background:rgba(0,0,0,.4);padding:2px 7px;}
.hd{width:100%;height:1px;background:linear-gradient(90deg,transparent,rgba(255,255,255,.05),transparent);margin:13px 0;}
.hs{margin-bottom:15px;}

/* SLOTS */
.scab{background:linear-gradient(160deg,#130810,#0a0408);border:1px solid rgba(var(--accent-rgb),.18);border-radius:8px;padding:22px;text-align:center;position:relative;overflow:hidden;}
.scab::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,transparent,var(--a1),#e8420a,var(--a1),transparent);animation:cg2 3s ease-in-out infinite alternate;}
@keyframes cg2{from{opacity:.55}to{opacity:1}}
.rwrap{display:flex;justify-content:center;gap:5px;margin:16px 0;background:rgba(0,0,0,.55);border:1px solid rgba(var(--accent-rgb),.14);padding:9px;border-radius:4px;}
.reel{width:82px;height:98px;background:#060208;border:1px solid rgba(var(--accent-rgb),.22);border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:46px;position:relative;overflow:hidden;box-shadow:inset 0 10px 22px rgba(0,0,0,.6),inset 0 -10px 22px rgba(0,0,0,.6);transition:border-color .3s,box-shadow .3s;}
.reel::before,.reel::after{content:'';position:absolute;left:0;right:0;height:28px;z-index:2;pointer-events:none;}
.reel::before{top:0;background:linear-gradient(180deg,#060208,transparent);}
.reel::after{bottom:0;background:linear-gradient(0deg,#060208,transparent);}
.rsym{display:block;line-height:1;}
.reel.sp .rsym{animation:rs .07s linear infinite;}
@keyframes rs{0%{transform:translateY(-11px);filter:blur(4px)}100%{transform:translateY(11px);filter:blur(4px)}}
.reel.wl{border-color:var(--a2);animation:rw .5s ease infinite alternate;}
@keyframes rw{from{box-shadow:0 0 0 2px var(--a1),inset 0 0 18px rgba(var(--accent-rgb),.18)}to{box-shadow:0 0 0 3px var(--a2),inset 0 0 36px rgba(var(--accent-rgb),.38)}}
.ptbl{display:grid;grid-template-columns:repeat(4,1fr);gap:4px;margin-top:13px;}
.prow{font-family:'Bebas Neue',sans-serif;font-size:10px;letter-spacing:1px;color:rgba(var(--accent-rgb),.38);padding:4px 5px;background:rgba(0,0,0,.3);border:1px solid rgba(var(--accent-rgb),.06);text-align:center;}
.prow span{color:var(--a2);}
.jpot{font-family:'Bebas Neue',sans-serif;font-size:26px;letter-spacing:4px;color:var(--a2);text-shadow:0 0 18px rgba(var(--accent-rgb),.45);text-align:center;}
.jlbl{font-family:'Cinzel',serif;font-size:7px;letter-spacing:5px;color:rgba(var(--accent-rgb),.38);text-align:center;margin-bottom:4px;}

/* screen shake */
@keyframes shk{0%,100%{transform:translate(0,0)}10%{transform:translate(-5px,3px)}20%{transform:translate(4px,-4px)}30%{transform:translate(-4px,4px)}40%{transform:translate(5px,-3px)}50%{transform:translate(-4px,4px)}60%{transform:translate(4px,-4px)}70%{transform:translate(-5px,3px)}80%{transform:translate(4px,-4px)}90%{transform:translate(-3px,4px)}}
.shk{animation:shk .48s ease;}

/* ROULETTE */
.rlayout{display:grid;grid-template-columns:220px 1fr;gap:20px;align-items:start;}
.rww{display:flex;flex-direction:column;align-items:center;gap:9px;}
#rlc{width:210px;height:210px;border-radius:50%;box-shadow:0 0 0 4px var(--a3),0 0 0 7px rgba(0,0,0,.6),0 0 0 8px rgba(var(--accent-rgb),.13),0 22px 56px rgba(0,0,0,.9);display:block;}
.rnd{font-family:'Bebas Neue',sans-serif;font-size:54px;letter-spacing:2px;line-height:1;min-height:58px;text-align:center;}
.rnd.r{color:#e74c3c;text-shadow:0 0 18px rgba(231,76,60,.55);}
.rnd.b2{color:#f5efe0;}
.rnd.g{color:#2ecc71;text-shadow:0 0 18px rgba(46,204,113,.55);}
.rbrd{display:flex;flex-direction:column;gap:6px;}
.rbrow{display:flex;gap:6px;}
.rbtn{flex:1;padding:9px 6px;font-family:'Cinzel',serif;font-size:8px;letter-spacing:2px;background:rgba(0,0,0,.4);border:1px solid rgba(255,255,255,.09);color:rgba(245,239,224,.43);cursor:none;transition:all .22s;}
.rbtn:hover{border-color:rgba(var(--accent-rgb),.38);color:#f5efe0;}
.rbtn.sr{background:rgba(192,57,43,.22);border-color:#c0392b;color:#e74c3c;}
.rbtn.sb{background:rgba(38,38,38,.65);border-color:rgba(255,255,255,.38);color:#f5efe0;}
.rbtn.sa{background:rgba(var(--accent-rgb),.13);border-color:var(--a1);color:var(--a2);}

/* TEXAS HOLD'EM */
.th-table{background:radial-gradient(ellipse at 50% 30%,rgba(20,80,40,.4),transparent 65%),#071a10;border:1px solid rgba(255,255,255,.05);border-radius:12px;padding:22px;position:relative;overflow:hidden;}
.th-table::before{content:'';position:absolute;inset:0;border-radius:12px;background:repeating-linear-gradient(90deg,transparent,transparent 60px,rgba(255,255,255,.006) 60px,rgba(255,255,255,.006) 61px);}
.th-section-lbl{font-family:'Cinzel',serif;font-size:8px;letter-spacing:5px;color:rgba(var(--accent-rgb),.35);margin-bottom:9px;text-align:center;}
.th-community{display:flex;gap:8px;justify-content:center;min-height:100px;align-items:center;padding:12px;background:rgba(0,0,0,.3);border-radius:6px;border:1px solid rgba(255,255,255,.04);flex-wrap:wrap;}
.th-hole{display:flex;gap:8px;justify-content:center;min-height:100px;align-items:center;flex-wrap:wrap;}
.th-divider{width:100%;height:1px;background:linear-gradient(90deg,transparent,rgba(255,255,255,.06),transparent);margin:14px 0;}
.th-pot{font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:3px;color:var(--a2);text-align:center;text-shadow:0 0 14px rgba(var(--accent-rgb),.35);}
.th-pot-lbl{font-family:'Cinzel',serif;font-size:7px;letter-spacing:5px;color:rgba(var(--accent-rgb),.35);text-align:center;margin-bottom:3px;}
.th-result{font-family:'Cinzel',serif;font-size:13px;letter-spacing:3px;color:var(--a1);text-align:center;padding:10px;background:rgba(var(--accent-rgb),.07);border:1px solid rgba(var(--accent-rgb),.18);margin-top:12px;min-height:42px;display:flex;align-items:center;justify-content:center;}
.th-result.pa{animation:pu .6s cubic-bezier(.34,1.56,.64,1);}
.th-street{font-family:'Bebas Neue',sans-serif;font-size:11px;letter-spacing:4px;color:rgba(var(--accent-rgb),.45);text-align:center;margin-bottom:8px;}
.th-vs{display:grid;grid-template-columns:1fr auto 1fr;gap:10px;align-items:center;margin-top:10px;}
.th-player-info{text-align:center;}
.th-player-name{font-family:'Cinzel',serif;font-size:9px;letter-spacing:3px;color:rgba(var(--accent-rgb),.5);margin-bottom:6px;}
.th-vs-badge{font-family:'Bebas Neue',sans-serif;font-size:18px;color:rgba(var(--accent-rgb),.3);}
@keyframes pu{from{transform:scale(.8);opacity:0}to{transform:scale(1);opacity:1}}

@media(max-width:680px){
  #lobby{grid-template-columns:repeat(2,1fr);}
  .rlayout{grid-template-columns:1fr;}
  .sgrid{grid-template-columns:repeat(2,1fr);}
  .apanel{grid-template-columns:1fr;}
}
</style>
</head>
<body>
<div id="cur"></div>
<div id="cur-ring"></div>
<canvas id="bgc"></canvas>
<canvas id="blmc"></canvas>
<canvas id="coinc"></canvas>
<div id="toast"><div class="ti" id="ti"></div></div>

<!-- INTRO -->
<div id="intro">
  <div class="ilv"></div>
  <div class="iwm">ROYAL ACE</div>
  <div class="iest">Games &nbsp;·&nbsp; Est. MMXXV</div>
  <div class="ihr"></div>
  <button class="ienter" onclick="enterCasino()">ENTER THE FLOOR</button>
</div>

<!-- SHELL -->
<div id="shell">
  <header id="hdr">
    <div class="wm">ROYAL ACE GAMES</div>
    <nav class="nav">
      <button class="ntab active" onclick="showSec('lobby',this)">THE FLOOR</button>
      <button class="ntab" onclick="showSec('stats',this)">STATISTICS</button>
      <button class="ntab" onclick="showSec('achievements',this)">ACHIEVEMENTS</button>
      <button class="ntab" onclick="showSec('leaderboard',this)">LEADERBOARD</button>
    </nav>
    <div class="hr">
      <div class="tdots">
        <div class="td tg on" onclick="setTheme('gold',this)"></div>
        <div class="td tc" onclick="setTheme('crimson',this)"></div>
        <div class="td ts" onclick="setTheme('sapphire',this)"></div>
        <div class="td te" onclick="setTheme('emerald',this)"></div>
        <div class="td to" onclick="setTheme('obsidian',this)"></div>
      </div>
      <div class="chips">
        <div class="chip ca"></div><div class="chip cr"></div>
        <div class="chip cb2"></div><div class="chip cg"></div>
      </div>
      <div class="bal" id="bal">$5,000</div>
    </div>
  </header>

  <!-- LOBBY -->
  <div id="lobby">
    <div class="gtile t-slots" onclick="openGame('slots')">
      <div class="tbg"></div><div class="tscan"></div><div class="tglow"></div><div class="tvig"></div>
      <div class="tjp">JACKPOT <span id="jpc">$24,800</span></div>
      <div class="tico">🎰</div>
      <div class="tnpcs" id="nl0"></div>
      <div class="tinfo"><div class="tname">SLOTS</div><div class="ttag">Fortune favors the bold</div><button class="tcta">PLAY NOW</button></div>
    </div>
    <div class="gtile t-bj" onclick="openGame('blackjack')">
      <div class="tbg"></div><div class="tscan"></div><div class="tglow"></div><div class="tvig"></div>
      <div class="tico">🃏</div>
      <div class="tnpcs" id="nl1"></div>
      <div class="tinfo"><div class="tname">BLACKJACK</div><div class="ttag">Beat the dealer to 21</div><button class="tcta">PLAY NOW</button></div>
    </div>
    <div class="gtile t-pk" onclick="openGame('poker')">
      <div class="tbg"></div><div class="tscan"></div><div class="tglow"></div><div class="tvig"></div>
      <div class="tico">♠️</div>
      <div class="tnpcs" id="nl2"></div>
      <div class="tinfo"><div class="tname">TEXAS HOLD'EM</div><div class="ttag">2 cards · 5 community · Best hand wins</div><button class="tcta">PLAY NOW</button></div>
    </div>
    <div class="gtile t-rl" onclick="openGame('roulette')">
      <div class="tbg"></div><div class="tscan"></div><div class="tglow"></div><div class="tvig"></div>
      <div class="tico">🎡</div>
      <div class="tnpcs" id="nl3"></div>
      <div class="tinfo"><div class="tname">ROULETTE</div><div class="ttag">European single zero</div><button class="tcta">PLAY NOW</button></div>
    </div>
  </div>

  <!-- STATS -->
  <div id="sec-stats" class="sec">
    <div class="sec-title">YOUR STATISTICS</div>
    <div class="sec-sub" id="ss-sub">Loading…</div>
    <div class="sgrid" id="sgrid"></div>
    <div class="hlbl2">SESSION HISTORY</div>
    <div id="hist"></div>
  </div>

  <!-- ACHIEVEMENTS -->
  <div id="sec-achievements" class="sec">
    <div class="sec-title">ACHIEVEMENTS</div>
    <div class="sec-sub" id="asp"></div>
    <div class="apanel" id="ap"></div>
  </div>

  <!-- LEADERBOARD -->
  <div id="sec-leaderboard" class="sec">
    <div class="sec-title">GLOBAL LEADERBOARD</div>
    <div class="sec-sub">Live rankings · Updated in real time</div>
    <div id="lbl"></div>
  </div>
</div>

<!-- MODAL -->
<div id="mov">
  <div id="mod">
    <div class="mhdr">
      <div class="mtitle" id="mtitle"></div>
      <button class="mcls" onclick="closeGame()">✕</button>
    </div>
    <div class="mbody" id="mbody"></div>
  </div>
</div>

<script>
/* ── CURSOR ── */
const cur=document.getElementById('cur'),ring=document.getElementById('cur-ring');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;cur.style.left=mx+'px';cur.style.top=my+'px';});
document.addEventListener('mouseover',e=>{document.body.classList.toggle('hov',!!e.target.closest('button,.gtile,.td,.bc,.rbtn'));});
(function cl(){rx+=(mx-rx)*.11;ry+=(my-ry)*.11;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(cl);})();

/* ── PARALLAX ── */
document.addEventListener('mousemove',e=>{
  const px=(e.clientX/innerWidth-.5)*16,py=(e.clientY/innerHeight-.5)*16;
  document.querySelectorAll('.tbg').forEach(t=>{t.style.transform=`translate(${px*.25}px,${py*.25}px) scale(1.07)`;});
  document.querySelectorAll('.tico').forEach(t=>{t.style.transform=`translate(calc(-50% + ${px*.45}px),calc(-66% + ${py*.45}px))`;});
});

/* ── THEME ── */
function setTheme(n,el){
  document.documentElement.setAttribute('data-theme',n);
  document.querySelectorAll('.td').forEach(d=>d.classList.remove('on'));
  el.classList.add('on');
}

/* ── PARTICLES ── */
const bgc=document.getElementById('bgc'),bgx=bgc.getContext('2d');
const blc=document.getElementById('blmc'),blx=blc.getContext('2d');
function rzC(){bgc.width=blc.width=innerWidth;bgc.height=blc.height=innerHeight;}
rzC();addEventListener('resize',rzC);
class Pt{
  constructor(){this.init(true);}
  init(s=false){this.x=Math.random()*bgc.width;this.y=s?Math.random()*bgc.height:bgc.height+10;this.sz=Math.random()*2+.25;this.vy=Math.random()*.65+.15;this.vx=(Math.random()-.5)*.45;this.life=0;this.ml=Math.random()*220+110;const p=[[200,164,90],[240,208,128],[232,66,10],[255,210,140]];const c=p[Math.floor(Math.random()*p.length)];this.r=c[0];this.g=c[1];this.b=c[2];this.bl=Math.random()>.72;}
  tick(){this.x+=this.vx;this.y-=this.vy;this.life++;if(this.life>this.ml)this.init();}
  draw(ctx,bl){if(this.bl!==bl)return;const a=Math.sin(this.life/this.ml*Math.PI)*(bl?.65:.38);ctx.beginPath();ctx.arc(this.x,this.y,bl?this.sz*2.2:this.sz,0,Math.PI*2);ctx.fillStyle=`rgba(${this.r},${this.g},${this.b},${a})`;ctx.fill();}
}
const pts=Array.from({length:150},()=>new Pt());
(function pl(){
  bgx.clearRect(0,0,bgc.width,bgc.height);blx.clearRect(0,0,blc.width,blc.height);
  const vg=bgx.createRadialGradient(bgc.width/2,bgc.height/2,bgc.width*.12,bgc.width/2,bgc.height/2,bgc.width*.88);
  vg.addColorStop(0,'rgba(0,0,0,0)');vg.addColorStop(1,'rgba(0,0,0,.62)');
  bgx.fillStyle=vg;bgx.fillRect(0,0,bgc.width,bgc.height);
  pts.forEach(p=>{p.tick();p.draw(bgx,false);p.draw(blx,true);});
  requestAnimationFrame(pl);
})();

/* ── COINS ── */
const cc=document.getElementById('coinc'),cx2=cc.getContext('2d');
cc.width=innerWidth;cc.height=innerHeight;
addEventListener('resize',()=>{cc.width=innerWidth;cc.height=innerHeight;});
let coins=[];
class Coin{
  constructor(){this.x=innerWidth/2;this.y=innerHeight/2;this.vx=(Math.random()-.5)*14;this.vy=Math.random()*-16-5;this.r=Math.random()*10+5;this.life=0;this.ml=80+Math.random()*40;this.rot=Math.random()*Math.PI*2;this.rv=(Math.random()-.5)*.28;this.col=`hsl(${42+Math.random()*16},78%,${55+Math.random()*20}%)`;}
  tick(){this.x+=this.vx;this.y+=this.vy;this.vy+=.58;this.rot+=this.rv;this.life++;}
  draw(){const a=1-this.life/this.ml;cx2.save();cx2.translate(this.x,this.y);cx2.rotate(this.rot);cx2.beginPath();cx2.ellipse(0,0,this.r,this.r*Math.abs(Math.cos(this.rot*2)),0,0,Math.PI*2);cx2.fillStyle=this.col;cx2.globalAlpha=a;cx2.fill();cx2.restore();}
}
function explode(n=40){for(let i=0;i<n;i++)setTimeout(()=>coins.push(new Coin()),i*11);}
(function coinL(){cx2.clearRect(0,0,cc.width,cc.height);coins=coins.filter(c=>c.life<c.ml);coins.forEach(c=>{c.tick();c.draw();});requestAnimationFrame(coinL);})();

/* ── NPCS ── */
[0,1,2,3].forEach(i=>{
  const l=document.getElementById('nl'+i);if(!l)return;
  for(let j=0;j<3;j++){
    const n=document.createElement('div');n.className='npc';
    const h=28+Math.random()*48,w=h*.34,dur=16+Math.random()*22,del=-Math.random()*dur;
    n.style.cssText=`width:${w}px;height:${h}px;left:0;animation-duration:${dur}s;animation-delay:${del}s;opacity:${.12+Math.random()*.28}`;
    l.appendChild(n);
  }
});

/* ── JACKPOT ── */
let jpv=24800;
setInterval(()=>{jpv+=Math.floor(Math.random()*18+2);const e=document.getElementById('jpc');if(e)e.textContent='$'+jpv.toLocaleString();const e2=document.getElementById('mjp');if(e2)e2.textContent='$'+jpv.toLocaleString();},400);

/* ── INTRO ── */
function enterCasino(){
  document.getElementById('intro').classList.add('gone');
  setTimeout(()=>{document.getElementById('shell').classList.add('on');document.getElementById('intro').style.display='none';},1400);
}

/* ── SECTION SWITCHER ── */
function showSec(name,tab){
  document.getElementById('lobby').style.display='none';
  document.querySelectorAll('.sec').forEach(s=>s.classList.remove('on'));
  document.querySelectorAll('.ntab').forEach(t=>t.classList.remove('active'));
  tab.classList.add('active');
  if(name==='lobby'){document.getElementById('lobby').style.display='grid';}
  else{const el=document.getElementById('sec-'+name);if(el)el.classList.add('on');
    if(name==='stats')renderStats();
    if(name==='achievements')renderAch();
    if(name==='leaderboard')renderLB();}
}

/* ── STATE ── */
let balance=5000,bet=50;
const BETS=[25,50,100,250,500,1000,2500,5000];
const S={gp:0,wins:0,losses:0,bw:0,tw:0,history:[],ach:{fw:false,bs:false,jp:false,hr:false,bjs:false,cb:false,l7:false,fh:false},bjs:0};

function fm(n){return '$'+n.toLocaleString();}
function setBalance(delta){
  balance+=delta;
  if(delta>0){S.wins++;if(delta>S.bw)S.bw=delta;}
  else if(delta<0)S.losses++;
  const el=document.getElementById('bal');
  el.textContent=fm(balance);el.classList.remove('fw','fl');void el.offsetWidth;
  el.classList.add(delta>0?'fw':'fl');
  checkAch(delta);
}
function rec(game,res,amt){S.gp++;S.tw+=bet;S.history.unshift({game,res,amt,bal:balance,t:new Date().toLocaleTimeString()});if(S.history.length>60)S.history.pop();}

/* ── TOAST ── */
function toast(msg,type){
  const t=document.getElementById('toast'),i=document.getElementById('ti');
  i.textContent=msg;i.className='ti '+type;t.classList.add('show');
  clearTimeout(t._t);t._t=setTimeout(()=>t.classList.remove('show'),3200);
}

/* ── ACHIEVEMENTS ── */
const ACHS=[
  {id:'fw',ico:'🏆',name:'FIRST WIN',desc:'Win your first hand'},
  {id:'bs',ico:'💸',name:'BIG SPENDER',desc:'Wager over $10,000 total'},
  {id:'jp',ico:'💰',name:'JACKPOT HUNTER',desc:'Hit a slots jackpot'},
  {id:'hr',ico:'🎲',name:'HIGH ROLLER',desc:'Place a $500 bet'},
  {id:'bjs',ico:'🃏',name:'BJ STREAK',desc:'Win 3 blackjack hands in a row'},
  {id:'cb',ico:'🔥',name:'COMEBACK KID',desc:'Win after balance below $500'},
  {id:'l7',ico:'7️⃣',name:'LUCKY SEVENS',desc:'Hit triple 7s on slots'},
  {id:'fh',ico:'♠️',name:'FULL HOUSE',desc:'Hit a Full House in poker'},
];
function checkAch(delta){
  if(!S.ach.fw&&delta>0){S.ach.fw=true;toast('🏆 ACHIEVEMENT · FIRST WIN','ach');}
  if(!S.ach.bs&&S.tw>=10000){S.ach.bs=true;toast('💸 ACHIEVEMENT · BIG SPENDER','ach');}
  if(!S.ach.hr&&bet>=500){S.ach.hr=true;toast('🎲 ACHIEVEMENT · HIGH ROLLER','ach');}
  if(!S.ach.cb&&balance<500&&delta>0){S.ach.cb=true;toast('🔥 ACHIEVEMENT · COMEBACK KID','ach');}
}
function renderAch(){
  const ul=Object.values(S.ach).filter(Boolean).length;
  document.getElementById('asp').textContent=`${ul} of ${ACHS.length} unlocked`;
  document.getElementById('ap').innerHTML=ACHS.map(a=>{
    const u=S.ach[a.id];
    return`<div class="acard ${u?'ul':'lk'}"><div class="aico">${a.ico}</div><div><div class="aname">${a.name}</div><div class="adesc">${a.desc}</div></div></div>`;
  }).join('');
}

/* ── STATS ── */
function renderStats(){
  const wr=S.gp>0?Math.round(S.wins/S.gp*100):0;
  document.getElementById('ss-sub').textContent=`${S.gp} games played this session`;
  document.getElementById('sgrid').innerHTML=`
    <div class="scard"><div class="sval">${S.gp}</div><div class="slbl">GAMES PLAYED</div></div>
    <div class="scard"><div class="sval">${wr}%</div><div class="slbl">WIN RATE</div></div>
    <div class="scard"><div class="sval">${fm(S.bw)}</div><div class="slbl">BIGGEST WIN</div></div>
    <div class="scard"><div class="sval">${fm(S.tw)}</div><div class="slbl">TOTAL WAGERED</div></div>
    <div class="scard"><div class="sval">${S.wins}</div><div class="slbl">TOTAL WINS</div></div>
    <div class="scard"><div class="sval">${fm(balance)}</div><div class="slbl">BALANCE</div></div>
  `;
  document.getElementById('hist').innerHTML=S.history.slice(0,20).map(h=>`
    <div class="hrow"><span style="color:rgba(var(--accent-rgb),.45)">${h.t}</span><span>${h.game.toUpperCase()}</span><span style="color:${h.amt>0?'#80ff80':'#ff8080'}">${h.amt>0?'+':''}${fm(h.amt)}</span><span style="color:var(--a2)">${fm(h.bal)}</span></div>
  `).join('')||'<div style="color:rgba(var(--accent-rgb),.28);font-family:Cinzel,serif;font-size:10px;letter-spacing:3px;padding:20px 0;text-align:center">NO HISTORY YET</div>';
}

/* ── LEADERBOARD ── */
const LBN=['Alessandro V.','Chen Wei','Natasha K.','James M.','Yuki T.','Carlos R.','Diana F.','Omar S.','Priya N.','Viktor B.'];
const LBS=[128400,94200,87650,76300,65800,58400,49200,42600,38900,31500];
function renderLB(){
  const all=[...LBS.map((s,i)=>({name:LBN[i],score:s,you:false})),{name:'YOU',score:balance,you:true}];
  all.sort((a,b)=>b.score-a.score);
  document.getElementById('lbl').innerHTML=all.map((e,i)=>`
    <div class="lbrow ${e.you?'lbyou':''}">
      <div class="lbrank ${i<3?'top':''}">${i+1}</div>
      <div class="lbname">${e.name}</div>
      <div class="lbscore">${fm(e.score)}</div>
    </div>
  `).join('');
}

/* ── BET BAR ── */
function betBarHTML(){
  return`<div class="bbar"><span class="bbarlbl">WAGER</span>${BETS.map(v=>`<button class="bc ${bet===v?'on':''}" onclick="setBet(${v},this)">${fm(v)}</button>`).join('')}<span class="bcur" id="bcur">${fm(bet)}</span></div>`;
}
function setBet(v,el){bet=v;document.querySelectorAll('.bc').forEach(b=>b.classList.toggle('on',b.textContent===fm(v)));const d=document.getElementById('bcur');if(d)d.textContent=fm(bet);}

/* ── MODAL ── */
let roulRAF=null;
function openGame(g){
  const ov=document.getElementById('mov');ov.style.display='flex';requestAnimationFrame(()=>ov.classList.add('open'));
  ({slots:loadSlots,blackjack:loadBJ,poker:loadPoker,roulette:loadRoulette})[g]();
}
function closeGame(){const ov=document.getElementById('mov');ov.classList.remove('open');setTimeout(()=>ov.style.display='none',420);if(roulRAF){cancelAnimationFrame(roulRAF);roulRAF=null;}}
function setModal(t,h){document.getElementById('mtitle').textContent=t;document.getElementById('mbody').innerHTML=h;}

/* ── SHAKE ── */
function shake(){const s=document.getElementById('shell');s.classList.remove('shk');void s.offsetWidth;s.classList.add('shk');setTimeout(()=>s.classList.remove('shk'),500);}

/* ══════════════════════════
   SLOTS
══════════════════════════ */
const SYMS=['🍒','💎','7️⃣','⭐','🍀','🔔','🍋'];
const PAYS={'💎':100,'7️⃣':50,'🔔':20,'⭐':15,'🍀':10,'🍒':8,'🍋':5};

function loadSlots(){
  setModal('VEGAS SLOTS',`${betBarHTML()}
    <div class="scab">
      <div class="jlbl">PROGRESSIVE JACKPOT</div>
      <div class="jpot" id="mjp">${fm(jpv)}</div>
      <div class="rwrap">
        <div class="reel" id="r0"><span class="rsym">🍒</span></div>
        <div class="reel" id="r1"><span class="rsym">💎</span></div>
        <div class="reel" id="r2"><span class="rsym">⭐</span></div>
      </div>
      <div class="ptbl">${Object.entries(PAYS).map(([s,m])=>`<div class="prow">${s}×3=<span>${m}×</span></div>`).join('')}</div>
    </div>
    <div class="arow"><button class="bgold" id="spnb" onclick="doSpin()">SPIN THE REELS</button></div>`);
}
function doSpin(){
  if(balance<bet){toast('Insufficient funds','lose');return;}
  const btn=document.getElementById('spnb');btn.disabled=true;
  setBalance(-bet);S.tw+=bet;
  const rs=[0,1,2].map(i=>document.getElementById('r'+i));
  rs.forEach(r=>r.classList.add('sp'));
  const res=[];
  [0,1,2].forEach(i=>{
    setTimeout(()=>{
      const s=SYMS[Math.floor(Math.random()*SYMS.length)];res[i]=s;
      rs[i].querySelector('.rsym').textContent=s;rs[i].classList.remove('sp');
      rs[i].style.transform='scaleY(1.1)';rs[i].style.transition='transform .18s cubic-bezier(.34,1.56,.64,1)';
      setTimeout(()=>{rs[i].style.transform='';},80);
      if(i===2)setTimeout(()=>resolveSlots(res,rs,btn),130);
    },350+i*310);
  });
}
function resolveSlots(res,rs,btn){
  const[a,b,c]=res;
  if(a===b&&b===c){
    const m=PAYS[a]||5,w=bet*m;
    rs.forEach(r=>r.classList.add('wl'));
    setBalance(w);rec('slots','jackpot',w);
    explode(65);shake();
    S.ach.jp=true;if(a==='7️⃣'){S.ach.l7=true;toast('7️⃣ ACHIEVEMENT · LUCKY SEVENS','ach');}
    toast(`✦ JACKPOT! +${fm(w)} · ${m}× ✦`,'win');
    setTimeout(()=>rs.forEach(r=>r.classList.remove('wl')),3000);
  } else if(a===b||b===c||a===c){
    const s=a===b?a:c,m=Math.max(1,Math.floor((PAYS[s]||5)/5)),w=bet*m;
    setBalance(w);rec('slots','partial',w);toast(`Partial match · +${fm(w)}`,'push');
  } else {rec('slots','lose',0);toast('No win this spin','lose');}
  btn.disabled=false;
}

/* ══════════════════════════
   BLACKJACK
══════════════════════════ */
const SS=['♠','♥','♦','♣'],RR=['A','2','3','4','5','6','7','8','9','10','J','Q','K'];
let bjdeck=[],bjp=[],bjd=[];
function mkD(){bjdeck=[];for(let s of SS)for(let r of RR)bjdeck.push({r,s});bjdeck.sort(()=>Math.random()-.5);}
const ir=s=>s==='♥'||s==='♦';
function cv(c){if(c.r==='A')return 11;if(['K','Q','J'].includes(c.r))return 10;return parseInt(c.r);}
function hv(h){let t=h.reduce((s,c)=>s+cv(c),0),a=h.filter(c=>c.r==='A').length;while(t>21&&a>0){t-=10;a--;}return t;}

function cardHTML(c,fd=false,dl=0){
  if(fd)return`<div class="csc"><div class="c3" style="animation-delay:${dl}ms"><div class="cbk"></div></div></div>`;
  return`<div class="csc"><div class="c3" style="animation-delay:${dl}ms"><div class="cf2 ${ir(c.s)?'r':'b2'}"><span class="crk">${c.r}</span><span class="cst">${c.s}</span></div></div></div>`;
}
function renderBJ(hd=true){
  const pv=hv(bjp),dv=hd?'?':hv(bjd);
  document.getElementById('bjpc').innerHTML=bjp.map((c,i)=>cardHTML(c,false,i*65)).join('');
  document.getElementById('bjdc').innerHTML=bjd.map((c,i)=>cardHTML(c,hd&&i>0,i*65)).join('');
  const pEl=document.getElementById('bjpv');if(pEl)pEl.textContent=pv;
  const dEl=document.getElementById('bjdv');if(dEl)dEl.textContent=dv;
}
function loadBJ(){
  setModal('BLACKJACK',`${betBarHTML()}
    <div class="felt">
      <div class="hs"><div class="hlbl">DEALER <span class="hval" id="bjdv">—</span></div><div class="hwrap" id="bjdc"></div></div>
      <div class="hd"></div>
      <div class="hs"><div class="hlbl">YOUR HAND <span class="hval" id="bjpv">—</span></div><div class="hwrap" id="bjpc"></div></div>
    </div>
    <div class="arow">
      <button class="bgold" id="bjdeal" onclick="bjDeal()">DEAL</button>
      <button class="bgh" id="bjhit" onclick="bjHit()" disabled>HIT</button>
      <button class="bgh" id="bjstand" onclick="bjStand()" disabled>STAND</button>
      <button class="bgh" id="bjdbl" onclick="bjDouble()" disabled>DOUBLE</button>
    </div>`);
}
function bjDeal(){
  if(balance<bet){toast('Insufficient funds','lose');return;}
  setBalance(-bet);S.tw+=bet;mkD();
  bjp=[bjdeck.pop(),bjdeck.pop()];bjd=[bjdeck.pop(),bjdeck.pop()];
  renderBJ(true);
  document.getElementById('bjdeal').disabled=true;
  ['bjhit','bjstand','bjdbl'].forEach(id=>document.getElementById(id).disabled=false);
  if(hv(bjp)===21)setTimeout(()=>bjReveal(true),600);
}
function bjHit(){bjp.push(bjdeck.pop());renderBJ(true);if(hv(bjp)>21)bjReveal(false);else if(hv(bjp)===21)bjStand();}
function bjDouble(){
  if(balance<bet){toast('Insufficient funds','lose');return;}
  setBalance(-bet);S.tw+=bet;bjp.push(bjdeck.pop());renderBJ(true);
  ['bjhit','bjstand','bjdbl'].forEach(id=>document.getElementById(id).disabled=true);
  while(hv(bjd)<17)bjd.push(bjdeck.pop());renderBJ(false);setTimeout(()=>bjReveal(false),600);
}
function bjStand(){
  ['bjhit','bjstand','bjdbl'].forEach(id=>document.getElementById(id).disabled=true);
  while(hv(bjd)<17)bjd.push(bjdeck.pop());renderBJ(false);setTimeout(()=>bjReveal(false),600);
}
function bjReveal(nat){
  ['bjhit','bjstand','bjdbl'].forEach(id=>document.getElementById(id).disabled=true);
  document.getElementById('bjdeal').disabled=false;renderBJ(false);
  const p=hv(bjp),d=hv(bjd);
  if(nat&&d!==21){const w=Math.floor(bet*2.5);setBalance(w);S.bjs++;rec('blackjack','bj',w);toast(`✦ BLACKJACK! +${fm(w)} ✦`,'win');explode(25);}
  else if(p>21){S.bjs=0;rec('blackjack','bust',-bet);toast('Bust — dealer wins','lose');}
  else if(d>21||p>d){const w=bet*2;setBalance(w);S.bjs++;rec('blackjack','win',w);toast(`You win · +${fm(w)}`,'win');if(S.bjs>=3&&!S.ach.bjs){S.ach.bjs=true;toast('🃏 ACHIEVEMENT · BJ STREAK','ach');}}
  else if(p<d){S.bjs=0;rec('blackjack','lose',-bet);toast('Dealer wins','lose');}
  else{setBalance(bet);rec('blackjack','push',0);toast('Push — bet returned','push');}
}

/* ══════════════════════════
   TEXAS HOLD'EM
══════════════════════════ */
const TH_SUITS=['♠','♥','♦','♣'],TH_RANKS=['2','3','4','5','6','7','8','9','10','J','Q','K','A'];
// rank index: 2=0 … A=12
let thDeck=[],thHole=[],thDlrHole=[],thCommunity=[],thPot=0,thPhase='idle',thCalled=false;
// phases: idle → preflop → flop → turn → river → showdown

function mkTHDeck(){thDeck=[];for(let s of TH_SUITS)for(let r of TH_RANKS)thDeck.push({r,s});thDeck.sort(()=>Math.random()-.5);}
function thDraw(){return thDeck.pop();}
const thIr=s=>s==='♥'||s==='♦';

function loadPoker(){
  thPhase='idle';thPot=0;thCalled=false;
  setModal("TEXAS HOLD'EM",`${betBarHTML()}
    <div class="th-table">
      <div class="th-section-lbl">COMMUNITY CARDS</div>
      <div class="th-community" id="thcomm"><span style="font-family:Cinzel,serif;font-size:9px;letter-spacing:3px;color:rgba(var(--accent-rgb),.25)">DEAL TO BEGIN</span></div>
      <div class="th-divider"></div>
      <div class="th-vs">
        <div class="th-player-info">
          <div class="th-player-name">DEALER</div>
          <div class="th-hole" id="thdlr" style="min-height:70px"></div>
        </div>
        <div class="th-vs-badge">VS</div>
        <div class="th-player-info">
          <div class="th-player-name">YOUR HAND</div>
          <div class="th-hole" id="thhole" style="min-height:70px"></div>
        </div>
      </div>
      <div class="th-pot-lbl" style="margin-top:14px">POT</div>
      <div class="th-pot" id="thpot">$0</div>
      <div class="th-result" id="thres" style="display:none"></div>
    </div>
    <div class="arow" id="tharow">
      <button class="bgold" id="thbtn1" onclick="thAction('deal')">DEAL HAND</button>
    </div>
    <div style="margin-top:11px;font-size:10px;letter-spacing:1px;line-height:2;color:rgba(var(--accent-rgb),.28)">
      ANTE: your bet · CALL: match dealer · RAISE: double down · FOLD: forfeit ante
    </div>`);
}

function thCardHTML(c,fd=false,dl=0){
  if(fd)return`<div class="csc"><div class="c3" style="animation-delay:${dl}ms"><div class="cbk"></div></div></div>`;
  return`<div class="csc"><div class="c3" style="animation-delay:${dl}ms"><div class="cf2 ${thIr(c.s)?'r':'b2'}"><span class="crk">${c.r}</span><span class="cst">${c.s}</span></div></div></div>`;
}

function thRender(showDlr=false){
  // community
  const comm=document.getElementById('thcomm');
  if(comm){
    if(thCommunity.length===0){
      comm.innerHTML='<span style="font-family:Cinzel,serif;font-size:9px;letter-spacing:3px;color:rgba(var(--accent-rgb),.25)">DEAL TO BEGIN</span>';
    } else {
      // show revealed + placeholder backs for unseen
      let html='';
      const total=5;
      for(let i=0;i<total;i++){
        if(i<thCommunity.length) html+=thCardHTML(thCommunity[i],false,i*60);
        else html+=thCardHTML(null,true,i*60);
      }
      comm.innerHTML=html;
    }
  }
  // hole cards
  const hole=document.getElementById('thhole');
  if(hole) hole.innerHTML=thHole.map((c,i)=>thCardHTML(c,false,i*80)).join('');
  // dealer
  const dlr=document.getElementById('thdlr');
  if(dlr){
    if(showDlr) dlr.innerHTML=thDlrHole.map((c,i)=>thCardHTML(c,false,i*80)).join('');
    else if(thDlrHole.length>0) dlr.innerHTML=thDlrHole.map((_,i)=>thCardHTML(null,true,i*80)).join('');
  }
  // pot
  const potEl=document.getElementById('thpot');
  if(potEl) potEl.textContent=fm(thPot);
  // street label
  const streets={preflop:'PRE-FLOP',flop:'THE FLOP',turn:'THE TURN',river:'THE RIVER',showdown:'SHOWDOWN'};
}

function thSetButtons(btns){
  // btns: array of {label, action, style}
  const row=document.getElementById('tharow');
  if(!row)return;
  row.innerHTML=btns.map(b=>`<button class="${b.style||'bgold'}" onclick="thAction('${b.action}')">${b.label}</button>`).join('');
}

function thAction(action){
  if(action==='deal'){
    if(balance<bet){toast('Insufficient funds','lose');return;}
    // ante up
    setBalance(-bet);S.tw+=bet;thPot=bet;
    mkTHDeck();
    thHole=[thDraw(),thDraw()];
    thDlrHole=[thDraw(),thDraw()];
    thCommunity=[];
    thPhase='preflop';
    thCalled=false;
    thRender(false);
    const resEl=document.getElementById('thres');if(resEl)resEl.style.display='none';
    thSetButtons([
      {label:'CALL',action:'call',style:'bgold'},
      {label:'RAISE',action:'raise',style:'bgold'},
      {label:'FOLD',action:'fold',style:'bgh'},
    ]);

  } else if(action==='call'){
    // call = match ante, deal flop
    if(balance<bet){toast('Insufficient funds','lose');return;}
    setBalance(-bet);S.tw+=bet;thPot+=bet;thCalled=true;
    thCommunity=[thDraw(),thDraw(),thDraw()];
    thPhase='flop';thRender(false);
    thSetButtons([
      {label:'CHECK',action:'check',style:'bgold'},
      {label:'RAISE',action:'raise',style:'bgold'},
    ]);

  } else if(action==='raise'){
    // raise = pay extra bet, accelerate
    if(balance<bet){toast('Insufficient funds','lose');return;}
    setBalance(-bet);S.tw+=bet;thPot+=bet;thCalled=true;
    if(thCommunity.length===0) thCommunity=[thDraw(),thDraw(),thDraw()];
    thCommunity.push(thDraw()); // turn
    thPhase='turn';thRender(false);
    thSetButtons([
      {label:'CHECK',action:'check',style:'bgold'},
      {label:'ALL IN',action:'allin',style:'bgold'},
    ]);

  } else if(action==='check'){
    // advance street
    if(thPhase==='flop'){
      thCommunity.push(thDraw());thPhase='turn';thRender(false);
      thSetButtons([{label:'CHECK TO RIVER',action:'check',style:'bgold'},{label:'RAISE',action:'raise',style:'bgold'}]);
    } else if(thPhase==='turn'){
      thCommunity.push(thDraw());thPhase='river';thRender(false);
      thSetButtons([{label:'SHOWDOWN',action:'showdown',style:'bgold'}]);
    } else {
      thShowdown();
    }

  } else if(action==='allin'){
    const allIn=Math.min(balance,bet*3);
    if(allIn>0){setBalance(-allIn);S.tw+=allIn;thPot+=allIn;}
    while(thCommunity.length<5) thCommunity.push(thDraw());
    thPhase='river';thRender(false);
    thSetButtons([{label:'SHOWDOWN',action:'showdown',style:'bgold'}]);

  } else if(action==='showdown'){
    thShowdown();

  } else if(action==='fold'){
    // lose ante
    rec('poker','fold',-bet);
    toast('Folded — dealer wins the pot','lose');
    thPhase='idle';thPot=0;
    thRender(false);
    thSetButtons([{label:'DEAL HAND',action:'deal',style:'bgold'}]);
  }
}

function thShowdown(){
  while(thCommunity.length<5) thCommunity.push(thDraw());
  thPhase='showdown';
  thRender(true); // reveal dealer
  setTimeout(()=>{
    const pRank=thBestHand([...thHole,...thCommunity]);
    const dRank=thBestHand([...thDlrHole,...thCommunity]);
    const resEl=document.getElementById('thres');
    resEl.style.display='flex';resEl.classList.remove('pa');void resEl.offsetWidth;resEl.classList.add('pa');

    if(pRank.score>dRank.score){
      const win=thPot*2;
      setBalance(win);rec('poker','win',win-thPot);
      resEl.textContent=`YOU WIN · ${pRank.name} beats ${dRank.name} · +${fm(win)}`;
      toast(`✦ ${pRank.name} · You win +${fm(win)} ✦`,'win');
      if(pRank.score>=600&&pRank.score<700){S.ach.fh=true;toast('♠️ ACHIEVEMENT · FULL HOUSE','ach');}
      if(pRank.score>=700) explode(30);
    } else if(dRank.score>pRank.score){
      rec('poker','lose',-thPot);
      resEl.textContent=`DEALER WINS · ${dRank.name} beats ${pRank.name}`;
      toast(`Dealer wins with ${dRank.name}`,'lose');
    } else {
      // tie → split
      const ret=Math.floor(thPot/2);
      setBalance(ret);rec('poker','push',0);
      resEl.textContent=`SPLIT POT · Both have ${pRank.name} · +${fm(ret)}`;
      toast(`Split pot · ${pRank.name}`,'push');
    }
    thPot=0;
    thSetButtons([{label:'DEAL HAND',action:'deal',style:'bgold'}]);
  },400);
}

// ── 5-card best hand evaluator from 7 cards ──
function thBestHand(seven){
  // generate all C(7,5)=21 combos, pick best
  let best=null;
  for(let i=0;i<7;i++)for(let j=i+1;j<7;j++){
    const five=seven.filter((_,k)=>k!==i&&k!==j);
    const rated=thRate5(five);
    if(!best||rated.score>best.score) best=rated;
  }
  return best;
}

function thRate5(hand){
  // returns {score, name} where higher score = better hand
  const rankIdx=c=>TH_RANKS.indexOf(c.r); // 0=2 … 12=A
  const vals=hand.map(rankIdx).sort((a,b)=>b-a);
  const suits=hand.map(c=>c.s);
  const cnt={};vals.forEach(v=>cnt[v]=(cnt[v]||0)+1);
  const freqs=Object.values(cnt).sort((a,b)=>b-a);
  const flush=new Set(suits).size===1;
  const sv=[...vals].sort((a,b)=>a-b);
  // check straight (including A-low: A2345)
  let straight=sv[4]-sv[0]===4&&new Set(sv).size===5;
  let straightHigh=sv[4];
  if(!straight&&JSON.stringify(sv)===JSON.stringify([0,1,2,3,12])){straight=true;straightHigh=3;} // A-2-3-4-5
  const royal=flush&&straight&&straightHigh===12;

  if(royal) return{score:900,name:'Royal Flush'};
  if(flush&&straight) return{score:800+straightHigh,name:'Straight Flush'};
  if(freqs[0]===4) return{score:700+vals[0],name:'Four of a Kind'};
  if(freqs[0]===3&&freqs[1]===2) return{score:600+vals[0],name:'Full House'};
  if(flush) return{score:500+vals[0],name:'Flush'};
  if(straight) return{score:400+straightHigh,name:'Straight'};
  if(freqs[0]===3) return{score:300+vals[0],name:'Three of a Kind'};
  if(freqs[0]===2&&freqs[1]===2){
    const pairs=Object.entries(cnt).filter(([v,c])=>c===2).map(([v])=>+v).sort((a,b)=>b-a);
    return{score:200+pairs[0],name:'Two Pair'};
  }
  if(freqs[0]===2){
    const pv=Object.entries(cnt).find(([v,c])=>c===2)[0];
    return{score:100+parseInt(pv),name:'One Pair'};
  }
  return{score:vals[0],name:'High Card ('+TH_RANKS[vals[0]]+')'};
}

/* ══════════════════════════
   ROULETTE
══════════════════════════ */
const RORD=[0,32,15,19,4,21,2,25,17,34,6,27,13,36,11,30,8,23,10,5,24,16,33,1,20,14,31,9,22,18,29,7,28,12,35,3,26];
const REDS=[1,3,5,7,9,12,14,16,18,19,21,23,25,27,30,32,34,36];
let rwa=0,rba=0,rbr=90,rsp=false,rbet='red';

function loadRoulette(){
  setModal('EUROPEAN ROULETTE',`${betBarHTML()}
    <div class="rlayout">
      <div class="rww">
        <canvas id="rlc" width="210" height="210"></canvas>
        <div class="rnd" id="rnd"></div>
      </div>
      <div class="rbrd">
        <div class="rbrow"><button class="rbtn sr" data-bt="red" onclick="setRB('red',this)">🔴 RED</button><button class="rbtn" data-bt="black" onclick="setRB('black',this)">⚫ BLACK</button></div>
        <div class="rbrow"><button class="rbtn" data-bt="even" onclick="setRB('even',this)">EVEN</button><button class="rbtn" data-bt="odd" onclick="setRB('odd',this)">ODD</button></div>
        <div class="rbrow"><button class="rbtn" data-bt="low" onclick="setRB('low',this)">1–18</button><button class="rbtn" data-bt="high" onclick="setRB('high',this)">19–36</button></div>
        <div class="rbrow"><button class="rbtn" data-bt="d1" onclick="setRB('d1',this)">1ST 12</button><button class="rbtn" data-bt="d2" onclick="setRB('d2',this)">2ND 12</button><button class="rbtn" data-bt="d3" onclick="setRB('d3',this)">3RD 12</button></div>
        <div style="font-family:'Cinzel',serif;font-size:8px;letter-spacing:3px;color:rgba(var(--accent-rgb),.28);margin-top:5px">EVEN MONEY ×2 · DOZENS ×3</div>
      </div>
    </div>
    <div class="arow"><button class="bgold" id="rspnb" onclick="spinRoulette()">SPIN THE WHEEL</button></div>`);
  startRoulette();
}
function setRB(t,el){
  rbet=t;
  document.querySelectorAll('.rbtn').forEach(b=>{const bt=b.dataset.bt;b.className='rbtn'+(bt===t?(t==='red'?' sr':t==='black'?' sb':' sa'):'');});
}
function startRoulette(){
  const c=document.getElementById('rlc');if(!c)return;
  const ctx=c.getContext('2d');
  function draw(){roulRAF=requestAnimationFrame(draw);if(!document.getElementById('rlc')){cancelAnimationFrame(roulRAF);return;}drawW(ctx);}
  draw();
}
function drawW(ctx){
  const W=210,cx=105,cy=105,n=RORD.length,step=Math.PI*2/n;
  ctx.clearRect(0,0,W,W);
  const rim=ctx.createRadialGradient(cx,cy,78,cx,cy,103);
  rim.addColorStop(0,'#2a2010');rim.addColorStop(.72,'#3a2e12');rim.addColorStop(1,'#c9a84c');
  ctx.beginPath();ctx.arc(cx,cy,103,0,Math.PI*2);ctx.fillStyle=rim;ctx.fill();
  ctx.save();ctx.translate(cx,cy);ctx.rotate(rwa);ctx.translate(-cx,-cy);
  for(let i=0;i<n;i++){
    const a1=i*step-Math.PI/2,a2=a1+step,num=RORD[i];
    const col=num===0?'#1a7a3a':REDS.includes(num)?'#7a1010':'#0e0e0e';
    ctx.beginPath();ctx.moveTo(cx,cy);ctx.arc(cx,cy,78,a1,a2);ctx.closePath();
    ctx.fillStyle=col;ctx.fill();ctx.strokeStyle='rgba(200,164,90,.32)';ctx.lineWidth=.35;ctx.stroke();
    const mid=(a1+a2)/2,tx=cx+61*Math.cos(mid),ty=cy+61*Math.sin(mid);
    ctx.save();ctx.translate(tx,ty);ctx.rotate(mid+Math.PI/2);
    ctx.fillStyle='rgba(255,255,255,.78)';ctx.font='bold 6px Cinzel,serif';
    ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(num,0,0);ctx.restore();
  }
  ctx.restore();
  const hub=ctx.createRadialGradient(cx-2,cy-2,0,cx,cy,23);
  hub.addColorStop(0,'#c8a45a');hub.addColorStop(.5,'#3a2a08');hub.addColorStop(1,'#1a1408');
  ctx.beginPath();ctx.arc(cx,cy,23,0,Math.PI*2);ctx.fillStyle=hub;ctx.fill();
  ctx.strokeStyle='rgba(200,164,90,.48)';ctx.lineWidth=1;ctx.stroke();
  ctx.beginPath();ctx.arc(cx,cy,5,0,Math.PI*2);ctx.fillStyle='#c8a45a';ctx.fill();
  // ball shadow
  const bx=cx+rbr*Math.cos(rba),by=cy+rbr*Math.sin(rba);
  ctx.save();ctx.beginPath();ctx.arc(bx+1,by+2,5,0,Math.PI*2);ctx.fillStyle='rgba(0,0,0,.5)';ctx.filter='blur(3px)';ctx.fill();ctx.filter='none';ctx.restore();
  // ball
  const bg=ctx.createRadialGradient(bx-1.5,by-1.5,0,bx,by,5);
  bg.addColorStop(0,'#fff');bg.addColorStop(.5,'#ddd');bg.addColorStop(1,'#999');
  ctx.beginPath();ctx.arc(bx,by,5,0,Math.PI*2);ctx.fillStyle=bg;ctx.fill();
}
function spinRoulette(){
  if(rsp)return;if(balance<bet){toast('Insufficient funds','lose');return;}
  setBalance(-bet);S.tw+=bet;rsp=true;document.getElementById('rspnb').disabled=true;
  const el=document.getElementById('rnd');if(el){el.textContent='';el.className='rnd';}
  const target=Math.floor(Math.random()*37);
  const dur=4200+Math.random()*2000;let st=null;const bwa=rwa,bba=rba;
  function anim(ts){
    if(!st)st=ts;const el2=ts-st,p=Math.min(el2/dur,1);
    const ease=1-Math.pow(1-p,3);
    rwa=bwa+(Math.PI*2*8+Math.PI)*ease;rba=bba-(Math.PI*2*14+Math.PI)*ease;rbr=90-8*Math.sin(p*Math.PI);
    if(p<1){roulRAF=requestAnimationFrame(anim);}
    else{rsp=false;document.getElementById('rspnb').disabled=false;resolveRoulette(target);}
  }
  cancelAnimationFrame(roulRAF);roulRAF=requestAnimationFrame(anim);
}
function resolveRoulette(num){
  const isR=REDS.includes(num),col=num===0?'g':isR?'r':'b2',label=num===0?'GREEN':isR?'RED':'BLACK';
  const el=document.getElementById('rnd');if(el){el.textContent=num;el.className='rnd '+col;}
  let win=false,mult=0;
  if(rbet==='red'&&isR){win=true;mult=2;}else if(rbet==='black'&&!isR&&num!==0){win=true;mult=2;}
  else if(rbet==='even'&&num>0&&num%2===0){win=true;mult=2;}else if(rbet==='odd'&&num%2===1){win=true;mult=2;}
  else if(rbet==='low'&&num>=1&&num<=18){win=true;mult=2;}else if(rbet==='high'&&num>=19&&num<=36){win=true;mult=2;}
  else if(rbet==='d1'&&num>=1&&num<=12){win=true;mult=3;}else if(rbet==='d2'&&num>=13&&num<=24){win=true;mult=3;}
  else if(rbet==='d3'&&num>=25&&num<=36){win=true;mult=3;}
  if(win){setBalance(bet*mult);rec('roulette','win',bet*mult);toast(`${num} · ${label} · +${fm(bet*mult)}`,'win');if(mult>=2)explode(18);}
  else{rec('roulette','lose',0);toast(`${num} · ${label} · No win`,'lose');}
}
</script>
</body>
</html>
