<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>RZ ROBLOX JOKI 2025</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@900&family=Exo+2:wght@700&display=swap');
    *{margin:0;padding:0;box-sizing:border-box;}
    body{background:#000;color:#0f0;font-family:'Exo 2',sans-serif;overflow-x:hidden;}
    #loader{position:fixed;top:0;left:0;width:100%;height:100%;background:#000;z-index:9999;display:flex;align-items:center;justify-content:center;}
    .roblox-logo{font-family:'Orbitron';font-size:8rem;color:#0f0;text-shadow:0 0 40px #0f0;animation:glow 2s infinite;}
    @keyframes glow{0%,100%{text-shadow:0 0 40px #0f0}50%{text-shadow:0 0 80px #0f0}}

    nav{background:#111;padding:15px 0;position:fixed;top:0;width:100%;z-index:998;border-bottom:4px solid #0f0;display:none;text-align:center;}
    .nav-logo{font-family:'Orbitron';font-size:2.5rem;background:linear-gradient(45deg,#0f0,#00ff00);-webkit-background-clip:text;color:transparent;}
    .nav-menu button{background:#0f0;color:#000;padding:12px 25px;margin:5px;border-radius:10px;font-weight:bold;border:none;cursor:pointer;}

    .container{margin-top:90px;padding:15px;display:none;}
    h1{font-family:'Orbitron';font-size:3.5rem;text-align:center;margin:20px 0;background:linear-gradient(45deg,#0f0,#00ff00);-webkit-background-clip:text;color:transparent;}
    .form{background:#001a00;padding:30px;border-radius:15px;max-width:700px;margin:20px auto;border:2px solid #0f0;box-shadow:0 0 40px #0f0;}
    input{width:100%;padding:15px;margin:10px 0;border-radius:10px;background:#000;border:2px solid #0f0;color:#0f0;font-size:1.1rem;}
    button.kirim{width:100%;padding:20px;background:#0f0;color:#000;font-size:1.8rem;border:none;border-radius:15px;margin-top:20px;cursor:pointer;font-weight:bold;}

    .price-header{background:#0f0;color:#000;padding:15px;border-radius:12px;text-align:center;cursor:pointer;font-weight:bold;}
    .pricelist{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:15px;display:none;margin-top:10px;}
    .price-btn{background:#001a00;border:2px solid #0f0;padding:16px;border-radius:12px;text-align:center;cursor:pointer;transition:0.3s;font-weight:bold;}
    .price-btn:hover,.price-btn.selected{background:#0f0;color:#000;transform:scale(1.08);}

    table{width:100%;border-collapse:collapse;margin:20px 0;}
    th{background:#0f0;color:#000;padding:12px;}
    td{padding:12px;background:#000;border-bottom:1px solid #0f0;color:#0f0;text-align:center;}
    .btn{padding:10px 18px;border:none;border-radius:8px;cursor:pointer;font-weight:bold;margin:3px;}
    .ambil{background:#39ff14;color:#000;}
    .done{background:#00ff00;color:#000;}
    .tab{display:none;}
    .tab.active{display:block;}
  </style>
</head>
<body>

<div id="loader"><div class="roblox-logo">R•Z</div></div>

<nav id="nav">
  <div class="nav-logo">RZ ROBLOX JOKI</div>
  <div class="nav-menu">
    <button onclick="show('order')" class="active">Order</button>
    <button onclick="show('antrian')">Antrian</button>
    <button onclick="show('selesai')">Selesai</button>
  </div>
</nav>

<div class="container" id="main">
  <div id="order" class="tab active">
    <h1>ORDER JOKI ROBLOX</h1>
    <div class="form">
      <input type="text" id="client" placeholder="Nama Client" autocomplete="off">
      <input type="text" id="username" placeholder="Username Roblox" autocomplete="off">
      <input type="text" id="password" placeholder="Password atau Cookie" autocomplete="off">

      <div class="price-header" onclick="togglePricelist()">PILIH PAKET JOKI</div>
      <div class="pricelist" id="pricelist">
        <div class="price-btn" onclick="pilih(5000,'3.5 Jam Playtime')">5K<br><small>3.5 Jam</small></div>
        <div class="price-btn" onclick="pilih(8000,'5 Jam Playtime')">8K<br><small>5 Jam</small></div>
        <div class="price-btn" onclick="pilih(10000,'7 Jam Playtime')">10K<br><small>7 Jam</small></div>
        <div class="price-btn" onclick="pilih(13000,'9 Jam Playtime')">13K<br><small>9 Jam</small></div>
        <div class="price-btn" onclick="pilih(15000,'12 Jam Playtime')">15K<br><small>12 Jam</small></div>
        <div class="price-btn" onclick="pilih(20000,'16 Jam Playtime')">20K<br><small>16 Jam</small></div>
        <div class="price-btn" onclick="pilih(25000,'20 Jam Playtime')">25K<br><small>20 Jam</small></div>
        <div class="price-btn" onclick="pilih(30000,'24 Jam Playtime')">30K<br><small>24 Jam</small></div>
      </div>

      <input type="text" id="target" readonly placeholder="Paket terpilih">
      <input type="text" id="harga" readonly placeholder="Harga">

      <button class="kirim" onclick="kirimOrder()">KIRIM ORDER → LANGSUNG KE WA</button>
    </div>
  </div>

  <div id="antrian" class="tab">
    <h1>ANTRIAN ORDER</h1>
    <table><thead><tr><th>No</th><th>Client</th><th>User</th><th>Paket</th><th>Harga</th><th>Aksi</th></tr></thead><tbody id="list-antrian"></tbody></table>
  </div>

  <div id="selesai" class="tab">
    <h1>ORDER SELESAI</h1>
    <table><thead><tr><th>No</th><th>Tanggal</th><th>Client</th><th>User</th><th>Paket</th><th>Harga</th></tr></thead><tbody id="list-selesai"></tbody></table>
  </div>
</div>

<script>
// GANTI NOMOR DI SINI AJA (format 628xxxxxxx)
const NOMOR_TUJUAN = "6285245644564";   // UBAH INI JADI NOMOR KAMU

let antrian = JSON.parse(localStorage.getItem('rz_antrian') || '[]');
let selesai = JSON.parse(localStorage.getItem('rz_selesai') || '[]');

// Loader
setTimeout(() => {
  document.getElementById('loader').style.opacity = '0';
  setTimeout(() => {
    document.getElementById('loader').remove();
    document.getElementById('nav').style.display = 'block';
    document.getElementById('main').style.display = 'block';
    renderAll();
  }, 600);
}, 2500);

function togglePricelist() {
  const pl = document.getElementById('pricelist');
  const h = document.querySelector('.price-header');
  pl.style.display = pl.style.display === 'grid' ? 'none' : 'grid';
  h.innerHTML = pl.style.display === 'grid' ? 'TUTUP PAKET' : 'PILIH PAKET JOKI';
}

function pilih(hrg, desc) {
  document.getElementById('harga').value = hrg;
  document.getElementById('target').value = desc;
  document.querySelectorAll('.price-btn').forEach(b => b.classList.remove('selected'));
  event.target.classList.add('selected');
}

// FUNGSI UTAMA — SUDAH 100% FIX
function kirimOrder() {
  const client = document.getElementById('client').value.trim();
  const username = document.getElementById('username').value.trim();
  const password = document.getElementById('password').value.trim();
  const target = document.getElementById('target').value;
  const harga = document.getElementById('harga').value;

  if (!client || !username || !password || !target || !harga) {
    alert('Isi semua data & pilih paket dulu bro!');
    return;
  }

  // Simpan ke antrian
  antrian.unshift({
    client, username, password, target,
    harga: parseInt(harga),
    tanggal: new Date().toLocaleDateString('id-ID')
  });
  localStorage.setItem('rz_antrian', JSON.stringify(antrian));

  // Pesan WhatsApp rapi
  const pesan = `*ORDER BARU - RZ ROBLOX JOKI*

*Client:* ${client}
*Username:* ${username}
*Password/Cookie:* ${password}
*Paket:* ${target}
*Harga:* Rp ${parseInt(harga).toLocaleString('id-ID')}

_Terima kasih sudah order di RZ Joki!_
Cepet dicek ya Raffi / Zaki!`;

  // Link WhatsApp yang benar
  const waLink = "https://wa.me/" + NOMOR_TUJUAN + "?text=" + encodeURIComponent(pesan);

  // Buka WhatsApp (di HP langsung masuk chat + pesan terisi)
  window.open(waLink, '_blank');

  alert('Order masuk antrian!\nWhatsApp sudah terbuka otomatis — tinggal klik KIRIM!');

  // Reset form
  document.getElementById('client').value = '';
  document.getElementById('username').value = '';
  document.getElementById('password').value = '';
  document.getElementById('target').value = '';
  document.getElementById('harga').value = '';
  document.querySelectorAll('.price-btn').forEach(b => b.classList.remove('selected'));
  renderAll();
}

// Render tabel
function renderAntrian() {
  const tbody = document.getElementById('list-antrian');
  tbody.innerHTML = '';
  antrian.forEach((o, i) => {
    tbody.innerHTML += `<tr>
      <td>${i+1}</td>
      <td>${o.client}</td>
      <td>${o.username}</td>
      <td>${o.target}</td>
      <td>Rp ${o.harga.toLocaleString('id-ID')}</td>
      <td>
        <button class="btn ambil" onclick="ambil(${i})">Ambil</button>
        <button class="btn done" onclick="selesaiOrder(${i})">Selesai</button>
      </td>
    </tr>`;
  });
}

function renderSelesai() {
  const tbody = document.getElementById('list-selesai');
  tbody.innerHTML = '';
  selesai.forEach((o, i) => {
    tbody.innerHTML += `<tr>
      <td>${i+1}</td>
      <td>${o.tanggal}</td>
      <td>${o.client}</td>
      <td>${o.username}</td>
      <td>${o.target}</td>
      <td>Rp ${o.harga.toLocaleString('id-ID')}</td>
    </tr>`;
  });
}

function ambil(i) {
  alert(`Order #\( {i+1} - \){antrian[i].client} telah diambil!`);
}

function selesaiOrder(i) {
  if (confirm('Yakin order ini sudah selesai?')) {
    selesai.unshift(antrian.splice(i, 1)[0]);
    localStorage.setItem('rz_antrian', JSON.stringify(antrian));
    localStorage.setItem('rz_selesai', JSON.stringify(selesai));
    renderAll();
  }
}

function show(tab) {
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.getElementById(tab).classList.add('active');
  document.querySelectorAll('.nav-menu button').forEach(b => b.classList.remove('active'));
  event.target.classList.add('active');
  renderAll();
}

function renderAll() {
  renderAntrian();
  renderSelesai();
}

// Jalankan saat dibuka
renderAll();
</script>
</body>
</html>
