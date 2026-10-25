
<!DOCTYPE html>
<html lang="si">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>EduLanka - A/L Education</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f1f5fb;
  color: #183653;
}

header {
  background: #123b65;
  color: white;
  text-align: center;
  padding: 22px 12px;
}

header h1 { margin: 0; font-size: 32px; }
header p { margin-bottom: 0; }

nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 7px;
  padding: 10px;
  background: #092b49;
}

nav button {
  border: 0;
  border-radius: 7px;
  padding: 10px 12px;
  background: transparent;
  color: white;
  cursor: pointer;
}

nav button:hover { background: #087f8c; }

main {
  max-width: 950px;
  margin: auto;
  padding: 18px 14px;
}

.page { display: none; }
.page.active { display: block; }

.hero {
  text-align: center;
  padding: 32px 15px;
  background: #dff5f3;
  border-radius: 16px;
}

.hero h2 { font-size: 28px; }

.hero p {
  line-height: 1.8;
}

h2.section-title { text-align: center; }

.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-top: 20px;
}

.card {
  padding: 18px 13px;
  background: white;
  border-radius: 14px;
  box-shadow: 0 3px 12px #dbe5ef;
  text-align: center;
}

.emoji { font-size: 38px; }

.card h3 { font-size: 18px; }

.card p {
  font-size: 14px;
  line-height: 1.7;
}

.btn {
  display: inline-block;
  width: 100%;
  padding: 12px;
  margin-top: 10px;
  border: 0;
  border-radius: 8px;
  background: #087f8c;
  color: white;
  text-decoration: none;
  font-weight: bold;
  font-size: 14px;
  cursor: pointer;
}

.btn:hover { background: #075d67; }

.btn.dark { background: #123b65; }

.panel {
  padding: 18px;
  margin: 18px 0;
  background: white;
  border-radius: 14px;
  box-shadow: 0 3px 12px #dbe5ef;
}

input, select, textarea {
  display: block;
  width: 100%;
  padding: 12px;
  margin: 8px 0 15px;
  border: 1px solid #b9c9da;
  border-radius: 8px;
  font-size: 16px;
  background: white;
}

label {
  display: block;
  font-weight: bold;
  margin-top: 12px;
}

.note {
  font-size: 13px;
  line-height: 1.7;
  color: #52657a;
}

.result {
  margin-top: 15px;
  padding: 14px;
  background: #e7f6f4;
  border-radius: 10px;
  line-height: 1.8;
  overflow-wrap: anywhere;
}

footer {
  margin-top: 25px;
  padding: 23px 12px;
  background: #123b65;
  color: white;
  text-align: center;
  line-height: 1.8;
}

@media (max-width: 380px) {
  .grid { grid-template-columns: 1fr; }
  .hero h2 { font-size: 23px; }
}
</style>
</head>

<body>

<header>
  <h1>🎓 EduLanka</h1>
  <p>ඔබේ A/L ගමනට ශක්තියක්!</p>
</header>

<nav>
  <button onclick="showPage('home')">🏠 Home</button>
  <button onclick="showPage('subjects')">📚 විෂයයන්</button>
  <button onclick="showPage('papers')">📄 Past Papers</button>
  <button onclick="showPage('notes')">📝 සටහන්</button>
  <button onclick="showPage('quiz')">🎯 Quiz</button>
</nav>

<main>

<!-- HOME PAGE -->
<section id="home" class="page active">
  <div class="hero">
    <h2>ඉගෙනුමෙන් ජයගමු! 🌟</h2>
    <p>
      A/L සිසුන් සඳහා විෂයයන්, ප්‍රශ්න පත්‍ර,
      පාඩම් සටහන් සහ දැනුම පරීක්ෂා කිරීමේ පහසුකම්
      එකම තැනකින් ලබාගන්න.
    </p>
    <button class="btn" style="max-width:250px"
      onclick="showPage('subjects')">
      ඉගෙනීම ආරම්භ කරන්න
    </button>
  </div>

  <h2 class="section-title">අපගේ සේවා</h2>

  <div class="grid">
    <div class="card">
      <div class="emoji">📚</div>
      <h3>A/L විෂයයන්</h3>
      <p>විෂය ධාරාව තෝරා අදාළ විෂයයන් බලන්න.</p>
      <button class="btn" onclick="showPage('subjects')">
        විෂයයන් බලන්න
      </button>
    </div>

    <div class="card">
      <div class="emoji">📄</div>
      <h3>Past Papers</h3>
      <p>විභාග වර්ෂය සහ විෂයය අනුව සොයන්න.</p>
      <button class="btn" onclick="showPage('papers')">
        ප්‍රශ්න පත්‍ර සොයන්න
      </button>
    </div>

    <div class="card">
      <div class="emoji">📝</div>
      <h3>පාඩම් සටහන්</h3>
      <p>විෂයයන් සඳහා අධ්‍යයන සම්පත් සොයන්න.</p>
      <button class="btn" onclick="showPage('notes')">
        සටහන් බලන්න
      </button>
    </div>

    <div class="card">
      <div class="emoji">🎯</div>
      <h3>Online Quiz</h3>
      <p>ප්‍රශ්නවලට පිළිතුරු දී දැනුම පරීක්ෂා කරන්න.</p>
      <button class="btn" onclick="showPage('quiz')">
        Quiz ආරම්භ කරන්න
      </button>
    </div>
  </div>

  <div class="panel">
    <h3>💙 EduLanka ගැන</h3>
    <p>ශ්‍රී ලංකාවේ A/L සිසුන්ට අධ්‍යාපනික සම්පත්
    පහසුවෙන් සොයාගැනීමට උදව් කිරීම අපේ අරමුණයි.</p>
  </div>
</section>

<!-- SUBJECTS PAGE -->
<section id="subjects" class="page">
  <h2>📚 A/L විෂය ධාරා</h2>
  <p>විෂය ධාරාවක් තෝරා විෂය ලැයිස්තුව බලන්න.</p>

  <label for="stream">විෂය ධාරාව සොයන්න</label>
  <input id="streamSearch" placeholder="උදා: ගණිත, වාණිජ"
    oninput="filterStreams()">

  <div class="grid" id="streamGrid">
    <div class="card stream-card">
      <div class="emoji">🔬</div>
      <h3>ජීව විද්‍යා අංශය</h3>
      <p>Biology, Physics, Chemistry</p>
      <button class="btn" onclick="showStream('bio')">විෂයයන් බලන්න</button>
    </div>

    <div class="card stream-card">
      <div class="emoji">📐</div>
      <h3>ගණිත අංශය</h3>
      <p>Combined Mathematics, Physics, Chemistry</p>
      <button class="btn" onclick="showStream('maths')">විෂයයන් බලන්න</button>
    </div>

    <div class="card stream-card">
      <div class="emoji">💼</div>
      <h3>වාණිජ අංශය</h3>
      <p>Accounting, Business Studies, Economics</p>
      <button class="btn" onclick="showStream('commerce')">විෂයයන් බලන්න</button>
    </div>

    <div class="card stream-card">
      <div class="emoji">📖</div>
      <h3>කලා අංශය</h3>
      <p>භාෂා, ඉතිහාසය සහ සමාජ විද්‍යාව</p>
      <button class="btn" onclick="showStream('arts')">විෂයයන් බලන්න</button>
    </div>

    <div class="card stream-card">
      <div class="emoji">💻</div>
      <h3>තාක්ෂණවේදය අංශය</h3>
      <p>ET, BST, SFT සහ ICT</p>
      <button class="btn" onclick="showStream('tech')">විෂයයන් බලන්න</button>
    </div>
  </div>

  <div id="streamDetails" class="panel" style="display:none">
    <h3 id="streamTitle"></h3>
    <div id="streamList"></div>
    <button class="btn dark" onclick="hideStream()">← ආපසු යන්න</button>
  </div>
</section>

<!-- PAST PAPERS PAGE -->
<section id="papers" class="page">
  <h2>📄 A/L Past Papers</h2>
  <p>විෂයය සහ වර්ෂය තෝරා ප්‍රශ්න පත්‍ර සොයන්න.</p>

  <div class="panel">
    <label for="paperSubject">විෂයය</label>
    <select id="paperSubject">
      <option value="Combined Mathematics">සංයුක්ත ගණිතය</option>
      <option value="Physics">භෞතික විද්‍යාව</option>
      <option value="Chemistry">රසායන විද්‍යාව</option>
      <option value="Biology">ජීව විද්‍යාව</option>
      <option value="Accounting">ගිණුම්කරණය</option>
      <option value="Business Studies">ව්‍යාපාර අධ්‍යයනය</option>
      <option value="Economics">ආර්ථික විද්‍යාව</option>
      <option value="ICT">ICT</option>
      <option value="History">ඉතිහාසය</option>
      <option value="Sinhala">සිංහල</option>
    </select>

    <label for="paperYear">වර්ෂය</label>
    <select id="paperYear">
      <option>2025</option>
      <option>2024</option>
      <option>2023</option>
      <option>2022</option>
      <option>2021</option>
      <option>2020</option>
      <option>2019</option>
      <option>2018</option>
      <option>2017</option>
      <option>2016</option>
      <option>2015</option>
    </select>

    <label for="paperLanguage">භාෂාව</label>
    <select id="paperLanguage">
      <option value="Sinhala">සිංහල</option>
      <option value="English">ඉංග්‍රීසි</option>
      <option value="Tamil">දෙමළ</option>
    </select>

    <label for="paperType">ලේඛනය</label>
    <select id="paperType">
      <option value="past paper PDF">ප්‍රශ්න පත්‍රය</option>
      <option value="marking scheme PDF">ලකුණු දීමේ පටිපාටිය</option>
    </select>

    <button class="btn" onclick="searchPapers()">🔎 සොයන්න</button>
    <div id="paperMessage" aria-live="polite"></div>
  </div>

  <div class="panel">
    <h3>නිල අධ්‍යාපනික සම්පත්</h3>
    <a href="https://www.exams.gov.lk/" target="_blank"
      rel="noopener" class="btn dark">
      විභාග දෙපාර්තමේන්තුව
    </a>
    <a href="https://e-thaksalawa.moe.gov.lk/"
      target="_blank" rel="noopener" class="btn dark">
      e-Thaksalawa
    </a>
    <p class="note">මෙම සෙවුම Google ප්‍රතිඵල පෙන්වයි.
    සියලුම ලේඛන නිල PDF බවට සහතිකයක් නැත.
    විශ්වාසදායක මූලාශ්‍ර තෝරන්න.</p>
  </div>
</section>

<!-- NOTES PAGE -->
<section id="notes" class="page">
  <h2>📝 පාඩම් සහ කෙටි සටහන්</h2>
  <p>විෂයය තෝරා අධ්‍යයන සම්පත් සොයන්න.</p>

  <div class="panel">
    <label for="noteSubject">විෂයය</label>
    <select id="noteSubject">
      <option value="Biology">ජීව විද්‍යාව</option>
      <option value="Combined Mathematics">සංයුක්ත ගණිතය</option>
      <option value="Physics">භෞතික විද්‍යාව</option>
      <option value="Chemistry">රසායන විද්‍යාව</option>
      <option value="Accounting">ගිණුම්කරණය</option>
      <option value="Economics">ආර්ථික විද්‍යාව</option>
      <option value="ICT">ICT</option>
      <option value="History">ඉතිහාසය</option>
      <option value="Sinhala">සිංහල</option>
    </select>

    <button class="btn" onclick="searchNotes()">සටහන් සොයන්න</button>
  </div>

  <div class="panel">
    <h3>අධ්‍යාපනික සම්පත්</h3>
    <p>අධ්‍යාපනික සම්පත් සඳහා e-Thaksalawa බලන්න.</p>
    <a class="btn dark" href="https://e-thaksalawa.moe.gov.lk/"
      target="_blank" rel="noopener">e-Thaksalawa විවෘත කරන්න</a>
  </div>
</section>

<!-- QUIZ PAGE -->
<section id="quiz" class="page">
  <h2>🎯 සාමාන්‍ය දැනුම Quiz</h2>
  <p>ප්‍රශ්න 5කට පිළිතුරු දෙන්න.</p>

  <div class="panel" id="quizBox">
    <div id="questionArea"></div>
    <button class="btn" id="nextBtn" onclick="nextQuestion()">ඊළඟ ප්‍රශ්නය</button>
    <div id="quizResult" aria-live="polite"></div>
  </div>

  <p class="note">මෙය වෙබ් අඩවියේ ක්‍රියාකාරීත්වය පරීක්ෂා කිරීමට
  ඇතුළත් කළ සරල පුහුණු Quiz එකකි.</p>
</section>

</main>

<footer>
  <strong>🎓 EduLanka</strong><br>
  ඉගෙනුමෙන් ජයගමු!<br>
  © 2026 EduLanka
</footer>

<script>
function showPage(id) {
  document.querySelectorAll(".page").forEach(function(page) {
    page.classList.remove("active");
  });

  document.getElementById(id).classList.add("active");
  window.scrollTo(0, 0);
}

const streams = {
  bio: {
    title: "🔬 ජීව විද්‍යා අංශය",
    list: ["ජීව විද්‍යාව (Biology)", "භෞතික විද්‍යාව (Physics)", "රසායන විද්‍යාව (Chemistry)"]
  },
  maths: {
    title: "📐 ගණිත අංශය",
    list: ["සංයුක්ත ගණිතය (Combined Mathematics)", "භෞතික විද්‍යාව (Physics)", "රසායන විද්‍යාව (Chemistry)"]
  },
  commerce: {
    title: "💼 වාණිජ අංශය",
    list: ["ගිණුම්කරණය (Accounting)", "ව්‍යාපාර අධ්‍යයනය (Business Studies)", "ආර්ථික විද්‍යාව (Economics)"]
  },
  arts: {
    title: "📖 කලා අංශය",
    list: ["සිංහල", "ඉතිහාසය", "දේශපාලන විද්‍යාව", "භූගෝල විද්‍යාව", "බෞද්ධ ශිෂ්ටාචාරය"]
  },
  tech: {
    title: "💻 තාක්ෂණවේදය අංශය",
    list: ["ඉංජිනේරු තාක්ෂණවේදය (ET)", "ජෛව පද්ධති තාක්ෂණවේදය (BST)", "තාක්ෂණවේදය සඳහා විද්‍යාව (SFT)", "ICT"]
  }
};

function showStream(key) {
  const data = streams[key];
  document.getElementById("streamTitle").textContent = data.title;

  const list = document.getElementById("streamList");
  list.replaceChildren();

  data.list.forEach(function(subject) {
    const p = document.createElement("p");
    p.textContent = "📘 " + subject;
    list.appendChild(p);
  });

  document.getElementById("streamDetails").style.display = "block";
  document.getElementById("streamGrid").style.display = "none";
}

function hideStream() {
  document.getElementById("streamDetails").style.display = "none";
  document.getElementById("streamGrid").style.display = "grid";
}

function filterStreams() {
  const query = document.getElementById("streamSearch").value.toLowerCase();

  document.querySelectorAll(".stream-card").forEach(function(card) {
    card.style.display = card.textContent.toLowerCase().includes(query)
      ? "" : "none";
  });
}

function searchPapers() {
  const subject = document.getElementById("paperSubject").value;
  const year = document.getElementById("paperYear").value;
  const language = document.getElementById("paperLanguage").value;
  const type = document.getElementById("paperType").value;

  const query = "Sri Lanka GCE A/L " + year + " " + subject +
    " " + language + " medium " + type + " official";

  document.getElementById("paperMessage").textContent =
    "ඔබගේ සෙවුම සකස් කළා: " + subject + " - " + year +
    ". සෙවුම් ප්‍රතිඵල නව ටැබයක විවෘත වේ.";

  window.open("https://www.google.com/search?q=" +
    encodeURIComponent(query), "_blank");
}

function searchNotes() {
  const subject = document.getElementById("noteSubject").value;
  const query = "Sri Lanka A/L " + subject +
    " lesson notes PDF e-thaksalawa";

  window.open("https://www.google.com/search?q=" +
    encodeURIComponent(query), "_blank");
}

const questions = [
  {
    q: "ශ්‍රී ලංකාවේ අගනුවර කුමක්ද?",
    options: ["කොළඹ", "ශ්‍රී ජයවර්ධනපුර කෝට්ටේ", "මහනුවර"],
    answer: 1
  },
  {
    q: "ජලයේ රසායනික සූත්‍රය කුමක්ද?",
    options: ["CO2", "O2", "H2O"],
    answer: 2
  },
  {
    q: "පෘථිවිය වටා ගමන් කරන්නේ කුමක්ද?",
    options: ["සඳ", "අඟහරු", "සූර්යයා"],
    answer: 0
  },
  {
    q: "ගණිතයේ 5 × 6 කීයද?",
    options: ["25", "30", "35"],
    answer: 1
  },
  {
    q: "ශාක ප්‍රභාසංස්ලේෂණයට අවශ්‍ය වන්නේ කුමක්ද?",
    options: ["ආලෝකය", "ප්ලාස්ටික්", "යකඩ පමණක්"],
    answer: 0
  }
];

let quizIndex = 0;
let quizScore = 0;
let quizAnswered = false;

function renderQuestion() {
  const q = questions[quizIndex];
  quizAnswered = false;

  document.getElementById("quizResult").textContent = "";
  document.getElementById("nextBtn").textContent =
    quizIndex === questions.length - 1 ? "ප්‍රතිඵල බලන්න" : "ඊළඟ ප්‍රශ්නය";

  let html = "<h3>ප්‍රශ්නය " + (quizIndex + 1) + " / " +
    questions.length + "</h3><p>" + q.q + "</p>";

  q.options.forEach(function(option, index) {
    html += '<label style="font-weight:normal;display:block;margin:12px 0">' +
      '<input type="radio" name="quizAnswer" value="' + index +
      '" style="display:inline;width:auto;margin-right:8px">' +
      option + '</label>';
  });

  document.getElementById("questionArea").innerHTML = html;
}

function nextQuestion() {
  if (quizIndex >= questions.length) {
    quizIndex = 0;
    quizScore = 0;
    renderQuestion();
    return;
  }

  const selected = document.querySelector('input[name="quizAnswer"]:checked');

  if (!selected) {
    document.getElementById("quizResult").textContent =
      "කරුණාකර පිළිතුරක් තෝරන්න.";
    return;
  }

  if (quizAnswered) return;
  quizAnswered = true;

  if (Number(selected.value) === questions[quizIndex].answer) {
    quizScore++;
  }

  quizIndex++;

  if (quizIndex < questions.length) {
    renderQuestion();
  } else {
    document.getElementById("questionArea").innerHTML =
      "<h3>Quiz එක අවසන්! 🎉</h3>";

    document.getElementById("nextBtn").textContent = "නැවත Quiz කරන්න";

    document.getElementById("quizResult").textContent =
      "ඔබගේ ලකුණු: " + quizScore + " / " + questions.length;

    quizIndex = questions.length;
  }
}

renderQuestion();
</script>

</body>
</html>
