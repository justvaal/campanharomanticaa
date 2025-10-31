<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Grande Surpresa</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg1:#021b0e;
      --bg2:#000;
      --accent:#bdf7c2;
      --card: rgba(255,255,255,0.06);
    }
    html,body{height:100%;margin:0;font-family:"Raleway",system-ui;}
    body{
      background: linear-gradient(135deg,var(--bg1),var(--bg2));
      color: var(--accent);
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }
    .container{
      width:min(980px,96%);
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.25));
      border-radius:18px;
      box-shadow: 0 10px 40px rgba(0,0,0,0.6);
      overflow:hidden;
      display:grid;
      grid-template-columns: 1fr 420px;
      min-height:520px;
      position:relative;
      z-index:2;
    }
    .left{
      padding:48px;
      display:flex;
      flex-direction:column;
      justify-content:center;
      gap:18px;
    }
    .title{
      font-family:"Playfair Display",serif;
      font-size:44px;
      color:#e9ffe7;
      text-shadow:0 8px 30px rgba(0,0,0,0.7);
      margin:0;
    }
    .subtitle{margin:0;font-size:18px;color:#bfffc5;}
    .message{color:#d8ffd8;font-size:16px;line-height:1.6;max-width:44ch;}
    .hearts{display:flex;gap:8px;margin-top:14px;}
    .heart{width:36px;height:36px;border-radius:50%;display:grid;place-items:center;
      background:rgba(255,255,255,0.06);animation:float 3s ease-in-out infinite;}
    .heart:nth-child(2){animation-delay:0.2s}
    .heart:nth-child(3){animation-delay:0.4s}
    .heart svg{width:18px;height:18px;fill:#9effae}
    @keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-10px)}100%{transform:translateY(0)}}
    .right{padding:36px;display:flex;flex-direction:column;align-items:center;justify-content:center;background:rgba(0,0,0,0.25);}
    .card{background:var(--card);border-radius:14px;padding:22px;width:100%;max-width:360px;text-align:center;}
    .stage-label{font-size:14px;text-transform:uppercase;letter-spacing:1.6px;color:#bfffc5;margin-bottom:10px;font-weight:600;}
    .timer{display:flex;gap:10px;justify-content:center;}
    .segment{background:rgba(255,255,255,0.04);padding:12px 14px;border-radius:10px;min-width:72px;}
    .segment .num{font-size:28px;font-weight:700;color:#e9ffe7;}
    .segment .lbl{font-size:12px;color:#bfffc5;margin-top:6px;}
    .btn{
      background:linear-gradient(90deg,#1d8b45,#3de072);
      color:white;border:none;padding:10px 16px;border-radius:12px;
      font-weight:600;cursor:pointer;margin-top:12px;
      box-shadow:0 6px 18px rgba(61,224,114,0.18);
    }
    footer{text-align:center;padding:12px;color:#bfffc5;font-size:13px;}

    /* Tela final */
    .final{
      position:fixed;
      inset:0;
      background: radial-gradient(circle at center, #042612 0%, #000 100%);
      display:flex;
      align-items:center;
      justify-content:center;
      flex-direction:column;
      opacity:0;
      transition:opacity 2s ease-in;
      z-index:10;
      text-align:center;
    }
    .final.show{opacity:1;}
    .final p{
      font-family:"Playfair Display",serif;
      font-size:32px;
      color:#bdf7c2;
      max-width:520px;
      line-height:1.6;
      white-space:pre-wrap;
      overflow:hidden;
      border-right:3px solid #bdf7c2;
      animation:typing 4s steps(40,end), blink 0.7s step-end infinite alternate;
    }
    @keyframes typing{
      from{width:0;}
      to{width:100%;}
    }
    @keyframes blink{
      50%{border-color:transparent;}
    }

    @media(max-width:900px){.container{grid-template-columns:1fr}.title{font-size:36px}}
  </style>
</head>
<body>
  <div class="container" id="mainContainer">
    <div class="left">
      <h1 class="title">Grande Surpresa</h1>
      <p class="subtitle">Um momento preparado com todo carinho 💚</p>
      <p class="message">O tempo está correndo... e algo muito especial está prestes a acontecer.  
      Acompanhe cada segundo até o grande dia chegar.</p>
      <div class="hearts">
        <div class="heart"><svg viewBox="0 0 32 29"><path d="M23.6 0c-2.6 0-4.9 1.3-6.1 3.3C15.3 1.3 13 0 10.4 0 4.6 0 0 4.6 0 10.4c0 6 5.6 10.6 13.8 17.7l2.2 1.8c.6.5 1.5.5 2.1 0l2.2-1.8C26.4 21 32 16.4 32 10.4 32 4.6 27.4 0 21.6 0z"/></svg></div>
        <div class="heart"><svg viewBox="0 0 32 29"><path d="M23.6 0c-2.6 0-4.9 1.3-6.1 3.3C15.3 1.3 13 0 10.4 0 4.6 0 0 4.6 0 10.4c0 6 5.6 10.6 13.8 17.7l2.2 1.8c.6.5 1.5.5 2.1 0l2.2-1.8C26.4 21 32 16.4 32 10.4 32 4.6 27.4 0 21.6 0z"/></svg></div>
        <div class="heart"><svg viewBox="0 0 32 29"><path d="M23.6 0c-2.6 0-4.9 1.3-6.1 3.3C15.3 1.3 13 0 10.4 0 4.6 0 0 4.6 0 10.4c0 6 5.6 10.6 13.8 17.7l2.2 1.8c.6.5 1.5.5 2.1 0l2.2-1.8C26.4 21 32 16.4 32 10.4 32 4.6 27.4 0 21.6 0z"/></svg></div>
      </div>
    </div>
    <div class="right">
      <div class="card">
        <div class="stage-label" id="stageLabel">Contagem</div>
        <div class="timer">
          <div class="segment"><div class="num" id="days">--</div><div class="lbl">Dias</div></div>
          <div class="segment"><div class="num" id="hours">--</div><div class="lbl">Horas</div></div>
          <div class="segment"><div class="num" id="minutes">--</div><div class="lbl">Min</div></div>
          <div class="segment"><div class="num" id="seconds">--</div><div class="lbl">Seg</div></div>
        </div>
        <button class="btn" id="shareBtn">Copiar link da surpresa</button>
        <p style="font-size:13px;margin-top:10px;">25/10/2025 → 07/11/2025</p>
      </div>
    </div>
  </div>

  <div class="final" id="finalScreen">
    <p>Você é o único que eu quero diante do sol escaldante.</p>
  </div>

  <footer>Alguns segredos são lindos demais para serem apressados 💫</footer>

  <script>
    const startDate = new Date("2025-10-25T00:00:00-03:00");
    const endDate   = new Date("2025-11-07T00:00:00-03:00");

    const stageLabel = document.getElementById('stageLabel');
    const daysEl = document.getElementById('days');
    const hoursEl = document.getElementById('hours');
    const minsEl = document.getElementById('minutes');
    const secsEl = document.getElementById('seconds');
    const finalScreen = document.getElementById('finalScreen');
    const mainContainer = document.getElementById('mainContainer');

    function pad(n){return String(n).padStart(2,'0');}
    function msToParts(ms){
      const t=Math.max(0,Math.floor(ms/1000));
      const d=Math.floor(t/86400);
      const h=Math.floor((t%86400)/3600);
      const m=Math.floor((t%3600)/60);
      const s=t%60;
      return {d,h,m,s};
    }
    function update(){
      const now=new Date();
      if(now<startDate){
        const diff=startDate-now;
        const {d,h,m,s}=msToParts(diff);
        stageLabel.textContent="Começa em";
        daysEl.textContent=pad(d);hoursEl.textContent=pad(h);minsEl.textContent=pad(m);secsEl.textContent=pad(s);
      }else if(now>=startDate && now<endDate){
        const diff=endDate-now;
        const {d,h,m,s}=msToParts(diff);
        stageLabel.textContent="Grande Surpresa — tempo restante";
        daysEl.textContent=pad(d);hoursEl.textContent=pad(h);minsEl.textContent=pad(m);secsEl.textContent=pad(s);
      }else{
        clearInterval(interval);
        mainContainer.style.display="none";
        finalScreen.classList.add("show");
      }
    }
    update();
    const interval=setInterval(update,1000);

    document.getElementById('shareBtn').addEventListener('click',async()=>{
      const text=location.href;
      try{
        await navigator.clipboard.writeText(text);
        document.getElementById('shareBtn').textContent="Link copiado!";
        setTimeout(()=>document.getElementById('shareBtn').textContent="Copiar link da surpresa",2000);
      }catch{alert("Copie manualmente: "+text);}
    });
  </script>
</body>
</html>
