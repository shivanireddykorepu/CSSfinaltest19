<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Instamart — Clone</title>
  <style>
    :root{
      --bg:#f6f7fb;
      --card:#ffffff;
      --muted:#6b7280;
      --accent1:#ff6b6b;
      --accent2:#ffb86b;
      --primary-gradient: linear-gradient(90deg,var(--accent1),var(--accent2));
      --shadow: 0 6px 18px rgba(20,20,50,0.08);
      --radius:14px;
      --maxw:1200px;
      --gap:18px;
    }
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; background:var(--bg); color:#0f172a; -webkit-font-smoothing:antialiased}
    .container{max-width:var(--maxw); margin:28px auto; padding:0 20px}/* Header */
header{display:flex;align-items:center;gap:18px;background:transparent}
.logo{display:flex;align-items:center;gap:10px}
.logo .mark{width:42px;height:42px;border-radius:10px;background:var(--primary-gradient);display:grid;place-items:center;color:white;font-weight:700}
.logo h1{font-size:18px;margin:0}

/* Search */
.search-bar{flex:1;display:flex;align-items:center;background:white;box-shadow:var(--shadow);padding:8px;border-radius:12px}
.search-bar input{border:0;outline:0;font-size:15px;padding:8px 12px;width:100%}

.actions{display:flex;gap:12px;align-items:center}
.pill{background:white;padding:8px 12px;border-radius:999px;box-shadow:var(--shadow);display:flex;gap:8px;align-items:center}

/* Hero */
.hero{margin-top:22px;background:linear-gradient(180deg, rgba(255,255,255,0.7), transparent);display:grid;grid-template-columns:1fr 360px;gap:20px}
.hero-card{background:var(--card);border-radius:var(--radius);padding:22px;box-shadow:var(--shadow);display:flex;flex-direction:column;gap:16px}
.promo{display:flex;gap:14px;align-items:center}
.promo h2{margin:0;font-size:22px}
.promo p{margin:0;color:var(--muted)}
.banner{background:linear-gradient(135deg,#fff1e6,#ffe4e0);border-radius:12px;padding:18px;display:flex;flex-direction:column;gap:10px}
.banner .cta{padding:10px 14px;border-radius:10px;background:var(--primary-gradient);color:white;border:0;cursor:pointer}

/* Categories */
.categories{display:grid;grid-template-columns:repeat(6,1fr);gap:14px;margin-top:18px}
.cat{background:linear-gradient(180deg,#fff,#fafafa);border-radius:12px;padding:12px;text-align:center;box-shadow:var(--shadow)}
.cat img{width:64px;height:64px;object-fit:cover;border-radius:10px;margin-bottom:8px}
.cat span{display:block;font-size:13px}

/* Main grid */
.main{display:grid;grid-template-columns:1fr 360px;gap:18px;margin-top:20px}
.products{background:transparent}
.product-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.card{background:var(--card);border-radius:12px;padding:12px;box-shadow:var(--shadow);display:flex;flex-direction:column;gap:8px}
.card img{width:100%;height:130px;object-fit:cover;border-radius:8px}
.card .title{font-weight:600;font-size:14px}
.card .meta{display:flex;justify-content:space-between;align-items:center;color:var(--muted);font-size:13px}
.add-btn{background:linear-gradient(90deg,#0ea5a4,#06b6d4);border:0;padding:8px;border-radius:10px;color:white;cursor:pointer}

/* Sidebar */
.sidebar{display:flex;flex-direction:column;gap:12px}
.slot{background:var(--card);padding:14px;border-radius:12px;box-shadow:var(--shadow)}

footer{margin-top:28px;padding:22px 0;color:var(--muted);text-align:center}

/* Responsive */
@media (max-width:1000px){
  .hero,.main{grid-template-columns:1fr}
  .categories{grid-template-columns:repeat(4,1fr)}
  .product-grid{grid-template-columns:repeat(2,1fr)}
}
@media (max-width:640px){
  .categories{grid-template-columns:repeat(3,1fr)}
  .product-grid{grid-template-columns:1fr}
  .logo h1{display:none}
  .pill{display:none}
}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">
        <div class="mark"><img width="60px"height="50px"src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT8o6tvEN_wYMu1g4HD4E89NatfI4yio1X8Jw&s" alt=""></div>
        <!-- <h1>Instamart</h1> -->
      </div><div class="search-bar" role="search">
    <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M21 21l-4.35-4.35" stroke="#9CA3AF" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><circle cx="11" cy="11" r="6" stroke="#9CA3AF" stroke-width="2"/></svg>
    <input placeholder="Search for products, brands and more" aria-label="Search" />
  </div>

  <div class="actions">
    <div class="pill">📍 <small>Deliver to</small> <strong style="margin-left:6px">500001</strong></div>
    <div class="pill">🛒 Cart</div>
  </div>
</header>

<section class="hero">
  <div class="hero-card">
    <div class="promo">
      <div>
        <h2>Groceries & Essentials — Delivered fast</h2>
        <p>Everyday essentials, fresh produce, and quick bites — in minutes.</p>
      </div>
      <div style="margin-left:auto;display:flex;flex-direction:column;gap:8px;align-items:flex-end">
        <div style="background:#fff;padding:8px 12px;border-radius:10px;box-shadow:var(--shadow)">Up to <strong>30% OFF</strong></div>
        <button class="cta">Shop Instamart</button>
      </div>
    </div>

    <div class="banner">
      <div style="display:flex;align-items:center;gap:12px">
        <img src="https://via.placeholder.com/90x90.png?text=IMG" alt="quick" style="width:90px;height:90px;border-radius:10px;object-fit:cover" />
        <div>
          <div style="font-weight:700">Delivery in 10 - 20 mins</div>
          <div style="color:var(--muted);font-size:13px">From local stores near you</div>
        </div>
      </div>
    </div>

    <div style="margin-top:6px;display:flex;gap:10px;flex-wrap:wrap">
      <div style="background:#fff;padding:10px;border-radius:10px;box-shadow:var(--shadow);flex:1">Fresh Fruits</div>
      <div style="background:#fff;padding:10px;border-radius:10px;box-shadow:var(--shadow);flex:1">Daily Staples</div>
      <div style="background:#fff;padding:10px;border-radius:10px;box-shadow:var(--shadow);flex:1">Beverages</div>
    </div>
  </div>

  <aside>
    <div class="slot">
      <strong>Track order</strong>
      <p style="margin:8px 0 0;color:var(--muted)">No active orders</p>
    </div>
    <div class="slot">
      <strong>Deals near you</strong>
      <p style="margin:8px 0 0;color:var(--muted)">Up to 30% off on selected items</p>
    </div>
  </aside>
</section>

<section class="categories">
  <div class="cat"><img src="https://static.vecteezy.com/system/resources/thumbnails/047/830/714/small/a-vibrant-assortment-of-fresh-vegetables-including-peppers-onions-lettuce-broccoli-tomatoes-corn-and-garlic-arranged-on-a-white-background-png.png" alt="Vegetables"/><span>Vegetables</span></div>
  <div class="cat"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT22bMjW4q9_ZWwaZveKsTKkP3rMscuyXxYYA&s" alt="Dairy"/><span>Dairy</span></div>
  <div class="cat"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRNy-6y9Z8Wh22cpBCWPbWVWKRC0QLuWE3ufg&s" alt="Bakery"/><span>Bakery</span></div>
  <div class="cat"><img src="https://cdn.zeptonow.com/production/tr:w-640,ar-1080-1080,pr-true,f-auto,q-80/cms/product_variant/47232a1b-757a-4623-8102-db9366aa067f.jpeg" alt="Snacks"/><span>Snacks</span></div>
  <div class="cat"><img src="https://png.pngtree.com/png-vector/20240807/ourmid/pngtree-juicy-fruits-and-vitamins-natural-organic-fruits-png-image_13146415.png" alt="Fruits"/><span>Fruits</span></div>
  <div class="cat"><img src="https://instamart-media-assets.swiggy.com/swiggy/image/upload/fl_lossy,f_auto,q_auto,h_272,w_252/NI_CATALOG/IMAGES/CIW/2024/7/23/36a7cb76-df61-47c9-a793-98fea55af66a_laundrydetergents_0FL19O48SR_MN.png" alt="Household"/><span>Household</span></div>
</section>

<section class="main">
  <main class="products">
    <h3 style="margin:0 0 12px">Popular near you</h3>
    <div class="product-grid">
      <article class="card">
        <img src="https://m.media-amazon.com/images/I/61duEBwvXdL._UF894,1000_QL80_.jpg" alt="Product 1">
        <div class="title">Amul Butter - 200g</div>
        <div class="meta"><div>₹ 120 <small style="text-decoration:line-through;color:var(--muted);margin-left:8px">₹ 150</small></div><button class="add-btn">Add</button></div>
      </article>

      <article class="card">
        <img src="https://5.imimg.com/data5/YY/PT/MY-51545753/sg-tomato-country-2c-1kg-500x500.png" alt="Product 2">
        <div class="title">Fresh Tomato - 1 kg</div>
        <div class="meta"><div>₹ 35</div><button class="add-btn">Add</button></div>
      </article>

      <article class="card">
        <img src="https://m.media-amazon.com/images/I/71h-V47-vFL._UF1000,1000_QL80_.jpg" alt="Product 3">
        <div class="title">Lay's Classic - 52g</div>
        <div class="meta"><div>₹ 20</div><button class="add-btn">Add</button></div>
      </article>

      <article class="card">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcShLssxCATKM3QY6tCGlsFZbQXcFtaqTebzEg&s" alt="Product 4">
        <div class="title">Milk — 1 L</div>
        <div class="meta"><div>₹ 48</div><button class="add-btn">Add</button></div>
      </article>

      <article class="card">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSwTg7LzehKd2syOK1DgFXcMR1dG8gKmC7qGg&s" alt="Product 5">
        <div class="title">White Bread — 400g</div>
        <div class="meta"><div>₹ 35</div><button class="add-btn">Add</button></div>
      </article>

      <article class="card">
        <img width="150px" height="150px" src="https://png.pngtree.com/png-vector/20241124/ourmid/pngtree-one-dozen-fresh-banana-in-the-basket-png-image_14507715.png" alt="Product 6">
        <div class="title">Banana - 1 dozen</div>
        <div class="meta"><div>₹ 60</div><button class="add-btn">Add</button></div>
      </article>

    </div>
  </main>

  <aside class="sidebar">
    <div class="slot">
      <strong>Express pickup</strong>
      <p style="margin:8px 0 0;color:var(--muted)">Order now & pick up in 15 minutes</p>
    </div>
    <div class="slot">
      <strong>Top brands</strong>
      <div style="display:flex;gap:8px;margin-top:8px;flex-wrap:wrap">
        <div style="background:#fff;padding:6px 10px;border-radius:10px;box-shadow:var(--shadow)">Amul</div>
        <div style="background:#fff;padding:6px 10px;border-radius:10px;box-shadow:var(--shadow)">Haldiram</div>
        <div style="background:#fff;padding:6px 10px;border-radius:10px;box-shadow:var(--shadow)">Tata</div>
      </div>
    </div>
  </aside>
</section>

<footer>
  © Instamart clone — UI demo • Not affiliated with Swiggy/Instamart
</footer>

  </div>
</body>
</html>
