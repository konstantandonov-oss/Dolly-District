
<!DOCTYPE html>
<html lang="bg">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dolly District | Онлайн бутик</title>
<meta name="description" content="Открий своя стил с Dolly District — дрехи, обувки, чанти и аксесоари.">
<style>
:root {
  --bg: #fff;
  --cream: #f7f2eb;
  --gold: #b89563;
  --ink: #29251f;
  --muted: #81786e;
  --line: #e9e1d7;
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: Arial, Helvetica, sans-serif;
}
button, input { font: inherit; }
button, a { cursor: pointer; }
a { color: inherit; text-decoration: none; }
.announcement {
  background: var(--cream);
  color: #806644;
  padding: 11px;
  text-align: center;
  font-size: 10px;
  letter-spacing: 2px;
}
.wrap { max-width: 1240px; margin: auto; padding: 0 28px; }
header {
  min-height: 82px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  border-bottom: 1px solid var(--line);
}
.logo {
  font-family: Georgia, serif;
  font-size: 27px;
  white-space: nowrap;
}
.logo span { color: var(--gold); }
.navlinks { display: flex; gap: 23px; }
.navlinks a, .footer-links a {
  font-size: 10px;
  letter-spacing: 1.2px;
  text-transform: uppercase;
}
.navright { display: flex; align-items: center; gap: 9px; }
.search {
  width: 165px;
  padding: 11px;
  border: 1px solid var(--line);
  background: white;
  outline-color: var(--gold);
}
.pillbtn {
  padding: 11px 13px;
  border: 1px solid var(--line);
  background: white;
  color: var(--ink);
  font-size: 11px;
}
.cart-count {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 21px;
  height: 21px;
  margin-left: 5px;
  border-radius: 50%;
  background: var(--gold);
  color: white;
}
.hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 35px;
  align-items: center;
  padding-top: 40px;
  padding-bottom: 65px;
}
.eyebrow {
  color: var(--gold);
  font-size: 10px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
}
.hero h1 {
  margin: 22px 0;
  font: 400 clamp(48px, 6vw, 84px)/.98 Georgia, serif;
  letter-spacing: -3px;
}
.hero h1 em { color: var(--gold); }
.hero p {
  max-width: 390px;
  color: var(--muted);
  font-size: 14px;
  line-height: 1.9;
}
.primary {
  display: inline-block;
  margin-top: 16px;
  padding: 16px 22px;
  border: 0;
  background: var(--ink);
  color: white;
  font-size: 10px;
  letter-spacing: 1.5px;
}
.hero-art {
  position: relative;
  min-height: 480px;
  overflow: hidden;
  background: linear-gradient(145deg, #eee3d5, #c9b39a 55%, #88735e);
  display: flex;
  align-items: center;
  justify-content: center;
}
.hero-art:before {
  content: "";
  position: absolute;
  width: 48%;
  height: 75%;
  top: 16%;
  left: 27%;
  border-radius: 45% 45% 4% 4%;
  background: linear-gradient(120deg, #f4ede2, #c7b49d 65%, #8f7a65);
  box-shadow: 20px 25px 50px #45382a30;
  transform: rotate(-5deg);
}
.hero-art:after {
  content: "D";
  position: absolute;
  right: 4%;
  bottom: -20%;
  color: #fff;
  opacity: .35;
  font: 300 320px Georgia, serif;
}
.art-label, .art-note {
  position: absolute;
  z-index: 1;
  font-size: 10px;
  letter-spacing: 2px;
}
.art-label { top: 20px; left: 20px; background: white; padding: 10px; }
.art-note { bottom: 20px; left: 20px; color: white; }
.ticker {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 15px;
  padding: 21px 0;
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
  color: var(--muted);
  font-size: 9px;
  letter-spacing: 2px;
  text-transform: uppercase;
}
.gender-switch {
  display: flex;
  justify-content: center;
  padding-top: 35px;
}
.gender-switch button, .filter {
  padding: 12px 17px;
  border: 1px solid var(--line);
  background: white;
  color: var(--ink);
  font-size: 10px;
  letter-spacing: 1px;
}
.gender-switch button.active, .filter.active {
  background: var(--ink);
  color: white;
  border-color: var(--ink);
}
.section { padding-top: 70px; padding-bottom: 35px; }
.section-head {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 20px;
  margin-bottom: 28px;
}
h2 {
  margin: 12px 0 0;
  font: 400 clamp(35px, 4vw, 51px)/1.1 Georgia, serif;
}
.filters { display: flex; gap: 7px; flex-wrap: wrap; }
.filter { padding: 10px 12px; }
.products {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 20px;
}
.product { min-width: 0; }
.product-art {
  height: 300px;
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--tone, #eee7dd);
}
.product-art:before {
  content: "";
  position: absolute;
  width: 48%;
  height: 70%;
  top: 13%;
  left: 26%;
  background: var(--item, #aaa);
  clip-path: polygon(25% 0,75% 0,100% 20%,83% 35%,74% 26%,80% 100%,20% 100%,26% 26%,17% 35%,0 20%);
  filter: drop-shadow(10px 12px 12px #0002);
}
.product-art.bag:before {
  width: 48%; height: 48%; top: 32%;
  clip-path: polygon(10% 20%,90% 20%,100% 100%,0 100%);
  border-radius: 5px;
}
.product-art.bag:after {
  content: "";
  position: absolute;
  width: 24%; height: 23%;
  top: 19%; left: 38%;
  border: 6px solid var(--item, #aaa);
  border-bottom: 0;
  border-radius: 50% 50% 0 0;
}
.product-art.shoes:before {
  width: 68%; height: 28%; top: 48%; left: 16%;
  border-radius: 40%;
  clip-path: polygon(0 45%,50% 45%,67% 15%,80% 15%,83% 48%,100% 72%,100% 100%,0 100%);
}
.product-art.jewel:before {
  width: 35%; height: 42%; top: 28%;
  border: 5px solid var(--item, #aaa);
  border-radius: 50%; background: transparent; clip-path: none;
}
.tag {
  position: absolute;
  top: 12px; left: 12px;
  padding: 7px 9px;
  background: white;
  color: #806644;
  font-size: 9px;
  letter-spacing: 1px;
}
.add {
  position: absolute;
  right: 12px; bottom: 12px;
  width: 40px; height: 40px;
  border: 1px solid var(--line);
  background: white;
  color: var(--ink);
  font-size: 23px;
}
.add:hover { background: var(--ink); color: white; }
.product-info {
  display: flex;
  justify-content: space-between;
  gap: 8px;
  padding: 14px 0;
}
.product-name { font: 16px Georgia, serif; }
.product-type { margin-top: 6px; color: var(--muted); font-size: 10px; }
.price { white-space: nowrap; font-size: 12px; font-weight: bold; }
.categories {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}
.category {
  min-height: 230px;
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: white;
  background: linear-gradient(135deg, #d1bca4, #82705e);
}
.category:nth-child(2) { background: linear-gradient(135deg, #e9d9ca, #aa876c); }
.category:nth-child(3) { background: linear-gradient(135deg, #d9d3c8, #8c8174); }
.category small { letter-spacing: 2px; font-size: 10px; }
.category h3 { margin: 0; font: 34px Georgia, serif; }
.category a { font-size: 10px; letter-spacing: 1px; }
.banner {
  padding: 40px;
  background: var(--cream);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 25px;
}
.banner p { max-width: 340px; color: var(--muted); line-height: 1.8; font-size: 13px; }
.banner button {
  padding: 14px 18px;
  border: 0;
  background: var(--ink);
  color: white;
  font-size: 10px;
  letter-spacing: 1px;
}
footer { margin-top: 55px; padding-top: 35px; padding-bottom: 25px; border-top: 1px solid var(--line); }
.footer-top { display: flex; justify-content: space-between; gap: 25px; flex-wrap: wrap; }
footer p { max-width: 350px; color: var(--muted); font-size: 12px; line-height: 1.8; }
.footer-links { display: flex; gap: 18px; flex-wrap: wrap; }
.legal { margin-top: 25px; padding-top: 18px; border-top: 1px solid var(--line); color: var(--muted); font-size: 10px; }
.toast {
  display: none;
  position: fixed;
  z-index: 20;
  bottom: 20px; left: 50%;
  transform: translateX(-50%);
  padding: 14px 20px;
  background: var(--ink);
  color: white;
  font-size: 12px;
  max-width: 90%;
}
.toast.show { display: block; }
.modal {
  display: none;
  position: fixed;
  inset: 0;
  z-index: 30;
  background: #0008;
  align-items: center;
  justify-content: center;
  padding: 20px;
}
.modal.open { display: flex; }
.modal-card {
  width: min(460px, 100%);
  max-height: 85vh;
  overflow: auto;
  padding: 28px;
  background: white;
}
.modal-card h3 { font: 30px Georgia, serif; }
.modal-card p { color: var(--muted); font-size: 13px; line-height: 1.7; }
.close { float: right; padding: 8px; border: 1px solid var(--line); background: white; }
.cart-list { margin-top: 20px; border-top: 1px solid var(--line); }
.cart-row {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  padding: 13px 0;
  border-bottom: 1px solid var(--line);
  font-size: 12px;
}
.qty button { margin: 0 3px; border: 1px solid var(--line); background: white; }
@media(max-width:850px) {
  .navlinks { display: none; }
  .hero { grid-template-columns: 1fr; }
  .hero-art { min-height: 370px; }
  .products { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .product-art { height: 260px; }
  .categories { grid-template-columns: 1fr; }
  .category { min-height: 180px; }
  .section-head { align-items: start; flex-direction: column; }
  .banner { align-items: start; flex-direction: column; }
}
@media(max-width:480px) {
  .wrap { padding-left: 16px; padding-right: 16px; }
  header { min-height: 72px; gap: 8px; }
  .logo { font-size: 21px; }
  .search { width: 110px; padding: 9px 6px; font-size: 11px; }
  .pillbtn { padding: 9px 7px; font-size: 10px; }
  .hero { padding-top: 25px; }
  .hero-art { min-height: 300px; }
  .products { gap: 10px; }
  .product-art { height: 205px; }
  .product-name { font-size: 13px; }
  .price { font-size: 11px; }
  .gender-switch button { min-width: 0; padding: 12px 10px; }
  .filter { padding: 9px; font-size: 9px; }
  .banner { padding: 25px; }
}
</style>
</head>
<body>
<div class="announcement">DOLLY DISTRICT · СТИЛЪТ Е ЛИЧЕН</div>

<header class="wrap">
  <a class="logo" href="#home">Dolly District<span>.</span></a>
  <nav class="navlinks">
    <a href="#shop">Колекция</a>
    <a href="#categories">Категории</a>
    <a href="#about">За нас</a>
  </nav>
  <div class="navright">
    <input class="search" id="search" placeholder="Търси..." aria-label="Търси продукт">
    <button class="pillbtn" id="cartBtn">Количка <span class="cart-count" id="cartCount">0</span></button>
  </div>
</header>

<main>
<section class="wrap hero" id="home">
  <div>
    <div class="eyebrow">Нова колекция · 2026</div>
    <h1>Твоят стил.<br><em>Твоите</em><br>правила.</h1>
    <p>Открий модерни дрехи, чанти, обувки и аксесоари, подбрани за твоята индивидуалност. По-малко шум. Повече стил.</p>
    <a class="primary" href="#shop">РАЗГЛЕДАЙ КОЛЕКЦИЯТА ↗</a>
  </div>
  <div class="hero-art">
    <span class="art-label">THE NEW EDIT · 2026</span>
    <span class="art-note">LESS, BUT BETTER — DOLLY DISTRICT</span>
  </div>
</section>

<div class="ticker">
  <span>Подбрани находки</span><span>Градска естетика</span>
  <span>Стил без усилие</span><span>Нови фаворити</span>
</div>

<div class="wrap gender-switch" aria-label="Избери колекция">
  <button class="active" data-gender="all">Всички</button>
  <button data-gender="women">Дамска</button>
  <button data-gender="men">Мъжка</button>
</div>

<section class="wrap section" id="shop">
  <div class="section-head">
    <div><div class="eyebrow">Подбрано за теб</div><h2>Колекцията</h2></div>
    <div class="filters" id="filters">
      <button class="filter active" data-cat="all">Всички</button>
      <button class="filter" data-cat="Дрехи">Дрехи</button>
      <button class="filter" data-cat="Чанти">Чанти</button>
      <button class="filter" data-cat="Обувки">Обувки</button>
      <button class="filter" data-cat="Аксесоари">Аксесоари</button>
    </div>
  </div>
  <div class="products" id="products"></div>
</section>

<section class="wrap section" id="categories">
  <div class="section-head"><div><div class="eyebrow">Намери своята посока</div><h2>Пазарувай по стил</h2></div></div>
  <div class="categories">
    <div class="category"><small>01 / EVERYDAY</small><h3>Дрехи</h3><a href="#shop" data-goto="Дрехи">РАЗГЛЕДАЙ ↗</a></div>
    <div class="category"><small>02 / YOUR ESSENTIAL</small><h3>Чанти</h3><a href="#shop" data-goto="Чанти">РАЗГЛЕДАЙ ↗</a></div>
    <div class="category"><small>03 / FINISHING TOUCH</small><h3>Аксесоари</h3><a href="#shop" data-goto="Аксесоари">РАЗГЛЕДАЙ ↗</a></div>
  </div>
</section>

<section class="wrap section" id="about">
  <div class="banner">
    <div><div class="eyebrow">DOLLY DISTRICT NOTES</div><h2>Повече личен стил.</h2></div>
    <div><p>Нови идеи, любими находки и вдъхновение за ежедневната ти визия — всичко на едно място.</p><button id="newsletterBtn">БЪДИ В ЧАС ↗</button></div>
  </div>
</section>
</main>

<footer class="wrap">
  <div class="footer-top">
    <div><a class="logo" href="#home">Dolly District<span>.</span></a><p>Модерен онлайн бутик за дрехи и аксесоари. Изрази себе си с подбрани находки.</p></div>
    <div class="footer-links"><a href="#shop">Магазин</a><a href="#about">За нас</a><a href="#delivery">Доставка</a><a href="mailto:hello@dollydistrict.example">Контакти</a></div>
  </div>
  <div class="legal">© 2026 Dolly District · Демо магазин · Цените са примерни</div>
</footer>

<div class="toast" id="toast" role="status"></div>

<div class="modal" id="cartModal" role="dialog" aria-modal="true">
  <div class="modal-card">
    <button class="close" id="closeCart">Затвори ✕</button>
    <h3>Твоята количка</h3>
    <p>Прегледай избраните продукти.</p>
    <div class="cart-list" id="cartList"></div>
    <div style="display:flex;justify-content:space-between;padding:16px 0;font-weight:bold">
      <span>Общо</span><span id="cartTotal">€0,00</span>
    </div>
    <button class="primary" id="checkout" style="width:100%">КЪМ ПОРЪЧКА ↗</button>
    <p>Демо магазин: реални плащания и поръчки все още не са активирани.</p>
  </div>
</div>

<div class="modal" id="newsModal" role="dialog" aria-modal="true">
  <div class="modal-card">
    <button class="close" id="closeNews">Затвори ✕</button>
    <h3>Dolly District Notes</h3>
    <p>Абонирай се за нови колекции и модни идеи.</p>
    <form id="newsForm">
      <input type="email" required placeholder="Твоят имейл" style="width:100%;padding:13px;border:1px solid var(--line)">
      <button class="primary" type="submit">ЗАПИШИ МЕ ↗</button>
    </form>
    <p>Демо форма — не записва имейли към реална услуга.</p>
  </div>
</div>

<script>
const items = [
 {id:1,name:"Oversized тениска",cat:"Дрехи",gender:"women",price:24.90,type:"Свободна кройка · Памук",tone:"#e4dfd5",item:"#393a35",shape:"shirt",tag:"Бестселър"},
 {id:2,name:"Мини чанта Studio",cat:"Чанти",gender:"women",price:39.90,type:"Ежедневна · Минимал",tone:"#d9c7b7",item:"#6a4637",shape:"bag",tag:"Ново"},
 {id:3,name:"City Runner",cat:"Обувки",gender:"men",price:59.90,type:"Градски стил · Унисекс",tone:"#d8d9d4",item:"#e8e5dc",shape:"shoes",tag:"Тренд"},
 {id:4,name:"Обеци Orbit",cat:"Аксесоари",gender:"women",price:16.90,type:"Минималистични · Метал",tone:"#d5d0c5",item:"#b2a16c",shape:"jewel",tag:"Любими"},
 {id:5,name:"Риза Soft Structure",cat:"Дрехи",gender:"men",price:34.90,type:"Свободна кройка · Крем",tone:"#d9d6ca",item:"#f1eee4",shape:"shirt",tag:"Ново"},
 {id:6,name:"Shoulder Bag Mono",cat:"Чанти",gender:"women",price:44.90,type:"Компактна · Черна",tone:"#b9b8ae",item:"#252522",shape:"bag",tag:"Лимитирана"},
 {id:7,name:"Weekend Sneakers",cat:"Обувки",gender:"men",price:64.90,type:"Леки · Ежедневни",tone:"#d7c7b7",item:"#f0e5d8",shape:"shoes",tag:"Тренд"},
 {id:8,name:"Слънчеви очила Muse",cat:"Аксесоари",gender:"women",price:19.90,type:"Ретро силует",tone:"#c8c9bf",item:"#343630",shape:"jewel",tag:"Ново"}
];

let selected = "all";
let gender = "all";
let cart = [];

const products = document.getElementById("products");
const toast = document.getElementById("toast");
const cartModal = document.getElementById("cartModal");
const newsModal = document.getElementById("newsModal");

function money(n) {
  return "€" + n.toFixed(2).replace(".", ",");
}

function render() {
  const q = document.getElementById("search").value.trim().toLowerCase();
  const shown = items.filter(p =>
    (gender === "all" || p.gender === gender) &&
    (selected === "all" || p.cat === selected) &&
    (p.name + " " + p.cat + " " + p.type).toLowerCase().includes(q)
  );

  products.innerHTML = shown.map(p => `
    <article class="product">
      <div class="product-art ${p.shape}" style="--tone:${p.tone};--item:${p.item}">
        <span class="tag">${p.tag}</span>
        <button class="add" aria-label="Добави ${p.name}" data-add="${p.id}">+</button>
      </div>
      <div class="product-info">
        <div><div class="product-name">${p.name}</div><div class="product-type">${p.type}</div></div>
        <div class="price">${money(p.price)}</div>
      </div>
    </article>
  `).join("") || "<p>Няма намерени продукти. Опитай друга дума.</p>";
}

function notify(message) {
  toast.textContent = message;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 2500);
}

function updateCart() {
  document.getElementById("cartCount").textContent =
    cart.reduce((sum, p) => sum + p.qty, 0);

  document.getElementById("cartList").innerHTML = cart.length
    ? cart.map(p => `
      <div class="cart-row">
        <div>
          <strong>${p.name}</strong><br>
          ${money(p.price)} × ${p.qty}
          <div class="qty">
            <button data-minus="${p.id}" aria-label="Намали количеството">−</button>
            <button data-plus="${p.id}" aria-label="Увеличи количеството">+</button>
            <button data-remove="${p.id}">Премахни</button>
          </div>
        </div>
        <strong>${money(p.price * p.qty)}</strong>
      </div>
    `).join("")
    : "<p>Количката е празна засега.</p>";

  document.getElementById("cartTotal").textContent =
    money(cart.reduce((sum, p) => sum + p.price * p.qty, 0));
}

document.getElementById("filters").addEventListener("click", e => {
  const b = e.target.closest("[data-cat]");
  if (!b) return;
  selected = b.dataset.cat;
  document.querySelectorAll(".filter").forEach(x =>
    x.classList.toggle("active", x === b)
  );
  render();
});

document.querySelector(".gender-switch").addEventListener("click", e => {
  const b = e.target.closest("[data-gender]");
  if (!b) return;
  gender = b.dataset.gender;
  document.querySelectorAll("[data-gender]").forEach(x =>
    x.classList.toggle("active", x === b)
  );
  render();
  document.getElementById("shop").scrollIntoView({behavior:"smooth"});
});

products.addEventListener("click", e => {
  const b = e.target.closest("[data-add]");
  if (!b) return;
  const p = items.find(x => x.id === Number(b.dataset.add));
  const existing = cart.find(x => x.id === p.id);
  if (existing) existing.qty++;
  else cart.push({...p, qty:1});
  updateCart();
  notify("Добавено в количката: " + p.name);
});

document.getElementById("search").addEventListener("input", render);

document.querySelectorAll("[data-goto]").forEach(a => {
  a.addEventListener("click", () => {
    selected = a.dataset.goto;
    document.querySelectorAll(".filter").forEach(x =>
      x.classList.toggle("active", x.dataset.cat === selected)
    );
    render();
  });
});

document.getElementById("cartBtn").onclick = () => {
  updateCart();
  cartModal.classList.add("open");
};
document.getElementById("closeCart").onclick = () => cartModal.classList.remove("open");
document.getElementById("newsletterBtn").onclick = () => newsModal.classList.add("open");
document.getElementById("closeNews").onclick = () => newsModal.classList.remove("open");

document.getElementById("cartList").addEventListener("click", e => {
  const minus = e.target.closest("[data-minus]");
  const plus = e.target.closest("[data-plus]");
  const remove = e.target.closest("[data-remove]");

  if (minus) {
    const p = cart.find(x => x.id === Number(minus.dataset.minus));
    if (p) p.qty--;
    cart = cart.filter(x => x.qty > 0);
  }
  if (plus) {
    const p = cart.find(x => x.id === Number(plus.dataset.plus));
    if (p) p.qty++;
  }
  if (remove) cart = cart.filter(x => x.id !== Number(remove.dataset.remove));
  updateCart();
});

document.getElementById("checkout").onclick = () =>
  notify("Това е демо магазин — реалните поръчки не са активирани.");

document.getElementById("newsForm").onsubmit = e => {
  e.preventDefault();
  newsModal.classList.remove("open");
  notify("Благодарим! Това е демо форма.");
};

[cartModal, newsModal].forEach(m => {
  m.addEventListener("click", e => {
    if (e.target === m) m.classList.remove("open");
  });
});

render();
updateCart();
</script>
</body>
</html>
