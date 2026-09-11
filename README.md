# SHEL-UNIFORMES-INDUSTRIALES
paguina web
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SHEL Industrial Uniforms — Uniformes de trabajo</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@600;700;800;900&family=Work+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --charcoal:#19191b;
    --charcoal-2:#232326;
    --navy:#212a35;
    --navy-2:#2b3745;
    --gold:#c9a24b;
    --gold-light:#e2c884;
    --cream:#f1eee6;
    --cream-2:#e8e3d6;
    --ink:#191917;
    --muted:#77767a;
    --muted-light:#a9a7ad;
    --line:#3a3a3d;
    --radius:3px;
    --wrap:1180px;
    --green:#2f7d5a;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Work Sans',sans-serif;
    background:var(--cream);
    color:var(--ink);
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,h4{
    font-family:'Big Shoulders Display',sans-serif;
    font-weight:800;
    line-height:0.98;
    letter-spacing:0.2px;
  }
  a{color:inherit;text-decoration:none;}
  ul{list-style:none;}
  img,svg{display:block;max-width:100%;}
  button{font-family:inherit;cursor:pointer;border:none;background:none;color:inherit;}
  input,select{font-family:inherit;font-size:0.95rem;}
  .wrap{max-width:var(--wrap);margin:0 auto;padding:0 28px;}
  :focus-visible{outline:2px solid var(--gold);outline-offset:2px;}
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important;transition-duration:0.01ms !important;}
  }

  /* ---------- LOGO ---------- */
  .logo-mark{display:flex;align-items:center;gap:12px;}
  .logo-mark .logo-svg{width:42px;height:42px;flex:none;}
  .logo-mark .word{
    font-family:'Big Shoulders Display',sans-serif;
    font-weight:800;
    font-size:1.5rem;
    letter-spacing:0.5px;
    line-height:1;
  }
  .logo-mark .word small{
    display:block;
    font-family:'Work Sans',sans-serif;
    font-weight:600;
    font-size:0.56rem;
    letter-spacing:2.2px;
    color:var(--muted-light);
    margin-top:3px;
  }
  .logo-mark.on-dark .word{color:var(--cream);}
  .logo-mark.on-dark .word small{color:var(--gold-light);}

  /* ---------- HEADER ---------- */
  header{
    position:sticky;top:0;z-index:60;
    background:rgba(25,25,27,0.96);
    border-bottom:1px solid var(--line);
    backdrop-filter:blur(6px);
  }
  .nav-row{display:flex;align-items:center;justify-content:space-between;height:74px;gap:20px;}
  nav.links{display:flex;align-items:center;gap:30px;}
  nav.links a{
    color:var(--muted-light);
    font-size:0.93rem;
    font-weight:500;
    transition:color .15s;
    position:relative;
  }
  nav.links a:hover,nav.links a.active{color:var(--cream);}
  nav.links a.active::after{
    content:"";position:absolute;left:0;right:0;bottom:-26px;height:2px;background:var(--gold);
  }
  .btn{
    display:inline-flex;align-items:center;justify-content:center;
    padding:12px 22px;
    border-radius:var(--radius);
    font-weight:600;
    font-size:0.92rem;
    border:1px solid transparent;
    transition:transform .12s ease, background .15s, border-color .15s, color .15s;
    white-space:nowrap;
  }
  .btn:active{transform:translateY(1px);}
  .btn-gold{background:var(--gold);color:#1a1508;}
  .btn-gold:hover{background:var(--gold-light);}
  .btn-outline-dark{border-color:var(--line);color:var(--cream);}
  .btn-outline-dark:hover{border-color:var(--gold);color:var(--gold-light);}
  .btn-outline-light{border-color:#c9c4b3;color:var(--ink);}
  .btn-outline-light:hover{border-color:var(--ink);}
  .menu-toggle{display:none;color:var(--cream);font-size:1.5rem;line-height:1;}
  .mobile-menu{
    display:none;
    background:var(--charcoal-2);
    border-top:1px solid var(--line);
    padding:10px 0 18px;
  }
  .mobile-menu.open{display:block;}
  .mobile-menu a{
    display:block;padding:13px 28px;color:var(--muted-light);
    border-bottom:1px solid var(--line);font-weight:500;
  }
  .mobile-menu a:hover{color:var(--gold-light);background:var(--navy);}

  /* ---------- HERO ---------- */
  .hero{
    background:linear-gradient(155deg,var(--navy) 0%, var(--charcoal) 62%);
    color:var(--cream);
    padding:90px 0 80px;
    position:relative;
    overflow:hidden;
    border-bottom:1px solid var(--line);
  }
  .hero::before{
    content:"";
    position:absolute;inset:0;
    background-image:
      repeating-linear-gradient(115deg, rgba(255,255,255,0.028) 0px, rgba(255,255,255,0.028) 1px, transparent 1px, transparent 5px);
    pointer-events:none;
  }
  .hero-grid{
    position:relative;
    display:grid;
    grid-template-columns:1.05fr 0.85fr;
    gap:56px;
    align-items:center;
  }
  .eyebrow{
    font-size:0.82rem;
    font-weight:600;
    color:var(--gold-light);
    margin-bottom:18px;
  }
  .hero h1{
    font-size:clamp(2.4rem, 5vw, 4rem);
    color:var(--cream);
    margin-bottom:22px;
  }
  .hero h1 em{font-style:normal;color:var(--gold-light);}
  .hero p.lead{
    font-size:1.08rem;
    color:var(--muted-light);
    max-width:46ch;
    margin-bottom:34px;
  }
  .hero-ctas{display:flex;gap:14px;flex-wrap:wrap;}
  .hero-stats{
    display:flex;gap:34px;
    margin-top:48px;
    padding-top:26px;
    border-top:1px solid var(--line);
    flex-wrap:wrap;
  }
  .hero-stats div strong{
    display:block;font-family:'Big Shoulders Display',sans-serif;
    font-size:1.9rem;color:var(--gold-light);font-weight:800;
  }
  .hero-stats div span{font-size:0.82rem;color:var(--muted-light);}

  .patch-frame{
    background:var(--charcoal-2);
    border:1px solid var(--line);
    border-radius:6px;
    padding:44px 32px;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
  }
  .patch-frame::after{
    content:"";
    position:absolute;inset:14px;
    border:1px dashed rgba(201,162,75,0.28);
    border-radius:4px;
    pointer-events:none;
  }
  .patch-inner{text-align:center;color:var(--gold);}
  .patch-inner svg{width:130px;height:130px;margin:0 auto;color:var(--gold);}
  .patch-frame .word{
    font-family:'Big Shoulders Display',sans-serif;
    font-weight:800;
    color:var(--gold);
    text-align:center;
    margin-top:16px;
    font-size:2rem;
    letter-spacing:1px;
  }
  .patch-frame .word small{
    display:block;
    font-family:'Work Sans',sans-serif;
    font-size:0.7rem;
    letter-spacing:2px;
    color:var(--cream);
    font-weight:600;
    margin-top:2px;
  }

  /* ---------- PROMO BANNER ---------- */
  .promo{
    background:linear-gradient(120deg,#1d2a24 0%, var(--navy) 55%, #2a2333 100%);
    color:var(--cream);
    padding:0;
    border-bottom:1px solid var(--line);
    position:relative;
    overflow:hidden;
  }
  .promo::before{
    content:"";
    position:absolute;inset:0;
    background-image:repeating-linear-gradient(60deg, rgba(201,162,75,0.06) 0 2px, transparent 2px 12px);
    pointer-events:none;
  }
  .promo-grid{
    position:relative;
    display:grid;
    grid-template-columns:1fr 0.85fr;
    gap:40px;
    align-items:center;
    padding:52px 0;
  }
  .promo-badge{
    display:inline-flex;align-items:center;gap:8px;
    background:var(--gold);color:#1a1508;
    font-size:0.75rem;font-weight:700;letter-spacing:1.5px;
    padding:6px 14px;border-radius:20px;margin-bottom:18px;
    text-transform:uppercase;
  }
  .promo h2{
    font-size:clamp(1.9rem,3.4vw,2.9rem);
    margin-bottom:14px;
  }
  .promo h2 em{font-style:normal;color:var(--gold-light);}
  .promo p{color:var(--muted-light);max-width:48ch;margin-bottom:22px;}
  .promo-prices{display:flex;align-items:baseline;gap:16px;margin-bottom:26px;flex-wrap:wrap;}
  .promo-old{
    font-family:'Big Shoulders Display',sans-serif;
    font-size:1.7rem;color:#8d7a5a;text-decoration:line-through;font-weight:700;
  }
  .promo-new{
    font-family:'Big Shoulders Display',sans-serif;
    font-size:3.6rem;color:var(--gold-light);font-weight:900;line-height:1;
  }
  .promo-new small{font-size:1rem;color:var(--muted-light);font-weight:600;font-family:'Work Sans',sans-serif;}
  .promo-art{
    display:flex;align-items:center;justify-content:center;
    background:rgba(255,255,255,0.03);
    border:1px solid var(--line);
    border-radius:8px;
    padding:26px;
    position:relative;
  }
  .promo-art svg{width:100%;max-width:250px;height:auto;color:var(--gold-light);}
  .promo-tag{
    position:absolute;top:-14px;right:-8px;
    background:#c0392b;color:#fff;
    font-weight:800;font-size:0.8rem;letter-spacing:1px;
    padding:8px 14px;border-radius:4px;
    transform:rotate(6deg);
    box-shadow:0 6px 16px rgba(0,0,0,.35);
  }

  /* ---------- SECTION SHELL ---------- */
  section{padding:92px 0;}
  .section-head{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:40px;
    align-items:end;
    margin-bottom:48px;
  }
  .section-head h2{font-size:clamp(2rem,3.4vw,2.7rem);}
  .section-head p{color:var(--muted);max-width:46ch;font-size:1.02rem;}
  .on-dark .section-head p{color:var(--muted-light);}

  /* ---------- NOSOTROS ---------- */
  #nosotros{background:var(--cream);}
  .values{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:#d8d2c0;border:1px solid #d8d2c0;}
  .value-card{background:var(--cream);padding:34px 30px;}
  .value-card .vicon{width:38px;height:38px;margin-bottom:20px;color:var(--gold);}
  .value-card h3{font-size:1.25rem;margin-bottom:10px;font-weight:700;}
  .value-card p{color:var(--muted);font-size:0.95rem;}

  .embroidery-gallery{
    margin-top:56px;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1px;
    background:#d8d2c0;
    border:1px solid #d8d2c0;
    border-radius:6px;
    overflow:hidden;
  }
  .embroidery-item{background:var(--charcoal-2);}
  .embroidery-item .art{
    height:200px;display:flex;align-items:center;justify-content:center;
    background:linear-gradient(140deg,#2b3745,#19191b);color:var(--gold);
    padding:24px;
  }
  .embroidery-item .art svg{width:110px;height:110px;}
  .embroidery-item .cap{
    background:var(--charcoal-2);
    color:var(--muted-light);
    padding:14px 16px;
    font-size:0.82rem;
    border-top:1px solid var(--line);
  }
  .embroidery-item .cap b{display:block;color:var(--cream);font-size:0.92rem;margin-bottom:2px;font-weight:600;}

  /* ---------- MODELOS ---------- */
  #modelos{background:var(--charcoal);color:var(--cream);border-top:1px solid var(--line);border-bottom:1px solid var(--line);}
  .model-layout{display:grid;grid-template-columns:290px 1fr;gap:0;border:1px solid var(--line);border-radius:6px;overflow:hidden;}
  .model-list{background:var(--charcoal-2);border-right:1px solid var(--line);}
  .model-btn{
    width:100%;text-align:left;
    padding:22px 24px;
    border-bottom:1px solid var(--line);
    color:var(--muted-light);
    display:block;
    transition:background .15s;
  }
  .model-btn .m-name{font-family:'Big Shoulders Display',sans-serif;font-weight:700;font-size:1.15rem;display:block;color:var(--cream);}
  .model-btn .m-tag{font-size:0.8rem;color:var(--muted-light);}
  .model-btn .m-price{display:inline-block;margin-top:6px;font-size:0.78rem;color:var(--gold-light);font-weight:700;letter-spacing:0.5px;}
  .model-btn.active{background:var(--navy);border-left:3px solid var(--gold);}
  .model-btn.active .m-name{color:var(--gold-light);}
  .model-btn:hover{background:var(--navy-2);}

  .model-view{padding:44px;display:grid;grid-template-columns:1fr 1.15fr;gap:40px;align-items:center;}
  .garment-stage{
    display:flex;align-items:center;justify-content:center;
    background:var(--navy);border:1px solid var(--line);border-radius:6px;
    padding:30px;min-height:340px;
  }
  .garment-stage svg{width:190px;height:auto;color:var(--gold-light);transition:color .25s;}
  .model-detail h3{font-size:1.9rem;margin-bottom:10px;}
  .model-detail p.desc{color:var(--muted-light);margin-bottom:22px;max-width:46ch;}
  .swatches{display:flex;gap:14px;margin-bottom:30px;padding-top:6px;}
  .swatch{
    width:34px;height:34px;border-radius:50%;
    border:2px solid transparent;
    position:relative;
    transition:transform .15s;
  }
  .swatch:hover{transform:scale(1.08);}
  .swatch.active{border-color:var(--gold);box-shadow:0 0 0 2px rgba(201,162,75,.25);}
  .swatch::after{
    content:attr(data-label);
    position:absolute;top:42px;left:50%;transform:translateX(-50%);
    font-size:0.7rem;color:var(--muted-light);white-space:nowrap;
  }
  .spec-list{display:grid;grid-template-columns:1fr 1fr;gap:10px 20px;margin-top:34px;padding-top:24px;border-top:1px solid var(--line);}
  .spec-list div{font-size:0.86rem;color:var(--muted-light);}
  .spec-list div b{display:block;color:var(--cream);font-size:0.92rem;font-weight:600;}
  .model-cta{margin-top:28px;display:flex;gap:12px;flex-wrap:wrap;align-items:center;}
  .model-price{font-family:'Big Shoulders Display',sans-serif;font-size:2.2rem;color:var(--gold-light);font-weight:800;}
  .model-price span{font-size:0.85rem;font-family:'Work Sans',sans-serif;color:var(--muted-light);font-weight:500;}

  /* ---------- FISCALIAS ---------- */
  #fiscalias{background:var(--charcoal-2);border-top:1px solid var(--line);border-bottom:1px solid var(--line);color:var(--cream);}
  .fisc-badge{
    display:inline-flex;align-items:center;gap:8px;
    padding:6px 14px;border:1px solid var(--line);border-radius:20px;
    font-size:0.78rem;color:var(--gold-light);margin-bottom:18px;
  }
  .fisc-badge svg{width:14px;height:14px;}
  .fisc-grid{display:grid;grid-template-columns:1.1fr 1fr;gap:0;border:1px solid var(--line);border-radius:6px;overflow:hidden;}
  .fisc-info{background:var(--navy);padding:44px;}
  .fisc-info p.fisc-desc{color:var(--muted-light);margin-bottom:26px;max-width:52ch;}
  .fisc-spec-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px 22px;margin-bottom:28px;}
  .fisc-spec-grid div{font-size:0.85rem;color:var(--muted-light);padding-left:16px;position:relative;}
  .fisc-spec-grid div::before{content:"";position:absolute;left:0;top:7px;width:6px;height:6px;background:var(--gold);border-radius:1px;}
  .fisc-spec-grid div b{display:block;color:var(--cream);font-size:0.92rem;font-weight:600;}
  .fisc-note{
    font-size:0.82rem;line-height:1.6;color:var(--muted-light);
    border-top:1px solid var(--line);padding-top:20px;
  }
  .fisc-note strong{color:var(--gold-light);}

  .fisc-chat{background:var(--charcoal);display:flex;flex-direction:column;height:100%;min-height:420px;}
  .fisc-chat-head{padding:20px 24px;border-bottom:1px solid var(--line);}
  .fisc-chat-head strong{display:block;color:var(--cream);font-size:1rem;margin-bottom:3px;font-family:'Work Sans',sans-serif;}
  .fisc-chat-head span{font-size:0.78rem;color:var(--muted-light);}
  #fisc-chat-body{flex:1;overflow-y:auto;padding:20px 24px;display:flex;flex-direction:column;gap:12px;max-height:340px;}
  .fisc-msg{max-width:88%;padding:11px 14px;border-radius:10px;font-size:0.87rem;line-height:1.5;white-space:pre-line;}
  .fisc-msg.bot{background:var(--navy);color:var(--cream);align-self:flex-start;border-bottom-left-radius:2px;}
  .fisc-msg.user{background:var(--gold);color:#1a1508;align-self:flex-end;border-bottom-right-radius:2px;}
  .fisc-chat-quick{display:flex;gap:8px;flex-wrap:wrap;padding:0 24px 14px;}
  .fisc-chip{
    font-size:0.74rem;color:var(--gold-light);
    border:1px solid var(--line);padding:6px 10px;border-radius:14px;
    transition:border-color .15s,background .15s;
  }
  .fisc-chip:hover{border-color:var(--gold);background:rgba(201,162,75,.08);}
  .fisc-chat-input-row{display:flex;border-top:1px solid var(--line);}
  .fisc-chat-input-row input{
    flex:1;background:transparent;border:none;color:var(--cream);
    padding:16px 20px;font-size:0.9rem;outline:none;
  }
  .fisc-chat-input-row input::placeholder{color:var(--muted);}
  .fisc-chat-input-row button{color:var(--gold);padding:0 22px;font-weight:700;}

  /* ---------- COTIZACION ---------- */
  #cotizacion{background:var(--cream-2);}
  .quote-grid{display:grid;grid-template-columns:1.3fr 1fr;gap:0;border:1px solid #d8d2c0;border-radius:6px;overflow:hidden;background:var(--cream);}
  form.quote-form{padding:44px;}
  .field{margin-bottom:20px;}
  .field label{display:block;font-size:0.85rem;font-weight:600;margin-bottom:7px;color:var(--ink);}
  .field-row{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
  .field input[type=text],
  .field input[type=email],
  .field input[type=tel],
  .field input[type=number],
  .field select{
    width:100%;padding:12px 14px;
    border:1px solid #cfc9b8;border-radius:var(--radius);
    background:#fff;color:var(--ink);
    font-size:0.95rem;
    transition:border-color .15s;
  }
  .field input:focus, .field select:focus{border-color:var(--gold);outline:none;}
  .toggle-group{display:flex;gap:10px;}
  .toggle-opt{
    flex:1;text-align:center;padding:10px 8px;
    border:1px solid #cfc9b8;border-radius:var(--radius);
    font-size:0.88rem;font-weight:600;color:var(--muted);
    background:#fff;
    transition:all .15s;
  }
  .toggle-opt.active{border-color:var(--gold);background:#fbf3df;color:#8a6a1a;}
  .size-grid{display:flex;flex-wrap:wrap;gap:8px;}
  .size-chip{
    padding:7px 13px;border:1px solid #cfc9b8;border-radius:20px;
    font-size:0.82rem;color:var(--muted);background:#fff;
    transition:all .15s;
  }
  .size-chip.active{background:var(--ink);color:var(--cream);border-color:var(--ink);}

  .quote-summary{
    background:var(--navy);color:var(--cream);
    padding:44px 38px;
    display:flex;flex-direction:column;
  }
  .quote-summary h3{font-size:1.5rem;margin-bottom:6px;}
  .quote-summary .sub{color:var(--muted-light);font-size:0.86rem;margin-bottom:28px;}
  .sum-row{display:flex;justify-content:space-between;padding:12px 0;border-bottom:1px solid var(--line);font-size:0.92rem;}
  .sum-row span:first-child{color:var(--muted-light);}
  .sum-row.discount span:last-child{color:var(--gold-light);}
  .sum-total{display:flex;justify-content:space-between;align-items:baseline;padding-top:20px;margin-top:6px;}
  .sum-total span:first-child{font-size:0.95rem;color:var(--muted-light);}
  .sum-total strong{font-family:'Big Shoulders Display',sans-serif;font-size:2.5rem;color:var(--gold-light);font-weight:800;}
  .quote-note{font-size:0.78rem;color:var(--muted-light);margin-top:18px;line-height:1.6;}
  .quote-summary .btn{margin-top:26px;}
  #quoteConfirm{
    margin-top:16px;font-size:0.86rem;color:var(--gold-light);
    display:none;padding:12px 14px;border:1px solid var(--gold);border-radius:var(--radius);
  }

  /* ---------- FOOTER ---------- */
  footer{background:var(--charcoal);color:var(--muted-light);padding:70px 0 30px;border-top:1px solid var(--line);}
  .foot-grid{display:grid;grid-template-columns:1.4fr 1fr 1fr;gap:50px;margin-bottom:56px;}
  .foot-grid h4{color:var(--cream);font-size:0.95rem;font-weight:700;margin-bottom:16px;font-family:'Work Sans',sans-serif;}
  .foot-grid p{font-size:0.9rem;max-width:38ch;margin-bottom:18px;}
  .foot-grid ul li{margin-bottom:10px;font-size:0.9rem;}
  .foot-grid ul li a:hover{color:var(--gold-light);}
  .foot-bottom{
    display:flex;justify-content:space-between;flex-wrap:wrap;gap:12px;
    padding-top:26px;border-top:1px solid var(--line);
    font-size:0.8rem;color:var(--muted);
  }

  /* ---------- CHAT ---------- */
  #chat-toggle{
    position:fixed;right:26px;bottom:26px;z-index:80;
    width:60px;height:60px;border-radius:50%;
    background:var(--gold);color:#1a1508;
    display:flex;align-items:center;justify-content:center;
    box-shadow:0 8px 22px rgba(0,0,0,0.32);
    transition:transform .15s;
  }
  #chat-toggle:hover{transform:scale(1.06);}
  #chat-toggle svg{width:26px;height:26px;}

  #chat-panel{
    position:fixed;right:26px;bottom:98px;z-index:80;
    width:340px;max-width:calc(100vw - 40px);
    height:440px;max-height:calc(100vh - 150px);
    background:var(--charcoal-2);
    border:1px solid var(--line);
    border-radius:8px;
    display:none;
    flex-direction:column;
    overflow:hidden;
    box-shadow:0 20px 50px rgba(0,0,0,0.45);
  }
  #chat-panel.open{display:flex;}
  .chat-head{
    background:var(--navy);padding:16px 18px;
    display:flex;align-items:center;justify-content:space-between;
    border-bottom:1px solid var(--line);
  }
  .chat-head .who{display:flex;align-items:center;gap:10px;}
  .chat-head .dot{width:8px;height:8px;border-radius:50%;background:#5fd58a;}
  .chat-head strong{color:var(--cream);font-size:0.92rem;font-family:'Work Sans',sans-serif;}
  .chat-head span{display:block;font-size:0.72rem;color:var(--muted-light);}
  .chat-close{color:var(--muted-light);font-size:1.2rem;line-height:1;}
  #chat-body{flex:1;overflow-y:auto;padding:16px;display:flex;flex-direction:column;gap:10px;}
  .msg{max-width:82%;padding:10px 13px;border-radius:10px;font-size:0.86rem;line-height:1.45;white-space:pre-line;}
  .msg.bot{background:var(--navy);color:var(--cream);align-self:flex-start;border-bottom-left-radius:2px;}
  .msg.user{background:var(--gold);color:#1a1508;align-self:flex-end;border-bottom-right-radius:2px;}
  .chat-quick{display:flex;gap:8px;flex-wrap:wrap;padding:0 16px 12px;}
  .chip{
    font-size:0.74rem;color:var(--gold-light);
    border:1px solid var(--line);padding:6px 10px;border-radius:14px;
    transition:border-color .15s,background .15s;
  }
  .chip:hover{border-color:var(--gold);background:rgba(201,162,75,.08);}
  .chat-input-row{display:flex;border-top:1px solid var(--line);}
  .chat-input-row input{
    flex:1;background:transparent;border:none;color:var(--cream);
    padding:14px 16px;font-size:0.88rem;outline:none;
  }
  .chat-input-row input::placeholder{color:var(--muted);}
  .chat-input-row button{color:var(--gold);padding:0 18px;font-weight:700;}

  /* ---------- RESPONSIVE ---------- */
  @media (max-width:960px){
    nav.links{display:none;}
    .menu-toggle{display:block;}
    .hero-grid{grid-template-columns:1fr;}
    .patch-frame{max-width:340px;}
    .promo-grid{grid-template-columns:1fr;}
    .promo-art{order:-1;max-width:360px;}
    .section-head{grid-template-columns:1fr;}
    .values{grid-template-columns:1fr;}
    .embroidery-gallery{grid-template-columns:1fr;}
    .model-layout{grid-template-columns:1fr;}
    .model-list{display:flex;overflow-x:auto;border-right:none;border-bottom:1px solid var(--line);}
    .model-btn{border-bottom:none;border-right:1px solid var(--line);white-space:nowrap;min-width:200px;}
    .model-btn.active{border-left:none;border-bottom:3px solid var(--gold);}
    .model-view{grid-template-columns:1fr;padding:30px;}
    .quote-grid{grid-template-columns:1fr;}
    .fisc-grid{grid-template-columns:1fr;}
    .field-row{grid-template-columns:1fr;}
    .foot-grid{grid-template-columns:1fr;gap:34px;}
    #chat-panel{right:14px;left:14px;width:auto;}
    #chat-toggle{right:18px;}
    section{padding:70px 0;}
  }
</style>
</head>
<body>

<!-- ============ HEADER ============ -->
<header>
  <div class="wrap nav-row">
    <a href="#inicio" class="logo-mark on-dark">
      <svg class="logo-svg" viewBox="0 0 100 100" aria-hidden="true">
        <circle cx="50" cy="50" r="47" fill="#121214" stroke="#c9a24b" stroke-width="2.5"/>
        <path d="M50 20 L57 36 L74 38 L61 50 L65 67 L50 57 L35 67 L39 50 L26 38 L43 36 Z" fill="#c9a24b"/>
        <rect x="46.5" y="60" width="7" height="18" rx="1" fill="#c9a24b"/>
      </svg>
      <span class="word">SHEL<small>INDUSTRIAL UNIFORMS</small></span>
    </a>
    <nav class="links" id="desktopNav">
      <a href="#inicio">Inicio</a>
      <a href="#nosotros">Nosotros</a>
      <a href="#promo">Promo</a>
      <a href="#modelos">Modelos</a>
      <a href="#fiscalias">Fiscalías</a>
      <a href="#cotizacion">Cotización</a>
      <a href="#contacto">Contacto</a>
    </nav>
    <a href="#cotizacion" class="btn btn-gold">Solicitar cotización</a>
    <button class="menu-toggle" id="menuToggle" aria-label="Abrir menú" aria-expanded="false">☰</button>
  </div>
  <div class="mobile-menu" id="mobileMenu">
    <a href="#inicio">Inicio</a>
    <a href="#nosotros">Nosotros</a>
    <a href="#promo">Promo batas $199</a>
    <a href="#modelos">Modelos</a>
    <a href="#fiscalias">Fiscalías</a>
    <a href="#cotizacion">Cotización</a>
    <a href="#contacto">Contacto</a>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero" id="inicio">
  <div class="wrap hero-grid">
    <div>
      <div class="eyebrow">Confección de uniformes industriales y de farmacia</div>
      <h1>Uniformes construidos para <em>el turno completo.</em></h1>
      <p class="lead">Camisolas, overoles y batas de mostrador en tela resistente, con tu logo bordado y curva de tallas ajustada por lote. Cotiza tu pedido en minutos, sin intermediarios.</p>
      <div class="hero-ctas">
        <a href="#modelos" class="btn btn-gold">Ver modelos</a>
        <a href="#promo" class="btn btn-outline-dark">Promo batas $199</a>
      </div>
      <div class="hero-stats">
        <div><strong>3</strong><span>líneas de prenda</span></div>
        <div><strong>10+</strong><span>unidades mínimas por pedido</span></div>
        <div><strong>$199</strong><span>precio por prenda</span></div>
      </div>
    </div>
    <div class="patch-frame">
      <div class="patch-inner">
        <svg viewBox="0 0 100 100" aria-hidden="true">
          <circle cx="50" cy="50" r="46" fill="none" stroke="currentColor" stroke-width="1.5" stroke-dasharray="4 4"/>
          <path d="M50 16 L58 34 L77 36 L63 49 L67 68 L50 57 L33 68 L37 49 L23 36 L42 34 Z" fill="currentColor"/>
          <rect x="46" y="60" width="8" height="20" rx="1.5" fill="currentColor"/>
        </svg>
        <div class="word">SHEL<small>BORDADO PERSONALIZADO</small></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ PROMO BANNER ============ -->
<section class="promo" id="promo">
  <div class="wrap promo-grid">
    <div>
      <span class="promo-badge">Promo del mes</span>
      <h2>Bata de mostrador para farmacia<br><em>antes $250 · ahora $199</em></h2>
      <p>Bata antifluido con cierre oculto, manga larga y bordado de tu farmacia. Ideal para personal de mostrador, consultorio y área de recetas. Precio especial por tiempo limitado.</p>
      <div class="promo-prices">
        <span class="promo-old">$250</span>
        <span class="promo-new">$199<small> c/u</small></span>
      </div>
      <div class="hero-ctas">
        <button class="btn btn-gold" id="promoBataBtn">Cotizar bata a $199</button>
        <a href="#modelos" class="btn btn-outline-dark">Ver todas las prendas</a>
      </div>
    </div>
    <div class="promo-art">
      <span class="promo-tag">-20%</span>
      <svg viewBox="0 0 220 280" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linejoin="round" stroke-linecap="round" aria-label="Bata de mostrador para farmacia">
        <!-- bata -->
        <path d="M82 46 L58 54 L18 120 L42 140 L50 124 L46 250 L174 250 L170 124 L178 140 L202 120 L162 54 L138 46 L110 74 Z"/>
        <path d="M82 46 L110 74 L138 46"/>
        <path d="M96 52 L110 74 L124 52"/>
        <path d="M110 74 L110 250"/>
        <circle cx="110" cy="120" r="3.5" fill="currentColor"/>
        <circle cx="110" cy="150" r="3.5" fill="currentColor"/>
        <circle cx="110" cy="180" r="3.5" fill="currentColor"/>
        <rect x="62" y="100" width="34" height="34" rx="2"/>
        <rect x="124" y="100" width="34" height="34" rx="2"/>
      </svg>
    </div>
  </div>
</section>

<!-- ============ NOSOTROS ============ -->
<section id="nosotros">
  <div class="wrap">
    <div class="section-head">
      <h2>Ropa de trabajo pensada para&nbsp;el&nbsp;turno completo</h2>
      <p>SHEL diseña y confecciona uniformes industriales y de farmacia para empresas que necesitan prendas resistentes, cómodas y con identidad visual consistente en todo el equipo.</p>
    </div>
    <div class="values">
      <div class="value-card">
        <svg class="vicon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M4 21V8l8-5 8 5v13"/><path d="M9 21v-7h6v7"/></svg>
        <h3>Tela de trabajo real</h3>
        <p>Drill y gabardina de gramaje industrial, con costuras reforzadas en zonas de mayor desgaste.</p>
      </div>
      <div class="value-card">
        <svg class="vicon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 3l1.9 4.6L19 9l-4.1 3.3L16 17l-4-2.7L8 17l1.1-4.7L5 9l5.1-1.4z"/></svg>
        <h3>Bordado de tu logo</h3>
        <p>Digitalizamos tu marca y la bordamos en pecho, espalda o manga, con hilo de color estable al lavado.</p>
      </div>
      <div class="value-card">
        <svg class="vicon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M3 12h18M3 6h18M3 18h18"/></svg>
        <h3>Tallas por lote</h3>
        <p>Curva de tallas ajustada a tu planilla de personal, de XS a 3XL, en un mismo pedido.</p>
      </div>
    </div>

    <div class="embroidery-gallery">
      <div class="embroidery-item">
        <div class="art">
          <svg viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2" stroke-linejoin="round">
            <path d="M38 22 L24 28 L10 56 L22 64 L26 54 L24 88 L76 88 L74 54 L78 64 L90 56 L76 28 L62 22 L50 34 Z"/>
            <path d="M38 22 L50 34 L62 22"/>
            <path d="M50 34 L50 88"/>
            <circle cx="50" cy="52" r="7"/>
          </svg>
        </div>
        <div class="cap"><b>Camisola industrial</b>Bordado en pecho, hilo dorado sobre drill</div>
      </div>
      <div class="embroidery-item">
        <div class="art">
          <svg viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2" stroke-linejoin="round">
            <path d="M30 20 L18 26 L8 52 L20 60 L24 50 L22 90 L48 90 L50 62 L52 90 L78 90 L76 50 L80 60 L92 52 L82 26 L70 20 L50 32 Z"/>
            <path d="M30 20 L50 32 L70 20"/>
            <path d="M22 58 L78 58"/>
          </svg>
        </div>
        <div class="cap"><b>Overol reforzado</b>Aplicación tipo parche en espalda o pierna</div>
      </div>
      <div class="embroidery-item">
        <div class="art">
          <svg viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="2" stroke-linejoin="round">
            <path d="M36 20 L22 26 L8 54 L20 62 L24 52 L22 92 L78 92 L76 52 L80 62 L92 54 L78 26 L64 20 L50 32 Z"/>
            <path d="M36 20 L50 32 L64 20"/>
            <path d="M50 32 L50 92"/>
            <rect x="28" y="46" width="14" height="14" rx="1"/>
            <rect x="58" y="46" width="14" height="14" rx="1"/>
          </svg>
        </div>
        <div class="cap"><b>Bata de mostrador</b>Bordado farmacia en pecho, tela antifluido</div>
      </div>
    </div>
  </div>
</section>

<!-- ============ MODELOS ============ -->
<section id="modelos" class="on-dark">
  <div class="wrap">
    <div class="section-head">
      <h2>Nuestras líneas de prenda</h2>
      <p>Elige la prenda, define el color y ajusta tu cotización. Camisola, overol y bata de mostrador para farmacias desde $199 por unidad.</p>
    </div>

    <div class="model-layout">
      <div class="model-list" id="modelList" role="tablist" aria-label="Líneas de prenda"></div>
      <div class="model-view" id="modelView"></div>
    </div>
  </div>
</section>

<!-- ============ FISCALIAS ============ -->
<section id="fiscalias" class="on-dark">
  <div class="wrap">
    <div class="section-head">
      <h2>Venta institucional a fiscalías</h2>
      <p>Atendemos licitaciones y compras institucionales con facturación, tiempos de entrega comprometidos y reposición por talla.</p>
    </div>

    <div class="fisc-grid">
      <div class="fisc-info">
        <span class="fisc-badge">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3l8 4v6c0 5-3.5 8-8 8s-8-3-8-8V7z"/><path d="M9 12l2 2 4-4"/></svg>
          Compra institucional
        </span>
        <h3 style="font-size:1.6rem;color:var(--cream);margin-bottom:12px;">Uniformes para fiscalías y personal ministerial</h2>
        <p class="fisc-desc">Camisolas, overoles y batas con bordado institucional, identificación por nombre y cargo, y curva de tallas por dependencia.</p>
        <div class="fisc-spec-grid">
          <div><b>Pedido mínimo</b>25 unidades por lote</div>
          <div><b>Facturación</b>CFDI y orden de compra</div>
          <div><b>Entrega</b>15 a 25 días hábiles</div>
          <div><b>Bordado</b>Escudo + nombre + cargo</div>
          <div><b>Precio unitario</b>Desde $199</div>
          <div><b>Reposición</b>Por talla individual</div>
        </div>
        <p class="fisc-note"><strong>Nota:</strong> para licitaciones solicitamos especificaciones técnicas, muestra de tela y ficha de tallas. Enviamos propuesta formal con vigencia y condiciones de pago.</p>
      </div>

      <div class="fisc-chat">
        <div class="fisc-chat-head">
          <strong>Mesa de licitaciones</strong>
          <span>Respuesta en horario laboral · Lun a Vie 9:00–18:00</span>
        </div>
        <div id="fisc-chat-body"></div>
        <div class="fisc-chat-quick">
          <button class="fisc-chip" data-q="¿Cuál es el pedido mínimo para fiscalías?">Pedido mínimo</button>
          <button class="fisc-chip" data-q="¿Qué documentación piden para licitar?">Documentación</button>
          <button class="fisc-chip" data-q="¿Cuál es el tiempo de entrega para 200 piezas?">Tiempos de entrega</button>
        </div>
        <div class="fisc-chat-input-row">
          <input type="text" id="fiscInput" placeholder="Escribe tu consulta institucional…" aria-label="Mensaje para licitaciones">
          <button id="fiscSend">Enviar</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ COTIZACION ============ -->
<section id="cotizacion">
  <div class="wrap">
    <div class="section-head">
      <h2>Cotiza tu pedido</h2>
      <p>Completa el formulario y obtén un resumen inmediato. El precio base es $199 por prenda, con descuentos por volumen.</p>
    </div>

    <div class="quote-grid">
      <form class="quote-form" id="quoteForm" novalidate>
        <div class="field-row">
          <div class="field">
            <label for="qNombre">Nombre y apellido</label>
            <input type="text" id="qNombre" placeholder="Ej. María González" required>
          </div>
          <div class="field">
            <label for="qEmpresa">Empresa o dependencia</label>
            <input type="text" id="qEmpresa" placeholder="Ej. Farmacia San Miguel">
          </div>
        </div>
        <div class="field-row">
          <div class="field">
            <label for="qEmail">Correo electrónico</label>
            <input type="email" id="qEmail" placeholder="correo@empresa.com" required>
          </div>
          <div class="field">
            <label for="qTel">Teléfono / WhatsApp</label>
            <input type="tel" id="qTel" placeholder="55 1234 5678">
          </div>
        </div>

        <div class="field">
          <label>Línea de prenda</label>
          <div class="toggle-group" id="lineGroup">
            <button type="button" class="toggle-opt active" data-line="camisola">Camisola</button>
            <button type="button" class="toggle-opt" data-line="overol">Overol</button>
            <button type="button" class="toggle-opt" data-line="bata">Bata de mostrador</button>
          </div>
        </div>

        <div class="field-row">
          <div class="field">
            <label>Cantidad de piezas</label>
            <input type="number" id="qCantidad" min="10" max="2000" value="25">
          </div>
          <div class="field">
            <label>Tipo de manga</label>
            <select id="qManga">
              <option value="larga">Manga larga</option>
              <option value="corta">Manga corta</option>
            </select>
          </div>
        </div>

        <div class="field">
          <label>Tallas requeridas (selecciona las que aplican)</label>
          <div class="size-grid" id="sizeGrid">
            <button type="button" class="size-chip" data-size="XS">XS</button>
            <button type="button" class="size-chip active" data-size="S">S</button>
            <button type="button" class="size-chip active" data-size="M">M</button>
            <button type="button" class="size-chip active" data-size="L">L</button>
            <button type="button" class="size-chip active" data-size="XL">XL</button>
            <button type="button" class="size-chip" data-size="2XL">2XL</button>
            <button type="button" class="size-chip" data-size="3XL">3XL</button>
          </div>
        </div>

        <div class="field">
          <label for="qNotas">Notas del pedido</label>
          <input type="text" id="qNotas" placeholder="Bordado, colores, fecha requerida…">
        </div>
      </form>

      <div class="quote-summary">
        <h3>Resumen</h3>
        <div class="sub" id="sumLinea">Camisola industrial</div>
        <div class="sum-row"><span>Precio unitario</span><span id="sumUnit">$199</span></div>
        <div class="sum-row"><span>Cantidad</span><span id="sumQty">25 piezas</span></div>
        <div class="sum-row discount"><span>Descuento por volumen</span><span id="sumDesc">0%</span></div>
        <div class="sum-total"><span>Total estimado</span><strong id="sumTotal">$4,975</strong></div>
        <p class="quote-note">Precios en MXN, sin IVA. El bordado de logo está incluido en pedidos de 25 piezas o más. Tiempo de producción: 15 a 25 días hábiles.</p>
        <button class="btn btn-gold" id="quoteSubmit">Enviar solicitud</button>
        <div id="quoteConfirm"></div>
      </div>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer id="contacto">
  <div class="wrap">
    <div class="foot-grid">
      <div>
        <div class="logo-mark on-dark" style="margin-bottom:16px;">
          <svg class="logo-svg" viewBox="0 0 100 100" aria-hidden="true">
            <circle cx="50" cy="50" r="47" fill="#121214" stroke="#c9a24b" stroke-width="2.5"/>
            <path d="M50 20 L57 36 L74 38 L61 50 L65 67 L50 57 L35 67 L39 50 L26 38 L43 36 Z" fill="#c9a24b"/>
            <rect x="46.5" y="60" width="7" height="18" rx="1" fill="#c9a24b"/>
          </svg>
          <span class="word">SHEL<small>INDUSTRIAL UNIFORMS</small></span>
        </div>
        <p>Confección de uniformes industriales y de farmacia con bordado personalizado. Camisola, overol y bata de mostrador desde $199.</p>
      </div>
      <div>
        <h4>Secciones</h4>
        <ul>
          <li><a href="#nosotros">Nosotros</a></li>
          <li><a href="#promo">Promo batas $199</a></li>
          <li><a href="#modelos">Modelos</a></li>
          <li><a href="#fiscalias">Fiscalías</a></li>
          <li><a href="#cotizacion">Cotización</a></li>
        </ul>
      </div>
      <div>
        <h4>Contacto</h4>
        <ul>
          <li>ventas@sheluniforms.mx</li>
          <li>+52 55 1234 5678</li>
          <li>Lun a Vie 9:00–18:00</li>
          <li>Ciudad de México</li>
        </ul>
      </div>
    </div>
    <div class="foot-bottom">
      <span>© <span id="year"></span> SHEL Industrial Uniforms. Todos los derechos reservados.</span>
      <span>Aviso de privacidad · Términos de servicio</span>
    </div>
  </div>
</footer>

<!-- ============ CHAT FLOTANTE ============ -->
<button id="chat-toggle" aria-label="Abrir chat">
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
    <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8z"/>
  </svg>
</button>

<div id="chat-panel">
  <div class="chat-head">
    <div class="who">
      <span class="dot"></span>
      <div>
        <strong>SHEL Ventas</strong>
        <span>En línea ahora</span>
      </div>
    </div>
    <button class="chat-close" id="chatClose" aria-label="Cerrar chat">✕</button>
  </div>
  <div id="chat-body"></div>
  <div class="chat-quick">
    <button class="chip" data-q="¿Cuánto cuesta la camisola?">Precio camisola</button>
    <button class="chip" data-q="¿Cuánto cuesta el overol?">Precio overol</button>
    <button class="chip" data-q="¿Cuánto cuesta la bata de farmacia?">Precio bata</button>
    <button class="chip" data-q="¿Cuál es el pedido mínimo?">Pedido mínimo</button>
  </div>
  <div class="chat-input-row">
    <input type="text" id="chatInput" placeholder="Escribe tu mensaje…" aria-label="Mensaje de chat">
    <button id="chatSend">Enviar</button>
  </div>
</div>

<script>
/* =========================================================
   DATOS DE LAS LÍNEAS DE PRENDA
   ========================================================= */
const LINEAS = {
  camisola: {
    nombre: 'Camisola Industrial',
    tag: 'Manga larga / corta · Drill',
    precio: 199,
    desc: 'Camisola de trabajo con cuello reforzado, dos bolsas de pecho y placket de botones. Confeccionada en drill de gramaje industrial, ideal para piso de planta y almacén.',
    specs: [
      ['Tela', 'Drill 100% algodón'],
      ['Gramaje', '250 g/m²'],
      ['Bolsas', '2 de pecho con solapa'],
      ['Cierre', 'Botones reforzados'],
      ['Tallas', 'XS a 3XL'],
      ['Bordado', 'Pecho izquierdo']
    ],
    swatches: [
      { color: '#2b3745', label: 'Azul marino' },
      { color: '#3b3b3b', label: 'Gris' },
      { color: '#5c6b4a', label: 'Verde' },
      { color: '#8a6a3b', label: 'Caqui' }
    ],
    svg: `<svg viewBox="0 0 220 260" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linejoin="round" stroke-linecap="round">
        <path d="M85 48 L62 56 L20 130 L46 148 L52 132 L46 228 L174 228 L168 132 L174 148 L200 130 L158 56 L135 48 L110 76 Z"/>
        <path d="M85 48 L110 76 L135 48"/>
        <path d="M110 76 L110 228"/>
        <rect x="64" y="120" width="32" height="36" rx="2"/>
        <rect x="124" y="120" width="32" height="36" rx="2"/>
        <circle cx="110" cy="100" r="3" fill="currentColor"/>
        <circle cx="110" cy="130" r="3" fill="currentColor"/>
        <circle cx="110" cy="160" r="3" fill="currentColor"/>
        <circle cx="110" cy="190" r="3" fill="currentColor"/>
      </svg>`
  },
  overol: {
    nombre: 'Overol Reforzado',
    tag: 'Cuerpo completo · Gabardina',
    precio: 199,
    desc: 'Overol de una pieza con cintura ajustable, rodillas reforzadas y bolsa de muslo. Pensado para mantenimiento, taller y trabajo pesado de planta.',
    specs: [
      ['Tela', 'Gabardina mixta'],
      ['Gramaje', '280 g/m²'],
      ['Refuerzos', 'Rodillas y codos'],
      ['Bolsas', 'Pecho, cadera y muslo'],
      ['Tallas', 'S a 3XL'],
      ['Bordado', 'Espalda o pecho']
    ],
    swatches: [
      { color: '#2b3745', label: 'Azul marino' },
      { color: '#4a4a4a', label: 'Grafito' },
      { color: '#7a5a34', label: 'Café' },
      { color: '#3f5c4a', label: 'Verde botella' }
    ],
    svg: `<svg viewBox="0 0 220 280" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linejoin="round" stroke-linecap="round">
        <path d="M85 42 L62 50 L20 118 L46 138 L52 122 L50 148 L62 258 L98 258 L106 176 L114 258 L150 258 L162 148 L170 122 L174 138 L200 118 L158 50 L135 42 L110 70 Z"/>
        <path d="M85 42 L110 70 L135 42"/>
        <path d="M110 70 L110 148"/>
        <path d="M50 148 L170 148"/>
        <rect x="64" y="96" width="30" height="32" rx="2"/>
        <rect x="126" y="96" width="30" height="32" rx="2"/>
        <rect x="150" y="170" width="26" height="36" rx="2"/>
      </svg>`
  },
  bata: {
    nombre: 'Bata de Mostrador Farmacia',
    tag: 'Antifluido · Uso comercial',
    precio: 199,
    precioAntes: 250,
    prom: true,
    desc: 'Bata de mostrador con cierre oculto, manga larga y tela antifluido. Diseñada para personal de farmacia, consultorio y área de recetas. Precio promocional por tiempo limitado.',
    specs: [
      ['Tela', 'Antifluido poliéster-algodón'],
      ['Largo', 'Media pierna (100 cm)'],
      ['Cierre', 'Oculto con botonadura'],
      ['Bolsas', '2 frontales + 1 interior'],
      ['Tallas', 'XS a 2XL'],
      ['Bordado', 'Nombre de farmacia en pecho']
    ],
    swatches: [
      { color: '#f2f0ea', label: 'Blanco clínico' },
      { color: '#d8e4ee', label: 'Azul cielo' },
      { color: '#bfe3d2', label: 'Verde menta' },
      { color: '#2b3745', label: 'Azul marino' }
    ],
    svg: `<svg viewBox="0 0 220 280" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linejoin="round" stroke-linecap="round">
        <path d="M82 46 L58 54 L18 120 L42 140 L50 124 L46 250 L174 250 L170 124 L178 140 L202 120 L162 54 L138 46 L110 74 Z"/>
        <path d="M82 46 L110 74 L138 46"/>
        <path d="M96 52 L110 74 L124 52"/>
        <path d="M110 74 L110 250"/>
        <circle cx="110" cy="118" r="3.5" fill="currentColor"/>
        <circle cx="110" cy="150" r="3.5" fill="currentColor"/>
        <circle cx="110" cy="182" r="3.5" fill="currentColor"/>
        <rect x="62" y="100" width="34" height="34" rx="2"/>
        <rect x="124" y="100" width="34" height="34" rx="2"/>
      </svg>`
  }
};

/* =========================================================
   ESTADO
   ========================================================= */
const state = {
  linea: 'camisola',
  swatch: 0
};

/* =========================================================
   RENDER: LISTA DE MODELOS
   ========================================================= */
const modelList = document.getElementById('modelList');
const modelView = document.getElementById('modelView');

function renderModelList(){
  modelList.innerHTML = Object.entries(LINEAS).map(([key, l]) => `
    <button class="model-btn ${key === state.linea ? 'active' : ''}" data-line="${key}" role="tab" aria-selected="${key === state.linea}">
      <span class="m-name">${l.nombre}</span>
      <span class="m-tag">${l.tag}</span>
      <span class="m-price">$${l.precio}${l.prom ? ' · antes $' + l.precioAntes : ''}</span>
    </button>
  `).join('');

  modelList.querySelectorAll('.model-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      state.linea = btn.dataset.line;
      state.swatch = 0;
      renderModelList();
      renderModelView();
    });
  });
}

/* =========================================================
   RENDER: DETALLE DEL MODELO
   ========================================================= */
function renderModelView(){
  const l = LINEAS[state.linea];
  const sw = l.swatches[state.swatch] || l.swatches[0];

  modelView.innerHTML = `
    <div class="garment-stage" style="color:${sw.color};">
      ${l.svg}
    </div>
    <div class="model-detail">
      <h3>${l.nombre}</h3>
      <p class="desc">${l.desc}</p>

      <div class="swatches" id="swatchWrap">
        ${l.swatches.map((s, i) => `
          <button class="swatch ${i === state.swatch ? 'active' : ''}"
                  data-index="${i}"
                  data-label="${s.label}"
                  style="background:${s.color};"
                  aria-label="Color ${s.label}"></button>
        `).join('')}
      </div>

      <div class="model-price">
        $${l.precio} <span>MXN por unidad${l.prom ? ' · antes $' + l.precioAntes : ''}</span>
      </div>

      <div class="model-cta">
        <button class="btn btn-gold" data-cotizar="${state.linea}">Cotizar ${l.nombre}</button>
        <span style="font-size:0.82rem;color:var(--muted-light);">Color: <b style="color:var(--cream)">${sw.label}</b></span>
      </div>

      <div class="spec-list">
        ${l.specs.map(([k, v]) => `<div><b>${v}</b>${k}</div>`).join('')}
      </div>
    </div>
  `;

  modelView.querySelectorAll('.swatch').forEach(b => {
    b.addEventListener('click', () => {
      state.swatch = Number(b.dataset.index);
      renderModelView();
    });
  });

  const cotizarBtn = modelView.querySelector('[data-cotizar]');
  if (cotizarBtn) {
    cotizarBtn.addEventListener('click', () => {
      setLinea(cotizarBtn.dataset.cotizar);
      document.getElementById('cotizacion').scrollIntoView({behavior:'smooth'});
    });
  }
}

/* =========================================================
   COTIZADOR
   ========================================================= */
const PRECIO_BASE = 199;
const lineGroup = document.getElementById('lineGroup');
const qCantidad = document.getElementById('qCantidad');
const sumLinea = document.getElementById('sumLinea');
const sumUnit = document.getElementById('sumUnit');
const sumQty = document.getElementById('sumQty');
const sumDesc = document.getElementById('sumDesc');
const sumTotal = document.getElementById('sumTotal');

function descuentoPorVolumen(q){
  if (q >= 100) return 0.20;
  if (q >= 50) return 0.15;
  if (q >= 25) return 0.10;
  if (q >= 10) return 0.05;
  return 0;
}

function formatearMXN(n){
  return '$' + n.toLocaleString('es-MX', {maximumFractionDigits:0});
}

function actualizarResumen(){
  const q = Math.max(1, Number(qCantidad.value) || 0);
  const desc = descuentoPorVolumen(q);
  const bruto = PRECIO_BASE * q;
  const total = bruto * (1 - desc);

  sumLinea.textContent = LINEAS[state.linea].nombre;
  sumUnit.textContent = formatearMXN(PRECIO_BASE);
  sumQty.textContent = q + (q === 1 ? ' pieza' : ' piezas');
  sumDesc.textContent = Math.round(desc * 100) + '%';
  sumTotal.textContent = formatearMXN(total);
}

function setLinea(linea){
  state.linea = linea;
  lineGroup.querySelectorAll('.toggle-opt').forEach(b => {
    b.classList.toggle('active', b.dataset.line === linea);
  });
  renderModelList();
  renderModelView();
  actualizarResumen();
}

lineGroup.querySelectorAll('.toggle-opt').forEach(btn => {
  btn.addEventListener('click', () => setLinea(btn.dataset.line));
});

qCantidad.addEventListener('input', actualizarResumen);

document.getElementById('sizeGrid').querySelectorAll('.size-chip').forEach(chip => {
  chip.addEventListener('click', () => chip.classList.toggle('active'));
});

document.getElementById('quoteForm').addEventListener('submit', e => e.preventDefault());

document.getElementById('quoteSubmit').addEventListener('click', () => {
  const nombre = document.getElementById('qNombre').value.trim();
  const email = document.getElementById('qEmail').value.trim();
  const confirmBox = document.getElementById('quoteConfirm');

  if (!nombre || !email) {
    confirmBox.style.display = 'block';
    confirmBox.style.borderColor = '#c0392b';
    confirmBox.style.color = '#e88';
    confirmBox.textContent = '⚠ Completa tu nombre y correo electrónico para enviar la solicitud.';
    return;
  }

  confirmBox.style.display = 'block';
  confirmBox.style.borderColor = 'var(--gold)';
  confirmBox.style.color = 'var(--gold-light)';
  confirmBox.textContent = `✓ Solicitud enviada. Te contactamos a ${email} con la cotización formal en menos de 24 h.`;

  setTimeout(() => { confirmBox.style.display = 'none'; }, 6000);
});

/* =========================================================
   PROMO BATA
   ========================================================= */
document.getElementById('promoBataBtn').addEventListener('click', () => {
  setLinea('bata');
  document.getElementById('cotizacion').scrollIntoView({behavior:'smooth'});
});

/* =========================================================
   MENU MOVIL
   ========================================================= */
const menuToggle = document.getElementById('menuToggle');
const mobileMenu = document.getElementById('mobileMenu');

menuToggle.addEventListener('click', () => {
  const open = mobileMenu.classList.toggle('open');
  menuToggle.setAttribute('aria-expanded', open);
  menuToggle.textContent = open ? '✕' : '☰';
});

mobileMenu.querySelectorAll('a').forEach(a => {
  a.addEventListener('click', () => {
    mobileMenu.classList.remove('open');
    menuToggle.setAttribute('aria-expanded', 'false');
    menuToggle.textContent = '☰';
  });
});

/* =========================================================
   SCROLL SPY
   ========================================================= */
const navLinks = document.querySelectorAll('#desktopNav a');
const secciones = ['inicio','nosotros','promo','modelos','fiscalias','cotizacion','contacto'];

const spy = new IntersectionObserver(entries => {
  entries.forEach(en => {
    if (en.isIntersecting) {
      navLinks.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + en.target.id));
    }
  });
}, { rootMargin: '-45% 0px -50% 0px' });

secciones.forEach(id => {
  const el = document.getElementById(id);
  if (el) spy.observe(el);
});

/* =========================================================
   CHAT FLOTANTE
   ========================================================= */
const chatToggle = document.getElementById('chat-toggle');
const chatPanel = document.getElementById('chat-panel');
const chatBody = document.getElementById('chat-body');
const chatInput = document.getElementById('chatInput');
const chatClose = document.getElementById('chatClose');

let chatIniciado = false;

function addMsg(text, who){
  const d = document.createElement('div');
  d.className = 'msg ' + who;
  d.textContent = text;
  chatBody.appendChild(d);
  chatBody.scrollTop = chatBody.scrollHeight;
}

function respuestaBot(texto){
  const t = texto.toLowerCase();

  if (t.includes('camisola')) {
    return 'La camisola industrial está a $199 por unidad en drill 250 g/m², manga larga o corta, con bordado en pecho incluido desde 25 piezas.';
  }
  if (t.includes('overol')) {
    return 'El overol reforzado está a $199 por unidad en gabardina 280 g/m², con rodillas y codos reforzados. Tallas S a 3XL.';
  }
  if (t.includes('bata') || t.includes('farmacia')) {
    return 'La bata de mostrador para farmacia está en promoción: antes $250, ahora $199. Tela antifluido, cierre oculto y bordado del nombre de tu farmacia.';
  }
  if (t.includes('mínimo') || t.includes('minimo') || t.includes('pedido')) {
    return 'El pedido mínimo es de 10 piezas en total. A partir de 25 piezas el bordado de logo va incluido y aplican descuentos por volumen.';
  }
  if (t.includes('precio') || t.includes('costo') || t.includes('cuánto') || t.includes('cuanto')) {
    return 'Todas nuestras líneas (camisola, overol y bata de mostrador) están a $199 por unidad. La bata tiene promo: antes $250.';
  }
  if (t.includes('descuento') || t.includes('volumen')) {
    return 'Descuentos por volumen: 10-24 pzas 5%, 25-49 pzas 10%, 50-99 pzas 15%, 100+ pzas 20%.';
  }
  if (t.includes('entrega') || t.includes('tiempo') || t.includes('tarda')) {
    return 'El tiempo de producción es de 15 a 25 días hábiles después de aprobar muestra y anticipo.';
  }
  if (t.includes('envío') || t.includes('envio') || t.includes('mandar')) {
    return 'Enviamos a toda la República. El costo de envío se cotiza según volumen y destino.';
  }
  if (t.includes('bordado') || t.includes('logo')) {
    return 'Digitalizamos tu logo sin costo y lo bordamos en pecho, espalda o manga. Incluido en pedidos de 25 piezas o más.';
  }
  if (t.includes('hola') || t.includes('buenas') || t.includes('buenos')) {
    return '¡Hola! Con gusto te ayudo. ¿Te interesa camisola, overol o la bata de farmacia en promo?';
  }
  if (t.includes('gracias')) {
    return 'Con gusto. Si quieres, llena la sección de Cotización y te enviamos la propuesta formal hoy mismo.';
  }
  return 'Gracias por tu mensaje. Para darte el precio exacto, ¿me indicas la línea de prenda (camisola, overol o bata), la cantidad y si llevas bordado?';
}

chatToggle.addEventListener('click', () => {
  chatPanel.classList.toggle('open');
  if (chatPanel.classList.contains('open') && !chatIniciado) {
    chatIniciado = true;
    addMsg('¡Hola! Soy el asistente de SHEL. Puedo darte precios de camisola, overol y bata de mostrador (promo $199). ¿Qué necesitas?', 'bot');
  }
});

chatClose.addEventListener('click', () => chatPanel.classList.remove('open'));

function enviarChat(texto){
  const val = (texto || chatInput.value).trim();
  if (!val) return;
  addMsg(val, 'user');
  chatInput.value = '';
  setTimeout(() => addMsg(respuestaBot(val), 'bot'), 420);
}

document.getElementById('chatSend').addEventListener('click', () => enviarChat());
chatInput.addEventListener('keydown', e => { if (e.key === 'Enter') enviarChat(); });

document.querySelectorAll('#chat-panel .chip').forEach(c => {
  c.addEventListener('click', () => enviarChat(c.dataset.q));
});

/* =========================================================
   CHAT DE FISCALÍAS
   ========================================================= */
const fiscBody = document.getElementById('fisc-chat-body');
const fiscInput = document.getElementById('fiscInput');

function addFisc(text, who){
  const d = document.createElement('div');
  d.className = 'fisc-msg ' + who;
  d.textContent = text;
  fiscBody.appendChild(d);
  fiscBody.scrollTop = fiscBody.scrollHeight;
}

function respuestaFisc(texto){
  const t = texto.toLowerCase();

  if (t.includes('mínimo') || t.includes('minimo')) {
    return 'Para fiscalías y dependencias el pedido mínimo es de 25 piezas por lote. Podemos mezclar tallas dentro del mismo lote.';
  }
  if (t.includes('document') || t.includes('licit') || t.includes('requisito')) {
    return 'Solicitamos: orden de compra o bases de licitación, especificaciones técnicas, ficha de tallas por persona y datos fiscales para CFDI.';
  }
  if (t.includes('entrega') || t.includes('tiempo')) {
    return 'Para 200 piezas el tiempo es de 25 a 30 días hábiles. Para 25 a 60 piezas, 15 a 20 días hábiles.';
  }
  if (t.includes('precio') || t.includes('costo')) {
    return 'El precio institucional es desde $199 por unidad, con descuento adicional según volumen y tipo de bordado (escudo, nombre y cargo).';
  }
  if (t.includes('pago') || t.includes('factura')) {
    return 'Facturamos con CFDI. Condiciones: 50% anticipo y 50% contra entrega para dependencias; 100% anticipo para empresas privadas.';
  }
  if (t.includes('bordado') || t.includes('escudo')) {
    return 'Bordamos escudo institucional, nombre y cargo. La digitalización del escudo es sin costo a partir de 50 piezas.';
  }
  if (t.includes('hola') || t.includes('buenas')) {
    return 'Buen día. Somos la mesa de licitaciones de SHEL. ¿Qué información necesita de la propuesta?';
  }
  return 'Gracias. Para preparar la propuesta formal necesito: dependencia, cantidad por talla y si llevan escudo, nombre o cargo bordado. ¿Me los comparte?';
}

function enviarFisc(texto){
  const val = (texto || fiscInput.value).trim();
  if (!val) return;
  addFisc(val, 'user');
  fiscInput.value = '';
  setTimeout(() => addFisc(respuestaFisc(val), 'bot'), 420);
}

document.getElementById('fiscSend').addEventListener('click', () => enviarFisc());
fiscInput.addEventListener('keydown', e => { if (e.key === 'Enter') enviarFisc(); });

document.querySelectorAll('.fisc-chip').forEach(c => {
  c.addEventListener('click', () => enviarFisc(c.dataset.q));
});

/* =========================================================
   INICIALIZACIÓN
   ========================================================= */
renderModelList();
renderModelView();
actualizarResumen();

addFisc('Bienvenido a la mesa de licitaciones de SHEL. Puedo ayudarle con pedidos institucionales para fiscalías: mínimos, documentación, tiempos y precios. ¿Qué necesita saber?', 'bot');

document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>