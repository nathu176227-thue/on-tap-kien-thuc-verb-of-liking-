<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ôn Tập: Cấu Trúc Diễn Đạt Sở Thích</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,500;0,700;1,600&family=Quicksand:wght@400;500;600;700&family=Caveat:wght@500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#f2f9ee; --bg2:#e6f4e0; --primary:#3f9d5f; --primary-dark:#276b3f; --primary-light:#c9ecc4;
    --accent:#ffc94a; --accent2:#ff8a5c; --card:#ffffff; --text:#1f4030; --muted:#6d8c78;
    --correct:#2e9e52; --correct-bg:#e3f7e6; --wrong:#e0523f; --wrong-bg:#fdeae7;
    --level1:#7fc7e0; --level2:#ffc94a; --level3:#ff8a5c;
    --shadow:0 8px 24px rgba(39,107,63,0.12); --radius:18px;
  }
  *{box-sizing:border-box;}
  body{margin:0; font-family:'Quicksand',sans-serif; background:radial-gradient(circle at 10% 10%, var(--bg2), transparent 40%),radial-gradient(circle at 90% 20%, var(--primary-light), transparent 45%), var(--bg); color:var(--text); min-height:100vh; position:relative; overflow-x:hidden; padding-bottom:60px;}
  h1,h2,h3{font-family:'Fraunces',serif;}
  .float-deco{position:fixed; opacity:0.16; z-index:0; pointer-events:none; animation:floaty 7s ease-in-out infinite;}
  @keyframes floaty{0%,100%{transform:translateY(0px) rotate(0deg);} 50%{transform:translateY(-18px) rotate(8deg);}}
  .deco1{top:6%; left:3%; width:65px;} .deco2{top:62%; left:2%; width:55px; animation-delay:1.5s;}
  .deco3{top:14%; right:4%; width:75px; animation-delay:0.8s;} .deco4{top:76%; right:6%; width:60px; animation-delay:2.2s;}
  .deco5{top:42%; left:47%; width:48px; animation-delay:3s;}

  .wrap{max-width:920px; margin:0 auto; padding:28px 18px; position:relative; z-index:1;}
  header.hero{text-align:center; background:linear-gradient(135deg, var(--primary) 0%, #63b57e 100%); color:#fff; border-radius:24px; padding:36px 24px; box-shadow:var(--shadow);}
  header.hero h1{font-size:2rem; margin:0 0 8px; font-weight:700;}
  header.hero p{margin:4px 0; opacity:0.95; font-size:0.98rem;}
  .badge-row{display:flex; gap:10px; justify-content:center; flex-wrap:wrap; margin-top:16px;}
  .badge{background:rgba(255,255,255,0.18); border:1px solid rgba(255,255,255,0.5); padding:6px 14px; border-radius:999px; font-size:0.82rem;}

  .info-toggle{display:block; margin:22px auto 0; background:#fff; color:var(--primary-dark); border:2px solid var(--primary-light); border-radius:14px; padding:14px 18px; cursor:pointer; font-family:'Quicksand'; font-weight:600; box-shadow:var(--shadow); width:100%; text-align:left; font-size:0.95rem;}
  .info-panel{display:none; background:#fff; border-radius:14px; padding:18px 20px; margin-top:8px; box-shadow:var(--shadow); font-size:0.88rem; line-height:1.7;}
  .info-panel.show{display:block;}
  .ref-table{width:100%; border-collapse:collapse; margin:10px 0; font-size:0.85rem;}
  .ref-table th, .ref-table td{border:1px solid #dcefd6; padding:6px 10px; text-align:left;}
  .ref-table th{background:var(--bg2); color:var(--primary-dark);}
  .ref-scale{display:flex; flex-wrap:wrap; gap:6px; margin:10px 0; align-items:center;}
  .scale-item{background:var(--bg2); padding:5px 10px; border-radius:8px; font-size:0.8rem; font-weight:600;}
  .scale-arrow{color:var(--muted);}

  .progress-bar-outer{background:#dcefd6; border-radius:999px; height:14px; overflow:hidden; margin-top:16px;}
  .progress-bar-inner{background:linear-gradient(90deg, var(--accent), var(--primary)); height:100%; width:0%; transition:width .4s ease;}

  section.block{background:var(--card); border-radius:var(--radius); padding:24px 22px; margin-top:26px; box-shadow:var(--shadow); border:1px solid #eaf5e6; border-top:6px solid var(--level1);}
  section.block.lvl2{border-top-color:var(--level2);}
  section.block.lvl3{border-top-color:var(--level3);}
  .block-head{display:flex; align-items:flex-start; gap:12px; margin-bottom:6px;}
  .block-icon{font-size:1.6rem;}
  .block-title{font-size:1.25rem; color:var(--primary-dark); margin:0;}
  .level-tag{display:inline-block; font-size:0.72rem; font-weight:700; padding:3px 10px; border-radius:999px; background:var(--level1); color:#053345; margin-bottom:8px;}
  .lvl2 .level-tag{background:var(--level2); color:#5a3d00;}
  .lvl3 .level-tag{background:var(--level3); color:#5a1e00;}
  .citation{font-family:'Caveat',cursive; color:var(--accent2); font-size:1.1rem; margin:0 0 14px;}
  .subtext{color:var(--muted); font-size:0.88rem; margin-bottom:16px;}

  .q{margin-bottom:16px; padding:14px 16px; border-radius:14px; background:#fbfdfa; border:1px solid #eef5ec;}
  .q-text{font-weight:600; margin-bottom:10px; font-size:0.96rem;}
  .options{display:flex; flex-direction:column; gap:8px;}
  .opt{background:#fff; border:2px solid var(--bg2); border-radius:10px; padding:9px 12px; cursor:pointer; font-size:0.9rem; transition:all .15s ease;}
  .opt:hover{border-color:var(--primary-light);}
  .opt.selected{border-color:var(--primary); background:var(--primary-light);}
  .opt.correct{border-color:var(--correct); background:var(--correct-bg); color:var(--correct); font-weight:700;}
  .opt.wrong{border-color:var(--wrong); background:var(--wrong-bg); color:var(--wrong);}
  .opt.disabled{pointer-events:none;}
  .tf-btns{display:flex; gap:10px;}
  .tf-btn{flex:1; padding:10px; border-radius:10px; border:2px solid var(--bg2); background:#fff; cursor:pointer; font-weight:700; font-size:0.88rem;}
  input.text-answer{padding:8px 10px; border-radius:10px; border:2px solid var(--bg2); font-family:'Quicksand'; font-size:0.92rem; width:150px;}
  input.text-answer:focus{outline:none; border-color:var(--primary);}
  .feedback-line{margin-top:8px; font-size:0.85rem; font-weight:600;}
  .feedback-line.ok{color:var(--correct);} .feedback-line.bad{color:var(--wrong);}
  .attempts-left{font-size:0.78rem; color:var(--muted); margin-top:4px;}
  .btn{background:var(--primary); color:#fff; border:none; padding:11px 22px; border-radius:12px; font-weight:700; cursor:pointer; font-family:'Quicksand'; font-size:0.94rem; box-shadow:0 4px 12px rgba(63,157,95,0.3);}
  .btn.small{padding:6px 14px; font-size:0.8rem; box-shadow:none;}
  .btn.retry{background:var(--accent2);}
  .btn.ghost{background:transparent; color:var(--primary-dark); border:2px solid var(--primary-light); box-shadow:none;}
  .btn:disabled{opacity:0.5; cursor:not-allowed;}
  .section-score{margin-top:14px; font-weight:700; color:var(--primary-dark);}
  .final-panel{background:linear-gradient(135deg, var(--accent) 0%, var(--accent2) 100%); border-radius:20px; padding:28px; margin-top:30px; text-align:center; color:#4a2600; box-shadow:var(--shadow); display:none;}
  .final-panel.show{display:block;}
  .final-score{font-size:2.4rem; font-weight:700; margin:10px 0;}
  .final-msg{font-family:'Caveat',cursive; font-size:1.3rem;}
  .history-panel{margin-top:16px; background:#fff; border-radius:14px; padding:16px; box-shadow:var(--shadow); font-size:0.85rem;}
  .history-panel h4{margin:0 0 8px; color:var(--primary-dark);}
  .history-row{display:flex; justify-content:space-between; padding:4px 0; border-bottom:1px solid #eef5ec;}
  footer.refs{margin-top:36px; background:#eef7ea; border-radius:16px; padding:20px 22px; font-size:0.82rem; color:var(--muted); line-height:1.7;}
  footer.refs h4{color:var(--primary-dark); margin:0 0 8px;}
</style>
</head>
<body>

<svg class="float-deco deco1" viewBox="0 0 64 64" fill="none"><circle cx="32" cy="32" r="26" fill="#ffffff" stroke="#3f9d5f" stroke-width="3"/><path d="M32 6 L32 58 M6 32 L58 32" stroke="#3f9d5f" stroke-width="2"/></svg>
<svg class="float-deco deco2" viewBox="0 0 64 64" fill="none"><path d="M32 4 L40 24 L60 24 L44 38 L50 58 L32 46 L14 58 L20 38 L4 24 L24 24 Z" fill="#ffc94a" stroke="#e0a53a" stroke-width="2"/></svg>
<svg class="float-deco deco3" viewBox="0 0 64 64" fill="none"><rect x="26" y="4" width="12" height="40" rx="6" fill="#e8dcc8" stroke="#a9895a" stroke-width="2"/><ellipse cx="32" cy="50" rx="16" ry="10" fill="#ff8a5c" stroke="#c9612f" stroke-width="2"/></svg>
<svg class="float-deco deco4" viewBox="0 0 64 64" fill="none"><polygon points="32,4 48,32 32,60 16,32" fill="#7fc7e0" stroke="#4c9db8" stroke-width="2"/></svg>
<svg class="float-deco deco5" viewBox="0 0 64 64" fill="none"><circle cx="32" cy="32" r="24" fill="#ffffff" stroke="#ff8a5c" stroke-width="3"/><path d="M20 20 L44 44 M44 20 L20 44" stroke="#ff8a5c" stroke-width="2"/></svg>

<div class="wrap">
  <header class="hero">
    <h1>💚 Ôn Tập: Cấu Trúc Diễn Đạt Sở Thích 💚</h1>
    <p>Verbs &amp; Structures of Liking</p>
    <p>3 mức độ tư duy &middot; 30 câu hỏi &middot; Chấm điểm tự động</p>
    <div class="badge-row">
      <span class="badge">Nhận biết</span>
      <span class="badge">Áp dụng</span>
      <span class="badge">Vận dụng cao</span>
    </div>
  </header>

  <button class="info-toggle" id="infoToggle">📖 Xem lại bảng tóm tắt kiến thức trước khi làm bài (bấm để mở)</button>
  <div class="info-panel" id="infoPanel">
    <p><strong>1. Thang mức độ thích/ghét (Verbs of liking):</strong></p>
    <div class="ref-scale">
      <span class="scale-item">Adore</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Love</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Like/Enjoy/Fancy</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Don't mind</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Dislike</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Hate</span><span class="scale-arrow">&gt;</span>
      <span class="scale-item">Detest</span>
    </div>
    <p><strong>2. Nhóm động từ CHỈ theo sau bởi V-ing:</strong> adore, enjoy, fancy, don't mind, detest</p>
    <table class="ref-table">
      <tr><th>Động từ</th><th>Ví dụ</th></tr>
      <tr><td>Adore</td><td>My sister adores dancing.</td></tr>
      <tr><td>Enjoy</td><td>Do you enjoy listening to music?</td></tr>
      <tr><td>Fancy</td><td>She fancies doing the gardening.</td></tr>
      <tr><td>Don't mind</td><td>I don't mind cleaning.</td></tr>
      <tr><td>Detest</td><td>I detest staying at home alone.</td></tr>
    </table>
    <p><strong>3. Nhóm động từ theo sau bởi CẢ V-ing và to-V:</strong> like, love, hate, prefer</p>
    <table class="ref-table">
      <tr><th>Động từ</th><th>Ví dụ</th></tr>
      <tr><td>Like</td><td>He likes reading / to read books.</td></tr>
      <tr><td>Love</td><td>I love walking / to walk to school.</td></tr>
      <tr><td>Hate</td><td>I hate eating / to eat out.</td></tr>
      <tr><td>Prefer</td><td>I prefer going / to go to the cinema.</td></tr>
    </table>
    <p><strong>4. Cấu trúc khác diễn đạt sở thích (thay vì lặp lại I like/I love):</strong></p>
    <table class="ref-table">
      <tr><th>Cấu trúc</th><th>Nghĩa</th><th>Ví dụ</th></tr>
      <tr><td>be quite into + Ving/N</td><td>khá thích</td><td>I am quite into playing football.</td></tr>
      <tr><td>be a big fan of + Ving/N</td><td>là fan cuồng của</td><td>I am a big fan of horror movies.</td></tr>
      <tr><td>be interested in + Ving</td><td>quan tâm, yêu thích</td><td>I am interested in taking photos.</td></tr>
      <tr><td>be addicted to + Ving</td><td>nghiện, say mê</td><td>He is addicted to playing games.</td></tr>
      <tr><td>be hooked on + Ving/N</td><td>bị mê hoặc bởi</td><td>She is hooked on going shopping.</td></tr>
      <tr><td>be keen on + Ving/N</td><td>say mê, yêu thích</td><td>She is keen on doing DIY.</td></tr>
    </table>
  </div>

  <div class="progress-bar-outer"><div class="progress-bar-inner" id="overallProgress"></div></div>
  <p style="text-align:center; font-size:0.82rem; color:var(--muted); margin-top:6px;" id="overallProgressLabel">Đã hoàn thành 0/3 phần</p>

  <!-- PHẦN 1: NHẬN BIẾT -->
  <section class="block" id="section1">
    <span class="level-tag">MỨC 1 - NHẬN BIẾT</span>
    <div class="block-head"><span class="block-icon">🔍</span><h2 class="block-title">Phần 1 - Nhận diện kiến thức</h2></div>
    <p class="citation">Dựa trên Thang tư duy Bloom sửa đổi (Anderson &amp; Krathwohl, 2001)</p>
    <p class="subtext">Nhận diện nghĩa, mức độ, và cấu trúc ngữ pháp của các động từ/cụm từ chỉ sở thích.</p>
    <div id="lvl1Container"></div>
    <button class="btn" id="checkLvl1">Kiểm tra Phần 1</button>
    <p class="section-score" id="lvl1Score"></p>
  </section>

  <!-- PHẦN 2: ÁP DỤNG -->
  <section class="block lvl2" id="section2">
    <span class="level-tag">MỨC 2 - ÁP DỤNG</span>
    <div class="block-head"><span class="block-icon">✏️</span><h2 class="block-title">Phần 2 - Vận dụng vào câu</h2></div>
    <p class="citation">"Test-Enhanced Learning" - Roediger &amp; Karpicke (2006)</p>
    <p class="subtext">Điền đúng dạng động từ hoặc giới từ phù hợp vào chỗ trống.</p>
    <div id="lvl2Container"></div>
    <button class="btn" id="checkLvl2">Kiểm tra Phần 2</button>
    <p class="section-score" id="lvl2Score"></p>
  </section>

  <!-- PHẦN 3: VẬN DỤNG CAO -->
  <section class="block lvl3" id="section3">
    <span class="level-tag">MỨC 3 - VẬN DỤNG CAO</span>
    <div class="block-head"><span class="block-icon">🧠</span><h2 class="block-title">Phần 3 - Phân tích &amp; Vận dụng linh hoạt</h2></div>
    <p class="citation">Phân tích - Đánh giá - Sáng tạo (Anderson &amp; Krathwohl, 2001)</p>
    <p class="subtext">Diễn đạt lại câu, phát hiện lỗi sai, và chọn cách diễn đạt tự nhiên nhất theo ngữ cảnh.</p>
    <div id="lvl3Container"></div>
    <button class="btn" id="checkLvl3">Kiểm tra Phần 3</button>
    <p class="section-score" id="lvl3Score"></p>
  </section>

  <div class="final-panel" id="finalPanel">
    <h2>🏆 Kết quả tổng kết</h2>
    <div class="final-score" id="finalScoreText">0 / 30</div>
    <p class="final-msg" id="finalMsg"></p>
    <button class="btn ghost" id="resetAllBtn">Làm lại toàn bộ bài ôn tập</button>
  </div>

  <div class="history-panel">
    <h4>📊 Lịch sử làm bài (lưu trên máy này)</h4>
    <div id="historyList"><p style="color:var(--muted);">Chưa có lần làm bài nào.</p></div>
  </div>

  <footer class="refs">
    <h4>Tài liệu tham khảo</h4>
    Anderson, L. W., &amp; Krathwohl, D. R. (2001). <em>A Taxonomy for Learning, Teaching, and Assessing: A Revision of Bloom's Taxonomy of Educational Objectives</em>. Longman.<br>
    Roediger, H. L., &amp; Karpicke, J. D. (2006). Test-enhanced learning. <em>Psychological Science, 17</em>(3), 249-255.<br>
    Craik, F. I. M., &amp; Lockhart, R. S. (1972). Levels of processing. <em>Journal of Verbal Learning, 11</em>(6), 671-684.
  </footer>
</div>

<script>
document.addEventListener('DOMContentLoaded', function(){

  document.getElementById('infoToggle').addEventListener('click', function(){
    document.getElementById('infoPanel').classList.toggle('show');
  });

  function normalize(str){ return str.trim().toLowerCase().replace(/\s+/g,' '); }

  // ================= DATA =================

  // ---- LEVEL 1: NHẬN BIẾT (MCQ + True/False) ----
  const lvl1Items = [
    {type:'mcq', q:"Trong các động từ sau, động từ nào thể hiện mức độ THÍCH mạnh nhất?", options:["Adore","Like","Don't mind","Dislike"], correct:0},
    {type:'mcq', q:"\"Detest\" có nghĩa gần nhất với:", options:["Thích","Không phiền","Ghét cay ghét đắng","Yêu"], correct:2},
    {type:'tf', q:"\"Don't mind\" thể hiện một cảm xúc YÊU THÍCH mạnh mẽ.", isTrue:false},
    {type:'mcq', q:"Động từ nào sau đây CHỈ được theo sau bởi V-ing (không dùng to-V)?", options:["Like","Love","Enjoy","Prefer"], correct:2},
    {type:'mcq', q:"Cấu trúc \"to be hooked on\" gần nghĩa nhất với:", options:["Bị mê hoặc, làm rất thường xuyên","Không thích chút nào","Chỉ thử một lần","Ghét bỏ hoàn toàn"], correct:0},
    {type:'mcq', q:"Động từ nào có thể theo sau bởi CẢ V-ing và to-V?", options:["Enjoy","Detest","Prefer","Adore"], correct:2},
    {type:'tf', q:"\"Fancy\" chỉ được dùng để nói về sở thích ăn uống.", isTrue:false},
    {type:'mcq', q:"Cấu trúc nào diễn tả mức độ NGHIỆN, SAY MÊ điều gì đó nhất?", options:["to be addicted to","to be interested in","don't mind","dislike"], correct:0},
    {type:'tf', q:"\"To be interested in\" thường theo sau bởi V-ing.", isTrue:true},
    {type:'mcq', q:"Theo thang mức độ, từ nào đứng GIỮA \"Like\" và \"Hate\"?", options:["Adore","Dislike/don't like","Detest","Love"], correct:1}
  ];

  // ---- LEVEL 2: ÁP DỤNG (fill blank) ----
  const lvl2Items = [
    {q:"My sister adores ___. (dance)", answers:["dancing"]},
    {q:"Do you enjoy ___ to music? (listen)", answers:["listening"]},
    {q:"She fancies ___ the garden. (do)", answers:["doing"]},
    {q:"I don't mind ___. (clean)", answers:["cleaning"]},
    {q:"I detest ___ at home alone. (stay)", answers:["staying"]},
    {q:"I am quite ___ playing football. (giới từ)", answers:["into"]},
    {q:"She is a big fan ___ horror movies. (giới từ)", answers:["of"]},
    {q:"I am interested ___ taking photos. (giới từ)", answers:["in"]},
    {q:"He is addicted ___ playing computer games. (giới từ)", answers:["to"]},
    {q:"She is keen ___ doing DIY. (giới từ)", answers:["on"]}
  ];

  // ---- LEVEL 3: VẬN DỤNG CAO (MCQ - paraphrase / error / context) ----
  const lvl3Items = [
    {q:"Chọn câu có nghĩa GẦN NHẤT với: \"My sister adores dancing.\"", options:["My sister is a big fan of dancing.","My sister doesn't mind dancing.","My sister detests dancing.","My sister is interested in reading."], correct:0},
    {q:"Chọn câu có nghĩa GẦN NHẤT với: \"He is addicted to playing computer games.\"", options:["He doesn't mind playing computer games occasionally.","He plays computer games all the time and can't stop.","He dislikes playing computer games.","He is a bit bored of computer games."], correct:1},
    {q:"Chọn câu có nghĩa GẦN NHẤT với: \"I don't mind cleaning.\"", options:["I absolutely hate cleaning.","I am a big fan of cleaning.","Cleaning is not a problem for me.","I refuse to clean."], correct:2},
    {q:"Chọn câu có nghĩa GẦN NHẤT với: \"She is hooked on shopping.\"", options:["She goes shopping sometimes but doesn't care much.","She dislikes shopping.","She is captivated by shopping and does it almost every day.","She has never been shopping."], correct:2},
    {q:"Câu nào sau đây có LỖI SAI về ngữ pháp?", options:["She enjoys swimming in the lake.","He detests to wait in long queues.","They love reading comics together.","I prefer walking to driving."], correct:1},
    {q:"Câu nào sau đây có LỖI SAI về ngữ pháp?", options:["My mother is keen on gardening.","He is interested in play the piano.","We are addicted to watching series.","She fancies trying new food."], correct:1},
    {q:"Câu nào sau đây có LỖI SAI về ngữ pháp?", options:["I don't mind to help you.","They adore travelling around the world.","He hates eating spicy food.","She is a big fan of K-pop music."], correct:0},
    {q:"Bạn muốn nói mình cực kỳ nghiện chơi game, chơi suốt ngày. Câu nào phù hợp nhất?", options:["I don't mind playing games.","I am addicted to playing games.","I dislike playing games.","I don't like playing games."], correct:1},
    {q:"Bạn muốn diễn đạt lịch sự rằng mình không phản đối làm bài tập (dù không hào hứng lắm). Câu nào phù hợp nhất?", options:["I adore doing homework.","I detest doing homework.","I don't mind doing homework.","I am hooked on doing homework."], correct:2},
    {q:"Bạn muốn nói mình rất quan tâm và thích tìm hiểu nhiếp ảnh. Câu nào tự nhiên nhất?", options:["I am interested in taking photos.","I hate taking photos.","I don't mind taking photos.","I detest taking photos."], correct:0}
  ];

  const sectionDone = {1:false,2:false,3:false};
  const scores = {1:{score:0,total:lvl1Items.length}, 2:{score:0,total:lvl2Items.length}, 3:{score:0,total:lvl3Items.length}};

  function updateOverallProgress(){
    const doneCount = Object.values(sectionDone).filter(Boolean).length;
    document.getElementById('overallProgress').style.width = (doneCount/3*100)+'%';
    document.getElementById('overallProgressLabel').textContent = 'Đã hoàn thành ' + doneCount + '/3 phần';
    if(doneCount === 3){ showFinal(); }
  }

  // ================= RENDER LEVEL 1 =================
  const lvl1Container = document.getElementById('lvl1Container');
  lvl1Items.forEach((item, idx) => {
    const qDiv = document.createElement('div');
    qDiv.className = 'q';
    qDiv.dataset.idx = idx;
    if(item.type === 'mcq'){
      let optsHtml = '<div class="options">';
      item.options.forEach((opt, oIdx) => { optsHtml += '<div class="opt" data-idx="'+idx+'" data-opt="'+oIdx+'">' + opt + '</div>'; });
      optsHtml += '</div>';
      qDiv.innerHTML = '<div class="q-text">' + (idx+1) + '. ' + item.q + '</div>' + optsHtml + '<p class="attempts-left" data-idx="'+idx+'">Còn 3 lần thử</p>';
    } else {
      qDiv.innerHTML = '<div class="q-text">' + (idx+1) + '. ' + item.q + '</div>' +
        '<div class="tf-btns"><button class="tf-btn" data-idx="'+idx+'" data-choice="true">Đúng</button><button class="tf-btn" data-idx="'+idx+'" data-choice="false">Sai</button></div>' +
        '<p class="attempts-left" data-idx="'+idx+'">Còn 3 lần thử</p>';
    }
    lvl1Container.appendChild(qDiv);
  });
  const lvl1Attempts = lvl1Items.map(()=>3);
  const lvl1Correct = lvl1Items.map(()=>false);

  function checkLvl1Mcq(idx, chosenOpt){
    if(lvl1Correct[idx]) return;
    const qDiv = lvl1Container.querySelector('.q[data-idx="'+idx+'"]');
    const opts = qDiv.querySelectorAll('.opt');
    const attemptsLabel = qDiv.querySelector('.attempts-left[data-idx="'+idx+'"]');
    if(chosenOpt === lvl1Items[idx].correct){
      opts[chosenOpt].classList.add('correct');
      opts.forEach(o=>o.classList.add('disabled'));
      lvl1Correct[idx] = true; scores[1].score++;
      attemptsLabel.textContent = '✓ Chính xác!';
    } else {
      lvl1Attempts[idx]--;
      opts[chosenOpt].classList.add('wrong');
      setTimeout(()=>opts[chosenOpt].classList.remove('wrong'),500);
      if(lvl1Attempts[idx] <= 0){
        opts[lvl1Items[idx].correct].classList.add('correct');
        opts.forEach(o=>o.classList.add('disabled'));
        attemptsLabel.textContent = 'Đã hết lượt. Đáp án đúng đã hiện màu xanh.';
      } else { attemptsLabel.textContent = 'Còn ' + lvl1Attempts[idx] + ' lần thử'; }
    }
  }
  function checkLvl1Tf(idx, chosenBool){
    if(lvl1Correct[idx]) return;
    const qDiv = lvl1Container.querySelector('.q[data-idx="'+idx+'"]');
    const btns = qDiv.querySelectorAll('.tf-btn');
    const attemptsLabel = qDiv.querySelector('.attempts-left[data-idx="'+idx+'"]');
    const clickedBtn = qDiv.querySelector('.tf-btn[data-choice="'+chosenBool+'"]');
    if(chosenBool === lvl1Items[idx].isTrue){
      clickedBtn.style.background='var(--correct-bg)'; clickedBtn.style.borderColor='var(--correct)';
      btns.forEach(b=>b.disabled=true);
      lvl1Correct[idx] = true; scores[1].score++;
      attemptsLabel.textContent = '✓ Chính xác!';
    } else {
      lvl1Attempts[idx]--;
      clickedBtn.style.background='var(--wrong-bg)'; clickedBtn.style.borderColor='var(--wrong)';
      if(lvl1Attempts[idx] <= 0){
        const rightBtn = qDiv.querySelector('.tf-btn[data-choice="'+lvl1Items[idx].isTrue+'"]');
        rightBtn.style.background='var(--correct-bg)'; rightBtn.style.borderColor='var(--correct)';
        btns.forEach(b=>b.disabled=true);
        attemptsLabel.textContent = 'Đã hết lượt. Đáp án đúng đã hiện màu xanh.';
      } else { attemptsLabel.textContent = 'Còn ' + lvl1Attempts[idx] + ' lần thử'; }
    }
  }

  lvl1Container.addEventListener('click', function(e){
    const opt = e.target.closest('.opt');
    if(opt && !opt.classList.contains('disabled')){
      const idx = parseInt(opt.dataset.idx);
      if(lvl1Attempts[idx] > 0 && !lvl1Correct[idx]) checkLvl1Mcq(idx, parseInt(opt.dataset.opt));
      return;
    }
    const tfBtn = e.target.closest('.tf-btn');
    if(tfBtn && !tfBtn.disabled){
      const idx = parseInt(tfBtn.dataset.idx);
      if(lvl1Attempts[idx] > 0 && !lvl1Correct[idx]) checkLvl1Tf(idx, tfBtn.dataset.choice === 'true');
    }
  });

  document.getElementById('checkLvl1').addEventListener('click', function(){
    document.getElementById('lvl1Score').textContent = 'Điểm Phần 1: ' + scores[1].score + '/' + scores[1].total;
    const allDone = lvl1Items.every((item,idx)=> lvl1Correct[idx] || lvl1Attempts[idx] <= 0);
    if(allDone){ sectionDone[1] = true; updateOverallProgress(); }
    else { alert('Em hãy trả lời tất cả các câu trước khi kiểm tra nhé!'); }
  });

  // ================= RENDER LEVEL 2 =================
  const lvl2Container = document.getElementById('lvl2Container');
  lvl2Items.forEach((item, idx) => {
    const qDiv = document.createElement('div');
    qDiv.className = 'q';
    qDiv.dataset.idx = idx;
    qDiv.innerHTML = '<div class="q-text">' + (idx+1) + '. ' + item.q.replace('___','<input type="text" class="text-answer" data-idx="'+idx+'">') + '</div>' +
      '<div class="feedback-line" data-idx="'+idx+'"></div><p class="attempts-left" data-idx="'+idx+'">Còn 3 lần thử</p>';
    lvl2Container.appendChild(qDiv);
  });
  const lvl2Attempts = lvl2Items.map(()=>3);
  const lvl2Correct = lvl2Items.map(()=>false);

  function checkLvl2Question(idx){
    if(lvl2Correct[idx]) return;
    const input = lvl2Container.querySelector('input[data-idx="'+idx+'"]');
    const feedback = lvl2Container.querySelector('.feedback-line[data-idx="'+idx+'"]');
    const attemptsLabel = lvl2Container.querySelector('.attempts-left[data-idx="'+idx+'"]');
    const userVal = normalize(input.value);
    const correctAnswers = lvl2Items[idx].answers.map(a=>normalize(a));
    if(correctAnswers.includes(userVal)){
      feedback.textContent = '✓ Chính xác!'; feedback.className='feedback-line ok';
      input.disabled = true; lvl2Correct[idx] = true; attemptsLabel.textContent=''; scores[2].score++;
    } else {
      lvl2Attempts[idx]--;
      if(lvl2Attempts[idx] <= 0){
        feedback.textContent = '✗ Đáp án đúng: ' + lvl2Items[idx].answers[0];
        feedback.className='feedback-line bad'; input.disabled = true; attemptsLabel.textContent='';
      } else {
        feedback.textContent = '✗ Chưa đúng, thử lại nhé.'; feedback.className='feedback-line bad';
        attemptsLabel.textContent = 'Còn ' + lvl2Attempts[idx] + ' lần thử';
      }
    }
  }

  document.getElementById('checkLvl2').addEventListener('click', function(){
    lvl2Items.forEach((item, idx) => { if(!lvl2Correct[idx] && lvl2Attempts[idx] > 0) checkLvl2Question(idx); });
    renderLvl2Retry();
    document.getElementById('lvl2Score').textContent = 'Điểm Phần 2: ' + scores[2].score + '/' + scores[2].total;
    const allDone = lvl2Items.every((item,idx)=> lvl2Correct[idx] || lvl2Attempts[idx] <= 0);
    if(allDone){ sectionDone[2] = true; updateOverallProgress(); this.disabled = true; }
  });

  function renderLvl2Retry(){
    lvl2Items.forEach((item, idx) => {
      const qDiv = lvl2Container.querySelector('.q[data-idx="'+idx+'"]');
      const attemptsLabel = qDiv.querySelector('.attempts-left[data-idx="'+idx+'"]');
      if(!lvl2Correct[idx] && lvl2Attempts[idx] > 0 && !qDiv.querySelector('.btn.retry')){
        const retryBtn = document.createElement('button');
        retryBtn.className = 'btn retry small'; retryBtn.textContent = 'Làm lại';
        retryBtn.addEventListener('click', function(){
          checkLvl2Question(idx);
          document.getElementById('lvl2Score').textContent = 'Điểm Phần 2: ' + scores[2].score + '/' + scores[2].total;
          if(lvl2Correct[idx] || lvl2Attempts[idx] <= 0) retryBtn.remove();
          const allDone = lvl2Items.every((it,i)=> lvl2Correct[i] || lvl2Attempts[i] <= 0);
          if(allDone){ sectionDone[2] = true; updateOverallProgress(); }
        });
        attemptsLabel.after(retryBtn);
      }
    });
  }

  // ================= RENDER LEVEL 3 =================
  const lvl3Container = document.getElementById('lvl3Container');
  lvl3Items.forEach((item, idx) => {
    const qDiv = document.createElement('div');
    qDiv.className = 'q';
    qDiv.dataset.idx = idx;
    let optsHtml = '<div class="options">';
    item.options.forEach((opt, oIdx) => { optsHtml += '<div class="opt" data-idx="'+idx+'" data-opt="'+oIdx+'">' + opt + '</div>'; });
    optsHtml += '</div>';
    qDiv.innerHTML = '<div class="q-text">' + (idx+1) + '. ' + item.q + '</div>' + optsHtml + '<p class="attempts-left" data-idx="'+idx+'">Còn 3 lần thử</p>';
    lvl3Container.appendChild(qDiv);
  });
  const lvl3Attempts = lvl3Items.map(()=>3);
  const lvl3Correct = lvl3Items.map(()=>false);

  function checkLvl3Question(idx, chosenOpt){
    if(lvl3Correct[idx]) return;
    const qDiv = lvl3Container.querySelector('.q[data-idx="'+idx+'"]');
    const opts = qDiv.querySelectorAll('.opt');
    const attemptsLabel = qDiv.querySelector('.attempts-left[data-idx="'+idx+'"]');
    if(chosenOpt === lvl3Items[idx].correct){
      opts[chosenOpt].classList.add('correct');
      opts.forEach(o=>o.classList.add('disabled'));
      lvl3Correct[idx] = true; scores[3].score++;
      attemptsLabel.textContent = '✓ Chính xác!';
    } else {
      lvl3Attempts[idx]--;
      opts[chosenOpt].classList.add('wrong');
      setTimeout(()=>opts[chosenOpt].classList.remove('wrong'),500);
      if(lvl3Attempts[idx] <= 0){
        opts[lvl3Items[idx].correct].classList.add('correct');
        opts.forEach(o=>o.classList.add('disabled'));
        attemptsLabel.textContent = 'Đã hết lượt. Đáp án đúng đã hiện màu xanh.';
      } else { attemptsLabel.textContent = 'Còn ' + lvl3Attempts[idx] + ' lần thử'; }
    }
  }

  lvl3Container.addEventListener('click', function(e){
    const opt = e.target.closest('.opt');
    if(!opt || opt.classList.contains('disabled')) return;
    const idx = parseInt(opt.dataset.idx);
    if(lvl3Attempts[idx] > 0 && !lvl3Correct[idx]) checkLvl3Question(idx, parseInt(opt.dataset.opt));
  });

  document.getElementById('checkLvl3').addEventListener('click', function(){
    document.getElementById('lvl3Score').textContent = 'Điểm Phần 3: ' + scores[3].score + '/' + scores[3].total;
    const allDone = lvl3Items.every((item,idx)=> lvl3Correct[idx] || lvl3Attempts[idx] <= 0);
    if(allDone){ sectionDone[3] = true; updateOverallProgress(); }
    else { alert('Em hãy chọn đáp án cho tất cả các câu trước khi kiểm tra nhé!'); }
  });

  // ================= FINAL PANEL + HISTORY =================
  const HISTORY_KEY = 'liking_grammar_test_history';

  function showFinal(){
    const totalScore = scores[1].score + scores[2].score + scores[3].score;
    const totalMax = scores[1].total + scores[2].total + scores[3].total;
    document.getElementById('finalScoreText').textContent = totalScore + ' / ' + totalMax;
    const pct = totalScore/totalMax;
    let msg = '';
    if(pct >= 0.9) msg = 'Xuất sắc! Em đã nắm rất vững các cấu trúc diễn đạt sở thích! 🌟';
    else if(pct >= 0.7) msg = 'Rất tốt! Em chỉ cần ôn lại một vài cấu trúc nữa thôi! 💪';
    else if(pct >= 0.5) msg = 'Khá ổn! Hãy xem lại bảng tóm tắt và làm lại những câu sai nhé! 📖';
    else msg = 'Em nên xem lại bảng tóm tắt kiến thức và làm lại bài ôn tập nhé! Cố lên! 🌱';
    document.getElementById('finalMsg').textContent = msg;
    document.getElementById('finalPanel').classList.add('show');

    let history = [];
    try{ history = JSON.parse(localStorage.getItem(HISTORY_KEY)) || []; }catch(e){ history = []; }
    history.push({date: new Date().toLocaleString('vi-VN'), score: totalScore, total: totalMax});
    localStorage.setItem(HISTORY_KEY, JSON.stringify(history));
    renderHistory();
  }

  function renderHistory(){
    let history = [];
    try{ history = JSON.parse(localStorage.getItem(HISTORY_KEY)) || []; }catch(e){ history = []; }
    const listEl = document.getElementById('historyList');
    if(history.length === 0){ listEl.innerHTML = '<p style="color:var(--muted);">Chưa có lần làm bài nào.</p>'; return; }
    listEl.innerHTML = '';
    history.slice().reverse().forEach(h => {
      const row = document.createElement('div');
      row.className = 'history-row';
      row.innerHTML = '<span>' + h.date + '</span><span>' + h.score + '/' + h.total + '</span>';
      listEl.appendChild(row);
    });
  }
  renderHistory();

  document.getElementById('resetAllBtn').addEventListener('click', function(){
    if(confirm('Em có chắc muốn làm lại toàn bộ bài ôn tập không? Bài làm hiện tại sẽ mất.')){ location.reload(); }
  });

});
</script>
</body>
</html>
