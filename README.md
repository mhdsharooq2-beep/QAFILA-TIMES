# QAFILA-TIMES
QAFILA TIMES Official Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>QAFILA TIMES</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
    font-family:Arial,sans-serif;
    background:#0b0b0b;
    color:#fff;
}
header{
    background:#050505;
    border-bottom:1px solid #d4af37;
    position:sticky;
    top:0;
    z-index:1000;
}
.nav{
    max-width:1200px;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:14px 20px;
}
.logo{
    color:#d4af37;
    font-size:24px;
    font-weight:bold;
}
nav a{
    color:#fff;
    text-decoration:none;
    margin:0 8px;
    cursor:pointer;
}
nav a:hover{color:#d4af37}

.container{
    max-width:1200px;
    margin:auto;
    padding:25px 18px;
}

.hero{
    min-height:430px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    background:
    linear-gradient(rgba(0,0,0,.65),rgba(0,0,0,.75)),
    url("https://images.unsplash.com/photo-1523170335258-f5ed11844a49?auto=format&fit=crop&w=1600&q=80")
    center/cover;
}
.hero h1{
    font-size:48px;
    color:#d4af37;
}
.hero p{
    max-width:650px;
    margin:15px auto;
    color:#ddd;
}
.btn{
    display:inline-block;
    background:#d4af37;
    color:#000;
    padding:12px 20px;
    border:none;
    border-radius:6px;
    font-weight:bold;
    cursor:pointer;
    text-decoration:none;
}

.section-title{
    text-align:center;
    margin:35px 0 20px;
    color:#d4af37;
}

.categories{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
    gap:15px;
}
.category{
    border:1px solid #333;
    padding:20px;
    text-align:center;
    border-radius:10px;
    cursor:pointer;
    background:#111;
}
.category:hover{
    border-color:#d4af37;
    color:#d4af37;
}

.products{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
}
.product{
    background:#111;
    border:1px solid #292929;
    border-radius:10px;
    overflow:hidden;
}
.product img{
    width:100%;
    height:220px;
    object-fit:cover;
}
.product-content{
    padding:15px;
}
.product h3{
    margin-bottom:8px;
}
.price{
    color:#d4af37;
    font-size:20px;
    font-weight:bold;
}
.old-price{
    color:#777;
    text-decoration:line-through;
    margin-left:8px;
}
.product button{
    margin-top:12px;
    width:100%;
}

footer{
    margin-top:50px;
    background:#050505;
    border-top:1px solid #d4af37;
    padding:30px 15px;
    text-align:center;
}
footer a{
    color:#d4af37;
    text-decoration:none;
    margin:5px 10px;
}

/* ADMIN */
.admin-login,
.admin-panel{
    display:none;
}
.card{
    background:#111;
    border:1px solid #333;
    border-radius:10px;
    padding:20px;
    margin-bottom:20px;
}
input,select,textarea{
    width:100%;
    padding:11px;
    margin:7px 0 14px;
    background:#080808;
    border:1px solid #444;
    color:#fff;
    border-radius:5px;
}
textarea{
    min-height:100px;
    resize:vertical;
}
label{
    color:#ccc;
    font-size:14px;
}
.admin-tabs{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
    margin-bottom:20px;
}
.admin-tabs button{
    background:#191919;
    color:#fff;
    border:1px solid #444;
    padding:10px 15px;
    border-radius:5px;
    cursor:pointer;
}
.admin-tabs button.active{
    background:#d4af37;
    color:#000;
}

.admin-section{
    display:none;
}
.admin-section.active{
    display:block;
}

.admin-product{
    display:flex;
    gap:15px;
    align-items:center;
    padding:12px;
    border-bottom:1px solid #333;
}
.admin-product img{
    width:70px;
    height:70px;
    object-fit:cover;
    border-radius:5px;
}
.admin-product-info{
    flex:1;
}
.admin-actions{
    display:flex;
    gap:5px;
    flex-wrap:wrap;
}
.small-btn{
    padding:7px 10px;
    border:1px solid #555;
    background:#181818;
    color:#fff;
    border-radius:4px;
    cursor:pointer;
}
.small-btn:hover{
    border-color:#d4af37;
    color:#d4af37;
}

.stats{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
    gap:15px;
}
.stat{
    background:#111;
    border:1px solid #333;
    padding:20px;
    border-radius:10px;
}
.stat h3{
    color:#d4af37;
    font-size:30px;
}

.modal{
    display:none;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.8);
    z-index:2000;
    align-items:center;
    justify-content:center;
    padding:20px;
}
.modal-box{
    width:100%;
    max-width:550px;
    background:#111;
    border:1px solid #d4af37;
    border-radius:10px;
    padding:20px;
    max-height:90vh;
    overflow:auto;
}

.cart-item{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:10px;
    padding:12px 0;
    border-bottom:1px solid #333;
}
.cart-total{
    text-align:right;
    color:#d4af37;
    font-size:22px;
    font-weight:bold;
    margin-top:20px;
}

.search-row{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:20px;
}
.search-row input,
.search-row select{
    flex:1;
    min-width:180px;
}

@media(max-width:700px){
    .nav{
        flex-direction:column;
        gap:12px;
    }
    nav{
        display:flex;
        flex-wrap:wrap;
        justify-content:center;
    }
    .hero h1{
        font-size:34px;
    }
    .admin-product{
        flex-direction:column;
        align-items:flex-start;
    }
}
</style>
</head>

<body>

<header>
<div class="nav">

<div class="logo" id="logoArea">
QAFILA TIMES
</div>

<nav>
<a onclick="showPage('home')">Home</a>
<a onclick="showPage('categories')">Categories</a>
<a onclick="showPage('products')">Products</a>
<a onclick="showPage('cart')">Cart (<span id="cartCount">0</span>)</a>
<a onclick="showPage('admin')">Admin</a>
</nav>

</div>
</header>

<!-- HOME -->
<section id="homePage">

<div class="hero">
<div>
<h1 id="homeTitle">TIMELESS STYLE FOR EVERY MOMENT</h1>
<p id="homeDescription">
Discover watches, perfumes, shoes, dresses, bags, accessories and more — all in one place.
</p>
<a class="btn" onclick="showPage('products')">Shop Now</a>
</div>
</div>

<div class="container">

<h2 class="section-title">Categories</h2>
<div class="categories" id="homeCategories"></div>

<h2 class="section-title">Special Offers</h2>
<div class="products" id="offerProducts"></div>

<h2 class="section-title">Featured Products</h2>
<div class="products" id="featuredProducts"></div>

</div>

</section>

<!-- CATEGORIES -->
<section id="categoriesPage" style="display:none">

<div class="container">

<h2 class="section-title">Shop By Category</h2>

<div class="categories" id="allCategories"></div>

</div>

</section>

<!-- PRODUCTS -->
<section id="productsPage" style="display:none">

<div class="container">

<h2 class="section-title">All Products</h2>

<div class="search-row">
<input id="searchInput" placeholder="Search products..." oninput="renderProducts()">

<select id="categoryFilter" onchange="renderProducts()">
<option value="">All Categories</option>
</select>
</div>

<div class="products" id="productsGrid"></div>

</div>

</section>

<!-- CART -->
<section id="cartPage" style="display:none">

<div class="container">

<h2 class="section-title">Your Cart</h2>

<div class="card">

<div id="cartItems"></div>

<div class="cart-total">
Total: ₹<span id="cartTotal">0</span>
</div>

<button class="btn" onclick="openOrderModal()">
Place Order
</button>

</div>

</div>

</section>

<!-- ADMIN LOGIN -->
<section id="adminLogin" class="admin-login">

<div class="container">

<div class="card" style="max-width:450px;margin:50px auto">

<h2 class="section-title">Admin Login</h2>

<label>Username</label>
<input id="adminUsername">

<label>Password</label>
<input id="adminPassword" type="password">

<button class="btn" onclick="adminLogin()">
Login
</button>

<p id="loginError" style="color:#f55;margin-top:10px"></p>

</div>

</div>

</section>

<!-- ADMIN PANEL -->
<section id="adminPanel" class="admin-panel">

<div class="container">

<h2 class="section-title">QAFILA TIMES ADMIN</h2>

<div class="admin-tabs">

<button onclick="openAdminTab('dashboard')" class="active">
Dashboard
</button>

<button onclick="openAdminTab('productsAdmin')">
Products
</button>

<button onclick="openAdminTab('addProduct')">
Add Product
</button>

<button onclick="openAdminTab('categoriesAdmin')">
Categories
</button>

<button onclick="openAdminTab('settingsAdmin')">
Website Settings
</button>

<button onclick="adminLogout()">
Logout
</button>

</div>

<!-- DASHBOARD -->
<div id="dashboard" class="admin-section active">

<div class="stats">

<div class="stat">
<h3 id="totalProducts">0</h3>
<p>Total Products</p>
</div>

<div class="stat">
<h3 id="totalCategories">0</h3>
<p>Categories</p>
</div>

<div class="stat">
<h3 id="totalStock">0</h3>
<p>Total Stock</p>
</div>

<div class="stat">
<h3 id="offerCount">0</h3>
<p>Offers</p>
</div>

</div>

</div>

<!-- PRODUCTS ADMIN -->
<div id="productsAdmin" class="admin-section">

<div class="card">

<div class="search-row">

<input
id="adminSearch"
placeholder="Search products..."
oninput="renderAdminProducts()">

<select id="adminCategoryFilter"
onchange="renderAdminProducts()">

<option value="">All Categories</option>

</select>

</div>

<div id="adminProductsList"></div>

</div>

</div>

<!-- ADD PRODUCT -->
<div id="addProduct" class="admin-section">

<div class="card">

<h2>Add / Edit Product</h2>

<input type="hidden" id="editProductId">

<label>Product Code / SKU</label>
<input id="productCode" placeholder="Example: QT001">

<label>Product Name</label>
<input id="productName">

<label>Category</label>
<select id="productCategory"></select>

<label>Stock Quantity</label>
<input id="productStock" type="number" min="0">

<label>Original Price</label>
<input id="originalPrice" type="number">

<label>Selling / Offer Price</label>
<input id="sellingPrice" type="number">

<label>Product Image</label>
<input id="productImageFile" type="file" accept="image/*">

<label>Or Image URL</label>
<input id="productImageUrl">

<label>Description</label>
<textarea id="productDescription"></textarea>

<label>
<input type="checkbox" id="productFeatured">
 Featured Product
</label>

<br><br>

<label>
<input type="checkbox" id="productOffer">
 Special Offer
</label>

<br><br>

<button class="btn" onclick="saveProduct()">
Save Product
</button>

<button
class="small-btn"
onclick="clearProductForm()">
Clear
</button>

</div>

</div>

<!-- CATEGORIES ADMIN -->
<div id="categoriesAdmin" class="admin-section">

<div class="card">

<h2>Add Category</h2>

<input id="newCategory" placeholder="Category name">

<button class="btn" onclick="addCategory()">
Add Category
</button>

</div>

<div class="card">

<h2>Categories</h2>

<div id="categoryAdminList"></div>

</div>

</div>

<!-- SETTINGS -->
<div id="settingsAdmin" class="admin-section">

<div class="card">

<h2>Website Settings</h2>

<label>Logo</label>
<input id="logoFile" type="file" accept="image/*">

<label>WhatsApp Number</label>
<input id="settingWhatsapp">

<label>Call Number</label>
<input id="settingPhone">

<label>Instagram Link</label>
<input id="settingInstagram">

<label>YouTube Link</label>
<input id="settingYoutube">

<label>Email</label>
<input id="settingEmail">

<label>Homepage Title</label>
<input id="settingTitle">

<label>Homepage Description</label>
<textarea id="settingDescription"></textarea>

<button class="btn" onclick="saveSettings()">
Save Settings
</button>

</div>

</div>

</div>

</section>

<!-- FOOTER -->
<footer>

<p>© 2026 QAFILA TIMES</p>

<div style="margin-top:15px">

<a id="footerWhatsapp" href="#" target="_blank">
WhatsApp
</a>

<a id="footerPhone" href="#">
Call
</a>

<a id="footerInstagram" href="#" target="_blank">
Instagram
</a>

<a id="footerYoutube" href="#" target="_blank">
YouTube
</a>

<a id="footerEmail" href="#">
Email
</a>

</div>

</footer>

<!-- ORDER MODAL -->
<div class="modal" id="orderModal">

<div class="modal-box">

<h2 class="section-title">Order Details</h2>

<label>Name</label>
<input id="orderName">

<label>Phone Number</label>
<input id="orderPhone">

<label>Address</label>
<textarea id="orderAddress"></textarea>

<button class="btn" onclick="sendOrderToWhatsapp()">
Send Order on WhatsApp
</button>

<button class="small-btn" onclick="closeModal('orderModal')">
Cancel
</button>

</div>

</div>

<!-- CATEGORY MODAL -->
<div class="modal" id="categoryModal">

<div class="modal-box">

<h2 class="section-title">Edit Category</h2>

<input type="hidden" id="editCategoryId">

<input id="editCategoryName">

<button class="btn" onclick="saveEditedCategory()">
Save
</button>

<button class="small-btn" onclick="closeModal('categoryModal')">
Cancel
</button>

</div>

</div>

<script>

const DB_NAME = "QAFILA_TIMES_DB";
const DB_VERSION = 3;

let db;

let cart =
JSON.parse(localStorage.getItem("qafila_cart") || "[]");

let settings = {};

let currentProducts = [];

let categories = [];

function openDB(){

return new Promise((resolve,reject)=>{

const request =
indexedDB.open(DB_NAME,DB_VERSION);

request.onupgradeneeded = e => {

db = e.target.result;

if(!db.objectStoreNames.contains("products")){
db.createObjectStore("products",{keyPath:"id",autoIncrement:true});
}

if(!db.objectStoreNames.contains("categories")){
db.createObjectStore("categories",{keyPath:"id",autoIncrement:true});
}

if(!db.objectStoreNames.contains("settings")){
db.createObjectStore("settings",{keyPath:"id"});
}

};

request.onsuccess = e => {
db=e.target.result;
resolve(db);
};

request.onerror = e => reject(e);

});

}

function getAll(storeName){

return new Promise((resolve,reject)=>{

const tx=db.transaction(storeName,"readonly");
const store=tx.objectStore(storeName);
const request=store.getAll();

request.onsuccess=()=>resolve(request.result);
request.onerror=()=>reject(request.error);

});

}

function addItem(storeName,item){

return new Promise((resolve,reject)=>{

const tx=db.transaction(storeName,"readwrite");
const request=tx.objectStore(storeName).add(item);

request.onsuccess=()=>resolve(request.result);
request.onerror=()=>reject(request.error);

});

}

function putItem(storeName,item){

return new Promise((resolve,reject)=>{

const tx=db.transaction(storeName,"readwrite");
const request=tx.objectStore(storeName).put(item);

request.onsuccess=()=>resolve(request.result);
request.onerror=()=>reject(request.error);

});

}

function deleteItem(storeName,id){

return new Promise((resolve,reject)=>{

const tx=db.transaction(storeName,"readwrite");
const request=tx.objectStore(storeName).delete(id);

request.onsuccess=()=>resolve();
request.onerror=()=>reject(request.error);

});

}

async function initialize(){

await openDB();

categories=await getAll("categories");

if(categories.length===0){

const defaults=[
"Watches",
"Perfumes",
"Shoes",
"Dresses",
"Bags",
"Accessories"
];

for(const name of defaults){

await addItem("categories",{name});

}

categories=await getAll("categories");

}

const savedSettings=await getAll("settings");

if(savedSettings.length){
settings=savedSettings[0];
}else{

settings={
id:1,
logo:"",
whatsapp:"",
phone:"",
instagram:"",
youtube:"",
email:"",
title:"TIMELESS STYLE FOR EVERY MOMENT",
description:"Discover watches, perfumes, shoes, dresses, bags, accessories and more — all in one place."
};

await putItem("settings",settings);

}

applySettings();

renderEverything();

}

function applySettings(){

document.getElementById("homeTitle").textContent =
settings.title ||
"TIMELESS STYLE FOR EVERY MOMENT";

document.getElementById("homeDescription").textContent =
settings.description || "";

if(settings.logo){

document.getElementById("logoArea").innerHTML =
`<img src="${settings.logo}" style="max-height:45px;max-width:180px;object-fit:contain">`;

}

document.getElementById("footerWhatsapp").href =
settings.whatsapp ?
"https://wa.me/"+settings.whatsapp :
"#";

document.getElementById("footerPhone").href =
settings.phone ?
"tel:"+settings.phone :
"#";

document.getElementById("footerInstagram").href =
settings.instagram || "#";

document.getElementById("footerYoutube").href =
settings.youtube || "#";

document.getElementById("footerEmail").href =
settings.email ?
"mailto:"+settings.email :
"#";

}

async function renderEverything(){

categories=await getAll("categories");
currentProducts=await getAll("products");

renderCategories();
renderProducts();
renderHomeProducts();
renderCart();
renderAdminProducts();
updateStats();

}

function renderCategories(){

const home=document.getElementById("homeCategories");
const all=document.getElementById("allCategories");
const filter=document.getElementById("categoryFilter");
const adminFilter=document.getElementById("adminCategoryFilter");
const productCategory=document.getElementById("productCategory");

home.innerHTML="";
all.innerHTML="";

filter.innerHTML='<option value="">All Categories</option>';
adminFilter.innerHTML='<option value="">All Categories</option>';
productCategory.innerHTML="";

categories.forEach(c=>{

home.innerHTML+=`
<div class="category" onclick="filterByCategory('${escapeHtml(c.name)}')">
${escapeHtml(c.name)}
</div>`;

all.innerHTML+=`
<div class="category" onclick="filterByCategory('${escapeHtml(c.name)}')">
${escapeHtml(c.name)}
</div>`;

filter.innerHTML+=`
<option value="${escapeHtml(c.name)}">
${escapeHtml(c.name)}
</option>`;

adminFilter.innerHTML+=`
<option value="${escapeHtml(c.name)}">
${escapeHtml(c.name)}
</option>`;

productCategory.innerHTML+=`
<option value="${escapeHtml(c.name)}">
${escapeHtml(c.name)}
</option>`;

});

renderCategoryAdmin();

}

function filterByCategory(category){

showPage("products");

document.getElementById("categoryFilter").value=category;

renderProducts();

}

function renderProducts(){

const grid=document.getElementById("productsGrid");

if(!grid)return;

const search=
(document.getElementById("searchInput")?.value || "")
.toLowerCase();

const category=
document.getElementById("categoryFilter")?.value || "";

let products=currentProducts.filter(p=>{

const matchSearch =
p.name.toLowerCase().includes(search) ||
(p.code || "").toLowerCase().includes(search);

const matchCategory =
!category || p.category===category;

return matchSearch && matchCategory;

});

grid.innerHTML="";

if(!products.length){

grid.innerHTML=
`<p style="text-align:center;color:#aaa">
No products found.
</p>`;

return;

}

products.forEach(p=>{
grid.innerHTML+=productCard(p);
});

}

function productCard(p){

const outOfStock =
Number(p.stock)<=0;

return `

<div class="product">

<img
src="${p.image || 'https://via.placeholder.com/500x500?text=QAFILA+TIMES'}"
alt="${escapeHtml(p.name)}">

<div class="product-content">

<h3>${escapeHtml(p.name)}</h3>

<p style="color:#999;font-size:13px">
${escapeHtml(p.category)}
</p>

<p style="margin:8px 0">

<span class="price">
₹${Number(p.price || 0).toLocaleString("en-IN")}
</span>

${p.originalPrice && Number(p.originalPrice)>Number(p.price)
?
`<span class="old-price">
₹${Number(p.originalPrice).toLocaleString("en-IN")}
</span>`
:""}

</p>

<p style="color:${outOfStock?'#f55':'#6f6'}">
${outOfStock ? "Out of Stock" : "Stock: "+p.stock}
</p>

<button
class="btn"
onclick="addToCart(${p.id})"
${outOfStock ? "disabled" : ""}>

${outOfStock ? "Out of Stock" : "Add to Cart"}

</button>

</div>
</div>

`;

}

function renderHomeProducts(){

const offers=document.getElementById("offerProducts");
const featured=document.getElementById("featuredProducts");

if(!offers || !featured)return;

offers.innerHTML="";
featured.innerHTML="";

const offerProducts=currentProducts
.filter(p=>p.offer)
.slice(0,8);

const featuredProducts=currentProducts
.filter(p=>p.featured)
.slice(0,8);

offerProducts.forEach(p=>{
offers.innerHTML+=productCard(p);
});

featuredProducts.forEach(p=>{
featured.innerHTML+=productCard(p);
});

}

function addToCart(id){

const product=currentProducts.find(p=>p.id===id);

if(!product)return;

if(Number(product.stock)<=0){
alert("Product is out of stock.");
return;
}

const existing=cart.find(x=>x.id===id);

if(existing){

if(existing.qty>=Number(product.stock)){
alert("No more stock available.");
return;
}

existing.qty++;

}else{

cart.push({
id:product.id,
qty:1
});

}

saveCart();

renderCart();

alert("Product added to cart.");

}

function saveCart(){

localStorage.setItem(
"qafila_cart",
JSON.stringify(cart)
);

document.getElementById("cartCount").textContent =
cart.reduce((sum,x)=>sum+x.qty,0);

}

function renderCart(){

const box=document.getElementById("cartItems");

if(!box)return;

box.innerHTML="";

let total=0;

cart.forEach(item=>{

const p=currentProducts.find(x=>x.id===item.id);

if(!p)return;

const subtotal=
Number(p.price || 0)*item.qty;

total+=subtotal;

box.innerHTML+=`

<div class="cart-item">

<div>
<strong>${escapeHtml(p.name)}</strong>
<br>
<span style="color:#aaa">
₹${Number(p.price).toLocaleString("en-IN")}
× ${item.qty}
</span>
</div>

<div>

<button class="small-btn"
onclick="changeCartQty(${p.id},-1)">
-
</button>

<button class="small-btn"
onclick="changeCartQty(${p.id},1)">
+
</button>

<button class="small-btn"
onclick="removeFromCart(${p.id})">
Remove
</button>

</div>

</div>

`;

});

document.getElementById("cartTotal").textContent =
total.toLocaleString("en-IN");

saveCart();

}

function changeCartQty(id,change){

const item=cart.find(x=>x.id===id);
const product=currentProducts.find(x=>x.id===id);

if(!item || !product)return;

item.qty+=change;

if(item.qty<=0){

cart=cart.filter(x=>x.id!==id);

}else if(item.qty>Number(product.stock)){

item.qty=Number(product.stock);

alert("Maximum available stock reached.");

}

saveCart();
renderCart();

}

function removeFromCart(id){

cart=cart.filter(x=>x.id!==id);

saveCart();
renderCart();

}

function showPage(page){

document.getElementById("homePage").style.display="none";
document.getElementById("categoriesPage").style.display="none";
document.getElementById("productsPage").style.display="none";
document.getElementById("cartPage").style.display="none";
document.getElementById("adminLogin").style.display="none";
document.getElementById("adminPanel").style.display="none";

if(page==="home")
document.getElementById("homePage").style.display="block";

if(page==="categories")
document.getElementById("categoriesPage").style.display="block";

if(page==="products")
document.getElementById("productsPage").style.display="block";

if(page==="cart")
document.getElementById("cartPage").style.display="block";

if(page==="admin"){

if(localStorage.getItem("qafila_admin")==="1"){
document.getElementById("adminPanel").style.display="block";
}else{
document.getElementById("adminLogin").style.display="block";
}

}

window.scrollTo(0,0);

}

function adminLogin(){

const username=
document.getElementById("adminUsername").value;

const password=
document.getElementById("adminPassword").value;

if(username==="admin" && password==="1234"){

localStorage.setItem("qafila_admin","1");

document.getElementById("loginError").textContent="";

showPage("admin");

}else{

document.getElementById("loginError").textContent=
"Invalid username or password.";

}

}

function adminLogout(){

localStorage.removeItem("qafila_admin");

showPage("admin");

}

function openAdminTab(id){

document.querySelectorAll(".admin-section")
.forEach(x=>x.classList.remove("active"));

document.querySelectorAll(".admin-tabs button")
.forEach(x=>x.classList.remove("active"));

document.getElementById(id).classList.add("active");

}

function renderAdminProducts(){

const box=document.getElementById("adminProductsList");

if(!box)return;

const search=
(document.getElementById("adminSearch")?.value || "")
.toLowerCase();

const category=
document.getElementById("adminCategoryFilter")?.value || "";

const products=currentProducts.filter(p=>{

const searchMatch=
p.name.toLowerCase().includes(search) ||
(p.code || "").toLowerCase().includes(search);

const categoryMatch=
!category || p.category===category;

return searchMatch && categoryMatch;

});

box.innerHTML="";

products.forEach(p=>{

box.innerHTML+=`

<div class="admin-product">

<img src="${p.image || 'https://via.placeholder.com/100'}">

<div class="admin-product-info">

<strong>${escapeHtml(p.name)}</strong>

<p style="color:#aaa">
Code: ${escapeHtml(p.code || "-")}
</p>

<p>
₹${Number(p.price || 0).toLocaleString("en-IN")}
|
Stock: ${p.stock}
</p>

<p>
${p.offer ? "🔥 Offer" : ""}
${p.featured ? " ⭐ Featured" : ""}
</p>

</div>

<div class="admin-actions">

<button class="small-btn"
onclick="editProduct(${p.id})">
Edit
</button>

<button class="small-btn"
onclick="toggleStock(${p.id})">
${Number(p.stock)>0 ? "Out of Stock" : "In Stock"}
</button>

<button class="small-btn"
onclick="toggleFeatured(${p.id})">
Featured
</button>

<button class="small-btn"
onclick="toggleOffer(${p.id})">
Offer
</button>

<button class="small-btn"
onclick="deleteProduct(${p.id})">
Delete
</button>

</div>

</div>

`;

});

}

async function saveProduct(){

const id=
document.getElementById("editProductId").value;

const code=
document.getElementById("productCode").value.trim();

const name=
document.getElementById("productName").value.trim();

const category=
document.getElementById("productCategory").value;

const stock=
Number(document.getElementById("productStock").value || 0);

const originalPrice=
Number(document.getElementById("originalPrice").value || 0);

const price=
Number(document.getElementById("sellingPrice").value || 0);

const description=
document.getElementById("productDescription").value.trim();

const featured=
document.getElementById("productFeatured").checked;

const offer=
document.getElementById("productOffer").checked;

const imageUrl=
document.getElementById("productImageUrl").value.trim();

const file=
document.getElementById("productImageFile").files[0];

let image=imageUrl;

if(file){

image=await readFileAsDataURL(file);

}

let product;

if(id){

product=currentProducts.find(p=>p.id===Number(id));

if(!product)return;

product.code=code;
product.name=name;
product.category=category;
product.stock=stock;
product.originalPrice=originalPrice;
product.price=price;
product.description=description;
product.featured=featured;
product.offer=offer;

if(image)product.image=image;

await putItem("products",product);

}else{

product={
code,
name,
category,
stock,
originalPrice,
price,
description,
featured,
offer,
image
};

await addItem("products",product);

}

clearProductForm();

currentProducts=await getAll("products");

renderEverything();

alert("Product saved successfully.");

}

function readFileAsDataURL(file){

return new Promise((resolve,reject)=>{

const reader=new FileReader();

reader.onload=()=>resolve(reader.result);
reader.onerror=reject;

reader.readAsDataURL(file);

});

}

function clearProductForm(){

document.getElementById("editProductId").value="";
document.getElementById("productCode").value="";
document.getElementById("productName").value="";
document.getElementById("productStock").value="";
document.getElementById("originalPrice").value="";
document.getElementById("sellingPrice").value="";
document.getElementById("productImageFile").value="";
document.getElementById("productImageUrl").value="";
document.getElementById("productDescription").value="";
document.getElementById("productFeatured").checked=false;
document.getElementById("productOffer").checked=false;

}

function editProduct(id){

const p=currentProducts.find(x=>x.id===id);

if(!p)return;

document.getElementById("editProductId").value=p.id;
document.getElementById("productCode").value=p.code || "";
document.getElementById("productName").value=p.name || "";
document.getElementById("productCategory").value=p.category || "";
document.getElementById("productStock").value=p.stock || 0;
document.getElementById("originalPrice").value=p.originalPrice || 0;
document.getElementById("sellingPrice").value=p.price || 0;
document.getElementById("productImageUrl").value=
p.image && !p.image.startsWith("data:") ? p.image : "";
document.getElementById("productDescription").value=p.description || "";
document.getElementById("productFeatured").checked=!!p.featured;
document.getElementById("productOffer").checked=!!p.offer;

openAdminTab("addProduct");

window.scrollTo(0,0);

}

async function deleteProduct(id){

if(!confirm("Delete this product?"))return;

await deleteItem("products",id);

currentProducts=await getAll("products");

renderEverything();

}

async function toggleStock(id){

const p=currentProducts.find(x=>x.id===id);

if(!p)return;

p.stock=Number(p.stock)>0 ? 0 : 1;

await putItem("products",p);

currentProducts=await getAll("products");

renderEverything();

}

async function toggleFeatured(id){

const p=currentProducts.find(x=>x.id===id);

if(!p)return;

p.featured=!p.featured;

await putItem("products",p);

currentProducts=await getAll("products");

renderEverything();

}

async function toggleOffer(id){

const p=currentProducts.find(x=>x.id===id);

if(!p)return;

p.offer=!p.offer;

await putItem("products",p);

currentProducts=await getAll("products");

renderEverything();

}

async function addCategory(){

const input=document.getElementById("newCategory");

const name=input.value.trim();

if(!name)return;

await addItem("categories",{name});

input.value="";

categories=await getAll("categories");

renderEverything();

}

function renderCategoryAdmin(){

const box=document.getElementById("categoryAdminList");

if(!box)return;

box.innerHTML="";

categories.forEach(c=>{

box.innerHTML+=`

<div class="admin-product">

<div class="admin-product-info">
<strong>${escapeHtml(c.name)}</strong>
</div>

<div class="admin-actions">

<button class="small-btn"
onclick="editCategory(${c.id})">
Edit
</button>

<button class="small-btn"
onclick="deleteCategory(${c.id})">
Delete
</button>

</div>

</div>

`;

});

}

function editCategory(id){

const c=categories.find(x=>x.id===id);

if(!c)return;

document.getElementById("editCategoryId").value=c.id;
document.getElementById("editCategoryName").value=c.name;

document.getElementById("categoryModal").style.display="flex";

}

async function saveEditedCategory(){

const id=
Number(document.getElementById("editCategoryId").value);

const name=
document.getElementById("editCategoryName").value.trim();

if(!id || !name)return;

const c=categories.find(x=>x.id===id);

if(!c)return;

c.name=name;

await putItem("categories",c);

closeModal("categoryModal");

categories=await getAll("categories");

renderEverything();

}

async function deleteCategory(id){

if(!confirm("Delete this category?"))return;

await deleteItem("categories",id);

categories=await getAll("categories");

renderEverything();

}

async function saveSettings(){

const file=
document.getElementById("logoFile").files[0];

let logo=settings.logo;

if(file){
logo=await readFileAsDataURL(file);
}

settings={
id:1,
logo,
whatsapp:
document.getElementById("settingWhatsapp").value.trim(),
phone:
document.getElementById("settingPhone").value.trim(),
instagram:
document.getElementById("settingInstagram").value.trim(),
youtube:
document.getElementById("settingYoutube").value.trim(),
email:
document.getElementById("settingEmail").value.trim(),
title:
document.getElementById("settingTitle").value.trim(),
description:
document.getElementById("settingDescription").value.trim()
};

await putItem("settings",settings);

applySettings();

alert("Website settings saved.");

}

function loadSettingsForm(){

document.getElementById("settingWhatsapp").value=
settings.whatsapp || "";

document.getElementById("settingPhone").value=
settings.phone || "";

document.getElementById("settingInstagram").value=
settings.instagram || "";

document.getElementById("settingYoutube").value=
settings.youtube || "";

document.getElementById("settingEmail").value=
settings.email || "";

document.getElementById("settingTitle").value=
settings.title || "";

document.getElementById("settingDescription").value=
settings.description || "";

}

function updateStats(){

document.getElementById("totalProducts").textContent=
currentProducts.length;

document.getElementById("totalCategories").textContent=
categories.length;

document.getElementById("totalStock").textContent=
currentProducts.reduce(
(sum,p)=>sum+Number(p.stock || 0),0
);

document.getElementById("offerCount").textContent=
currentProducts.filter(p=>p.offer).length;

}

function openOrderModal(){

if(!cart.length){

alert("Your cart is empty.");

return;

}

document.getElementById("orderModal").style.display="flex";

}

function closeModal(id){

document.getElementById(id).style.display="none";

}

function sendOrderToWhatsapp(){

const name=
document.getElementById("orderName").value.trim();

const phone=
document.getElementById("orderPhone").value.trim();

const address=
document.getElementById("orderAddress").value.trim();

if(!name || !phone || !address){

alert("Please fill all details.");

return;

}

let message=
"*QAFILA TIMES ORDER*%0A%0A";

message+=
"Name: "+encodeURIComponent(name)+"%0A";

message+=
"Phone: "+encodeURIComponent(phone)+"%0A";

message+=
"Address: "+encodeURIComponent(address)+"%0A%0A";

message+="*Products:*%0A";

let total=0;

cart.forEach(item=>{

const p=currentProducts.find(x=>x.id===item.id);

if(!p)return;

const subtotal=
Number(p.price || 0)*item.qty;

total+=subtotal;

message+=
encodeURIComponent(p.name)+
" × "+
item.qty+
" = ₹"+
subtotal.toLocaleString("en-IN")+
"%0A";

});

message+=
"%0A*Total: ₹"+
total.toLocaleString("en-IN")+
"*";

if(!settings.whatsapp){

alert("Please add WhatsApp number from Admin > Website Settings.");

return;

}

const url=
"https://wa.me/"+
settings.whatsapp+
"?text="+
message;

window.open(url,"_blank");

}

function escapeHtml(text){

return String(text || "")
.replace(/&/g,"&amp;")
.replace(/</g,"&lt;")
.replace(/>/g,"&gt;")
.replace(/"/g,"&quot;")
.replace(/'/g,"&#039;");

}

document.addEventListener("DOMContentLoaded",async()=>{

await initialize();

loadSettingsForm();

saveCart();

});

</script>

</body>
</html>
