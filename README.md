# Lo-cutieeeeee-

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Something For You 🫙</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lora:ital@0;1&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
  :root {
    --blush: #f7d4c8;
    --rose: #e8a09a;
    --deep: #b05a6f;
    --cream: #fdf6f0;
    --warm: #f2e0d0;
    --text: #5c2d3a;
    --gold: #d4956a;
  }
 
  body {
    min-height: 100vh;
    background: var(--cream);
    font-family: 'Lora', serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow-x: hidden;
    position: relative;
  }
 
  /* Soft background blobs */
  body::before, body::after {
    content: '';
    position: fixed;
    border-radius: 50%;
    filter: blur(80px);
    opacity: 0.35;
    pointer-events: none;
    z-index: 0;
  }
  body::before {
    width: 500px; height: 500px;
    background: radial-gradient(circle, #f5c6c0, #f7d4c8);
    top: -150px; left: -150px;
  }
  body::after {
    width: 400px; height: 400px;
    background: radial-gradient(circle, #fde8d8, #f9d5c5);
    bottom: -100px; right: -100px;
  }
 
  .page { position: relative; z-index: 1; text-align: center; padding: 2rem 1rem; }
 
  .intro {
    animation: fadeSlideUp 1s ease both;
  }
  .intro h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 5vw, 3rem);
    color: var(--deep);
    line-height: 1.2;
    margin-bottom: 0.6rem;
  }
  .intro p {
    font-size: 1rem;
    color: var(--gold);
    font-style: italic;
    margin-bottom: 2.5rem;
    letter-spacing: 0.02em;
  }
 
  /* JAR */
  .jar-wrap {
    position: relative;
    display: inline-block;
    animation: fadeSlideUp 1.2s ease both;
    cursor: pointer;
    margin-bottom: 1.5rem;
  }
 
  .jar {
    width: 160px;
    height: 200px;
    background: linear-gradient(135deg, rgba(255,255,255,0.7) 0%, rgba(247,212,200,0.4) 60%, rgba(232,160,154,0.3) 100%);
    border: 2.5px solid rgba(176,90,111,0.25);
    border-radius: 12px 12px 30px 30px;
    position: relative;
    backdrop-filter: blur(6px);
    box-shadow:
      inset 8px 0 20px rgba(255,255,255,0.5),
      inset -4px 0 12px rgba(176,90,111,0.1),
      0 20px 60px rgba(176,90,111,0.2);
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .jar:hover { transform: translateY(-6px) rotate(-1deg); box-shadow: 0 30px 70px rgba(176,90,111,0.3); }
 
  /* shine */
  .jar::before {
    content: '';
    position: absolute;
    top: 10px; left: 15px;
    width: 30px; height: 80px;
    background: rgba(255,255,255,0.45);
    border-radius: 20px;
    transform: rotate(10deg);
  }
 
  /* notes inside */
  .notes-in-jar {
    position: absolute;
    bottom: 12px; left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    justify-content: center;
    width: 120px;
  }
  .note-peek {
    width: 30px; height: 32px;
    border-radius: 4px;
    transform-origin: bottom center;
    animation: notePeek 3s ease-in-out infinite;
  }
  .note-peek:nth-child(1) { background: #f9b8c0; transform: rotate(-12deg); animation-delay: 0s; }
  .note-peek:nth-child(2) { background: #fad6a5; transform: rotate(5deg); animation-delay: 0.4s; }
  .note-peek:nth-child(3) { background: #c8e6c9; transform: rotate(-4deg); animation-delay: 0.8s; }
  .note-peek:nth-child(4) { background: #bbdefb; transform: rotate(10deg); animation-delay: 1.2s; }
  .note-peek:nth-child(5) { background: #e1bee7; transform: rotate(-8deg); animation-delay: 0.2s; }
  .note-peek:nth-child(6) { background: #fff9c4; transform: rotate(6deg); animation-delay: 0.6s; }
 
  @keyframes notePeek {
    0%, 100% { transform-origin: bottom; }
    50% { transform: translateY(-4px) rotate(var(--r, 5deg)); }
  }
 
  /* Lid */
  .jar-lid {
    width: 180px;
    height: 28px;
    background: linear-gradient(to bottom, #d4956a, #c07850);
    border-radius: 10px 10px 4px 4px;
    margin: 0 auto -2px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.12);
    position: relative;
    z-index: 2;
  }
  .jar-lid::after {
    content: '';
    position: absolute;
    top: 5px; left: 15px; right: 15px; height: 5px;
    background: rgba(255,255,255,0.25);
    border-radius: 3px;
  }
 
  .jar-label {
    position: absolute;
    bottom: 50px; left: 50%;
    transform: translateX(-50%);
    background: rgba(255,255,255,0.75);
    border: 1px solid rgba(176,90,111,0.2);
    border-radius: 6px;
    padding: 5px 10px;
    font-size: 0.6rem;
    color: var(--deep);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-family: 'Playfair Display', serif;
    white-space: nowrap;
  }
 
  .tap-hint {
    font-size: 0.8rem;
    color: var(--rose);
    font-style: italic;
    margin-top: 0.2rem;
    animation: pulse 2s ease infinite;
  }
 
  /* MODAL / NOTE CARD */
  .overlay {
    position: fixed; inset: 0;
    background: rgba(92,45,58,0.35);
    backdrop-filter: blur(6px);
    display: flex; align-items: center; justify-content: center;
    z-index: 100;
    opacity: 0; pointer-events: none;
    transition: opacity 0.35s ease;
  }
  .overlay.active { opacity: 1; pointer-events: all; }
 
  .note-card {
    background: var(--cream);
    border-radius: 20px;
    padding: 2.5rem 2rem;
    max-width: 340px;
    width: 90%;
    position: relative;
    text-align: center;
    transform: scale(0.85) translateY(30px);
    transition: transform 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
    box-shadow: 0 30px 80px rgba(92,45,58,0.25);
    border: 1.5px solid rgba(176,90,111,0.15);
  }
  .overlay.active .note-card { transform: scale(1) translateY(0); }
 
  .note-color-strip {
    height: 6px;
    border-radius: 10px;
    margin: 0 auto 1.5rem;
    width: 60px;
  }
 
  .note-number {
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--rose);
    margin-bottom: 0.6rem;
  }
 
  .note-text {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    color: var(--text);
    line-height: 1.5;
    font-style: italic;
    margin-bottom: 0.5rem;
  }
 
  .note-emoji {
    font-size: 2.2rem;
    margin-bottom: 1.2rem;
    display: block;
  }
 
  .note-close {
    background: var(--deep);
    color: white;
    border: none;
    border-radius: 50px;
    padding: 0.65rem 2rem;
    font-family: 'Lora', serif;
    font-size: 0.9rem;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
    margin-top: 0.5rem;
  }
  .note-close:hover { background: var(--rose); transform: scale(1.04); }
 
  .counter {
    font-size: 0.75rem;
    color: var(--blush);
    margin-top: 1rem;
    font-style: italic;
  }
 
  /* floating hearts */
  .hearts { position: fixed; inset: 0; pointer-events: none; z-index: 50; }
  .heart {
    position: absolute;
    font-size: 1.2rem;
    animation: floatHeart 3s ease-out forwards;
    opacity: 0;
  }
  @keyframes floatHeart {
    0% { opacity: 1; transform: translateY(0) scale(1); }
    100% { opacity: 0; transform: translateY(-200px) scale(0.4); }
  }
 
  /* progress */
  .progress-wrap {
    margin-top: 1.5rem;
    animation: fadeSlideUp 1.4s ease both;
  }
  .progress-label {
    font-size: 0.75rem;
    color: var(--gold);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  .progress-dots {
    display: flex; gap: 6px; justify-content: center; flex-wrap: wrap;
    max-width: 280px; margin: 0 auto;
  }
  .dot {
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--blush);
    border: 1.5px solid var(--rose);
    transition: background 0.3s ease, transform 0.3s ease;
  }
  .dot.done { background: var(--deep); transform: scale(1.2); }
 
  @keyframes fadeSlideUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; } 50% { opacity: 0.5; }
  }
</style>
</head>
<body>
 
<div class="page">
  <div class="intro">
    <h1>A Little Jar<br><em>Just For You</em> 🫙</h1>
    <p>Pull out a note whenever you need a smile ✨</p>
  </div>
 
  <div class="jar-wrap" onclick="openNote()">
    <div class="jar-lid"></div>
    <div class="jar">
      <div class="jar-label">With Love 💕</div>
      <div class="notes-in-jar">
        <div class="note-peek"></div>
        <div class="note-peek"></div>
        <div class="note-peek"></div>
        <div class="note-peek"></div>
        <div class="note-peek"></div>
        <div class="note-peek"></div>
      </div>
    </div>
  </div>
 
  <p class="tap-hint">tap the jar to pull a note 🎀</p>
 
  <div class="progress-wrap">
    <p class="progress-label">Notes discovered</p>
    <div class="progress-dots" id="dots"></div>
  </div>
</div>
 
<div class="hearts" id="hearts"></div>
 
<!-- Note Modal -->
<div class="overlay" id="overlay" onclick="closeNote(event)">
  <div class="note-card" id="noteCard">
    <div class="note-color-strip" id="noteStrip"></div>
    <p class="note-number" id="noteNum"></p>
    <span class="note-emoji" id="noteEmoji"></span>
    <p class="note-text" id="noteText"></p>
    <button class="note-close" onclick="closeNote()">Put it back 🫙</button>
    <p class="counter" id="counter"></p>
  </div>
</div>
 
<script>
const notes = [
  { text: "Kal exam hai! 📚 Thoda sa padh lena — bas thoda sa, I know you've got this. All the best, you smart, beautiful girl. Jaao top karo Cutie! 🌟", emoji: "✏️", color: "#fff9c4", first: true },
  { text: "The way you smile can completely rearrange someone's entire day.", emoji: "🌸", color: "#f9b8c0" },
  { text: "You're allowed to feel sad sometimes. It just means you care deeply, and that's beautiful.", emoji: "🌧️", color: "#bbdefb" },
  { text: "Even on the hard days, you are still so incredibly loveable.", emoji: "💗", color: "#e1bee7" },
  { text: "You deserve the same kindness you give to everyone else.", emoji: "🌷", color: "#fad6a5" },
  { text: "Your laugh is one of the best sounds in the whole world.", emoji: "✨", color: "#c8e6c9" },
  { text: "You are thought about, chosen, and adored — more than you probably know.", emoji: "🥰", color: "#f9b8c0" },
  { text: "This feeling will pass. And when it does, you'll still be wonderful.", emoji: "🌈", color: "#fff9c4" },
  { text: "The world is genuinely better with you in it.", emoji: "🌍", color: "#c8e6c9" },
  { text: "Being upset doesn't make you weak. It makes you human — and beautifully so.", emoji: "🫶", color: "#e1bee7" },
  { text: "You are someone worth waiting for, fighting for, and showing up for.", emoji: "💌", color: "#fad6a5" },
  { text: "Right now, someone is thinking about you and smiling.", emoji: "🌙", color: "#bbdefb" },
  { text: "You carry more warmth in you than you give yourself credit for.", emoji: "☀️", color: "#fff9c4" },
];
 
const seen = new Set();
let lastIdx = -1;
 
function buildDots() {
  const wrap = document.getElementById('dots');
  wrap.innerHTML = '';
  notes.forEach((_, i) => {
    const d = document.createElement('div');
    d.className = 'dot' + (seen.has(i) ? ' done' : '');
    d.id = `dot-${i}`;
    wrap.appendChild(d);
  });
}
 
function openNote() {
  let idx;
  const unseen = notes.map((_, i) => i).filter(i => !seen.has(i));
  if (unseen.length === 0) {
    seen.clear();
    buildDots();
    idx = Math.floor(Math.random() * notes.length);
  } else if (seen.size === 0 && notes[0].first) {
    idx = 0; // always show the special first note first
  } else {
    const pool = unseen.filter(i => i !== lastIdx);
    idx = pool.length ? pool[Math.floor(Math.random() * pool.length)] : unseen[0];
  }
  lastIdx = idx;
  seen.add(idx);
 
  const note = notes[idx];
  document.getElementById('noteStrip').style.background = note.color;
  document.getElementById('noteEmoji').textContent = note.emoji;
  document.getElementById('noteText').textContent = note.text;
  document.getElementById('noteNum').textContent = `Note ${seen.size} of ${notes.length}`;
  document.getElementById('counter').textContent =
    seen.size === notes.length ? '🎉 You found all the notes! Tap again to start over.' :
    `${notes.length - seen.size} note${notes.length - seen.size !== 1 ? 's' : ''} still waiting in the jar…`;
 
  document.getElementById('overlay').classList.add('active');
  buildDots();
  spawnHearts();
}
 
function closeNote(e) {
  if (!e || e.target === document.getElementById('overlay')) {
    document.getElementById('overlay').classList.remove('active');
  }
}
 
function spawnHearts() {
  const container = document.getElementById('hearts');
  const emojis = ['💕', '🌸', '✨', '💗', '🩷', '🌷'];
  for (let i = 0; i < 8; i++) {
    setTimeout(() => {
      const h = document.createElement('div');
      h.className = 'heart';
      h.textContent = emojis[Math.floor(Math.random() * emojis.length)];
      h.style.left = Math.random() * 90 + 5 + 'vw';
      h.style.top = Math.random() * 60 + 20 + 'vh';
      h.style.animationDelay = Math.random() * 0.5 + 's';
      container.appendChild(h);
      setTimeout(() => h.remove(), 3500);
    }, i * 80);
  }
}
 
buildDots();
</script>
</body>
</html>
