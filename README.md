[index.html](https://github.com/user-attachments/files/31093859/index.html)
<!doctype html>
<html lang="ja">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>千葉県豆腐商工業協同組合</title>

<style>
:root {
  --paper:#faf8f1;
  --paper-dark:#f1ebdd;
  --navy:#17324d;
  --ink:#29333a;
  --red:#b84035;
  --line:rgba(23,50,77,.25);
}

* {
  box-sizing:border-box;
}

html {
  scroll-behavior:smooth;
}

body {
  margin:0;
  color:var(--ink);
  background-color:var(--paper);
  font-family:"Yu Gothic","Hiragino Kaku Gothic ProN",sans-serif;
}

button,
input {
  font:inherit;
}

.wrap {
  width:min(1240px,calc(100% - 48px));
  margin:auto;
}

/* 上部 */

.utility {
  height:44px;
  border-bottom:1px solid var(--line);
  font-size:12px;
}

.utility .wrap {
  display:flex;
  align-items:center;
  justify-content:space-between;
  height:100%;
}

.header {
  display:flex;
  align-items:center;
  justify-content:space-between;
  height:84px;
}

.logo {
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:22px;
  font-weight:bold;
  letter-spacing:.08em;
}

nav {
  display:flex;
  gap:45px;
}

nav a {
  color:var(--ink);
  font-size:14px;
  font-weight:bold;
  text-decoration:none;
}

nav a:hover {
  color:var(--red);
}

/* メイン画像部分 */

.hero {
  display:grid;
  grid-template-columns:1fr 1.1fr;
  min-height:555px;
  overflow:hidden;
}

.hero-copy {
  padding-top:65px;
  padding-right:40px;
  padding-bottom:55px;
  padding-left:max(48px,calc((100vw - 1240px)/2));
}

.english {
  color:var(--red);
  font-size:11px;
  font-weight:bold;
  letter-spacing:.22em;
}

h1 {
  margin:25px 0;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:clamp(48px,5vw,72px);
  font-weight:600;
  line-height:1.4;
  letter-spacing:.07em;
  white-space:nowrap;
}

.stamp {
  display:inline-block;
  margin-left:14px;
  padding:4px;
  border:2px solid var(--red);
  color:var(--red);
  font:700 12px "Yu Mincho",serif;
  letter-spacing:0;
  vertical-align:middle;
}

.hero-text {
  font-family:"Yu Mincho",serif;
  font-size:18px;
  line-height:2;
  letter-spacing:.1em;
}

.main-button {
  display:flex;
  align-items:center;
  justify-content:space-around;
  width:min(390px,100%);
  height:70px;
  margin-top:28px;
  border:2px solid var(--navy);
  background:transparent;
  color:var(--navy);
  cursor:pointer;
  font-size:17px;
  font-weight:bold;
  letter-spacing:.1em;
}

.main-button:hover {
  background:var(--navy);
  color:white;
}

/*
写真の指定です。
HTMLと同じ場所にある「tofu-photo.png」を表示します。
*/

.hero-photo {
  min-height:555px;

  background-image:
    linear-gradient(
      90deg,
      var(--paper) 0%,
      rgba(250,248,241,.75) 8%,
      transparent 25%
    ),
    url("tofu-photo.png");

  background-position:center;
  background-size:cover;
  background-repeat:no-repeat;
}

/* 地域ボタン */

.regions {
  padding:35px 0 72px;
}

.regions h2 {
  display:flex;
  align-items:center;
  justify-content:center;
  gap:25px;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:25px;
  letter-spacing:.12em;
}

.regions h2::before,
.regions h2::after {
  width:65px;
  height:1px;
  background:var(--line);
  content:"";
}

.region-grid {
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:13px;
  margin-top:28px;
}

.region-grid button {
  display:flex;
  align-items:center;
  justify-content:space-between;
  height:100px;
  padding:18px 22px;
  border:1px solid rgba(23,50,77,.55);
  background:rgba(255,255,255,.3);
  color:var(--navy);
  cursor:pointer;
  font-family:"Yu Mincho",serif;
  font-size:18px;
  font-weight:bold;
}

.region-grid button:hover {
  background:var(--paper-dark);
  transform:translateY(-2px);
}

.region-symbol {
  display:grid;
  place-items:center;
  width:42px;
  height:42px;
  border:1px solid var(--navy);
  border-radius:50%;
  font-size:13px;
}

.arrow {
  color:var(--red);
  font-size:25px;
}

/* 店舗検索 */

.search-section {
  padding:95px 0 105px;
  border-top:1px solid var(--line);
  background:#fffdf8;
}

.section-english {
  color:var(--red);
  font-size:11px;
  font-weight:bold;
  letter-spacing:.22em;
}

.search-section > .wrap > h2 {
  margin:14px 0;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:40px;
  letter-spacing:.08em;
}

.search-description {
  margin:0 0 38px;
  color:#687078;
}

.search-container {
  display:grid;
  grid-template-columns:330px 1fr;
  border:1px solid var(--line);
  background:var(--paper);
  box-shadow:0 20px 60px rgba(23,50,77,.08);
}

/* 左側の市区町村 */

.city-panel {
  padding:28px;
  border-right:1px solid var(--line);
  background:var(--paper-dark);
}

.city-panel label {
  font-size:12px;
  font-weight:bold;
}

.keyword-box {
  display:flex;
  align-items:center;
  height:48px;
  margin:10px 0 28px;
  border:1px solid var(--line);
  background:white;
}

.keyword-box input {
  width:100%;
  height:100%;
  padding:0 13px;
  border:0;
  outline:0;
  background:transparent;
}

.city-panel h3 {
  padding-bottom:12px;
  border-bottom:2px solid var(--navy);
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:18px;
}

.city-list {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:1px;
  background:var(--line);
}

.city-list button {
  display:flex;
  align-items:center;
  justify-content:space-between;
  height:45px;
  padding:0 10px;
  border:0;
  background:#fffdf8;
  color:var(--ink);
  cursor:pointer;
  font-size:13px;
}

.city-list button:hover,
.city-list button.active {
  background:var(--navy);
  color:white;
}

.city-list button b {
  color:var(--red);
  font-size:10px;
}

.city-list button.active b {
  color:#f2bbb5;
}

/* 右側の店舗一覧 */

.results-panel {
  padding:32px 40px;
}

.results-header {
  display:flex;
  align-items:end;
  justify-content:space-between;
  padding-bottom:17px;
  border-bottom:2px solid var(--navy);
}

.results-header small {
  display:block;
  color:#777;
  letter-spacing:.14em;
}

.results-header h3 {
  margin:5px 0 0;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:31px;
}

.shop-count {
  padding:8px 17px;
  background:var(--navy);
  color:white;
  font-size:13px;
}

.shop-card {
  display:grid;
  grid-template-columns:48px 1fr auto;
  gap:20px;
  align-items:center;
  padding:27px 0;
  border-bottom:1px solid var(--line);
}

.shop-number {
  color:var(--red);
  font-family:"Yu Mincho",serif;
  font-size:18px;
}

.shop-category {
  margin:0 0 5px;
  color:#6f7471;
  font-size:11px;
}

.shop-card h4 {
  margin:0 0 9px;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:22px;
}

.shop-address {
  margin:0 0 7px;
  font-size:13px;
}

.shop-card a {
  color:var(--navy);
  font-size:13px;
  font-weight:bold;
}

.map-link {
  white-space:nowrap;
  text-decoration:none;
  border-bottom:1px solid var(--navy);
  padding-bottom:4px;
}

.empty {
  padding:75px 20px;
  text-align:center;
}

.empty-symbol {
  display:inline-grid;
  place-items:center;
  width:58px;
  height:58px;
  border:1px solid var(--red);
  border-radius:50%;
  color:var(--red);
}

.empty h4 {
  margin-bottom:8px;
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:22px;
}

.data-note {
  margin-top:26px;
  color:#8a8178;
  font-size:11px;
  line-height:1.7;
}

/* 組合紹介 */

.about {
  padding:100px 20px;
  text-align:center;
}

.about h2 {
  color:var(--navy);
  font-family:"Yu Mincho",serif;
  font-size:36px;
}

.about p {
  font-family:"Yu Mincho",serif;
  line-height:2;
}

/* フッター */

footer {
  padding:32px 0;
  background:var(--navy);
  color:white;
}

footer .wrap {
  display:flex;
  align-items:center;
  justify-content:space-between;
}

footer strong {
  font-family:"Yu Mincho",serif;
}

footer small {
  opacity:.7;
}

/* スマートフォン対応 */

@media(max-width:900px) {
  nav {
    display:none;
  }

  .header {
    height:70px;
  }

  .hero {
    grid-template-columns:1fr;
  }

  .hero-photo {
    order:-1;
    min-height:340px;

    background-image:
      linear-gradient(
        0deg,
        var(--paper) 0%,
        transparent 28%
      ),
      url("tofu-photo.png");
  }

  .hero-copy {
    padding:40px 24px 55px;
  }

  h1 {
    white-space:normal;
  }

  .region-grid {
    grid-template-columns:1fr 1fr;
  }

  .search-container {
    grid-template-columns:1fr;
  }

  .city-panel {
    border-right:0;
    border-bottom:1px solid var(--line);
  }

  .results-panel {
    padding:28px 22px;
  }

  .shop-card {
    grid-template-columns:38px 1fr;
  }

  .map-link {
    grid-column:2;
    justify-self:start;
  }
}

@media(max-width:560px) {
  .wrap {
    width:calc(100% - 28px);
  }

  .utility {
    height:36px;
  }

  .utility span:last-child {
    display:none;
  }

  .logo {
    font-size:17px;
  }

  .hero-photo {
    min-height:260px;
  }

  h1 {
    font-size:39px;
  }

  .region-grid {
    grid-template-columns:1fr;
  }

  .region-grid button {
    height:72px;
  }

  .search-section {
    padding:70px 0;
  }

  .search-section > .wrap > h2 {
    font-size:30px;
  }

  .city-panel {
    padding:22px 16px;
  }

  .city-list button {
    height:48px;
  }

  .results-header h3 {
    font-size:26px;
  }

  .shop-card h4 {
    font-size:19px;
  }

  footer .wrap {
    display:grid;
    gap:12px;
  }
}
</style>
</head>

<body>

<div class="utility">
  <div class="wrap">
    <span>千葉県豆腐商工業協同組合</span>
    <span>お知らせ一覧　｜　組合員専用ページ</span>
  </div>
</div>

<header class="header wrap">
  <div class="logo">千葉県豆腐商工業協同組合</div>

  <nav>
    <a href="#about">組合について</a>
    <a href="#shop-search">豆腐店を探す</a>
    <a href="#about">豆腐のこと</a>
    <a href="#about">お知らせ</a>
  </nav>
</header>

<section class="hero">
  <div class="hero-copy">
    <div class="english">CHIBA TOFU ASSOCIATION</div>

    <h1>
      千葉のまちの、<br>
      おとうふ屋さん。
      <span class="stamp">豆腐</span>
    </h1>

    <p class="hero-text">
      毎日の食卓を支える、<br>
      千葉県内の豆腐店をご紹介します。
    </p>

    <button class="main-button" onclick="goToSearch()">
      <span>お近くの豆腐店を探す</span>
      <span>→</span>
    </button>
  </div>

  <div
    class="hero-photo"
    role="img"
    aria-label="木枠で豆腐を作る職人の手元">
  </div>
</section>

<section class="regions">
  <h2>地域から探す</h2>

  <div class="region-grid wrap">
    <button onclick="selectRegion('千葉市')">
      <span class="region-symbol">灯</span>
      <span>千葉</span>
      <span class="arrow">›</span>
    </button>

    <button onclick="selectRegion('松戸市')">
      <span class="region-symbol">森</span>
      <span>東葛</span>
      <span class="arrow">›</span>
    </button>

    <button onclick="selectRegion('成田市')">
      <span class="region-symbol">城</span>
      <span>北総</span>
      <span class="arrow">›</span>
    </button>

    <button onclick="selectRegion('茂原市')">
      <span class="region-symbol">波</span>
      <span>九十九里</span>
      <span class="arrow">›</span>
    </button>

    <button onclick="selectRegion('木更津市')">
      <span class="region-symbol">山</span>
      <span>南房総</span>
      <span class="arrow">›</span>
    </button>
  </div>
</section>

<section class="search-section" id="shop-search">
  <div class="wrap">
    <div class="section-english">TOFU SHOP SEARCH</div>

    <h2>お近くの豆腐店を探す</h2>

    <p class="search-description">
      左の市区町村を選ぶと、その地域の豆腐店が右側に表示されます。
    </p>

    <div class="search-container">
      <aside class="city-panel">
        <label for="keyword">店名・住所から絞り込む</label>

        <div class="keyword-box">
          <input
            id="keyword"
            type="text"
            placeholder="例：国産大豆"
            oninput="displayShops()">
        </div>

        <h3>市区町村から探す</h3>

        <div class="city-list" id="cityList"></div>
      </aside>

      <div class="results-panel">
        <div class="results-header">
          <div>
            <small>選択中の地域</small>
            <h3 id="selectedCity">千葉市</h3>
          </div>

          <span class="shop-count" id="shopCount">0 店舗</span>
        </div>

        <div id="shopList"></div>

        <p class="data-note">
          ※現在の店舗情報は画面確認用のサンプルです。
          正式公開時に組合加盟店の実データへ差し替えてください。
        </p>
      </div>
    </div>
  </div>
</section>

<section class="about" id="about">
  <div class="section-english">ABOUT US</div>

  <h2>千葉の豆腐文化を、次の世代へ。</h2>

  <p>
    千葉県豆腐商工業協同組合は、地域の豆腐店とともに、<br>
    安全でおいしい豆腐づくりと食文化の発展を支えています。
  </p>
</section>

<footer>
  <div class="wrap">
    <strong>千葉県豆腐商工業協同組合</strong>
    <small>© Chiba Tofu Association</small>
  </div>
</footer>

<script>
const municipalities = [
  "千葉市",
  "市川市",
  "船橋市",
  "松戸市",
  "柏市",
  "市原市",
  "習志野市",
  "八千代市",
  "浦安市",
  "流山市",
  "我孫子市",
  "鎌ケ谷市",
  "成田市",
  "佐倉市",
  "八街市",
  "印西市",
  "木更津市",
  "君津市",
  "茂原市",
  "館山市"
];

/*
店舗情報はここで変更できます。
同じ形式で追加してください。
*/

const shops = [
  {
    name:"とうふ工房 しろかわ",
    city:"千葉市",
    address:"千葉県千葉市中央区本町2-8-4",
    phone:"043-000-1028",
    category:"国産大豆・店頭販売"
  },
  {
    name:"豆の香 千葉店",
    city:"千葉市",
    address:"千葉県千葉市稲毛区小仲台4-12-6",
    phone:"043-000-1182",
    category:"木綿豆腐・絹ごし豆腐"
  },
  {
    name:"房総とうふ店",
    city:"千葉市",
    address:"千葉県千葉市若葉区桜木5-3-2",
    phone:"043-000-2350",
    category:"手づくり豆腐・油揚げ"
  },
  {
    name:"いちかわ豆腐舗",
    city:"市川市",
    address:"千葉県市川市八幡3-6-1",
    phone:"047-000-1028",
    category:"国産大豆・おぼろ豆腐"
  },
  {
    name:"船橋まちの豆腐屋",
    city:"船橋市",
    address:"千葉県船橋市本町4-18-7",
    phone:"047-000-1120",
    category:"店頭販売・豆乳"
  },
  {
    name:"とうふ処 松の葉",
    city:"松戸市",
    address:"千葉県松戸市小根本15-3",
    phone:"047-000-2102",
    category:"手揚げ油揚げ"
  },
  {
    name:"柏大豆工房",
    city:"柏市",
    address:"千葉県柏市柏3-5-8",
    phone:"04-0000-1028",
    category:"国産大豆・直売"
  },
  {
    name:"上総とうふ",
    city:"木更津市",
    address:"千葉県木更津市中央1-9-5",
    phone:"0438-00-1028",
    category:"寄せ豆腐・がんも"
  },
  {
    name:"九十九里豆腐店",
    city:"茂原市",
    address:"千葉県茂原市町保7-12",
    phone:"0475-00-1028",
    category:"昔ながらの木綿豆腐"
  }
];

let currentCity = "千葉市";

function escapeHtml(text) {
  return String(text).replace(/[&<>"']/g,function(character) {
    const replacements = {
      "&":"&amp;",
      "<":"&lt;",
      ">":"&gt;",
      '"':"&quot;",
      "'":"&#39;"
    };

    return replacements[character];
  });
}

function createCityButtons() {
  const cityList = document.getElementById("cityList");

  cityList.innerHTML = municipalities.map(function(city) {
    const numberOfShops = shops.filter(function(shop) {
      return shop.city === city;
    }).length;

    const activeClass =
      city === currentCity ? "active" : "";

    return `
      <button
        class="${activeClass}"
        onclick="selectCity('${city}')">

        <span>${city}</span>
        <b>${numberOfShops || "–"}</b>
      </button>
    `;
  }).join("");
}

function selectCity(city) {
  currentCity = city;
  createCityButtons();
  displayShops();
}

function displayShops() {
  const keyword =
    document.getElementById("keyword")
    .value
    .trim()
    .toLowerCase();

  const filteredShops = shops.filter(function(shop) {
    const matchesCity =
      shop.city === currentCity;

    const searchableText =
      shop.name +
      shop.address +
      shop.category;

    const matchesKeyword =
      keyword === "" ||
      searchableText.toLowerCase().includes(keyword);

    return matchesCity && matchesKeyword;
  });

  document.getElementById("selectedCity").textContent =
    currentCity;

  document.getElementById("shopCount").textContent =
    filteredShops.length + " 店舗";

  if (filteredShops.length === 0) {
    document.getElementById("shopList").innerHTML = `
      <div class="empty">
        <span class="empty-symbol">豆</span>
        <h4>掲載準備中です</h4>
        <p>
          ${escapeHtml(currentCity)}の組合加盟店情報は、
          順次追加いたします。
        </p>
      </div>
    `;

    return;
  }

  document.getElementById("shopList").innerHTML =
    filteredShops.map(function(shop,index) {
      const mapUrl =
        "https://www.google.com/maps/search/?api=1&query=" +
        encodeURIComponent(shop.address);

      return `
        <article class="shop-card">
          <span class="shop-number">
            ${String(index + 1).padStart(2,"0")}
          </span>

          <div>
            <p class="shop-category">
              ${escapeHtml(shop.category)}
            </p>

            <h4>${escapeHtml(shop.name)}</h4>

            <p class="shop-address">
              ${escapeHtml(shop.address)}
            </p>

            <a href="tel:${escapeHtml(shop.phone)}">
              TEL ${escapeHtml(shop.phone)}
            </a>
          </div>

          <a
            class="map-link"
            href="${mapUrl}"
            target="_blank"
            rel="noopener">
            地図を見る ↗
          </a>
        </article>
      `;
    }).join("");
}

function goToSearch() {
  document.getElementById("shop-search").scrollIntoView({
    behavior:"smooth"
  });
}

function selectRegion(city) {
  selectCity(city);
  goToSearch();
}

createCityButtons();
displayShops();
</script>

</body>
</html>
