# Bba-sem3-mlsu-ED

<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#10233f">
<title>Venture Capital — BBA Semester III</title>
<style>
:root{--navy:#10233f;--blue:#2259a6;--teal:#23a995;--gold:#ffc857;--ink:#18263a;--muted:#66748a;--paper:#f4f7fc;--white:#fff;--green:#17864b;--red:#c94f4f}
*{box-sizing:border-box}
body{margin:0;background:var(--paper);color:var(--ink);font:16px/1.55 system-ui,-apple-system,"Segoe UI",sans-serif}
button,select{font:inherit}
button{cursor:pointer}
header{position:sticky;top:0;z-index:5;background:var(--navy);color:white;padding:10px 14px;box-shadow:0 2px 12px #10233f33}
.top{display:flex;align-items:center;gap:10px;max-width:1100px;margin:auto}
.brand{font-weight:800;white-space:nowrap}
select{min-width:0;max-width:45vw;padding:8px;border-radius:8px;border:0;background:white;color:var(--ink)}
.spacer{flex:1}
.iconbtn,.navbtn{border:0;border-radius:10px;padding:9px 12px;background:#ffffff1c;color:white}
.progress{height:4px;background:#ffffff38;margin:10px auto 0;max-width:1100px;border-radius:4px}
#bar{height:100%;width:0;background:var(--gold);border-radius:4px;transition:width .3s}
main{max-width:1000px;margin:22px auto;padding:0 14px 90px}
.slide{display:none;background:white;border-radius:20px;padding:clamp(20px,5vw,42px);min-height:65vh;box-shadow:0 8px 28px #172b4910;animation:enter .35s ease}
.slide.active{display:block}
@keyframes enter{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:none}}
.eyebrow{color:var(--blue);font-weight:800;text-transform:uppercase;letter-spacing:.09em;font-size:.78rem}
h1,h2,h3{line-height:1.2;color:var(--navy)}
h1{font-size:clamp(2rem,6vw,3.5rem);margin:.25em 0}
h2{font-size:clamp(1.5rem,4vw,2.15rem);margin:.25em 0 .7em}
h3{margin:.3em 0}
p{margin:.65em 0}
.lead{font-size:1.12rem;color:#42516a}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,220px),1fr));gap:12px;margin:16px 0}
.card,.callout{padding:16px;border-radius:14px;background:#f1f6ff;border:1px solid #dce8fb}
.card h3{font-size:1.05rem}
.callout{background:#fff7df;border-color:#ffe7a2}
.exam{background:#edf9f5;border-left:5px solid var(--teal);padding:15px 18px;border-radius:8px;margin:14px 0}
.tag{display:inline-block;background:#e4efff;color:#194c91;border-radius:99px;padding:3px 10px;font-size:.82rem;font-weight:700}
.flow{display:flex;flex-wrap:wrap;align-items:center;gap:7px;margin:18px 0}
.flow span{background:var(--navy);color:white;border-radius:10px;padding:10px 12px;font-weight:700}
.flow b{color:var(--teal)}
table{width:100%;border-collapse:collapse;margin:14px 0;font-size:.94rem}
th,td{text-align:left;padding:10px;border-bottom:1px solid #e4e9f1;vertical-align:top}
th{background:#edf3fc;color:var(--navy)}
svg{width:100%;height:auto;max-height:300px;margin:10px 0}
.controls{position:fixed;bottom:0;left:0;right:0;background:#10233fee;color:white;padding:10px max(12px,calc((100vw - 1000px)/2));display:flex;align-items:center;gap:9px;z-index:6;backdrop-filter:blur(8px)}
.controls button{border:0;border-radius:10px;padding:10px 14px;background:white;color:var(--navy);font-weight:700}
.controls .toggle{background:#dce8fb}
#counter{min-width:70px;text-align:center;font-variant-numeric:tabular-nums}
.quiz-option{display:block;width:100%;text-align:left;margin:8px 0;padding:12px;border:2px solid #dce4ef;border-radius:11px;background:white;color:var(--ink)}
.quiz-option:hover{border-color:var(--blue)}
.quiz-option.correct{background:#e4f8eb;border-color:var(--green);box-shadow:0 0 0 3px #17864b22}
.quiz-option.wrong{background:#fff0f0;border-color:var(--red)}
.timer{font-size:1.2rem;font-weight:800;color:var(--blue)}
.flipgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:12px}
.flip{min-height:155px;border:0;background:transparent;perspective:700px;padding:0}
.flipinner{position:relative;display:block;min-height:155px;transform-style:preserve-3d;transition:transform .5s}
.flip.flipped .flipinner{transform:rotateY(180deg)}
.face{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;text-align:center;padding:16px;border-radius:14px;backface-visibility:hidden;background:#edf3fc;border:1px solid #dce8fb;font-weight:700}
.back{transform:rotateY(180deg);background:#e9f8f1;border-color:#bde8d2;font-weight:500}
.small{color:var(--muted);font-size:.9rem}
.hidden{display:none!important}
@media(max-width:600px){.brand{font-size:.88rem}.navbtn{padding:8px}.controls{gap:6px}.controls button{padding:10px}.slide{min-height:70vh}table{font-size:.85rem}th,td{padding:7px}}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:.01ms!important;transition-duration:.01ms!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<header>
  <div class="top">
    <div class="brand">📘 Venture Capital</div>
    <div class="spacer"></div>
    <select id="sceneMenu" aria-label="Jump to slide"></select>
    <button class="iconbtn" id="soundBtn" title="Toggle narration" aria-label="Toggle narration">🔊</button>
  </div>
  <div class="progress"><div id="bar"></div></div>
</header>

<main id="deck">

<section class="slide" data-title="Welcome">
<div class="eyebrow">BBA · Semester III · Entrepreneurship Development</div>
<h1>Venture Capital</h1>
<p class="lead">Meaning · Features · Process · Financing stages · Sources · Documents</p>
<div class="callout"><b>Desi story:</b> Ayesha from Pune has an app idea that helps local tiffin services find customers. She has a prototype, but not enough money to launch. A venture capital investor funds the company in return for part ownership—and supports its growth. That investment is venture capital.</div>
<h3>By the end, you can:</h3>
<ul><li>Define VC and explain why it is called risk or patient capital.</li><li>Describe its features, investment cycle, and six financing stages.</li><li>Explain how entrepreneurs raise funds and identify common sources and documents.</li><li>Practise exam answers and revise with quizzes and memory aids.</li></ul>
<p class="small">Use the slide menu, arrow keys, or Previous/Next. Narration requires browser speech synthesis.</p>
</section>

<section class="slide" data-title="Meaning and definition">
<div class="eyebrow">01 · Meaning</div><h2>What is Venture Capital?</h2>
<div class="exam"><b>Exam-ready definition:</b> Venture Capital (VC) is long-term equity finance provided by investors to new, small, or emerging businesses with high growth potential, in exchange for an ownership stake.</div>
<p><b>In simple Hinglish:</b> Investor company ko paisa deta hai aur badle mein company ka kuch hissa—shares—leta hai. Yeh normal interest wala loan nahi hota.</p>
<div class="grid">
<div class="card"><h3>Risk Capital</h3><p>It backs ventures without a proven track record. Failure is possible, but success may bring high returns.</p></div>
<div class="card"><h3>Patient Capital</h3><p>It is generally invested for the long term while a business grows; it is not usually withdrawn like a bank deposit.</p></div>
<div class="card"><h3>Example</h3><p>A VC invests ₹2 crore for a 20% ownership stake in a promising app business and helps it scale.</p></div>
</div>
<p><b>Key words:</b> long-term · equity · growth potential · risk · ownership stake</p>
</section>

<section class="slide" data-title="Features">
<div class="eyebrow">02 · Concept</div><h2>Key features of VC</h2>
<div class="grid">
<div class="card"><h3>Equity participation</h3><p>Investor receives ownership shares, not just interest.</p></div>
<div class="card"><h3>High risk, high return</h3><p>Funding may go to ventures banks consider too risky.</p></div>
<div class="card"><h3>Long-term investment</h3><p>The notes describe a usual horizon of 5–10 years.</p></div>
<div class="card"><h3>Active involvement</h3><p>Investors may offer mentoring, strategic advice, or a board seat—“smart money.”</p></div>
<div class="card"><h3>Innovation focus</h3><p>Often supports innovative or technology-based startups.</p></div>
<div class="card"><h3>Professionally managed</h3><p>Funds are managed by VC firms or professional fund managers.</p></div>
<div class="card"><h3>Exit-oriented</h3><p>Investors seek to realise returns by selling their stake, such as through a sale or IPO.</p></div>
<div class="card"><h3>Illiquid</h3><p>Shares in a private venture cannot usually be withdrawn or sold easily before an exit.</p></div>
</div>
<div class="callout"><b>Remember:</b> VC is not a loan. No fixed repayment or regular loan interest is promised in the basic equity arrangement; investor returns depend on the value realised at exit.</div>
</section>

<section class="slide" data-title="Investment cycle">
<div class="eyebrow">03 · Process</div><h2>VC investment cycle</h2>
<p>Investors assess a venture before investing, then track progress and seek an eventual exit.</p>
<div class="flow"><span>1. Deal origination</span><b>→</b><span>2. Screening</span><b>→</b><span>3. Due diligence</span><b>→</b><span>4. Deal structuring</span><b>→</b><span>5. Documentation &amp; investment</span><b>→</b><span>6. Monitoring</span><b>→</b><span>7. Exit</span></div>
<svg viewBox="0 0 800 150" role="img" aria-label="Investment cycle arrow diagram">
<defs><marker id="arrow" markerWidth="10" markerHeight="10" refX="8" refY="3" orient="auto"><path d="M0,0 L0,6 L9,3 z" fill="#23a995"/></marker></defs>
<path d="M45 75 H745" fill="none" stroke="#23a995" stroke-width="4" marker-end="url(#arrow)"/>
<g fill="#2259a6"><circle cx="70" cy="75" r="13"/><circle cx="180" cy="75" r="13"/><circle cx="290" cy="75" r="13"/><circle cx="400" cy="75" r="13"/><circle cx="510" cy="75" r="13"/><circle cx="620" cy="75" r="13"/><circle cx="720" cy="75" r="13"/></g>
<g font-family="system-ui" font-size="13" fill="#10233f" text-anchor="middle"><text x="70" y="112">Originate</text><text x="180" y="112">Screen</text><text x="290" y="112">Evaluate</text><text x="400" y="112">Structure</text><text x="510" y="112">Document</text><text x="620" y="112">Monitor</text><text x="720" y="112">Exit</text></g></svg>
<div class="callout"><b>Memory trick:</b> D-S-D-D-D-M-E — Deal origination, Screening, Due diligence, Deal structuring, Documentation, Monitoring, Exit.</div>
</section>

<section class="slide" data-title="Financing stages">
<div class="eyebrow">04 · Stages</div><h2>Six stages of VC financing</h2>
<p>Funding is matched to a venture’s development. The notes show risk generally decreasing as the business matures.</p>
<table><thead><tr><th>Stage</th><th>Also called</th><th>What happens</th><th>Risk in notes</th></tr></thead><tbody>
<tr><td>1. Seed</td><td>Seed capital</td><td>Idea or concept; research, prototype, and business plan.</td><td>Very high</td></tr>
<tr><td>2. Start-up</td><td>Start-up capital</td><td>Product development is complete; company is being formally set up.</td><td>High</td></tr>
<tr><td>3. First stage</td><td>Early stage</td><td>Commercial production and marketing begin.</td><td>High</td></tr>
<tr><td>4. Second stage</td><td>Growth stage</td><td>Working capital for an already-selling company to expand.</td><td>Medium</td></tr>
<tr><td>5. Third stage</td><td>Mezzanine / expansion</td><td>Major expansion, diversification, or marketing.</td><td>Medium-low</td></tr>
<tr><td>6. Bridge stage</td><td>Bridge financing</td><td>Short-term funding before IPO, merger, or acquisition.</td><td>Low</td></tr>
</tbody></table>
<div class="flow"><span>Seed</span><b>→</b><span>Start-up</span><b>→</b><span>First</span><b>→</b><span>Second</span><b>→</b><span>Third</span><b>→</b><span>Bridge</span></div>
<div class="exam"><b>Exam tip:</b> Give all six stages in sequence and add one line about what each stage finances.</div>
</section>

<section class="slide" data-title="Raising funds">
<div class="eyebrow">05 · Entrepreneur’s steps</div><h2>How to raise VC funds</h2>
<div class="flow"><span>Business plan</span><b>→</b><span>Approach firms</span><b>→</b><span>Pitch</span><b>→</b><span>Due diligence</span><b>→</b><span>Term sheet</span><b>→</b><span>Legal documents</span><b>→</b><span>Disbursement</span></div>
<ol>
<li><b>Prepare a business plan:</b> explain the idea, market, team, and financials.</li>
<li><b>Approach suitable VC firms:</b> shortlist investors whose industry and stage focus fit the venture.</li>
<li><b>Present or pitch:</b> explain the plan to the investor or investment committee.</li>
<li><b>Due diligence:</b> the investor checks financial, legal, technical, and market claims.</li>
<li><b>Negotiate the term sheet:</b> discuss valuation, equity percentage, and investor rights.</li>
<li><b>Complete legal documentation:</b> sign the formal agreements.</li>
<li><b>Receive funds:</b> disbursement may happen in tranches (instalments).</li>
</ol>
<div class="exam"><b>Term Sheet:</b> A non-binding document setting out key proposed investment terms—such as valuation, equity percentage, and investor rights—before final legal agreements are prepared.</div>
</section>

<section class="slide" data-title="Sources of VC">
<div class="eyebrow">06 · Sources</div><h2>Formal and informal sources</h2>
<h3>Formal / institutional sources</h3>
<ul><li><b>VC firms or funds:</b> dedicated professional venture funds.</li><li><b>Bank-sponsored VC funds:</b> VC arms of banks or financial institutions.</li><li><b>State Financial Corporations (SFCs):</b> state-level bodies supporting small and medium enterprises.</li><li><b>All-India financial institutions:</b> the notes cite SIDBI, IDBI, and ICICI Venture as examples.</li><li><b>Mutual funds with VC schemes:</b> pooled funds allocating some capital to venture investments.</li></ul>
<h3>Informal / non-institutional sources</h3>
<ul><li><b>Angel investors:</b> individuals investing personal funds, often at an early stage.</li><li><b>Friends and family:</b> personal-network funding, often very early.</li><li><b>High-net-worth individuals (HNIs):</b> wealthy individuals seeking high-risk, high-return opportunities.</li><li><b>Corporate venturing:</b> companies invest in startups for strategic benefit.</li><li><b>Crowdfunding platforms:</b> small amounts raised from many people online.</li></ul>
<div class="callout"><b>Angel vs. VC:</b> In the notes, angels invest their own money, often earlier and in smaller amounts. VCs invest pooled institutional money, commonly at later stages and through more formal processes.</div>
</section>

<section class="slide" data-title="Documents">
<div class="eyebrow">07 · Documentation</div><h2>Documents for VC funding</h2>
<p>The notes list the following items as commonly required or relevant before funds are released. Exact requirements depend on the transaction.</p>
<div class="grid">
<div class="card"><h3>Business plan</h3><p>Business idea, market, team, and financial plan.</p></div>
<div class="card"><h3>Term sheet</h3><p>Proposed key investment terms.</p></div>
<div class="card"><h3>Shareholders’ agreement (SHA)</h3><p>Agreement addressing shareholder rights and arrangements.</p></div>
<div class="card"><h3>Share subscription agreement</h3><p>Documents subscription to company shares.</p></div>
<div class="card"><h3>MOA / AOA</h3><p>Memorandum and Articles of Association.</p></div>
<div class="card"><h3>Due diligence materials</h3><p>Information used for financial, legal, technical, and market review.</p></div>
<div class="card"><h3>Valuation report</h3><p>Material supporting the proposed company valuation.</p></div>
<div class="card"><h3>Board resolution</h3><p>Relevant company approval recorded by the board.</p></div>
<div class="card"><h3>Financials</h3><p>Financial statements and projections, as requested.</p></div>
<div class="card"><h3>KYC and NDA</h3><p>Know Your Customer information and a Non-Disclosure Agreement where applicable.</p></div>
</div>
<div class="callout"><b>Memory trick from the notes:</b> B-T-S-S-M-D-V-B-F-K-N. Use it to recall the list, but expand each abbreviation accurately in your answer.</div>
<p class="small"><b>VERIFY WITH TEXTBOOK:</b> Document names, legal requirements, and whether each item is mandatory can vary by company structure, transaction, and current rules.</p>
</section>

<section class="slide" data-title="Quick revision">
<div class="eyebrow">08 · Rapid recap</div><h2>Quick revision zone</h2>
<div class="grid">
<div class="card"><h3>Meaning</h3><p>Risk-bearing long-term equity finance for high-growth ventures.</p></div>
<div class="card"><h3>Process</h3><p>Origination → screening → due diligence → structuring → documentation → monitoring → exit.</p></div>
<div class="card"><h3>Stages</h3><p>Seed → start-up → first → second → third → bridge.</p></div>
<div class="card"><h3>Sources</h3><p>Formal: funds, banks, institutions. Informal: angels, family, HNIs, corporates, crowdfunding.</p></div>
<div class="card"><h3>Documents</h3><p>Business plan, term sheet, agreements, MOA/AOA, valuation, board approval, financials, KYC, NDA.</p></div>
</div>
<div class="exam"><b>Exam answer structure:</b> Definition → features → diagram/process → example → conclusion.</div>
</section>

<section class="slide" data-title="Quiz 1">
<div class="eyebrow">09 · Quiz 1 of 5</div><h2>How does a VC investor typically earn a return?</h2>
<div class="timer" data-timer>Choose within 5 seconds</div>
<div class="options"></div><div class="explanation hidden"></div>
</section>
<section class="slide" data-title="Quiz 2">
<div class="eyebrow">09 · Quiz 2 of 5</div><h2>Which step comes immediately after screening in the investment cycle?</h2>
<div class="timer" data-timer>Choose within 5 seconds</div>
<div class="options"></div><div class="explanation hidden"></div>
</section>
<section class="slide" data-title="Quiz 3">
<div class="eyebrow">09 · Quiz 3 of 5</div><h2>Which stage funds research, a prototype, and a business plan?</h2>
<div class="timer" data-timer>Choose within 5 seconds</div>
<div class="options"></div><div class="explanation hidden"></div>
</section>
<section class="slide" data-title="Quiz 4">
<div class="eyebrow">09 · Quiz 4 of 5</div><h2>What is a term sheet in the supplied notes?</h2>
<div class="timer" data-timer>Choose within 5 seconds</div>
<div class="options"></div><div class="explanation hidden"></div>
</section>
<section class="slide" data-title="Quiz 5">
<div class="eyebrow">09 · Quiz 5 of 5</div><h2>Which statement best distinguishes an angel investor from a VC?</h2>
<div class="timer" data-timer>Choose within 5 seconds</div>
<div class="options"></div><div class="explanation hidden"></div>
</section>

<section class="slide" data-title="Memory tricks">
<div class="eyebrow">10 · Memorise</div><h2>Memory tricks that match the notes</h2>
<ul>
<li><b>VC process: D-S-D-D-D-M-E.</b> Deal origination, Screening, Due diligence, Deal structuring, Documentation, Monitoring, Exit.</li>
<li><b>Financing stages: S-S-F-S-T-B.</b> Seed, Start-up, First, Second, Third, Bridge. Say: “Start Small, Fund Scale, Then Bridge.”</li>
<li><b>Documents: B-T-S-S-M-D-V-B-F-K-N.</b> Business plan, Term sheet, Shareholders’ agreement, Share subscription, MOA/AOA, Due diligence, Valuation, Board resolution, Financials, KYC, NDA.</li>
<li><b>Core idea:</b> Equity means ownership; exit is when investor sells or otherwise realises the stake’s value.</li>
</ul>
<div class="callout"><b>Check yourself:</b> Don’t confuse the VC investment cycle (investor’s process) with the entrepreneur’s fundraising steps. They overlap, but are not identical.</div>
</section>

<section class="slide" data-title="Flip-card test">
<div class="eyebrow">11 · Tap a card to flip</div><h2>12-card mini test</h2><p class="small">Tap or click a card to reveal the answer.</p><div class="flipgrid" id="flipgrid"></div>
</section>

<section class="slide" data-title="Rapid fire">
<div class="eyebrow">12 · Rapid-fire round</div><h2>Recall it before the answer appears</h2>
<p id="rapidQ" class="lead"></p><p id="rapidA" class="callout hidden"></p>
<div class="grid"><button id="rapidNext">Start / Next question</button><button id="rapidReplay">Replay round</button></div>
<p class="small">Each answer appears after 3 seconds. Use Replay to start again.</p>
</section>

<section class="slide" data-title="Mind map">
<div class="eyebrow">13 · Connect the ideas</div><h2>Venture capital mind map</h2>
<svg viewBox="0 0 760 470" role="img" aria-label="Mind map of venture capital topics">
<g stroke="#23a995" stroke-width="3" fill="none">
<path d="M380 225L160 90M380 225L600 90M380 225L150 225M380 225L610 225M380 225L170 370M380 225L590 370"/>
</g>
<g font-family="system-ui" text-anchor="middle">
<ellipse cx="380" cy="225" rx="105" ry="48" fill="#10233f"/><text x="380" y="231" fill="white" font-weight="700">VENTURE CAPITAL</text>
<g fill="#e7f0ff" stroke="#aac6ee"><rect x="65" y="50" width="190" height="75" rx="16"/><rect x="505" y="50" width="190" height="75" rx="16"/><rect x="50" y="188" width="200" height="75" rx="16"/><rect x="510" y="188" width="200" height="75" rx="16"/><rect x="70" y="333" width="200" height="75" rx="16"/><rect x="490" y="333" width="200" height="75" rx="16"/></g>
<g fill="#10233f" font-size="16" font-weight="700"><text x="160" y="82">Meaning &amp; features</text><text x="600" y="82">Investment cycle</text><text x="150" y="220">Six stages</text><text x="610" y="220">Raising funds</text><text x="170" y="365">Sources</text><text x="590" y="365">Documents &amp; exit</text></g>
</g></svg>
<p>Centre idea: long-term equity for growth-potential ventures. Branches connect the definition to the investor’s process, venture stages, fundraising, sources, documents, and exit.</p>
</section>

<section class="slide" data-title="Exam practice">
<div class="eyebrow">14 · Exam preparation</div><h2>Practice questions</h2>
<h3>Short-answer practice</h3>
<ul><li>Define Venture Capital.</li><li>What is a term sheet?</li><li>Name two formal and two informal sources of VC.</li><li>State any four features of venture capital.</li><li>What is meant by bridge financing?</li></ul>
<h3>Long-answer practice</h3>
<ul><li>Explain the six stages of Venture Capital financing.</li><li>Describe the VC investment cycle with a flowchart.</li><li>Explain the process of raising venture capital funds.</li><li>Discuss formal and informal sources of venture capital.</li><li>Explain the meaning, features, and importance of venture capital.</li></ul>
<p class="small">These are practice prompts based on the supplied notes, not predictions of what will appear in an examination.</p>
</section>

<section class="slide" data-title="Mistakes and verification">
<div class="eyebrow">15 · Accuracy check</div><h2>Common mistakes &amp; verification flags</h2>
<ul>
<li>Calling VC a loan with fixed repayment and regular interest: the notes describe equity finance.</li>
<li>Mixing up the investment cycle with the entrepreneur’s fundraising sequence.</li>
<li>Leaving out a stage or writing the six financing stages out of order.</li>
<li>Confusing the term sheet with the final legal agreements; the notes describe it as non-binding.</li>
<li>Assuming every VC deal uses identical documents, terms, or funding timelines.</li>
</ul>
<div class="callout"><b>VERIFY WITH TEXTBOOK:</b> The notes’ “usually 5 to 10 years” duration, the risk labels for stages, listed institutional examples, and document requirements may depend on context or syllabus edition. Confirm exact wording expected by your university.</div>
</section>

<section class="slide" data-title="Revision plan">
<div class="eyebrow">16 · Study plan</div><h2>A practical revision plan</h2>
<ol>
<li><b>First pass (15 min):</b> Learn the definition, ownership idea, and eight features.</li>
<li><b>Draw from memory (10 min):</b> Recreate the seven-step investment cycle and six financing stages.</li>
<li><b>Explain aloud (10 min):</b> Practise fundraising steps, sources, and angel-vs-VC distinction.</li>
<li><b>Recall (10 min):</b> Use the flip cards and quiz without looking at notes.</li>
<li><b>Exam practice (15 min):</b> Write one long answer with a flowchart and one short answer on term sheets.</li>
<li><b>Final check (5 min):</b> Review textbook verification flags and correct any syllabus-specific wording.</li>
</ol>
<div class="exam"><b>Quick self-test:</b> Can you define VC, distinguish it from a loan, list all six stages, and draw the process without help?</div>
</section>

</main>

<div class="controls">
<button id="prev" aria-label="Previous slide">← Prev</button>
<span id="counter"></span>
<button id="next" aria-label="Next slide">Next →</button>
<div class="spacer"></div>
<button class="toggle" id="narrate" title="Toggle narration">Narration: On</button>
<button class="toggle" id="pause" title="Pause or resume narration">Pause</button>
<button class="toggle" id="replay" title="Replay narration">Replay</button>
<button class="toggle" id="full" title="Toggle fullscreen">⛶</button>
<button class="toggle" id="restart" title="Restart slideshow">Restart</button>
</div>

<script>
(()=> {
"use strict";
const slides=[...document.querySelectorAll(".slide")], menu=document.getElementById("sceneMenu");
let index=0, narrationOn=true, quizTimer=null, rapidIndex=-1, rapidTimer=null;
const quizData=[
{opts:["By collecting regular loan interest","By selling or realising its ownership stake","By charging a fixed monthly fee","By receiving a government grant"],correct:1,why:"VC receives equity. Its return generally depends on the value realised when it exits its investment."},
{opts:["Deal structuring","Due diligence / evaluation","Exit","Disbursement"],correct:1,why:"Screening is followed by due diligence or evaluation in the investment cycle."},
{opts:["Bridge stage","Seed stage","Second stage","Third stage"],correct:1,why:"Seed capital supports the idea or concept, including research and prototype work."},
{opts:["A final binding shareholder agreement","A non-binding outline of proposed key investment terms","A bank loan application","A company’s annual report"],correct:1,why:"The notes define a term sheet as a non-binding summary of proposed terms before final legal agreements."},
{opts:["Angels invest pooled institutional money; VCs invest their own personal money","Angels often invest personal funds early; VCs usually invest pooled funds through formal processes","There is no difference","VCs only invest after an IPO"],correct:1,why:"That is the distinction given in the supplied notes: personal, often early-stage angel funds versus pooled, more formal VC funds."}
];
const cards=[
["Define Venture Capital.","Long-term equity finance for growth-potential ventures in exchange for ownership."],
["Why is VC called risk capital?","It funds ventures without a proven track record; failure is possible."],
["What does patient capital mean here?","Long-term capital that stays invested while the venture grows."],
["Name the first step in the investment cycle.","Deal origination."],
["What follows screening?","Due diligence / evaluation."],
["What are the six financing stages?","Seed, start-up, first, second, third, and bridge."],
["What is seed capital used for?","Research, prototype, and business-plan work at the idea stage."],
["What is a term sheet?","A non-binding summary of proposed key investment terms."],
["Who is an angel investor?","An individual investing personal money, often in early-stage startups."],
["Give two formal sources.","Examples in the notes include VC funds and bank-sponsored funds."],
["What does exit mean?","The investor realises the value of its stake, such as by selling shares."],
["Name two documents from the notes.","Examples: shareholders’ agreement and share subscription agreement."]
];
const rapid=[
["What does VC receive in exchange for investment?","An equity or ownership stake."],
["Name the last step of the investment cycle.","Exit."],
["Which stage is associated with major expansion or diversification?","Third stage, also called mezzanine / expansion."],
["What does KYC stand for?","Know Your Customer."],
["Name one informal VC source from the notes.","Angel investors, friends and family, HNIs, corporate venturing, or crowdfunding."]
];
slides.forEach((s,i)=>{let o=document.createElement("option");o.value=i;o.textContent=(i+1)+". "+s.dataset.title;menu.appendChild(o)});
function speakSlide(){
 if("speechSynthesis" in window){speechSynthesis.cancel();if(!narrationOn)return;
 const s=slides[index], title=s.dataset.title||"Study slide";
 let text=(s.innerText||"").replace(/Narration: On|Pause|Replay|Prev|Next/g," ").replace(/\s+/g," ").trim();
 const utter=new SpeechSynthesisUtterance(title+". "+text);
 utter.lang="en-IN";utter.rate=.94;utter.pitch=1.04;
 const voices=speechSynthesis.getVoices();const v=voices.find(x=>/en-IN/i.test(x.lang))||voices.find(x=>/en/i.test(x.lang));
 if(v)utter.voice=v;
 speechSynthesis.speak(utter);
 }
}
function show(n){
 index=Math.max(0,Math.min(slides.length-1,n));
 slides.forEach((s,i)=>s.classList.toggle("active",i===index));
 menu.value=index;document.getElementById("counter").textContent=(index+1)+" / "+slides.length;
 document.getElementById("bar").style.width=((index+1)/slides.length*100)+"%";
 clearInterval(quizTimer);clearTimeout(rapidTimer);
 if(slides[index].querySelector(".options"))setupQuiz(slides[index]);
 if(slides[index].dataset.title==="Rapid fire"){document.getElementById("rapidQ").textContent="Press Start / Next question.";document.getElementById("rapidA").classList.add("hidden")}
 speakSlide();window.scrollTo({top:0,behavior:"smooth"});
}
function setupQuiz(slide){
 const q=quizData[Number(slide.dataset.title.match(/\d+/)?.[0])-1];
 if(!q)return;
 const area=slide.querySelector(".options"), exp=slide.querySelector(".explanation"), timer=slide.querySelector("[data-timer]");
 area.innerHTML="";exp.classList.add("hidden");exp.textContent="";
 let locked=false, remaining=5;
 q.opts.forEach((o,i)=>{const b=document.createElement("button");b.className="quiz-option";b.textContent=String.fromCharCode(65+i)+". "+o;b.onclick=()=>reveal(i);area.appendChild(b)});
 function reveal(choice=-1){
  if(locked)return;locked=true;clearInterval(quizTimer);
  [...area.children].forEach((b,i)=>{if(i===q.correct)b.classList.add("correct");else if(i===choice)b.classList.add("wrong");b.disabled=true});
  timer.textContent=choice===q.correct?"Correct!":choice<0?"Time’s up!":"Answer revealed";
  exp.textContent=(choice===q.correct?"Correct. ":"")+q.why;exp.classList.remove("hidden");
 }
 timer.textContent="Choose within "+remaining+" seconds";
 quizTimer=setInterval(()=>{remaining--;if(remaining<=0)reveal();else timer.textContent="Choose within "+remaining+" seconds"},1000);
}
document.getElementById("prev").onclick=()=>show(index-1);
document.getElementById("next").onclick=()=>show(index+1);
menu.onchange=()=>show(Number(menu.value));
document.getElementById("restart").onclick=()=>show(0);
document.getElementById("full").onclick=async()=>{try{if(!document.fullscreenElement)await document.documentElement.requestFullscreen();else await document.exitFullscreen()}catch(e){alert("Fullscreen is not available in this browser.")}};
document.getElementById("soundBtn").onclick=()=>{narrationOn=!narrationOn;document.getElementById("soundBtn").textContent=narrationOn?"🔊":"🔇";if(!narrationOn&&"speechSynthesis"in window)speechSynthesis.cancel();else speakSlide()};
document.getElementById("narrate").onclick=()=>{narrationOn=!narrationOn;document.getElementById("narrate").textContent="Narration: "+(narrationOn?"On":"Off");if(!narrationOn&&"speechSynthesis"in window)speechSynthesis.cancel();else speakSlide()};
document.getElementById("pause").onclick=()=>{if(!("speechSynthesis"in window))return;let b=document.getElementById("pause");if(speechSynthesis.paused){speechSynthesis.resume();b.textContent="Pause"}else if(speechSynthesis.speaking){speechSynthesis.pause();b.textContent="Resume"}};
document.getElementById("replay").onclick=speakSlide;
document.addEventListener("keydown",e=>{if(e.target.matches("select,button"))return;if(e.key==="ArrowRight")show(index+1);if(e.key==="ArrowLeft")show(index-1)});
document.getElementById("flipgrid").innerHTML=cards.map((c,i)=>`<button class="flip" aria-label="Flip study card ${i+1}"><span class="flipinner"><span class="face">Q${i+1}. ${c[0]}</span><span class="face back">${c[1]}</span></span></button>`).join("");
document.querySelectorAll(".flip").forEach(b=>b.onclick=()=>b.classList.toggle("flipped"));
function runRapid(){
 rapidIndex++;
 if(rapidIndex>=rapid.length)rapidIndex=0;
 const [q,a]=rapid[rapidIndex], qEl=document.getElementById("rapidQ"),aEl=document.getElementById("rapidA");
 qEl.textContent=(rapidIndex+1)+". "+q;aEl.classList.add("hidden");clearTimeout(rapidTimer);
 rapidTimer=setTimeout(()=>{aEl.textContent="Answer: "+a;aEl.classList.remove("hidden")},3000);
}
document.getElementById("rapidNext").onclick=runRapid;
document.getElementById("rapidReplay").onclick=()=>{rapidIndex=-1;runRapid()};
if("speechSynthesis"in window)speechSynthesis.onvoiceschanged=()=>{};
show(0);
})();
</script>
</body>
</html>
