# biznet-tibubeneng
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Catatan Foto</title>
<meta name="theme-color" content="#eaf1f5" media="(prefers-color-scheme: light)">
<meta name="theme-color" content="#0b161c" media="(prefers-color-scheme: dark)">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%230a7ea4'/%3E%3Ccircle cx='16' cy='16' r='9' fill='none' stroke='white' stroke-width='2.4'/%3E%3Ccircle cx='16' cy='16' r='3.4' fill='white'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,600;12..96,800&display=swap" rel="stylesheet">
<style>
  :root {
    color-scheme: light dark;
    --bg: #eaf1f5;
    --surface: #ffffff;
    --ink: #0f2530;
    --muted: #56707d;
    --line: #c6d6de;
    --accent: #0a7ea4;
    --accent-deep: #075f7d;
    --accent-2: #f2a93b;
    --accent-soft: #d9eef6;
    --accent-ink: #ffffff;
    --danger: #b3261e;
    --ok: #127a55;
    --glow: 10 126 164;
    --glow-2: 242 169 59;
    --radius: 16px;
    --ease: cubic-bezier(0.2, 0.8, 0.2, 1);
    --font: "Bricolage Grotesque", system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #0b161c;
      --surface: #13232b;
      --ink: #e6f1f5;
      --muted: #93aeba;
      --line: #25404b;
      --accent: #38bde0;
      --accent-deep: #1e9cc0;
      --accent-2: #ffc15e;
      --accent-soft: #12303a;
      --accent-ink: #04212b;
      --danger: #ff8a80;
      --ok: #5be3a1;
      --glow: 56 189 224;
      --glow-2: 255 193 94;
    }
  }
  * { box-sizing: border-box; }
  html { -webkit-text-size-adjust: 100%; }
  body {
    position: relative;
    min-height: 100vh;
    overflow-x: hidden;
    margin: 0;
    background: var(--bg);
    color: var(--ink);
    font-family: var(--font);
    font-size: 17px;
    line-height: 1.5;
  }
  /* Cahaya latar yang bergerak pelan */
  body::before {
    content: "";
    position: fixed;
    inset: -20%;
    z-index: -1;
    pointer-events: none;
    background:
      radial-gradient(40% 32% at 18% 8%, rgb(var(--glow) / 0.22), transparent 70%),
      radial-gradient(34% 28% at 88% 18%, rgb(var(--glow-2) / 0.18), transparent 70%),
      radial-gradient(40% 30% at 60% 100%, rgb(var(--glow) / 0.14), transparent 70%);
    animation: hanyut 28s ease-in-out infinite alternate;
  }
  main { position: relative; max-width: 520px; margin: 0 auto; padding: 28px 18px 60px; }

  /* Muncul berurutan saat halaman dibuka */
  main > * { animation: naik 0.55s var(--ease) backwards; }
  main > *:nth-child(2) { animation-delay: 70ms; }
  main > *:nth-child(3) { animation-delay: 130ms; }
  main > *:nth-child(4) { animation-delay: 180ms; }
  main > *:nth-child(5) { animation-delay: 230ms; }
  main > *:nth-child(6) { animation-delay: 290ms; }
  main > *:nth-child(7) { animation-delay: 340ms; }
  main > *:nth-child(8) { animation-delay: 380ms; }
  main > *:nth-child(9) { animation-delay: 420ms; }

  header { margin-bottom: 22px; }
  .judul-baris { display: flex; align-items: center; gap: 12px; }
  .logo {
    flex: none;
    width: 46px; height: 46px;
    display: grid; place-items: center;
    border-radius: 14px;
    background: linear-gradient(135deg, var(--accent), var(--accent-deep));
    box-shadow: 0 8px 20px -8px rgb(var(--glow) / 0.7);
    animation: putarLogo 0.9s var(--ease) backwards;
  }
  h1 { margin: 0; font-size: 2rem; font-weight: 800; letter-spacing: -0.02em; line-height: 1.1; }
  .sekarang { margin: 8px 0 0; color: var(--muted); font-size: 1rem; }

  /* Area foto: elemen utama halaman */
  .foto {
    appearance: none;
    font: inherit;
    padding: 0;
    position: relative;
    display: block;
    width: 100%;
    aspect-ratio: 4 / 3;
    border: 2px dashed var(--line);
    border-radius: var(--radius);
    background: var(--surface);
    overflow: hidden;
    cursor: pointer;
    color: var(--muted);
    text-align: center;
    transition: border-color 0.25s, transform 0.25s var(--ease), box-shadow 0.25s;
  }
  .foto:focus-visible { outline: 3px solid var(--accent); outline-offset: 2px; }
  .foto:not(.terisi)::after {
    content: "";
    position: absolute; inset: 0;
    border-radius: inherit;
    pointer-events: none;
    animation: cahaya 3.4s ease-in-out infinite;
  }
  .foto.terisi { border-style: solid; border-color: var(--accent); box-shadow: 0 14px 32px -18px rgb(var(--glow) / 0.8); }
  @media (hover: hover) {
    .foto:hover { border-color: var(--accent); transform: translateY(-2px); }
  }
  .foto:active { transform: scale(0.99); }
  .foto .kosong {
    position: absolute; inset: 0;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    gap: 10px; padding: 16px;
  }
  .foto .kosong svg { width: 56px; height: 56px; stroke: var(--accent); animation: melayang 3.4s ease-in-out infinite; }
  .foto .kosong strong { color: var(--ink); font-size: 1.2rem; }
  .foto img { width: 100%; height: 100%; object-fit: contain; background: #000; display: none; }
  .foto.terisi img { display: block; }
  .foto.terisi .kosong { display: none; }
  .foto.baru img { animation: muncul 0.5s var(--ease); }

  .catatan { margin: 10px 0 0; font-size: 0.9rem; color: var(--muted); }

  .aksi-foto { display: flex; gap: 10px; margin: 12px 0 0; }
  .aksi-foto label, .aksi-foto button {
    flex: 1;
    text-align: center;
    padding: 10px 12px;
    border: 1px solid var(--line);
    border-radius: 12px;
    background: var(--surface);
    color: var(--ink);
    font: inherit;
    font-size: 0.95rem;
    cursor: pointer;
    position: relative;
    transition: border-color 0.2s, background 0.2s, transform 0.15s var(--ease);
  }
  @media (hover: hover) {
    .aksi-foto label:hover, .aksi-foto button:hover { border-color: var(--accent); background: var(--accent-soft); }
  }
  .aksi-foto label:active, .aksi-foto button:active { transform: scale(0.97); }
  .aksi-foto input { position: absolute; inset: 0; opacity: 0; cursor: pointer; width: 100%; }
  .aksi-foto label:focus-within, .aksi-foto button:focus-visible { outline: 3px solid var(--accent); outline-offset: 2px; }

  form {
    margin-top: 22px;
    display: grid; gap: 18px;
    padding: 18px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    box-shadow: 0 16px 34px -24px rgb(var(--glow) / 0.7);
  }
  .kolom { display: grid; gap: 6px; }
  .kolom > label, .kolom > .judul { font-weight: 600; font-size: 0.98rem; }
  .hari { font-size: 1.5rem; font-weight: 800; letter-spacing: -0.01em; line-height: 1.2; }
  .hari small { display: block; font-size: 1rem; font-weight: 400; color: var(--muted); }
  .hari .ganti { animation: geser 0.35s var(--ease); }
  .hari small.ganti { display: block; }
  input[type="datetime-local"], input[type="text"], textarea, .pengaturan input {
    width: 100%;
    padding: 12px 14px;
    border: 1px solid var(--line);
    border-radius: 12px;
    background: var(--bg);
    color: var(--ink);
    font: inherit;
    transition: border-color 0.2s, box-shadow 0.2s, background 0.2s;
  }
  input[readonly] { opacity: 0.75; }
  textarea { min-height: 110px; resize: vertical; }
  input:focus-visible, textarea:focus-visible {
    outline: 2px solid transparent;
    border-color: var(--accent);
    box-shadow: 0 0 0 4px rgb(var(--glow) / 0.2);
    background: var(--surface);
  }
  .tautan {
    justify-self: start;
    background: none; border: 0; padding: 0;
    color: var(--accent); font: inherit; font-size: 0.95rem;
    text-decoration: underline; cursor: pointer;
  }
  .tautan[hidden] { display: none; }
  .petunjuk { margin: 0; font-size: 0.9rem; color: var(--muted); }

  .simpan {
    position: relative;
    overflow: hidden;
    padding: 15px 18px;
    border: 0;
    border-radius: var(--radius);
    background: linear-gradient(135deg, var(--accent), var(--accent-deep));
    color: var(--accent-ink);
    font: inherit;
    font-size: 1.1rem;
    font-weight: 700;
    cursor: pointer;
    box-shadow: 0 10px 22px -10px rgb(var(--glow) / 0.85);
    transition: transform 0.15s var(--ease), box-shadow 0.2s;
  }
  .simpan::after {
    content: "";
    position: absolute; inset: 0;
    background: linear-gradient(110deg, transparent 30%, rgba(255, 255, 255, 0.3) 50%, transparent 70%);
    transform: translateX(-100%);
    pointer-events: none;
  }
  @media (hover: hover) {
    .simpan:hover:not([disabled]) { transform: translateY(-1px); }
    .simpan:hover:not([disabled])::after { animation: kilau 0.8s var(--ease); }
  }
  .simpan:active:not([disabled]) { transform: scale(0.98); }
  .simpan:focus-visible { outline: 3px solid var(--ink); outline-offset: 3px; }
  .simpan[disabled] { opacity: 0.85; cursor: progress; }
  .simpan.memuat::before {
    content: "";
    display: inline-block;
    width: 1em; height: 1em;
    margin-right: 0.6em;
    border: 2px solid currentColor;
    border-right-color: transparent;
    border-radius: 50%;
    vertical-align: -0.15em;
    animation: putar 0.7s linear infinite;
  }

  .status { min-height: 1.5em; margin: 0; font-weight: 600; }
  .status > span { display: inline-block; animation: geser 0.35s var(--ease); }
  .status.ok { color: var(--ok); }
  .status.gagal { color: var(--danger); }
  .centang {
    width: 1.15em; height: 1.15em;
    margin-right: 0.4em;
    vertical-align: -0.2em;
    fill: none; stroke: currentColor; stroke-width: 3;
    stroke-linecap: round; stroke-linejoin: round;
    stroke-dasharray: 24; stroke-dashoffset: 24;
    animation: gambarCentang 0.5s 0.1s var(--ease) forwards;
  }

  h2 { font-size: 1.2rem; margin: 36px 0 10px; letter-spacing: -0.01em; }
  .riwayat { list-style: none; margin: 0; padding: 0; display: grid; gap: 10px; }
  .riwayat li {
    background: var(--surface);
    border: 1px solid var(--line);
    border-left: 4px solid var(--accent);
    border-radius: 12px;
    padding: 12px 14px;
    animation: geser 0.4s var(--ease) backwards;
  }
  .riwayat li.baru { animation: muncul 0.5s var(--ease) backwards, sorot 1.8s ease-out; }
  .riwayat .waktu { font-weight: 600; }
  .riwayat .isi { color: var(--muted); margin: 2px 0 0; overflow-wrap: anywhere; }
  .riwayat a { color: var(--accent); }
  .kosong-riwayat { color: var(--muted); }

  details.detail-lembur { color: var(--muted); }
  details.detail-lembur summary { cursor: pointer; }
  details.detail-lembur .kolom { margin-top: 12px; }
  .ket { margin: 0; padding: 10px 12px; border-radius: 12px; background: var(--accent-soft); color: var(--ink); font-size: 0.95rem; font-weight: 600; overflow-wrap: anywhere; }
  .hasil-tes { display: block; margin-top: 10px; font-weight: 600; }
  .hasil-tes.ok { color: var(--ok); }
  .hasil-tes.gagal { color: var(--danger); }
  details.pengaturan { margin-top: 36px; color: var(--muted); }
  details.pengaturan summary { cursor: pointer; }
  .pengaturan .kolom { margin-top: 12px; }
  .pengaturan p { font-size: 0.92rem; }

  /* Layar kamera */
  .kamera {
    position: fixed; inset: 0; z-index: 50;
    display: none; flex-direction: column;
    background: #000; color: #fff;
  }
  .kamera.aktif { display: flex; animation: bukaKamera 0.25s var(--ease); }
  .kamera video { flex: 1; min-height: 0; width: 100%; object-fit: cover; background: #000; }
  .kamera .info {
    position: absolute; top: 0; left: 0; right: 0;
    padding: calc(12px + env(safe-area-inset-top)) 16px 28px;
    background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0));
    font-size: 0.95rem; line-height: 1.4;
  }
  .kamera .info .jam { font-weight: 800; font-size: 1.1rem; }
  .titik {
    position: relative;
    display: inline-block;
    width: 0.6em; height: 0.6em;
    margin-right: 0.5em;
    border-radius: 50%;
    background: #ffc15e;
    vertical-align: 0.05em;
  }
  .titik::after {
    content: "";
    position: absolute; inset: 0;
    border-radius: 50%;
    background: inherit;
    animation: denyut 1.4s ease-out infinite;
  }
  .titik.siap { background: #5be3a1; }
  .titik.gagal { background: #ff7a70; }
  .titik.siap::after, .titik.gagal::after { animation: none; }
  .kilat { position: absolute; inset: 0; background: #fff; opacity: 0; pointer-events: none; }
  .kilat.jalan { animation: kilat 0.22s ease-out; }
  .kamera .bar {
    display: flex; align-items: center; justify-content: space-between; gap: 12px;
    padding: 14px 18px calc(14px + env(safe-area-inset-bottom));
    background: #000;
  }
  .kamera .bar .kanan { width: 76px; }
  .kamera .batal {
    width: 76px;
    color: #fff; background: none; border: 1px solid rgba(255, 255, 255, 0.5);
    border-radius: 12px; padding: 10px 0; font: inherit; cursor: pointer;
  }
  .rana {
    position: relative;
    width: 76px; height: 76px; padding: 0;
    border-radius: 50%; border: 4px solid #fff; background: transparent; cursor: pointer;
    transition: border-color 0.3s;
  }
  .rana.siap { border-color: #5be3a1; }
  .rana::after {
    content: "";
    position: absolute; inset: 6px;
    border-radius: 50%; background: #fff;
    transition: transform 0.12s var(--ease), background 0.12s;
  }
  .rana:active::after { transform: scale(0.82); background: #cfd8d5; }
  .kamera button:focus-visible { outline: 3px solid #7fe3cf; outline-offset: 3px; }

  /* Animasi */
  @keyframes naik { from { opacity: 0; transform: translateY(14px); } to { opacity: 1; transform: none; } }
  @keyframes muncul { from { opacity: 0; transform: scale(0.96); } to { opacity: 1; transform: none; } }
  @keyframes geser { from { opacity: 0; transform: translateX(-8px); } to { opacity: 1; transform: none; } }
  @keyframes hanyut { from { transform: translate3d(-3%, -2%, 0) scale(1); } to { transform: translate3d(3%, 2%, 0) scale(1.08); } }
  @keyframes cahaya {
    0%, 100% { box-shadow: inset 0 0 0 rgb(var(--glow) / 0); }
    50% { box-shadow: inset 0 0 46px rgb(var(--glow) / 0.2); }
  }
  @keyframes melayang { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-5px); } }
  @keyframes putar { to { transform: rotate(360deg); } }
  @keyframes putarLogo { from { transform: rotate(-120deg) scale(0.6); opacity: 0; } to { transform: none; opacity: 1; } }
  @keyframes gambarCentang { to { stroke-dashoffset: 0; } }
  @keyframes denyut { 0% { transform: scale(0.9); opacity: 0.6; } 70%, 100% { transform: scale(2.4); opacity: 0; } }
  @keyframes kilat { 0% { opacity: 0; } 20% { opacity: 0.9; } 100% { opacity: 0; } }
  @keyframes bukaKamera { from { opacity: 0; transform: scale(1.03); } to { opacity: 1; transform: none; } }
  @keyframes kilau { to { transform: translateX(100%); } }
  @keyframes sorot { 0% { background: var(--accent-soft); } 100% { background: var(--surface); } }

  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after { animation: none !important; transition: none !important; }
    .centang { stroke-dashoffset: 0; }
  }
</style>
</head>
<body>
<main>
  <header>
    <div class="judul-baris">
      <span class="logo" aria-hidden="true">
        <svg viewBox="0 0 24 24" width="26" height="26" fill="none" stroke="#fff" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="9"/><circle cx="12" cy="12" r="3.5"/>
          <path d="M12 8.5V3"/><path d="M12 8.5V3" transform="rotate(120 12 12)"/><path d="M12 8.5V3" transform="rotate(240 12 12)"/>
        </svg>
      </span>
      <h1>Catatan Foto</h1>
    </div>
    <p class="sekarang" id="sekarang" aria-live="off"></p>
  </header>

  <button type="button" class="foto" id="areaFoto" aria-label="Buka kamera">
    <img id="pratinjau" alt="Pratinjau foto yang dipilih">
    <span class="kosong">
      <svg viewBox="0 0 24 24" fill="none" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
        <path d="M4 8h3l1.6-2.4h6.8L17 8h3a1 1 0 0 1 1 1v9a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V9a1 1 0 0 1 1-1z"/>
        <circle cx="12" cy="13" r="3.6"/>
      </svg>
      <strong>Ambil foto</strong>
      <span>Foto diberi stempel jam dan lokasi otomatis</span>
    </span>
  </button>
  <p class="catatan">Stempel jam mengikuti jam HP. Aktifkan "Tanggal dan waktu otomatis" di pengaturan HP, lalu izinkan akses kamera, lokasi, dan sensor gerak (untuk kompas) saat diminta.</p>

  <div class="aksi-foto">
    <label>Pilih dari galeri
      <input type="file" id="inputGaleri" accept="image/*" aria-label="Pilih foto dari galeri">
    </label>
    <button type="button" id="hapusFoto">Ganti foto</button>
  </div>

  <form id="form" novalidate>
    <div class="kolom">
      <span class="judul">Waktu foto</span>
      <div class="hari" id="tampilHari" aria-live="polite"></div>
      <input type="datetime-local" id="waktu" aria-label="Tanggal dan jam foto">
      <p class="petunjuk" id="petunjukWaktu" hidden>Waktu mengikuti stempel pada foto.</p>
      <button type="button" class="tautan" id="pakaiSekarang">Pakai waktu sekarang</button>
    </div>

    <div class="kolom">
      <label for="jenis">Jenis kegiatan</label>
      <input type="text" id="jenis" value="TROUBLESHOOT FTTH" autocomplete="off" autocapitalize="characters">
    </div>
    <div class="kolom">
      <label for="tiket">Nomor tiket</label>
      <input type="text" id="tiket" inputmode="numeric" autocomplete="off" placeholder="Contoh: 18182637">
    </div>
    <div class="kolom">
      <label for="customer">Nama customer</label>
      <input type="text" id="customer" autocomplete="off" autocapitalize="characters" placeholder="Nama pelanggan">
    </div>
    <p class="ket" id="pratinjauKet" aria-live="polite"></p>
    <div class="kolom">
      <label for="lokasi">Lokasi</label>
      <input type="text" id="lokasi" autocomplete="off" placeholder="Otomatis dari GPS">
    </div>
    <details class="detail-lembur">
      <summary>Detail lembur (Shift Pagi, mulai 18.00)</summary>
      <div class="kolom">
        <label for="jadwal">Jadwal kerja</label>
        <input type="text" id="jadwal" value="Shift Pagi" autocomplete="off">
      </div>
      <div class="kolom">
        <label for="mulai">Mulai jam lembur</label>
        <input type="text" id="mulai" value="18.00" inputmode="decimal" autocomplete="off">
      </div>
    </details>

    <button type="submit" class="simpan" id="tombolSimpan">Simpan foto</button>
    <p class="status" id="status" role="status" aria-live="polite"></p>
  </form>

  <h2>Tersimpan terakhir</h2>
  <ul class="riwayat" id="riwayat"></ul>
  <p class="kosong-riwayat" id="riwayatKosong">Belum ada foto yang disimpan dari perangkat ini.</p>

  <details class="pengaturan" id="pengaturan">
    <summary>Pengaturan koneksi</summary>
    <p>Isi dengan alamat Web App dari Google Apps Script dan kunci yang sama dengan di Code.gs. Data ini disimpan hanya di perangkat ini.</p>
    <div class="kolom">
      <label for="urlScript">Alamat Web App</label>
      <input type="url" id="urlScript" placeholder="https://script.google.com/macros/s/.../exec" autocomplete="off">
    </div>
    <div class="kolom">
      <label for="kunci">Kunci rahasia</label>
      <input type="text" id="kunci" autocomplete="off">
    </div>
    <div class="kolom">
      <label for="indeks">Nomor indeks foto berikutnya</label>
      <input type="text" id="indeks" inputmode="numeric" autocomplete="off">
    </div>
    <button type="button" class="tautan" id="simpanPengaturan" style="margin-top:12px">Simpan pengaturan</button>
    <button type="button" class="tautan" id="tesKoneksi" style="margin:12px 0 0 18px">Tes koneksi</button>
    <span class="hasil-tes" id="hasilTes" role="status" aria-live="polite"></span>
  </details>
</main>

<!-- Layar kamera -->
<div class="kamera" id="kamera" role="dialog" aria-modal="true" aria-label="Kamera">
  <div class="info">
    <div class="jam" id="infoJam"></div>
    <div><span class="titik" id="titikGps"></span><span id="teksGps"></span></div>
    <div id="infoArah"></div>
    <div id="infoAlamat"></div>
  </div>
  <video id="video" playsinline muted autoplay></video>
  <div class="kilat" id="kilat"></div>
  <div class="bar">
    <button type="button" class="batal" id="batalKamera">Batal</button>
    <button type="button" class="rana" id="rana" aria-label="Ambil foto"></button>
    <span class="kanan"></span>
  </div>
</div>

<script>
  // Bisa diisi langsung di sini, atau lewat panel "Pengaturan koneksi" di halaman.
  const CONFIG = {
    SCRIPT_URL: "https://script.google.com/a/macros/smk.belajar.id/s/AKfycbxF0acQ_t0GDqX2CRGgmjz4K0pixKm3znfV137Yth6NNRpaA4EOVPPvgSVgDviW35fb/exec",
    SECRET: ""
  };

  const $ = (id) => document.getElementById(id);
  const HARI_FMT = new Intl.DateTimeFormat("id-ID", { weekday: "long" });
  const TGL_FMT = new Intl.DateTimeFormat("id-ID", { day: "numeric", month: "long", year: "numeric" });
  const BLN = ["Jan", "Feb", "Mar", "Apr", "Mei", "Jun", "Jul", "Agu", "Sep", "Okt", "Nov", "Des"];
  const pad = (n) => String(n).padStart(2, "0");

  let fotoBlob = null;
  let fotoStempel = null;   // diisi hanya untuk foto yang diambil langsung lewat kamera website
  let urlPratinjau = null;
  let sedangKirim = false;

  const PESAN_KONEKSI = "Tidak bisa terhubung ke Apps Script. Pastikan deployment diatur Who has access: Anyone dan alamatnya berakhiran /exec.";

  const kamera = { stream: null, pos: null, gpsError: null, watchId: null, alamat: [], alamatPos: null, alamatWaktu: 0, timer: null, heading: null, jejak: [], onOri: null };

  function ambil(k) { try { return localStorage.getItem(k); } catch (e) { return null; } }
  function simpan(k, v) { try { localStorage.setItem(k, v); } catch (e) { /* abaikan */ } }
  function urlScript() { return (ambil("urlScript") || CONFIG.SCRIPT_URL || "").trim(); }
  function kunci() { return (ambil("kunci") || CONFIG.SECRET || "").trim(); }

  function nilaiInput(d) {
    return `${d.getFullYear()}-${pad(d.getMonth() + 1)}-${pad(d.getDate())}T${pad(d.getHours())}:${pad(d.getMinutes())}`;
  }
  function teksWaktu(d) {
    return `${d.getDate()} ${BLN[d.getMonth()]} ${d.getFullYear()} ${pad(d.getHours())}.${pad(d.getMinutes())}.${pad(d.getSeconds())}`;
  }
  function zonaWaktu(d) {
    try {
      const p = new Intl.DateTimeFormat("id-ID", { timeZoneName: "short" }).formatToParts(d).find((x) => x.type === "timeZoneName");
      return p ? p.value : "";
    } catch (e) { return ""; }
  }

  function perbaruiJam() {
    const d = new Date();
    $("sekarang").textContent =
      `${HARI_FMT.format(d)}, ${TGL_FMT.format(d)}, pukul ${pad(d.getHours())}.${pad(d.getMinutes())}`;
  }

  function perbaruiHari() {
    const v = $("waktu").value;
    const wadah = $("tampilHari");
    if (!v) { wadah.textContent = "Pilih tanggal dan jam"; return; }
    const d = new Date(v);
    wadah.textContent = "";
    const namaHari = document.createElement("span");
    namaHari.className = "ganti";
    namaHari.textContent = HARI_FMT.format(d);
    wadah.append(namaHari);
    const kecil = document.createElement("small");
    kecil.className = "ganti";
    kecil.textContent = `${TGL_FMT.format(d)}, pukul ${pad(d.getHours())}.${pad(d.getMinutes())}`;
    wadah.append(kecil);
  }

  function setStatus(teks, jenis) {
    const s = $("status");
    s.className = "status" + (jenis ? " " + jenis : "");
    s.textContent = "";
    if (!teks) return;
    const span = document.createElement("span");
    if (jenis === "ok") {
      const NS = "http://www.w3.org/2000/svg";
      const svg = document.createElementNS(NS, "svg");
      svg.setAttribute("viewBox", "0 0 24 24");
      svg.setAttribute("class", "centang");
      svg.setAttribute("aria-hidden", "true");
      const path = document.createElementNS(NS, "path");
      path.setAttribute("d", "M5 13l4 4L19 7");
      svg.append(path);
      span.append(svg);
    }
    span.append(document.createTextNode(teks));
    s.append(span);
  }

  /* ---------- Pratinjau dan pilihan foto ---------- */

  function tampilkanPratinjau(blob) {
    if (urlPratinjau) URL.revokeObjectURL(urlPratinjau);
    urlPratinjau = URL.createObjectURL(blob);
    $("pratinjau").src = urlPratinjau;
    const area = $("areaFoto");
    area.classList.remove("baru");
    void area.offsetWidth;
    area.classList.add("terisi", "baru");
  }

  function kunciWaktu(kunciIya) {
    $("waktu").readOnly = kunciIya;
    $("petunjukWaktu").hidden = !kunciIya;
    $("pakaiSekarang").hidden = kunciIya;
  }

  function pilihDariGaleri(file) {
    if (!file) return;
    if (!file.type.startsWith("image/")) { setStatus("File harus berupa gambar.", "gagal"); return; }
    fotoBlob = file;
    fotoStempel = null;
    tampilkanPratinjau(file);
    kunciWaktu(false);
    if (file.lastModified) {
      $("waktu").value = nilaiInput(new Date(file.lastModified));
      perbaruiHari();
    }
    setStatus("Foto dari galeri disimpan apa adanya, tanpa stempel jam dan lokasi.");
  }

  function hapusFoto() {
    fotoBlob = null;
    fotoStempel = null;
    if (urlPratinjau) { URL.revokeObjectURL(urlPratinjau); urlPratinjau = null; }
    $("pratinjau").removeAttribute("src");
    $("areaFoto").classList.remove("terisi");
    $("inputGaleri").value = "";
    kunciWaktu(false);
  }

  /* ---------- Kamera, GPS, dan stempel ---------- */

  function jarakMeter(a, b) {
    const R = 6371000, rad = (x) => x * Math.PI / 180;
    const dLat = rad(b.lat - a.lat), dLon = rad(b.lon - a.lon);
    const h = Math.sin(dLat / 2) ** 2 + Math.cos(rad(a.lat)) * Math.cos(rad(b.lat)) * Math.sin(dLon / 2) ** 2;
    return 2 * R * Math.asin(Math.sqrt(h));
  }

  function susunAlamat(j) {
    const a = (j && j.address) || {};
    const jalan = a.road || "";
    const desa = a.village || a.suburb || a.neighbourhood || a.hamlet || "";
    const kecRaw = a.city_district || a.municipality || "";
    const kec = kecRaw ? (/^kecamatan\b/i.test(kecRaw) ? kecRaw : "Kecamatan " + kecRaw) : "";
    let kab = "";
    if (a.county) kab = /^(kabupaten|kota)\b/i.test(a.county) ? a.county : "Kabupaten " + a.county;
    else if (a.city) kab = /^(kabupaten|kota)\b/i.test(a.city) ? a.city : "Kota " + a.city;
    const baris = [jalan, desa, kec, kab, a.state || ""].filter(Boolean);
    const unik = baris.filter((t, i) => i === 0 || t !== baris[i - 1]);
    if (unik.length) return unik;
    if (j && j.display_name) return j.display_name.split(",").map((x) => x.trim()).slice(0, 5);
    return [];
  }

  async function cariAlamat(lat, lon) {
    const sekarang = Date.now();
    if (kamera.alamat.length && kamera.alamatPos && jarakMeter(kamera.alamatPos, { lat, lon }) < 50) return;
    if (sekarang - kamera.alamatWaktu < 8000) return;
    kamera.alamatWaktu = sekarang;
    try {
      const r = await fetch(
        "https://nominatim.openstreetmap.org/reverse?format=jsonv2&zoom=18&addressdetails=1&accept-language=id" +
        `&lat=${encodeURIComponent(lat)}&lon=${encodeURIComponent(lon)}`
      );
      if (!r.ok) return;
      const j = await r.json();
      const alamat = susunAlamat(j);
      if (alamat.length) { kamera.alamat = alamat; kamera.alamatPos = { lat, lon }; }
    } catch (e) { /* tanpa internet: stempel memakai koordinat saja */ }
  }

  function mulaiGps() {
    kamera.pos = null; kamera.gpsError = null; kamera.alamat = []; kamera.alamatPos = null; kamera.alamatWaktu = 0; kamera.jejak = [];
    if (!navigator.geolocation) { kamera.gpsError = "GPS tidak didukung browser ini"; return; }
    kamera.watchId = navigator.geolocation.watchPosition(
      (p) => {
        kamera.pos = p; kamera.gpsError = null;
        kamera.jejak.push({ lat: p.coords.latitude, lon: p.coords.longitude, acc: p.coords.accuracy, t: Date.now() });
        if (kamera.jejak.length > 30) kamera.jejak.shift();
        cariAlamat(p.coords.latitude, p.coords.longitude);
      },
      (err) => { kamera.gpsError = err.code === 1 ? "Izin lokasi ditolak" : "GPS belum dapat sinyal"; },
      { enableHighAccuracy: true, maximumAge: 0, timeout: 20000 }
    );
  }

  /* ---------- Kompas, kecepatan, dan nomor indeks ---------- */

  const ARAH8 = ["N", "NE", "E", "SE", "S", "SW", "W", "NW"];
  function hurufArah(d) { return ARAH8[Math.round(d / 45) % 8]; }

  function arahDariSensor(alpha, beta, gamma) {
    const rad = Math.PI / 180;
    const x = beta * rad, y = gamma * rad, z = alpha * rad;
    const cY = Math.cos(y), cZ = Math.cos(z), sX = Math.sin(x), sY = Math.sin(y), sZ = Math.sin(z);
    const vx = -cZ * sY - sZ * sX * cY;
    const vy = -sZ * sY + cZ * sX * cY;
    let h = Math.atan(vx / vy);
    if (vy < 0) h += Math.PI; else if (vx < 0) h += 2 * Math.PI;
    return h * 180 / Math.PI;
  }

  function haluskan(lama, baru) {
    if (lama === null) return baru;
    const selisih = ((baru - lama + 540) % 360) - 180;
    return (lama + selisih * 0.3 + 360) % 360;
  }

  function pasangKompas() {
    if (kamera.onOri) return;
    kamera.onOri = (e) => {
      let h = null;
      if (typeof e.webkitCompassHeading === "number") h = e.webkitCompassHeading;
      else if ((e.type === "deviceorientationabsolute" || e.absolute === true) && e.alpha !== null && e.beta !== null && e.gamma !== null) {
        h = arahDariSensor(e.alpha, e.beta, e.gamma);
      }
      if (h !== null && !isNaN(h)) kamera.heading = haluskan(kamera.heading, ((h % 360) + 360) % 360);
    };
    window.addEventListener("deviceorientationabsolute", kamera.onOri, true);
    window.addEventListener("deviceorientation", kamera.onOri, true);
  }

  function mulaiKompas() {
    kamera.heading = null;
    const DOE = window.DeviceOrientationEvent;
    if (DOE && typeof DOE.requestPermission === "function") {
      DOE.requestPermission().then((r) => { if (r === "granted") pasangKompas(); }).catch(() => {});
    } else {
      pasangKompas();
    }
  }

  function hentikanKompas() {
    if (kamera.onOri) {
      window.removeEventListener("deviceorientationabsolute", kamera.onOri, true);
      window.removeEventListener("deviceorientation", kamera.onOri, true);
      kamera.onOri = null;
    }
  }

  // Arah dari kompas HP; bila tidak ada, dari arah gerak GPS saat bergerak. Bila tidak ada keduanya: null.
  function arahSekarang() {
    if (kamera.heading !== null) return kamera.heading;
    const p = kamera.pos;
    if (p && typeof p.coords.heading === "number" && !isNaN(p.coords.heading) && (p.coords.speed || 0) > 1) return p.coords.heading;
    return null;
  }

  // Kecepatan (km/jam) dari GPS; bila sensor tidak melapor, dihitung dari selisih posisi. Bila tidak bisa: null.
  function kecepatanSekarang() {
    const p = kamera.pos;
    if (!p) return null;
    const v = p.coords.speed;
    if (typeof v === "number" && !isNaN(v) && v >= 0) return v * 3.6;
    const j = kamera.jejak;
    if (j.length < 2) return null;
    const akhir = j[j.length - 1];
    const awal = j.find((x) => akhir.t - x.t <= 15000) || j[0];
    const dt = (akhir.t - awal.t) / 1000;
    if (dt < 3) return null;
    const jarak = jarakMeter({ lat: awal.lat, lon: awal.lon }, { lat: akhir.lat, lon: akhir.lon });
    const batas = Math.max(akhir.acc || 0, awal.acc || 0, 10);
    return jarak <= batas ? 0 : (jarak / dt) * 3.6;
  }

  function ambilIndeks() {
    const n = parseInt(ambil("indeksFoto") || "1", 10);
    return isNaN(n) || n < 1 ? 1 : n;
  }

  function perbaruiInfoKamera() {
    const d = new Date();
    $("infoJam").textContent = `Jam HP ${teksWaktu(d)} ${zonaWaktu(d)}`;
    let gps;
    if (kamera.pos) gps = `GPS siap, akurasi sekitar ${Math.round(kamera.pos.coords.accuracy)} m`;
    else if (kamera.gpsError) gps = `GPS: ${kamera.gpsError}`;
    else gps = "GPS: mencari sinyal...";
    $("teksGps").textContent = gps;
    $("titikGps").className = "titik" + (kamera.pos ? " siap" : kamera.gpsError ? " gagal" : "");
    $("rana").classList.toggle("siap", !!kamera.pos);
    $("infoAlamat").textContent = kamera.alamat.length ? kamera.alamat.join(", ") : "";
    const ar = arahSekarang();
    $("infoArah").textContent = ar === null ? "" : `Arah ${Math.round(ar) % 360}° ${hurufArah(ar)}`;
  }

  async function bukaKamera() {
    mulaiKompas();
    if (!navigator.mediaDevices || !navigator.mediaDevices.getUserMedia) {
      setStatus("Kamera tidak didukung di browser ini. Pakai Pilih dari galeri.", "gagal");
      return;
    }
    try {
      kamera.stream = await navigator.mediaDevices.getUserMedia({
        video: { facingMode: { ideal: "environment" }, width: { ideal: 1920 }, height: { ideal: 1080 } },
        audio: false
      });
    } catch (e) {
      hentikanKompas();
      setStatus("Kamera tidak bisa dibuka. Izinkan akses kamera di browser, atau pakai Pilih dari galeri.", "gagal");
      return;
    }
    const v = $("video");
    v.srcObject = kamera.stream;
    try { await v.play(); } catch (e) { /* diputar otomatis */ }
    $("kamera").classList.add("aktif");
    document.body.style.overflow = "hidden";
    mulaiGps();
    perbaruiInfoKamera();
    kamera.timer = setInterval(perbaruiInfoKamera, 1000);
    $("rana").focus();
  }

  function tutupKamera() {
    if (kamera.stream) { kamera.stream.getTracks().forEach((t) => t.stop()); kamera.stream = null; }
    if (kamera.watchId !== null && navigator.geolocation) { navigator.geolocation.clearWatch(kamera.watchId); kamera.watchId = null; }
    if (kamera.timer) { clearInterval(kamera.timer); kamera.timer = null; }
    kamera.mengambil = false;
    hentikanKompas();
    $("video").srcObject = null;
    $("kamera").classList.remove("aktif");
    document.body.style.overflow = "";
  }

  function bungkus(ctx, teks, maksLebar) {
    const kata = teks.split(" ");
    const baris = [];
    let cur = "";
    kata.forEach((k) => {
      const uji = cur ? cur + " " + k : k;
      if (ctx.measureText(uji).width > maksLebar && cur) { baris.push(cur); cur = k; } else { cur = uji; }
    });
    if (cur) baris.push(cur);
    return baris;
  }

  const FONT_STEMPEL = 'Roboto, "Segoe UI", system-ui, -apple-system, sans-serif';

  function gambarKompas(ctx, w, arah) {
    const r = Math.round(w * 0.1);
    const m = Math.round(w * 0.004);
    const cx = m + r, cy = m + r;
    const tebal = r * 0.28;
    ctx.save();
    ctx.beginPath();
    ctx.arc(cx, cy, r - tebal / 2, 0, Math.PI * 2);
    ctx.lineWidth = tebal;
    ctx.strokeStyle = "rgba(38, 38, 38, 0.88)";
    ctx.stroke();

    ctx.fillStyle = "#ffffff";
    ctx.font = `700 ${Math.round(tebal * 0.78)}px ${FONT_STEMPEL}`;
    ctx.textAlign = "center";
    ctx.textBaseline = "middle";
    [["N", 0], ["E", 90], ["S", 180], ["W", 270]].forEach(([huruf, bearing]) => {
      ctx.save();
      ctx.translate(cx, cy);
      ctx.rotate((bearing - arah) * Math.PI / 180);
      ctx.fillText(huruf, 0, -(r - tebal / 2));
      ctx.restore();
    });

    ctx.beginPath();
    ctx.moveTo(cx, cy - r * 0.55);
    ctx.lineTo(cx - r * 0.12, cy + r * 0.58);
    ctx.lineTo(cx + r * 0.12, cy + r * 0.58);
    ctx.closePath();
    ctx.fillStyle = "#1fa3d8";
    ctx.fill();
    ctx.restore();
  }

  // Susunan stempel: jam, arah, jalan, desa, kecamatan, kabupaten, provinsi, altitude, speed, index number.
  // Semua nilai dari sensor HP; baris yang datanya tidak tersedia dilewati, tidak diisi karangan.
  function gambarStempel(ctx, w, h, d, info) {
    const fs = Math.max(14, Math.round(Math.min(w, h) * 0.036));
    const pitch = Math.round(fs * 1.33);
    const marginKanan = Math.round(w * 0.008);
    const marginBawah = Math.round(fs * 0.4);

    const baris = [teksWaktu(d)];
    if (info.arah !== null) baris.push(`${Math.round(info.arah) % 360}° ${hurufArah(info.arah)}`);
    info.alamat.forEach((t) => baris.push(t));
    const alt = info.pos ? info.pos.alt : null;
    if (typeof alt === "number" && !isNaN(alt)) baris.push(`Altitude:${alt.toFixed(1)}msnm`);
    if (info.kecepatan !== null) baris.push(`Speed:${info.kecepatan.toFixed(1)}km/h`);
    baris.push(`Index number: ${info.indeks}`);

    ctx.save();
    ctx.font = `500 ${fs}px ${FONT_STEMPEL}`;
    ctx.textAlign = "right";
    ctx.textBaseline = "alphabetic";
    ctx.fillStyle = "#ffffff";
    ctx.shadowColor = "rgba(0, 0, 0, 0.7)";
    ctx.shadowBlur = Math.max(2, fs * 0.12);
    ctx.shadowOffsetX = fs * 0.03;
    ctx.shadowOffsetY = fs * 0.03;
    baris.forEach((t, i) => {
      const y = h - marginBawah - (baris.length - 1 - i) * pitch;
      ctx.fillText(t, w - marginKanan, y, w * 0.78);
      ctx.fillText(t, w - marginKanan, y, w * 0.78);
    });
    ctx.restore();

    if (info.arah !== null) gambarKompas(ctx, w, info.arah);
  }

  async function ambilFoto() {
    const v = $("video");
    if (!v.videoWidth || kamera.mengambil) { return; }
    kamera.mengambil = true;

    // Jam diambil dari HP tepat saat tombol ditekan; lokasi dari GPS terakhir.
    const waktu = new Date();
    const p = kamera.pos;
    const pos = p ? { lat: p.coords.latitude, lon: p.coords.longitude, acc: p.coords.accuracy, alt: p.coords.altitude } : null;
    const alamat = kamera.alamat.slice();
    const arah = arahSekarang();
    const kecepatan = kecepatanSekarang();
    const indeks = ambilIndeks();
    simpan("indeksFoto", String(indeks + 1));
    $("indeks").value = String(indeks + 1);

    const skala = Math.min(1, 1600 / Math.max(v.videoWidth, v.videoHeight));
    const w = Math.round(v.videoWidth * skala);
    const h = Math.round(v.videoHeight * skala);
    const c = document.createElement("canvas");
    c.width = w; c.height = h;
    const ctx = c.getContext("2d");
    ctx.drawImage(v, 0, 0, w, h);
    gambarStempel(ctx, w, h, waktu, { pos, alamat, arah, kecepatan, indeks });

    const blob = await new Promise((res) => c.toBlob(res, "image/jpeg", 0.88));
    const kilat = $("kilat");
    kilat.classList.remove("jalan");
    void kilat.offsetWidth;
    kilat.classList.add("jalan");
    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) await new Promise((r) => setTimeout(r, 200));
    tutupKamera();
    if (!blob) { setStatus("Foto gagal diproses. Coba ambil lagi.", "gagal"); return; }

    fotoBlob = blob;
    fotoStempel = {
      waktuIso: waktu.toISOString(),
      koordinat: pos ? `${pos.lat.toFixed(6)}, ${pos.lon.toFixed(6)} (±${Math.round(pos.acc)} m)` : "",
      alamat: alamat.join(", ")
    };
    tampilkanPratinjau(blob);
    $("waktu").value = nilaiInput(waktu);
    $("lokasi").value = lokasiSingkat(alamat, pos);
    kunciWaktu(true);
    perbaruiHari();
    if (pos) setStatus("Foto berstempel jam dan lokasi siap disimpan.", "ok");
    else setStatus("Foto ini tanpa lokasi GPS. Ambil ulang setelah GPS siap jika lokasi diperlukan.", "gagal");
  }

  /* ---------- Keterangan dan lokasi ---------- */

  function susunKeterangan() {
    return [$("jenis").value, $("tiket").value, $("customer").value]
      .map((x) => x.trim()).filter(Boolean).join(" ").toUpperCase();
  }

  function perbaruiKeterangan() {
    const k = susunKeterangan();
    $("pratinjauKet").textContent = k ? "Keterangan: " + k : "Keterangan masih kosong";
  }

  function lokasiSingkat(alamat, pos) {
    if (alamat.length) return alamat[0].replace(/^Jalan\s+/i, "Jl. ");
    return pos ? `${pos.lat.toFixed(5)}, ${pos.lon.toFixed(5)}` : "";
  }

  /* ---------- Simpan ---------- */

  function kompres(file, sisiMaks = 1600, mutu = 0.82) {
    return new Promise((resolve, reject) => {
      const url = URL.createObjectURL(file);
      const img = new Image();
      img.onload = () => {
        const skala = Math.min(1, sisiMaks / Math.max(img.width, img.height));
        const w = Math.round(img.width * skala);
        const h = Math.round(img.height * skala);
        const c = document.createElement("canvas");
        c.width = w; c.height = h;
        c.getContext("2d").drawImage(img, 0, 0, w, h);
        URL.revokeObjectURL(url);
        c.toBlob((b) => b ? resolve(b) : reject(new Error("Foto gagal diproses.")), "image/jpeg", mutu);
      };
      img.onerror = () => { URL.revokeObjectURL(url); reject(new Error("Foto tidak bisa dibaca.")); };
      img.src = url;
    });
  }

  function keBase64(blob) {
    return new Promise((resolve, reject) => {
      const r = new FileReader();
      r.onload = () => resolve(String(r.result).split(",")[1]);
      r.onerror = () => reject(new Error("Foto gagal dibaca."));
      r.readAsDataURL(blob);
    });
  }

  function muatRiwayat() {
    try { return JSON.parse(ambil("riwayat") || "[]"); } catch (e) { return []; }
  }

  function gambarRiwayat(baru) {
    const daftar = muatRiwayat();
    const ul = $("riwayat");
    ul.textContent = "";
    $("riwayatKosong").style.display = daftar.length ? "none" : "block";
    daftar.forEach((item, i) => {
      const li = document.createElement("li");
      if (baru) {
        if (i === 0) li.className = "baru";
        else li.style.animation = "none";
      } else {
        li.style.animationDelay = `${Math.min(i, 8) * 60}ms`;
      }
      const w = document.createElement("div");
      w.className = "waktu";
      w.textContent = `${item.hari}, ${item.tanggalPanjang}, pukul ${item.jam}`;
      li.append(w);
      if (item.deskripsi) {
        const p = document.createElement("p");
        p.className = "isi";
        p.textContent = item.deskripsi;
        li.append(p);
      }
      if (typeof item.link === "string" && item.link.startsWith("https://")) {
        const a = document.createElement("a");
        a.href = item.link;
        a.target = "_blank";
        a.rel = "noopener";
        a.textContent = "Buka foto di Drive";
        const p2 = document.createElement("p");
        p2.className = "isi";
        p2.append(a);
        li.append(p2);
      }
      ul.append(li);
    });
  }

  async function kirim(e) {
    e.preventDefault();
    if (sedangKirim) return;

    if (!urlScript()) {
      $("pengaturan").open = true;
      setStatus("Isi alamat Web App di Pengaturan koneksi dulu.", "gagal");
      return;
    }
    if (!fotoBlob) { setStatus("Ambil atau pilih foto dulu.", "gagal"); return; }
    if (!$("waktu").value) { setStatus("Isi tanggal dan jam foto.", "gagal"); return; }

    sedangKirim = true;
    $("tombolSimpan").disabled = true;
    $("tombolSimpan").classList.add("memuat");
    $("tombolSimpan").textContent = "Menyimpan...";
    setStatus("Menyimpan foto...");

    try {
      const d = new Date($("waktu").value);
      const hari = HARI_FMT.format(d);
      const tanggal = `${d.getFullYear()}-${pad(d.getMonth() + 1)}-${pad(d.getDate())}`;
      const jam = `${pad(d.getHours())}:${pad(d.getMinutes())}`;
      const keterangan = susunKeterangan();
      const lokasi = $("lokasi").value.trim();
      const jadwal = $("jadwal").value.trim() || "Shift Pagi";
      const mulai = $("mulai").value.trim() || "18.00";

      // Foto berstempel sudah berupa JPEG final, jangan dikompres ulang.
      const jpg = fotoStempel ? fotoBlob : await kompres(fotoBlob);
      const data = await keBase64(jpg);

      const payload = {
        secret: kunci(),
        hari, tanggal, jam, keterangan, lokasi, jadwal, mulai,
        koordinat: fotoStempel ? fotoStempel.koordinat : "",
        alamat: fotoStempel ? fotoStempel.alamat : "",
        stempel: !!fotoStempel,
        namaFile: `foto_${tanggal}_${jam.replace(":", "")}.jpg`,
        mimeType: "image/jpeg",
        data
      };

      // text/plain menghindari preflight CORS pada Google Apps Script.
      const res = await fetch(urlScript(), {
        method: "POST",
        headers: { "Content-Type": "text/plain;charset=utf-8" },
        body: JSON.stringify(payload)
      });
      const hasil = await res.json();
      if (!hasil.ok) throw new Error(hasil.error || "Server menolak permintaan.");

      const daftar = muatRiwayat();
      daftar.unshift({ hari, tanggalPanjang: TGL_FMT.format(d), jam: jam.replace(":", "."), deskripsi: keterangan, link: hasil.link });
      simpan("riwayat", JSON.stringify(daftar.slice(0, 15)));
      gambarRiwayat(true);

      hapusFoto();
      $("tiket").value = "";
      $("customer").value = "";
      $("lokasi").value = "";
      perbaruiKeterangan();
      $("waktu").value = nilaiInput(new Date());
      perbaruiHari();
      setStatus("Foto tersimpan di Drive dan Sheet.", "ok");
    } catch (err) {
      const masalahJaringan = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      setStatus("Gagal menyimpan: " + (masalahJaringan ? PESAN_KONEKSI : err.message) + " Data masih ada, coba lagi.", "gagal");
    } finally {
      sedangKirim = false;
      $("tombolSimpan").disabled = false;
      $("tombolSimpan").classList.remove("memuat");
      $("tombolSimpan").textContent = "Simpan foto";
    }
  }

  async function tesKoneksi() {
    const hasil = $("hasilTes");
    const url = ($("urlScript").value || urlScript()).trim();
    const tulis = (t, j) => { hasil.textContent = t; hasil.className = "hasil-tes" + (j ? " " + j : ""); };
    if (!url) { tulis("Isi alamat Web App dulu.", "gagal"); return; }
    tulis("Menguji koneksi...");
    try {
      const r = await fetch(url, { method: "GET" });
      const j = await r.json();
      if (j && j.ok) tulis("Koneksi berhasil, server aktif.", "ok");
      else tulis("Server menjawab, tapi isinya tidak dikenali.", "gagal");
    } catch (e) {
      tulis(PESAN_KONEKSI, "gagal");
    }
  }

  /* ---------- Inisialisasi ---------- */

  $("waktu").value = nilaiInput(new Date());
  $("waktu").addEventListener("input", perbaruiHari);
  $("pakaiSekarang").addEventListener("click", () => { $("waktu").value = nilaiInput(new Date()); perbaruiHari(); });
  $("areaFoto").addEventListener("click", bukaKamera);
  $("rana").addEventListener("click", ambilFoto);
  $("batalKamera").addEventListener("click", tutupKamera);
  $("inputGaleri").addEventListener("change", (e) => pilihDariGaleri(e.target.files[0]));
  $("hapusFoto").addEventListener("click", hapusFoto);
  $("form").addEventListener("submit", kirim);
  ["jenis", "tiket", "customer"].forEach((id) => $(id).addEventListener("input", perbaruiKeterangan));
  document.addEventListener("keydown", (e) => { if (e.key === "Escape" && $("kamera").classList.contains("aktif")) tutupKamera(); });
  window.addEventListener("pagehide", tutupKamera);
  $("tesKoneksi").addEventListener("click", tesKoneksi);
  $("simpanPengaturan").addEventListener("click", () => {
    simpan("urlScript", $("urlScript").value.trim());
    simpan("kunci", $("kunci").value.trim());
    const nomor = parseInt($("indeks").value, 10);
    if (!isNaN(nomor) && nomor >= 1) simpan("indeksFoto", String(nomor));
    $("pengaturan").open = false;
    setStatus("Pengaturan tersimpan.", "ok");
  });
  $("urlScript").value = ambil("urlScript") || CONFIG.SCRIPT_URL;
  $("kunci").value = ambil("kunci") || CONFIG.SECRET;
  $("indeks").value = String(ambilIndeks());

  perbaruiJam();
  setInterval(perbaruiJam, 30000);
  perbaruiHari();
  gambarRiwayat();
  perbaruiKeterangan();
</script>
</body>
</html>
