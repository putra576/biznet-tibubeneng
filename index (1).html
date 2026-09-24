<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Catatan Foto</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js" defer></script>
<meta name="theme-color" content="#f4f7f9" media="(prefers-color-scheme: light)">
<meta name="theme-color" content="#0a1217" media="(prefers-color-scheme: dark)">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%230a7ea4'/%3E%3Ccircle cx='16' cy='16' r='9' fill='none' stroke='white' stroke-width='2.4'/%3E%3Ccircle cx='16' cy='16' r='3.4' fill='white'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,600;12..96,800&display=swap" rel="stylesheet">
<style>
  :root {
    color-scheme: light dark;
    --bg: #f4f7f9;
    --surface: #ffffff;
    --ink: #12252e;
    --muted: #5e7682;
    --line: #d5e1e8;
    --accent: #0b7fa3;
    --accent-deep: #066484;
    --accent-2: #e8a43a;
    --accent-soft: #e6f4f9;
    --accent-ink: #ffffff;
    --danger: #c0392b;
    --ok: #0f8a5f;
    --glow: 11 127 163;
    --glow-2: 232 164 58;
    --radius: 18px;
    --radius-sm: 12px;
    --shadow: 0 1px 2px rgb(15 37 46 / 0.04), 0 8px 24px -12px rgb(15 37 46 / 0.12);
    --shadow-lg: 0 4px 8px rgb(15 37 46 / 0.04), 0 20px 40px -20px rgb(var(--glow) / 0.35);
    --ease: cubic-bezier(0.22, 1, 0.36, 1);
    --font: "Bricolage Grotesque", system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #0a1217;
      --surface: #121f27;
      --ink: #e8f2f6;
      --muted: #8aa3b0;
      --line: #1e3340;
      --accent: #3bc4e6;
      --accent-deep: #1ea8cc;
      --accent-2: #ffc15e;
      --accent-soft: #0f2833;
      --accent-ink: #04212b;
      --danger: #ff8a80;
      --ok: #5be3a1;
      --glow: 59 196 230;
      --glow-2: 255 193 94;
      --shadow: 0 1px 2px rgb(0 0 0 / 0.2), 0 8px 24px -12px rgb(0 0 0 / 0.45);
      --shadow-lg: 0 4px 12px rgb(0 0 0 / 0.25), 0 24px 48px -20px rgb(var(--glow) / 0.25);
    }
  }
  *, *::before, *::after { box-sizing: border-box; }
  [hidden] { display: none !important; }
  html {
    -webkit-text-size-adjust: 100%;
    text-size-adjust: 100%;
    scroll-behavior: smooth;
    /* Cegah overscroll bounce mengganggu di iOS */
    overscroll-behavior-y: none;
  }
  body {
    position: relative;
    min-height: 100vh;
    min-height: 100dvh;
    overflow-x: hidden;
    margin: 0;
    padding: env(safe-area-inset-top) 0 0;
    background: var(--bg);
    color: var(--ink);
    font-family: var(--font);
    font-size: 16px; /* minimal 16px = cegah zoom otomatis di iOS saat fokus input */
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    -webkit-tap-highlight-color: transparent;
    touch-action: manipulation; /* hilangkan delay 300ms di tombol */
  }
  body::before {
    content: "";
    position: fixed;
    inset: -20%;
    z-index: -1;
    pointer-events: none;
    will-change: transform;
    background:
      radial-gradient(38% 30% at 12% 6%, rgb(var(--glow) / 0.12), transparent 70%),
      radial-gradient(30% 26% at 92% 12%, rgb(var(--glow-2) / 0.08), transparent 70%);
    animation: hanyut 36s ease-in-out infinite alternate;
  }
  /* Di HP hemat baterai/CPU: kurangi animasi latar */
  @media (max-width: 600px) {
    body::before {
      animation: none;
      inset: 0;
      will-change: auto;
      background:
        radial-gradient(50% 40% at 10% 0%, rgb(var(--glow) / 0.1), transparent 70%),
        radial-gradient(40% 30% at 100% 10%, rgb(var(--glow-2) / 0.07), transparent 70%);
    }
  }
  main {
    position: relative;
    max-width: 440px;
    margin: 0 auto;
    padding: 16px 14px calc(40px + env(safe-area-inset-bottom));
    padding-left: max(14px, env(safe-area-inset-left));
    padding-right: max(14px, env(safe-area-inset-right));
  }
  @media (min-width: 400px) {
    main { padding-top: 20px; padding-left: 16px; padding-right: 16px; }
  }
  /* Animasi masuk hanya di layar lebar / tidak reduced-motion */
  @media (min-width: 600px) {
    main > * { animation: naik 0.45s var(--ease) backwards; }
    main > *:nth-child(2) { animation-delay: 40ms; }
    main > *:nth-child(3) { animation-delay: 80ms; }
    main > *:nth-child(4) { animation-delay: 110ms; }
    main > *:nth-child(5) { animation-delay: 140ms; }
  }

  header { margin-bottom: 18px; }
  .judul-baris { display: flex; align-items: center; gap: 12px; }
  .logo {
    flex: none;
    width: 42px; height: 42px;
    display: grid; place-items: center;
    border-radius: 13px;
    background: linear-gradient(145deg, var(--accent), var(--accent-deep));
    box-shadow: 0 6px 16px -6px rgb(var(--glow) / 0.55);
    animation: putarLogo 0.8s var(--ease) backwards;
  }
  h1 {
    margin: 0;
    font-size: 1.55rem;
    font-weight: 800;
    letter-spacing: -0.03em;
    line-height: 1.15;
  }
  .sekarang {
    margin: 6px 0 0;
    padding-left: 54px;
    color: var(--muted);
    font-size: 0.9rem;
  }
  h2 {
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--muted);
    margin: 28px 0 10px;
  }

  /* Area foto */
  .foto {
    appearance: none;
    font: inherit;
    padding: 0;
    position: relative;
    display: block;
    width: 100%;
    aspect-ratio: 4 / 3;
    border: 1.5px dashed var(--line);
    border-radius: var(--radius);
    background: var(--surface);
    overflow: hidden;
    cursor: pointer;
    color: var(--muted);
    text-align: center;
    box-shadow: var(--shadow);
    transition: border-color 0.25s, transform 0.25s var(--ease), box-shadow 0.25s;
  }
  .foto:focus-visible { outline: 2px solid var(--accent); outline-offset: 3px; }
  .foto:not(.terisi)::after {
    content: "";
    position: absolute; inset: 0;
    border-radius: inherit;
    pointer-events: none;
    animation: cahaya 4s ease-in-out infinite;
  }
  .foto.terisi {
    border-style: solid;
    border-color: var(--accent);
    box-shadow: var(--shadow-lg);
  }
  @media (hover: hover) {
    .foto:hover { border-color: var(--accent); transform: translateY(-1px); }
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

  /* catatan di bawah area foto — didefinisikan ulang di .aksi-foto */

  .aksi-foto { display: flex; gap: 8px; margin: 10px 0 0; }
  .aksi-foto label, .aksi-foto button {
    flex: 1;
    text-align: center;
    padding: 10px 12px;
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
    background: var(--surface);
    color: var(--ink);
    font: inherit;
    font-size: 0.88rem;
    font-weight: 600;
    cursor: pointer;
    position: relative;
    box-shadow: var(--shadow);
    transition: border-color 0.2s, background 0.2s, transform 0.15s var(--ease);
  }
  @media (hover: hover) {
    .aksi-foto label:hover, .aksi-foto button:hover { border-color: var(--accent); background: var(--accent-soft); }
  }
  .aksi-foto label:active, .aksi-foto button:active { transform: scale(0.97); }
  .aksi-foto input { position: absolute; inset: 0; opacity: 0; cursor: pointer; width: 100%; }
  .aksi-foto label:focus-within, .aksi-foto button:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
  .catatan { margin: 8px 0 0; font-size: 0.82rem; color: var(--muted); line-height: 1.4; }

  form {
    margin-top: 16px;
    display: grid; gap: 14px;
    padding: 16px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
  }
  .kolom { display: grid; gap: 5px; }
  .kolom > label, .kolom > .judul {
    font-weight: 600;
    font-size: 0.84rem;
    color: var(--muted);
    letter-spacing: 0.01em;
  }
  .hari { font-size: 1.28rem; font-weight: 800; letter-spacing: -0.02em; line-height: 1.2; color: var(--ink); }
  .hari small { display: block; font-size: 0.9rem; font-weight: 400; color: var(--muted); margin-top: 2px; }
  .hari .ganti { animation: geser 0.35s var(--ease); }
  .hari small.ganti { display: block; }
  input[type="datetime-local"], input[type="month"], input[type="date"], input[type="text"],
  input[type="password"], input[type="url"], input[type="email"], input[type="number"],
  select, textarea, .pengaturan input {
    width: 100%;
    min-height: 44px; /* target sentuh Apple HIG */
    padding: 11px 13px;
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
    background: var(--bg);
    color: var(--ink);
    font: inherit;
    font-size: 16px; /* wajib ≥16px di iOS agar tidak auto-zoom */
    transition: border-color 0.2s, box-shadow 0.2s, background 0.2s;
    -webkit-appearance: none;
    appearance: none;
  }
  select {
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath fill='%235e7682' d='M1 1l5 5 5-5'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 14px center;
    padding-right: 36px;
  }
  input[readonly] { opacity: 0.75; }
  textarea { min-height: 100px; resize: vertical; }
  input:focus-visible, textarea:focus-visible, select:focus-visible {
    outline: 2px solid transparent;
    border-color: var(--accent);
    box-shadow: 0 0 0 3px rgb(var(--glow) / 0.18);
    background: var(--surface);
  }
  .tautan {
    justify-self: start;
    background: none; border: 0; padding: 0;
    color: var(--accent); font: inherit; font-size: 0.9rem; font-weight: 600;
    text-decoration: none; cursor: pointer;
  }
  .tautan:hover { text-decoration: underline; }
  .tautan[hidden] { display: none; }
  .petunjuk { margin: 0; font-size: 0.85rem; color: var(--muted); line-height: 1.45; }

  .simpan {
    position: relative;
    overflow: hidden;
    min-height: 48px;
    padding: 14px 16px;
    border: 0;
    border-radius: var(--radius-sm);
    background: linear-gradient(145deg, var(--accent), var(--accent-deep));
    color: var(--accent-ink);
    font: inherit;
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: -0.01em;
    cursor: pointer;
    box-shadow: 0 8px 20px -8px rgb(var(--glow) / 0.7);
    transition: transform 0.15s var(--ease), box-shadow 0.2s, opacity 0.2s;
    -webkit-user-select: none;
    user-select: none;
  }
  .simpan::after {
    content: "";
    position: absolute; inset: 0;
    background: linear-gradient(110deg, transparent 30%, rgba(255, 255, 255, 0.22) 50%, transparent 70%);
    transform: translateX(-100%);
    pointer-events: none;
  }
  @media (hover: hover) {
    .simpan:hover:not([disabled]) { transform: translateY(-1px); box-shadow: 0 12px 24px -10px rgb(var(--glow) / 0.75); }
    .simpan:hover:not([disabled])::after { animation: kilau 0.75s var(--ease); }
  }
  .simpan:active:not([disabled]) { transform: scale(0.985); }
  .simpan:focus-visible { outline: 2px solid var(--ink); outline-offset: 2px; }
  .simpan[disabled] { opacity: 0.8; cursor: progress; }
  .simpan.memuat::before {
    content: "";
    display: inline-block;
    width: 1em; height: 1em;
    margin-right: 0.55em;
    border: 2px solid currentColor;
    border-right-color: transparent;
    border-radius: 50%;
    vertical-align: -0.15em;
    animation: putar 0.7s linear infinite;
  }

  .status { min-height: 1.35em; margin: 0; font-weight: 600; font-size: 0.9rem; }
  .status > span { display: inline-block; animation: geser 0.3s var(--ease); }
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

  .riwayat { list-style: none; margin: 0; padding: 0; padding-inline-start: 0; margin-inline: 0; display: grid; gap: 8px; content-visibility: auto; contain-intrinsic-size: auto 200px; }
  .riwayat li, .daftar-data li { list-style: none; margin: 0; margin-inline: 0; }
  .riwayat li {
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
    padding: 12px 14px;
    box-shadow: var(--shadow);
    animation: geser 0.35s var(--ease) backwards;
  }
  .riwayat li.baru { animation: muncul 0.45s var(--ease) backwards, sorot 1.6s ease-out; }
  .riwayat .waktu { font-weight: 700; font-size: 0.92rem; }
  .riwayat .isi { color: var(--muted); margin: 2px 0 0; font-size: 0.88rem; overflow-wrap: anywhere; }
  .riwayat a { color: var(--accent); font-weight: 600; text-decoration: none; }
  .kosong-riwayat { color: var(--muted); font-size: 0.9rem; }

  .form-lembur {
    display: grid; gap: 12px;
    padding: 16px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
  }
  .ringkas { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; }
  .ringkas div {
    padding: 12px 8px; text-align: center;
    background: var(--accent-soft); border-radius: var(--radius-sm);
    animation: muncul 0.4s var(--ease) backwards;
  }
  .ringkas strong { display: block; font-size: 1.25rem; font-weight: 800; line-height: 1.1; color: var(--accent); letter-spacing: -0.02em; }
  .ringkas span { font-size: 0.75rem; color: var(--muted); font-weight: 500; }
  .daftar-data {
    list-style: none; margin: 0; padding: 0; padding-inline-start: 0; margin-inline: 0;
    display: grid; gap: 8px;
    content-visibility: auto;
    contain-intrinsic-size: auto 240px;
  }
  .daftar-data li {
    display: grid; gap: 3px;
    padding: 12px 14px;
    background: var(--bg);
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
    contain: layout style;
  }
  .daftar-data .tgl, .daftar-data .waktu { font-weight: 800; }
  .daftar-data .isi { color: var(--muted); overflow-wrap: anywhere; }
  .daftar-data a { color: var(--accent); font-weight: 600; }
  .daftar-data .tgl { font-weight: 800; }
  .daftar-data .jam { color: var(--accent); font-weight: 700; font-size: 0.92rem; }
  .daftar-data .ket-data { font-weight: 600; overflow-wrap: anywhere; }
  .daftar-data .lok { color: var(--muted); font-size: 0.92rem; }
  .aksi-data { display: flex; gap: 6px; margin-top: 8px; flex-wrap: wrap; }
  .mini {
    flex: 1; min-width: 0;
    min-height: 40px;
    padding: 9px 10px;
    border: 1px solid var(--line); border-radius: 10px;
    background: var(--surface); color: var(--ink);
    font: inherit; font-size: 0.84rem; font-weight: 600;
    cursor: pointer;
    transition: border-color 0.2s, background 0.2s, transform 0.15s var(--ease);
    -webkit-user-select: none;
    user-select: none;
  }
  @media (hover: hover) { .mini:hover { border-color: var(--accent); background: var(--accent-soft); } }
  .mini:active { transform: scale(0.97); }
  .mini:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }
  .mini.bahaya { color: var(--danger); border-color: color-mix(in srgb, var(--danger) 45%, var(--line)); }
  @media (hover: hover) { .mini.bahaya:hover { background: color-mix(in srgb, var(--danger) 10%, transparent); } }
  .mini.utama { background: var(--accent); border-color: var(--accent); color: var(--accent-ink); font-weight: 700; }
  dialog {
    width: min(92vw, 400px);
    max-height: 90vh; overflow: auto;
    padding: 18px;
    border: 0; border-radius: var(--radius);
    background: var(--surface); color: var(--ink);
    box-shadow: var(--shadow-lg);
  }
  dialog::backdrop { background: rgba(8, 16, 22, 0.5); backdrop-filter: blur(4px); }
  dialog[open] { animation: muncul 0.22s var(--ease); }
  dialog h3 { margin: 0 0 10px; font-size: 1.1rem; letter-spacing: -0.02em; font-weight: 800; }
  dialog .kolom { margin-bottom: 10px; }
  dialog .aksi-data { margin-top: 12px; }
  dialog img { width: 100%; border-radius: 10px; display: block; background: #000; }
  dialog p { margin: 0 0 8px; overflow-wrap: anywhere; font-size: 0.92rem; }
  .hasil-form { display: grid; gap: 8px; }
  .peringatan {
    margin: -8px 0 16px; padding: 12px 14px;
    border-radius: 12px; border: 1px solid var(--accent-2);
    background: rgb(var(--glow-2) / 0.16); color: var(--ink);
    font-weight: 600; line-height: 1.4;
  }
  .peringatan.kritis { border-color: var(--danger); background: rgb(179 38 30 / 0.12); }
  .peringatan[hidden] { display: none; }
  .meter { display: grid; gap: 6px; }
  .meter-atas { display: flex; justify-content: space-between; gap: 10px; align-items: baseline; flex-wrap: wrap; }
  .meter-judul { font-weight: 700; }
  .meter-nilai { color: var(--muted); font-size: 0.92rem; }
  .meter-bar { height: 12px; border-radius: 99px; background: var(--line); overflow: hidden; }
  .meter-bar i { display: block; height: 100%; width: 0; border-radius: inherit; background: var(--accent); transition: width 0.9s var(--ease); }
  .meter.waspada .meter-bar i { background: var(--accent-2); }
  .meter.kritis .meter-bar i { background: var(--danger); }
  .meter-cat { font-size: 0.88rem; color: var(--muted); }
  .meter.waspada .meter-cat { color: var(--ink); }
  .meter.kritis .meter-cat { color: var(--danger); font-weight: 700; }
  .info-simpan { display: grid; gap: 2px; padding: 10px 12px; border-radius: 12px; background: var(--accent-soft); font-size: 0.93rem; }
  .info-simpan strong { font-size: 0.95rem; }
  /* Tumpukan halaman scan — horizontal, ringkas */
  .tumpukan {
    list-style: none; margin: 0; padding: 4px 2px 8px;
    display: flex; gap: 10px; overflow-x: auto; -webkit-overflow-scrolling: touch;
    scroll-snap-type: x mandatory;
  }
  .tumpukan li {
    flex: 0 0 auto; width: 112px;
    display: flex; flex-direction: column; gap: 6px;
    padding: 8px; background: var(--bg);
    border: 1px solid var(--line); border-radius: 14px;
    scroll-snap-align: start;
    animation: muncul 0.3s var(--ease) backwards;
  }
  .tumpukan img {
    width: 100%; aspect-ratio: 3 / 4; object-fit: contain;
    border-radius: 8px; background: #fff; border: 1px solid var(--line);
  }
  .tumpukan li.ls img { aspect-ratio: 4 / 3; }
  .tumpukan .no { font-weight: 700; font-size: 0.82rem; text-align: center; color: var(--muted); }
  .tumpukan .aksi-hal {
    display: grid; grid-template-columns: 1fr 1fr; gap: 4px;
  }
  .tumpukan .aksi-hal .mini {
    flex: none; padding: 6px 4px; font-size: 0.75rem; border-radius: 8px;
  }
  .mini.kecil { flex: none; padding: 6px 10px; font-size: 0.85rem; }
  .mini[disabled] { opacity: 0.45; cursor: default; }
  .target-scan {
    display: flex; align-items: center; justify-content: space-between; gap: 10px;
    padding: 10px 12px; border-radius: 12px;
    background: var(--accent-soft); border-left: 4px solid var(--accent); font-weight: 600;
  }
  .target-scan[hidden] { display: none; }
  .aksi-scan { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .aksi-scan .mini { position: relative; text-align: center; padding: 12px 10px; font-weight: 600; }
  .aksi-scan .mini.utama { background: var(--accent); border-color: var(--accent); color: var(--accent-ink); }
  .aksi-scan input[type="file"] { position: absolute; inset: 0; opacity: 0; cursor: pointer; width: 100%; }
  .scan-opsi {
    display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 4px;
  }
  .scan-opsi .kolom { margin: 0; }
  .scan-opsi label.cek { margin: 0; align-self: end; padding-bottom: 10px; }
  .ket-tumpuk {
    display: flex; align-items: center; justify-content: space-between; gap: 8px;
    margin: 4px 0 0; font-size: 0.9rem; color: var(--muted);
  }
  .ket-tumpuk strong { color: var(--ink); font-weight: 700; }

  /* Kamera scan: ikut orientasi HP */
  #kameraScan { background: #0a0a0a; }
  #kameraScan .vf {
    flex: 1; min-height: 0; position: relative;
    display: flex; align-items: center; justify-content: center;
    overflow: hidden; background: #000;
  }
  #kameraScan video {
    width: 100%; height: 100%;
    object-fit: cover; background: #000;
  }
  @media (orientation: landscape) {
    #kameraScan { flex-direction: row; }
    #kameraScan .info {
      position: absolute; top: 0; left: 0; right: auto; bottom: 0;
      width: min(42vw, 280px);
      padding: calc(12px + env(safe-area-inset-top)) 14px calc(12px + env(safe-area-inset-bottom));
      background: linear-gradient(90deg, rgba(0,0,0,0.75), rgba(0,0,0,0.25) 70%, transparent);
      display: flex; flex-direction: column; justify-content: flex-start; gap: 6px;
      z-index: 2;
    }
    #kameraScan .bar {
      position: absolute; right: 0; top: 0; bottom: 0;
      width: 96px; flex-direction: column;
      justify-content: center; gap: 18px;
      padding: 16px calc(10px + env(safe-area-inset-right));
      background: linear-gradient(270deg, rgba(0,0,0,0.7), transparent);
      z-index: 2;
    }
    #kameraScan .bar .kanan { width: auto; height: 40px; }
    #kameraScan .batal { width: 72px; }
  }
  /* Bingkai panduan dokumen (A4 portrait / landscape) */
  .panduan-dok {
    position: absolute; inset: 0; pointer-events: none; z-index: 1;
  }
  .panduan-dok .bingkai-a4 {
    position: absolute; left: 50%; top: 50%;
    transform: translate(-50%, -50%);
    border: 2px solid rgba(255, 255, 255, 0.55);
    border-radius: 4px;
    box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.28);
    transition: width 0.25s var(--ease), height 0.25s var(--ease), border-color 0.3s;
  }
  .panduan-dok.stabil .bingkai-a4 { border-color: #5be3a1; }
  .panduan-dok .sudut {
    position: absolute; width: 18px; height: 18px;
    border: 3px solid #fff; border-radius: 2px;
  }
  .panduan-dok .sudut.tl { top: -2px; left: -2px; border-right: 0; border-bottom: 0; }
  .panduan-dok .sudut.tr { top: -2px; right: -2px; border-left: 0; border-bottom: 0; }
  .panduan-dok .sudut.bl { bottom: -2px; left: -2px; border-right: 0; border-top: 0; }
  .panduan-dok .sudut.br { bottom: -2px; right: -2px; border-left: 0; border-top: 0; }
  .panduan-dok.stabil .sudut { border-color: #5be3a1; }
  .badge-ori {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 4px 10px; border-radius: 999px;
    background: rgba(255,255,255,0.14); font-size: 0.8rem; font-weight: 600;
  }
  .progress-stabil {
    height: 3px; border-radius: 2px; background: rgba(255,255,255,0.2);
    margin-top: 8px; overflow: hidden;
  }
  .progress-stabil > i {
    display: block; height: 100%; width: 0%;
    background: #ffc15e; border-radius: 2px;
    transition: width 0.15s linear;
  }
  .progress-stabil.ok > i { background: #5be3a1; }
  .tombol-senter {
    width: 44px; height: 44px; border-radius: 50%;
    border: 1px solid rgba(255,255,255,0.45); background: rgba(0,0,0,0.35);
    color: #fff; font-size: 1.1rem; cursor: pointer;
    display: grid; place-items: center;
  }
  .tombol-senter.nyala { background: rgba(255, 193, 94, 0.35); border-color: #ffc15e; }
  .bingkai { position: absolute; inset: 9% 6% 4%; border: 2px dashed rgba(255, 255, 255, 0.55); border-radius: 6px; pointer-events: none; }
  .kamera .vf { position: relative; }
  .lapis { position: absolute; inset: 0; width: 100%; height: 100%; pointer-events: none; z-index: 2; }
  .kamera .info .cek { color: #fff; margin-top: 6px; font-size: 0.9rem; }
  .kamera .info .petunjuk-scan { font-weight: 700; color: #ffc15e; margin-top: 4px; }
  #dialogPotong canvas { display: block; margin: 0 auto; max-width: 100%; height: auto; touch-action: none; border-radius: 10px; background: #000; }
  #urutGabung { margin: 0 0 12px; padding-left: 22px; }
  #urutGabung li { margin-bottom: 4px; overflow-wrap: anywhere; }
  .daftar-data .aksi-data { flex-wrap: wrap; }
  .daftar-data .aksi-data .mini { flex: 1 1 30%; }
  .hasil-form button.mini { padding: 11px 14px; font-weight: 600; }
  .gerbang[hidden] { display: none; }
  .gerbang {
    position: fixed; inset: 0; z-index: 200;
    display: flex; flex-direction: column; align-items: center; justify-content: flex-start;
    padding: max(20px, env(safe-area-inset-top)) max(16px, env(safe-area-inset-right))
             max(20px, env(safe-area-inset-bottom)) max(16px, env(safe-area-inset-left));
    overflow-y: auto;
    -webkit-overflow-scrolling: touch;
    overscroll-behavior: contain;
    background:
      radial-gradient(40% 32% at 18% 8%, rgb(var(--glow) / 0.18), transparent 70%),
      radial-gradient(34% 28% at 88% 18%, rgb(var(--glow-2) / 0.12), transparent 70%),
      var(--bg);
  }
  .splash { display: flex; flex-direction: column; align-items: center; gap: 14px; margin: auto; transition: opacity 0.35s var(--ease), transform 0.35s var(--ease); }
  .splash.usai { opacity: 0; transform: scale(0.92) translateY(-8px); }
  .splash-logo {
    width: 76px; height: 76px; border-radius: 22px;
    display: grid; place-items: center;
    background: linear-gradient(135deg, var(--accent), var(--accent-deep));
    box-shadow: 0 14px 34px -10px rgb(var(--glow) / 0.8);
    animation: splashMasuk 0.7s var(--ease);
  }
  .splash-logo svg { width: 40px; height: 40px; }
  .splash-judul { font-family: var(--font); font-weight: 800; font-size: 1.3rem; letter-spacing: -0.01em; color: var(--ink); animation: splashMasuk 0.7s var(--ease) 0.15s backwards; }
  @keyframes splashMasuk { from { opacity: 0; transform: scale(0.5) translateY(10px); } to { opacity: 1; transform: none; } }

  .kartu-auth {
    width: 100%; max-width: 360px; margin: auto;
    background: var(--surface); border: 1px solid var(--line); border-radius: var(--radius);
    padding: 20px 18px; box-shadow: var(--shadow-lg);
    animation: muncul 0.4s var(--ease);
    display: grid; gap: 12px;
  }
  .tab-auth {
    display: flex; gap: 4px;
    background: var(--bg); padding: 3px; border-radius: 11px;
    border: 1px solid var(--line);
  }
  .tab-auth button {
    flex: 1; padding: 9px 8px; border: 0; border-radius: 9px;
    background: transparent; color: var(--muted);
    font: inherit; font-size: 0.9rem; font-weight: 700; cursor: pointer;
    transition: background 0.2s, color 0.2s, box-shadow 0.2s;
  }
  .tab-auth button.tab-aktif {
    background: var(--surface); color: var(--ink);
    box-shadow: var(--shadow);
  }
  .kartu-auth form { display: grid; gap: 11px; }
  .kartu-auth form[hidden] { display: none; }
  .kartu-auth select {
    width: 100%; padding: 11px 13px; border: 1px solid var(--line); border-radius: var(--radius-sm);
    background: var(--bg); color: var(--ink); font: inherit;
  }
  .pengaturan-gerbang { color: var(--muted); font-size: 0.84rem; }
  .pengaturan-gerbang summary { cursor: pointer; font-weight: 500; }
  .pengaturan-gerbang .kolom { margin-top: 10px; }

  .alat-cepat {
    display: flex; gap: 8px;
    margin: 0 0 14px;
    padding: 4px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: 16px;
    box-shadow: var(--shadow);
  }
  .alat-cepat button {
    flex: 1; display: flex; flex-direction: column; align-items: center; gap: 4px;
    padding: 12px 6px; border: 0; border-radius: 12px;
    background: transparent; color: var(--ink);
    font: inherit; font-size: 0.75rem; font-weight: 700;
    letter-spacing: 0.01em;
    cursor: pointer;
    transition: transform 0.15s var(--ease), background 0.2s, color 0.2s;
  }
  .ikon-alat { font-size: 1.35rem; line-height: 1; }
  @media (hover: hover) {
    .alat-cepat button:hover { background: var(--accent-soft); color: var(--accent-deep); }
  }
  .alat-cepat button:active { transform: scale(0.96); background: var(--accent-soft); }

  .kartu-profil {
    display: grid; gap: 6px;
    margin-bottom: 14px; padding: 14px 16px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
  }
  .profil-baris {
    display: flex; justify-content: space-between; align-items: baseline; gap: 12px;
    font-size: 0.88rem; padding: 2px 0;
  }
  .profil-baris span { color: var(--muted); font-weight: 500; }
  .profil-baris strong { text-align: right; overflow-wrap: anywhere; font-weight: 700; }
  .kartu-profil .aksi-data { margin-top: 8px; padding-top: 8px; border-top: 1px solid var(--line); }

  .reveal { opacity: 0; transform: translateY(18px); transition: opacity 0.6s var(--ease), transform 0.6s var(--ease); }
  .reveal.tampak { opacity: 1; transform: none; }

  .cek {
    display: flex; align-items: center; gap: 10px;
    font-size: 0.88rem; cursor: pointer; color: var(--ink);
  }
  .cek input { width: 18px; height: 18px; accent-color: var(--accent); flex: none; }
  .hasil-form a {
    display: block; padding: 11px 14px;
    border: 1px solid var(--line);
    border-radius: var(--radius-sm); background: var(--bg);
    color: var(--accent); font-weight: 600; font-size: 0.9rem; text-decoration: none;
    animation: geser 0.3s var(--ease) backwards;
  }
  details.detail-lembur { color: var(--muted); font-size: 0.9rem; }
  details.detail-lembur summary { cursor: pointer; font-weight: 600; }
  details.detail-lembur .kolom { margin-top: 10px; }
  .ket {
    margin: 0; padding: 10px 12px;
    border-radius: var(--radius-sm);
    background: var(--accent-soft); color: var(--ink);
    font-size: 0.88rem; font-weight: 600; overflow-wrap: anywhere;
  }
  .hasil-tes { display: block; margin-top: 8px; font-weight: 600; font-size: 0.88rem; }
  .hasil-tes.ok { color: var(--ok); }
  .hasil-tes.gagal { color: var(--danger); }
  details.pengaturan {
    margin-top: 28px; color: var(--muted);
    padding: 14px 16px;
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
  }
  details.pengaturan summary { cursor: pointer; font-weight: 600; color: var(--ink); font-size: 0.9rem; }
  .pengaturan .kolom { margin-top: 10px; }
  .pengaturan p { font-size: 0.85rem; margin: 8px 0 0; }

  /* Layar kamera */
  .kamera {
    position: fixed; inset: 0; z-index: 50;
    height: 100vh; height: 100dvh;
    max-height: -webkit-fill-available;
    display: none; flex-direction: column;
    background: #000; color: #fff;
  }
  .kamera.aktif { display: flex; animation: bukaKamera 0.25s var(--ease); }
  .kamera .vf { flex: 1; min-height: 0; display: grid; place-items: center; overflow: hidden; background: #000; }
  .kamera video { width: 100%; max-height: 100%; aspect-ratio: 3 / 4; object-fit: cover; background: #000; }
  @media (orientation: landscape) { .kamera video { width: auto; height: 100%; max-width: 100%; aspect-ratio: 4 / 3; } }
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
    body::before { animation: none !important; }
    .reveal { opacity: 1; transform: none; }
  }

  /* —— Optimasi mobile (sentuh, performa, safe-area) —— */
  @media (max-width: 600px) {
    /* Shadow lebih ringan = lebih hemat GPU */
    :root {
      --shadow: 0 1px 3px rgb(15 37 46 / 0.06);
      --shadow-lg: 0 4px 16px -6px rgb(15 37 46 / 0.14);
    }
    @media (prefers-color-scheme: dark) {
      :root {
        --shadow: 0 1px 3px rgb(0 0 0 / 0.25);
        --shadow-lg: 0 6px 20px -8px rgb(0 0 0 / 0.4);
      }
    }
    /* Matikan animasi masuk berurutan di HP */
    main > * { animation: none !important; }
    .reveal { opacity: 1; transform: none; transition: none; }
    .foto:not(.terisi)::after { animation: none; }
    .logo { animation: none; }
    /* Area sentuh minimum */
    .aksi-foto label, .aksi-foto button { min-height: 44px; }
    .alat-cepat button { min-height: 56px; }
    .tab-auth button { min-height: 40px; }
    /* Tumpukan scan: scroll horizontal lebih mulus */
    .tumpukan {
      -webkit-overflow-scrolling: touch;
      overscroll-behavior-x: contain;
      scrollbar-width: none;
    }
    .tumpukan::-webkit-scrollbar { display: none; }
    /* Dialog full-width lebih nyaman di HP kecil */
    dialog {
      width: calc(100vw - 28px);
      max-width: 400px;
      margin: auto;
      padding: 16px;
    }
  }

  /* Layar sangat sempit */
  @media (max-width: 360px) {
    main { padding-left: 12px; padding-right: 12px; }
    h1 { font-size: 1.35rem; }
    .alat-cepat button { font-size: 0.7rem; padding: 10px 4px; }
    .scan-opsi { grid-template-columns: 1fr; }
    .aksi-scan { grid-template-columns: 1fr; }
  }

  /* Hemat baterai / aksesibilitas transparansi */
  @media (prefers-reduced-transparency: reduce) {
    body::before { display: none; }
    dialog::backdrop { backdrop-filter: none; background: rgba(8, 16, 22, 0.7); }
  }
</style>
</head>
<body>
<div class="gerbang" id="gerbang">
  <div class="splash" id="splash">
    <span class="splash-logo" aria-hidden="true">
      <svg viewBox="0 0 24 24" width="40" height="40" fill="none" stroke="#fff" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="12" cy="12" r="9"/><circle cx="12" cy="12" r="3.5"/>
        <path d="M12 8.5V3"/><path d="M12 8.5V3" transform="rotate(120 12 12)"/><path d="M12 8.5V3" transform="rotate(240 12 12)"/>
      </svg>
    </span>
    <p class="splash-judul">Catatan Foto</p>
  </div>

  <div class="kartu-auth" id="kartuAuth" hidden>
    <div class="tab-auth">
      <button type="button" class="tab-aktif" id="tabMasuk">Masuk</button>
      <button type="button" id="tabDaftar">Daftar akun</button>
    </div>

    <form id="formMasuk" novalidate>
      <div class="kolom"><label for="mUsername">Username</label><input type="text" id="mUsername" autocomplete="username" autocapitalize="none" required></div>
      <div class="kolom"><label for="mSandi">Kata sandi</label><input type="password" id="mSandi" autocomplete="current-password" required></div>
      <button type="submit" class="simpan">Masuk</button>
      <p class="status" id="statusMasuk" role="status" aria-live="polite"></p>
    </form>

    <form id="formDaftar" novalidate hidden>
      <div class="kolom"><label for="dUsername">Username</label><input type="text" id="dUsername" autocomplete="username" autocapitalize="none" placeholder="huruf kecil, tanpa spasi" required></div>
      <div class="kolom"><label for="dSandi">Kata sandi</label><input type="password" id="dSandi" autocomplete="new-password" required></div>
      <div class="kolom"><label for="dNama">Nama lengkap</label><input type="text" id="dNama" autocapitalize="characters" required></div>
      <div class="kolom"><label for="dJabatan">Jabatan</label>
        <select id="dJabatan"><option value="NOA/NOE">NOA/NOE</option><option value="NOD">NOD</option></select>
      </div>
      <div class="kolom"><label for="dKantor">Tempat kerja</label><input type="text" id="dKantor" placeholder="Contoh: Branch Tibubeneng"></div>
      <div class="kolom"><label for="dNik">NIK Biznet</label><input type="text" id="dNik" inputmode="numeric"></div>
      <div class="kolom"><label for="dOc">OC</label>
        <select id="dOc"><option value="S3">Biznet S3</option><option value="DGM">Biznet DGM (menyusul template)</option></select>
      </div>
      <div class="kolom"><label for="dEmail">Email (opsional, untuk notifikasi status)</label><input type="email" id="dEmail" autocomplete="email"></div>
      <button type="submit" class="simpan">Daftar</button>
      <p class="status" id="statusDaftar" role="status" aria-live="polite"></p>
    </form>

    <details class="pengaturan-gerbang" id="pengaturanGerbang">
      <summary>Pengaturan alamat server (biasanya tidak perlu diubah)</summary>
      <div class="kolom"><label for="urlScriptGerbang">Alamat Web App</label><input type="url" id="urlScriptGerbang" autocomplete="off"></div>
      <button type="button" class="tautan" id="simpanUrlGerbang" style="margin-top:8px">Simpan alamat</button>
    </details>
  </div>
</div>

<main id="app" hidden>
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

  <nav class="alat-cepat" aria-label="Pintasan">
    <button type="button" data-tuju="#areaFoto"><span class="ikon-alat">📷</span>Foto</button>
    <button type="button" data-tuju="#bagianScan"><span class="ikon-alat">📄</span>Scan</button>
    <button type="button" data-tuju="#bagianData"><span class="ikon-alat">🧾</span>Data &amp; Form</button>
  </nav>

  <div class="kartu-profil">
    <div class="profil-baris"><span>Nama</span><strong id="pNama">-</strong></div>
    <div class="profil-baris"><span>Jabatan</span><strong id="pJabatan">-</strong></div>
    <div class="profil-baris"><span>Tempat kerja</span><strong id="pKantor">-</strong></div>
    <div class="profil-baris"><span>NIK Biznet</span><strong id="pNik">-</strong></div>
    <div class="profil-baris"><span>OC</span><strong id="pOc">-</strong></div>
    <div class="aksi-data">
      <button type="button" class="mini" id="ubahProfil">Ubah profil</button>
      <button type="button" class="mini bahaya" id="keluarAkun">Keluar</button>
    </div>
  </div>

  <div class="peringatan" id="peringatan" role="alert" hidden></div>

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

    <label class="cek"><input type="checkbox" id="autoPdf" checked> Buat PDF form lembur otomatis setelah foto disimpan</label>
    <label class="cek"><input type="checkbox" id="emailPdf" checked> Kirim PDF ke email yang tertaut</label>
    <button type="submit" class="simpan" id="tombolSimpan">Simpan foto</button>
    <p class="status" id="status" role="status" aria-live="polite"></p>
    <p class="status" id="statusOtomatis" role="status" aria-live="polite"></p>
    <div class="hasil-form" id="hasilOtomatis"></div>
  </form>

  <h2 class="reveal">Tersimpan terakhir</h2>
  <p class="status" id="statusTerakhir" role="status" aria-live="polite"></p>
  <ul class="daftar-data reveal" id="riwayat"></ul>
  <p class="kosong-riwayat" id="riwayatKosong">Belum ada foto yang disimpan.</p>
  <button type="button" class="mini" id="muatTerakhir" style="margin-top:10px">Muat ulang</button>

  <h2 class="reveal">Data lembur</h2>
  <section class="form-lembur reveal" id="bagianData">
    <div class="kolom">
      <label for="bulanForm">Periode berakhir di bulan</label>
      <input type="month" id="bulanForm">
    </div>
    <p class="ket" id="ketPeriode"></p>
    <div class="ringkas" id="ringkasData" hidden>
      <div><strong id="rDataJumlah">0</strong><span>Data</span></div>
      <div><strong id="rHari">0</strong><span>Hari lembur</span></div>
      <div><strong id="rJam">0</strong><span>Total jam</span></div>
    </div>
    <p class="status" id="statusDaftar" role="status" aria-live="polite"></p>
    <ul class="daftar-data" id="daftarData"></ul>
    <button type="button" class="mini" id="muatData">Muat ulang data</button>
  </section>

  <h2 class="reveal">Form lembur</h2>
  <section class="form-lembur reveal">
    <p class="petunjuk">Membuat PDF Form Tunjangan Kerja sesuai template dari data periode di atas, disusul satu Surat Perintah Lembur per hari lembur lengkap dengan fotonya. PDF juga disimpan ke folder "Form Lembur" di Drive.</p>
    <button type="button" class="simpan" id="tombolForm">Buat PDF form lembur</button>
    <p class="status" id="statusForm" role="status" aria-live="polite"></p>
    <div class="hasil-form" id="hasilForm"></div>
  </section>

  <h2 class="reveal">Scan dokumen</h2>
  <section class="form-lembur reveal" id="bagianScan">
    <div class="target-scan" id="targetScan" hidden>
      <span id="teksTargetScan"></span>
      <button type="button" class="mini kecil" id="batalTargetScan">Batal</button>
    </div>
    <div class="kolom">
      <label for="namaScan">Nama dokumen</label>
      <input type="text" id="namaScan" placeholder="Contoh: Surat tugas" autocomplete="off">
    </div>
    <div class="scan-opsi">
      <div class="kolom">
        <label for="filterScan">Hasil scan</label>
        <select id="filterScan">
          <option value="dokumen">Dokumen tajam</option>
          <option value="hitamputih">Hitam putih</option>
          <option value="asli">Warna asli</option>
        </select>
      </div>
      <label class="cek"><input type="checkbox" id="potongOtomatis" checked> Potong otomatis</label>
    </div>
    <div class="aksi-scan">
      <button type="button" class="mini utama" id="mulaiScan">📷 Scan halaman</button>
      <label class="mini">📁 Dari galeri<input type="file" id="galeriScan" accept="image/*" multiple aria-label="Tambah halaman dari galeri"></label>
    </div>
    <div class="ket-tumpuk">
      <span id="ketTumpukan">Belum ada halaman</span>
      <strong id="badgeHalaman" hidden>0</strong>
    </div>
    <ul class="tumpukan" id="tumpukan"></ul>
    <button type="button" class="simpan" id="tombolSimpanScan" disabled>Simpan sebagai PDF</button>
    <p class="status" id="statusScan" role="status" aria-live="polite"></p>
    <div class="hasil-form" id="hasilScan"></div>
  </section>

  <h2 class="reveal">Dokumen tersimpan</h2>
  <section class="form-lembur reveal" id="bagianDaftarScan">
    <p class="status" id="statusDaftarScan" role="status" aria-live="polite"></p>
    <ul class="daftar-data" id="daftarScan"></ul>
    <div class="aksi-data" id="aksiGabung" hidden><button type="button" class="mini utama" id="tombolGabung" disabled>Gabungkan yang dipilih (0)</button></div>
    <button type="button" class="mini" id="muatScan">Muat ulang</button>
  </section>

  <h2 class="reveal">Penyimpanan</h2>
  <section class="form-lembur reveal" id="bagianKapasitas">
    <div id="isiKapasitas"><p class="petunjuk">Belum dimuat.</p></div>
    <p class="petunjuk" id="waktuKapasitas"></p>
    <button type="button" class="mini" id="muatKapasitas">Perbarui penyimpanan</button>
  </section>

  <section class="form-lembur reveal" id="bagianAdmin" hidden>
    <h2 style="margin:0 0 10px">Kelola akun</h2>
    <p class="petunjuk" style="margin:0 0 12px">Hanya terlihat untuk admin. Gunakan ini jika tautan Setujui/Tolak di email gagal dibuka.</p>
    <p class="status" id="statusAdmin" role="status" aria-live="polite"></p>
    <ul class="daftar-data" id="daftarAkun"></ul>
    <button type="button" class="mini" id="muatAkun" style="margin-top:10px">Muat ulang daftar akun</button>
  </section>

  <details class="pengaturan reveal" id="pengaturan">
    <summary>Pengaturan koneksi</summary>
    <p>Isi dengan alamat Web App dari Google Apps Script dan kunci yang sama dengan di Code.gs. Data ini disimpan hanya di perangkat ini.</p>
    <div class="kolom">
      <label for="urlScript">Alamat Web App</label>
      <input type="url" id="urlScript" placeholder="https://script.google.com/macros/s/.../exec" autocomplete="off">
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

<!-- Kamera scan dokumen -->
<div class="kamera" id="kameraScan" role="dialog" aria-modal="true" aria-label="Kamera scan dokumen">
  <div class="info">
    <div class="jam" id="infoScan"></div>
    <span class="badge-ori" id="badgeOri">Portrait</span>
    <div class="petunjuk-scan" id="petunjukScan">Arahkan kamera ke dokumen</div>
    <div class="progress-stabil" id="progressStabil" hidden><i id="progressStabilBar"></i></div>
    <label class="cek"><input type="checkbox" id="autoAmbil" checked> Ambil otomatis</label>
  </div>
  <div class="vf">
    <video id="videoScan" playsinline muted autoplay></video>
    <div class="panduan-dok" id="panduanDok" aria-hidden="true">
      <div class="bingkai-a4" id="bingkaiA4">
        <span class="sudut tl"></span><span class="sudut tr"></span>
        <span class="sudut bl"></span><span class="sudut br"></span>
      </div>
    </div>
    <canvas class="lapis" id="lapisScan"></canvas>
  </div>
  <div class="kilat" id="kilatScan"></div>
  <div class="bar">
    <button type="button" class="batal" id="selesaiScan">Selesai</button>
    <button type="button" class="rana" id="ranaScan" aria-label="Ambil halaman"></button>
    <button type="button" class="tombol-senter" id="senterScan" aria-label="Senter" title="Senter">💡</button>
  </div>
</div>

<dialog id="dialogPotong" aria-labelledby="judulPotong">
  <h3 id="judulPotong">Atur sudut potong</h3>
  <p class="petunjuk">Geser empat lingkaran ke sudut dokumen. Hasilnya diluruskan otomatis.</p>
  <canvas id="kanvasPotong"></canvas>
  <div class="aksi-data">
    <button type="button" class="mini" id="deteksiUlangPotong">Deteksi ulang</button>
    <button type="button" class="mini" id="tanpaPotong">Tanpa potong</button>
  </div>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalPotong">Batal</button>
    <button type="button" class="mini utama" id="terapkanPotong">Terapkan</button>
  </div>
</dialog>

<dialog id="dialogGabung" aria-labelledby="judulGabung">
  <h3 id="judulGabung">Gabungkan dokumen</h3>
  <p class="petunjuk">Urutan sesuai urutan yang kamu pilih:</p>
  <ol id="urutGabung"></ol>
  <div class="kolom"><label for="namaGabung">Nama dokumen gabungan</label><input type="text" id="namaGabung" autocomplete="off"></div>
  <label class="cek"><input type="checkbox" id="hapusAsalGabung"> Hapus dokumen asal setelah digabung</label>
  <p class="status" id="statusGabung" role="status" aria-live="polite"></p>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalGabung">Batal</button>
    <button type="button" class="mini utama" id="yakinGabung">Gabungkan</button>
  </div>
</dialog>

<dialog id="dialogScanHapus" aria-labelledby="judulScanHapus">
  <h3 id="judulScanHapus">Hapus dokumen ini?</h3>
  <p id="ketScanHapus"></p>
  <p class="petunjuk">File PDF dihapus dari folder Drive (masuk sampah Drive, terhapus permanen otomatis setelah 30 hari) dan barisnya dihapus dari tab Scan di Sheet.</p>
  <p class="status" id="statusScanHapus" role="status" aria-live="polite"></p>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalScanHapus">Batal</button>
    <button type="button" class="mini bahaya" id="yakinHapusScan">Hapus</button>
  </div>
</dialog>

<!-- Dialog ubah, hapus, dan lihat foto -->
<dialog id="dialogEdit" aria-labelledby="judulEdit">
  <h3 id="judulEdit">Ubah data</h3>
  <div class="kolom"><label for="edJenis">Jenis kegiatan</label><input type="text" id="edJenis" autocomplete="off" autocapitalize="characters"></div>
  <div class="kolom"><label for="edTiket">Nomor tiket</label><input type="text" id="edTiket" inputmode="numeric" autocomplete="off"></div>
  <div class="kolom"><label for="edCustomer">Nama customer</label><input type="text" id="edCustomer" autocomplete="off" autocapitalize="characters"></div>
  <p class="ket" id="edPratinjau"></p>
  <div class="kolom"><label for="edTanggal">Tanggal</label><input type="date" id="edTanggal"></div>
  <div class="kolom"><label for="edLokasi">Lokasi</label><input type="text" id="edLokasi" autocomplete="off"></div>
  <div class="kolom"><label for="edJadwal">Jadwal kerja</label><input type="text" id="edJadwal" autocomplete="off"></div>
  <div class="kolom"><label for="edMulai">Mulai jam lembur</label><input type="text" id="edMulai" inputmode="decimal" autocomplete="off" placeholder="18.00"></div>
  <div class="kolom"><label for="edSelesai">Selesai jam lembur</label><input type="text" id="edSelesai" inputmode="decimal" autocomplete="off" placeholder="21.24"></div>
  <p class="status" id="statusEdit" role="status" aria-live="polite"></p>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalEdit">Batal</button>
    <button type="button" class="mini utama" id="simpanEdit">Simpan</button>
  </div>
</dialog>

<dialog id="dialogHapus" aria-labelledby="judulHapus">
  <h3 id="judulHapus">Hapus data ini?</h3>
  <p id="ketHapus"></p>
  <p class="petunjuk">Data dihapus dari Sheet dan fotonya dihapus dari folder Drive. Foto masuk ke sampah Drive dan terhapus permanen otomatis setelah 30 hari (kosongkan sampah Drive untuk menghapusnya sekarang). PDF form lembur ikut diperbarui.</p>
  <p class="status" id="statusHapus" role="status" aria-live="polite"></p>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalHapus">Batal</button>
    <button type="button" class="mini bahaya" id="yakinHapus">Hapus</button>
  </div>
</dialog>

<dialog id="dialogProfil" aria-labelledby="judulProfil">
  <h3 id="judulProfil">Ubah profil</h3>
  <div class="kolom"><label for="pfNama">Nama lengkap</label><input type="text" id="pfNama" autocapitalize="characters"></div>
  <div class="kolom"><label for="pfJabatan">Jabatan</label>
    <select id="pfJabatan"><option value="NOA/NOE">NOA/NOE</option><option value="NOD">NOD</option></select>
  </div>
  <div class="kolom"><label for="pfKantor">Tempat kerja</label><input type="text" id="pfKantor"></div>
  <div class="kolom"><label for="pfNik">NIK Biznet</label><input type="text" id="pfNik" inputmode="numeric"></div>
  <div class="kolom"><label for="pfOc">OC</label>
    <select id="pfOc"><option value="S3">Biznet S3</option><option value="DGM">Biznet DGM (menyusul template)</option></select>
  </div>
  <p class="status" id="statusProfil" role="status" aria-live="polite"></p>
  <div class="aksi-data">
    <button type="button" class="mini" id="batalProfil">Batal</button>
    <button type="button" class="mini utama" id="simpanProfil">Simpan</button>
  </div>
</dialog>

<dialog id="dialogFoto" aria-label="Foto">
  <p id="ketFoto" class="petunjuk"></p>
  <img id="gambarFoto" alt="Foto bukti lembur">
  <div class="aksi-data"><button type="button" class="mini" id="tutupFoto">Tutup</button></div>
</dialog>

<!-- Layar kamera -->
<div class="kamera" id="kamera" role="dialog" aria-modal="true" aria-label="Kamera">
  <div class="info">
    <div class="jam" id="infoJam"></div>
    <div><span class="titik" id="titikGps"></span><span id="teksGps"></span></div>
    <div id="infoArah"></div>
    <div id="infoAlamat"></div>
  </div>
  <div class="vf"><video id="video" playsinline muted autoplay></video></div>
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
    SCRIPT_URL: "https://script.google.com/a/macros/smk.belajar.id/s/AKfycbxF0acQ_t0GDqX2CRGgmjz4K0pixKm3znfV137Yth6NNRpaA4EOVPPvgSVgDviW35fb/exec"
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

  const VERSI_SERVER = "2026.09.24.1";   // harus sama dengan VERSI_ di Code.gs
  const PESAN_KONEKSI = "Tidak bisa terhubung ke Apps Script. Pastikan deployment diatur Who has access: Anyone dan alamatnya berakhiran /exec.";

  const kamera = { stream: null, pos: null, gpsError: null, watchId: null, alamat: [], alamatPos: null, alamatWaktu: 0, timer: null, heading: null, jejak: [], onOri: null };

  function ambil(k) { try { return localStorage.getItem(k); } catch (e) { return null; } }
  function simpan(k, v) { try { localStorage.setItem(k, v); } catch (e) { /* abaikan */ } }
  function urlScript() { return (ambil("urlScript") || CONFIG.SCRIPT_URL || "").trim(); }
  function pengguna() { return ambil("pengguna") || ""; }
  function tokenAktif() { return ambil("token") || ""; }
  function hapusSesi() { try { localStorage.removeItem("pengguna"); localStorage.removeItem("token"); } catch (e) { /* abaikan */ } }

  /* ---------- Akun: gerbang, login, daftar, profil ---------- */

  let profilAktif = null;

  function ambilProfilCache() { try { return JSON.parse(ambil("profil") || "null"); } catch (e) { return null; } }
  function simpanProfilCache(p) { simpan("profil", JSON.stringify(p)); }

  function terapkanProfil(p) {
    profilAktif = p;
    simpanProfilCache(p);
    $("pNama").textContent = p.nama || "-";
    $("pJabatan").textContent = p.jabatan || "-";
    $("pKantor").textContent = p.kantor || "-";
    $("pNik").textContent = p.nik || "-";
    $("pOc").textContent = p.oc === "DGM" ? "Biznet DGM" : "Biznet S3";
    const admin = !!(p && p.admin);
    $("bagianAdmin").hidden = !admin;
    if (admin) muatDaftarAkun();
  }

  function tampilkanApp() {
    $("gerbang").hidden = true;
    $("app").hidden = false;
    pasangRevealObserver();
    mulaiApp();
  }

  /* ---------- Admin: kelola akun menunggu persetujuan ---------- */
  function setStatusAdmin(t, j) {
    const el = $("statusAdmin");
    if (!el) return;
    el.className = "status" + (j === "ok" ? " ok" : j === "gagal" ? " gagal" : "");
    el.textContent = t || "";
  }

  async function muatDaftarAkun() {
    if (!$("bagianAdmin") || $("bagianAdmin").hidden) return;
    const ul = $("daftarAkun");
    ul.innerHTML = "<li class=\"kosong-riwayat\">Memuat…</li>";
    setStatusAdmin("");
    try {
      const h = await panggil({ aksi: "daftarAkun" });
      const daftar = h.daftar || [];
      ul.innerHTML = "";
      if (!daftar.length) {
        ul.innerHTML = "<li class=\"kosong-riwayat\">Belum ada akun terdaftar.</li>";
        return;
      }
      daftar.forEach(function (a) {
        const li = document.createElement("li");
        const badge = a.status === "Menunggu"
          ? '<span class="jam">Menunggu</span>'
          : a.status === "Disetujui"
            ? '<span style="color:var(--ok);font-weight:700">Disetujui</span>'
            : '<span style="color:var(--danger);font-weight:700">' + (a.status || "-") + "</span>";
        li.innerHTML =
          '<div class="tgl">' + (a.username || "-") + " · " + badge + "</div>" +
          '<div class="ket-data">' + (a.nama || "-") + " · " + (a.jabatan || "-") + "</div>" +
          '<div class="lok">' + (a.kantor || "-") + " · NIK " + (a.nik || "-") + " · OC " + (a.oc || "-") + "</div>" +
          (a.email ? '<div class="lok">' + a.email + "</div>" : "");
        if (a.status === "Menunggu") {
          const aksi = document.createElement("div");
          aksi.className = "aksi-data";
          const btnOk = document.createElement("button");
          btnOk.type = "button";
          btnOk.className = "mini utama";
          btnOk.textContent = "Setujui";
          btnOk.addEventListener("click", function () { aksiAkun("setujuAkun", a.username); });
          const btnNo = document.createElement("button");
          btnNo.type = "button";
          btnNo.className = "mini bahaya";
          btnNo.textContent = "Tolak";
          btnNo.addEventListener("click", function () { aksiAkun("tolakAkun", a.username); });
          aksi.appendChild(btnOk);
          aksi.appendChild(btnNo);
          li.appendChild(aksi);
        }
        ul.appendChild(li);
      });
    } catch (err) {
      ul.innerHTML = "";
      setStatusAdmin(err.message || String(err), "gagal");
    }
  }

  async function aksiAkun(aksi, username) {
    if (!confirm((aksi === "setujuAkun" ? "Setujui" : "Tolak") + " akun \"" + username + "\"?")) return;
    setStatusAdmin("Memproses…");
    try {
      const h = await panggil({ aksi: aksi, username: username });
      setStatusAdmin(h.pesan || "Berhasil.", "ok");
      await muatDaftarAkun();
    } catch (err) {
      setStatusAdmin(err.message || String(err), "gagal");
    }
  }

  function tampilkanFormLogin(pesan) {
    $("splash").classList.add("usai");
    setTimeout(() => { $("splash").hidden = true; $("kartuAuth").hidden = false; }, 260);
    if (pesan) setStatus(pesan, "gagal", "statusMasuk");
  }

  async function cobaSesiTersimpan() {
    if (!pengguna() || !tokenAktif()) { tampilkanFormLogin(); return; }
    try {
      await panggil({ aksi: "terakhir", jumlah: 1 });
      const cache = ambilProfilCache();
      terapkanProfil(cache || { nama: pengguna() });
      $("kartuAuth").hidden = true;
      tampilkanApp();
    } catch (e) {
      hapusSesi();
      tampilkanFormLogin();
    }
  }

  function mulaiSplash() {
    $("urlScriptGerbang").value = urlScript();
    setTimeout(cobaSesiTersimpan, 1400);
  }

  function gantiTabAuth(keMasuk) {
    $("tabMasuk").classList.toggle("tab-aktif", keMasuk);
    $("tabDaftar").classList.toggle("tab-aktif", !keMasuk);
    $("formMasuk").hidden = !keMasuk;
    $("formDaftar").hidden = keMasuk;
  }

  async function prosesMasuk(e) {
    e.preventDefault();
    const status = (t, j) => setStatus(t, j, "statusMasuk");
    const tombol = e.target.querySelector("button[type=submit]");
    const u = $("mUsername").value.trim(), s = $("mSandi").value;
    if (!u || !s) { status("Isi username dan kata sandi.", "gagal"); return; }
    tombol.disabled = true;
    status("Masuk...");
    try {
      const h = await panggil({ aksi: "login", username: u, sandi: s });
      simpan("pengguna", h.profil.username);
      simpan("token", h.token);
      terapkanProfil(h.profil);
      status("");
      tampilkanApp();
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      status(masalah ? PESAN_KONEKSI : err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  async function prosesDaftar(e) {
    e.preventDefault();
    const status = (t, j) => setStatus(t, j, "statusDaftar");
    const tombol = e.target.querySelector("button[type=submit]");
    const u = $("dUsername").value.trim(), s = $("dSandi").value, nama = $("dNama").value.trim();
    if (!u || !s || !nama) { status("Username, kata sandi, dan nama wajib diisi.", "gagal"); return; }
    tombol.disabled = true;
    status("Mengirim pendaftaran...");
    try {
      const h = await panggil({
        aksi: "daftar", username: u, sandi: s, nama: nama,
        jabatan: $("dJabatan").value, kantor: $("dKantor").value.trim(),
        nik: $("dNik").value.trim(), oc: $("dOc").value, email: $("dEmail").value.trim()
      });
      status(h.pesan || "Pendaftaran terkirim. Menunggu persetujuan admin.", "ok");
      e.target.reset();
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      status(masalah ? PESAN_KONEKSI : err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  function keluarAkun() {
    hapusSesi();
    try { localStorage.removeItem("profil"); } catch (e) { /* abaikan */ }
    location.reload();
  }

  function bukaDialogProfil() {
    if (!profilAktif) return;
    $("pfNama").value = profilAktif.nama || "";
    $("pfJabatan").value = profilAktif.jabatan || "NOA/NOE";
    $("pfKantor").value = profilAktif.kantor || "";
    $("pfNik").value = profilAktif.nik || "";
    $("pfOc").value = profilAktif.oc || "S3";
    setStatus("", "", "statusProfil");
    $("dialogProfil").showModal();
  }

  async function simpanProfilBaru() {
    const status = (t, j) => setStatus(t, j, "statusProfil");
    const tombol = $("simpanProfil");
    tombol.disabled = true;
    status("Menyimpan...");
    try {
      const h = await panggil({
        aksi: "perbaruiProfil", nama: $("pfNama").value.trim(),
        jabatan: $("pfJabatan").value, kantor: $("pfKantor").value.trim(),
        nik: $("pfNik").value.trim(), oc: $("pfOc").value
      });
      terapkanProfil(h.profil);
      $("dialogProfil").close();
    } catch (err) {
      status(err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  /* ---------- Animasi saat scroll ---------- */

  let revealObserver = null;

  function pasangRevealObserver() {
    if (revealObserver || typeof IntersectionObserver === "undefined") {
      document.querySelectorAll(".reveal").forEach((el) => el.classList.add("tampak"));
      return;
    }
    revealObserver = new IntersectionObserver((masuk) => {
      masuk.forEach((entri) => {
        if (entri.isIntersecting) { entri.target.classList.add("tampak"); revealObserver.unobserve(entri.target); }
      });
    }, { threshold: 0.08, rootMargin: "0px 0px -8% 0px" });
    document.querySelectorAll(".reveal").forEach((el) => revealObserver.observe(el));
  }


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

  function setStatus(teks, jenis, target) {
    const s = $(target || "status");
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

    // Dipotong dari tengah menjadi 3:4 (potret) atau 4:3 (lanskap), sama seperti hasil aplikasi kamera.
    const vw = v.videoWidth, vh = v.videoHeight;
    const rasio = vw >= vh ? 4 / 3 : 3 / 4;
    let sw = vw, sh = vh;
    if (vw / vh > rasio) sw = Math.round(vh * rasio); else sh = Math.round(vw / rasio);
    const sx = Math.round((vw - sw) / 2), sy = Math.round((vh - sh) / 2);
    const skala = Math.min(1, 1600 / Math.max(sw, sh));
    const w = Math.round(sw * skala);
    const h = Math.round(sh * skala);
    const c = document.createElement("canvas");
    c.width = w; c.height = h;
    const ctx = c.getContext("2d");
    ctx.drawImage(v, sx, sy, sw, sh, 0, 0, w, h);
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
        pengguna: pengguna(), token: tokenAktif(),
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
      muatTerakhir();
      try { cacheFoto.set(idDariLink(hasil.link), new Uint8Array(await jpg.arrayBuffer())); } catch (e) { /* abaikan */ }
      mintaPdfOtomatis(tanggal);

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
      if (j && j.ok && j.versi === VERSI_SERVER) tulis("Koneksi berhasil, server aktif (versi " + j.versi + ", sudah terbaru).", "ok");
      else if (j && j.ok) tulis("Koneksi berhasil, tetapi Apps Script di server masih versi lama" + (j.versi ? " (" + j.versi + ")" : "") + ". Tempel Code.gs terbaru, lalu Deploy > Manage deployments > Edit > Version: New version > Deploy.", "gagal");
      else tulis("Server menjawab, tapi isinya tidak dikenali.", "gagal");
    } catch (e) {
      tulis(PESAN_KONEKSI, "gagal");
    }
  }

  /* ---------- Form lembur ---------- */

  const BULAN_PANJANG = ["Januari", "Februari", "Maret", "April", "Mei", "Juni", "Juli", "Agustus", "September", "Oktober", "November", "Desember"];

  // Sebelum tanggal 16: periode yang berakhir bulan lalu. Mulai tanggal 16: periode yang berakhir bulan ini.
  function bulanFormDefault() {
    const d = new Date();
    let y = d.getFullYear(), m = d.getMonth() + 1;
    if (d.getDate() < 16) { m -= 1; if (m === 0) { m = 12; y -= 1; } }
    return `${y}-${pad(m)}`;
  }

  function periodeTeks(ym) {
    const [y, m] = ym.split("-").map(Number);
    let ay = y, am = m - 1;
    if (am === 0) { am = 12; ay -= 1; }
    return `16 ${BULAN_PANJANG[am - 1]} ${ay} s/d 15 ${BULAN_PANJANG[m - 1]} ${y}`;
  }

  function perbaruiPeriode() {
    const v = $("bulanForm").value;
    $("ketPeriode").textContent = /^\d{4}-\d{2}$/.test(v) ? "Periode: " + periodeTeks(v) : "Pilih bulan periode";
  }

  function dariBase64(b64) {
    const bin = atob(b64);
    const u = new Uint8Array(bin.length);
    for (let i = 0; i < bin.length; i++) u[i] = bin.charCodeAt(i);
    return u;
  }

  function keBase64Bytes(bytes) {
    let s = "";
    const CH = 0x8000;
    for (let i = 0; i < bytes.length; i += CH) s += String.fromCharCode.apply(null, bytes.subarray(i, i + CH));
    return btoa(s);
  }

  async function panggil(muatan) {
    const res = await fetch(urlScript(), {
      method: "POST",
      headers: { "Content-Type": "text/plain;charset=utf-8" },
      body: JSON.stringify(Object.assign({ pengguna: pengguna(), token: tokenAktif() }, muatan))
    });
    const h = await res.json();
    if (!h.ok) {
      // Versi Apps Script lama tidak mengenal aksi baru dan menjawab seolah ini unggahan foto
      if (muatan.aksi && h.error === "Foto kosong.") {
        throw new Error("Apps Script di server masih versi lama. Tempel Code.gs terbaru, lalu Deploy > Manage deployments > Edit (ikon pensil) > Version: New version > Deploy.");
      }
      throw new Error(h.error || "Server menolak permintaan.");
    }
    return h;
  }

  // Tanggal 16 bulan sebelumnya sampai tanggal 15; jumlah baris mengikuti jumlah hari sebenarnya.
  function hitungPeriodeForm(ym) {
    const [y, m] = ym.split("-").map(Number);
    const ay = m === 1 ? y - 1 : y, am = m === 1 ? 12 : m - 1;
    const dim = (yy, mm) => new Date(yy, mm, 0).getDate();
    const hari = [];
    let yy = ay, mm = am, dd = 16;
    for (let i = 0; i < dim(ay, am); i++) {
      hari.push({ y: yy, m: mm, d: dd });
      dd++;
      if (dd > dim(yy, mm)) { dd = 1; mm++; if (mm > 12) { mm = 1; yy++; } }
    }
    const akhir = { y: y, m: m, d: 15 };
    return { hari, akhir, teks: periodeTeks(ym) };
  }

  function menit(t) {
    const m = String(t).match(/(\d{1,2})[.:](\d{2})/);
    return m ? Number(m[1]) * 60 + Number(m[2]) : 0;
  }

  // Satu baris form per tanggal. Bila ada beberapa kegiatan di tanggal yang sama: mulai paling awal, selesai paling akhir.
  function susunBaris(periode, entri) {
    const grup = {};
    entri.forEach((e) => { (grup[e.tanggal] = grup[e.tanggal] || []).push(e); });
    const unik = (arr) => arr.filter((x, i) => x && arr.indexOf(x) === i);
    return periode.hari.map((h) => {
      const g = grup[`${h.y}-${pad(h.m)}-${pad(h.d)}`];
      if (!g) return null;
      const urut = g.slice().sort((a, b) => menit(a.selesai) - menit(b.selesai));
      const mulai = urut.map((x) => x.mulai).filter(Boolean).sort((a, b) => menit(a) - menit(b))[0] || "18.00";
      return {
        lokasi: unik(urut.map((x) => x.lokasi)).join(", "),
        jadwal: urut[0].jadwal || "Shift Pagi",
        mulai: mulai,
        selesai: urut[urut.length - 1].selesai,
        keterangan: unik(urut.map((x) => x.keterangan)),
        fotoIds: urut.map((x) => x.fotoId).filter(Boolean),
        fotos: []
      };
    });
  }

  let urlPdf = null;
  let sedangForm = false;
  const cacheFoto = new Map();     // ID foto -> byte JPEG, supaya foto yang sama tidak diunduh berulang
  const antrianPdf = new Set();    // periode (yyyy-MM) yang PDF-nya perlu diperbarui
  let antrianJalan = false;
  let jedaPdfMs = 8000;            // tunggu sebentar agar beberapa foto berturut-turut menjadi satu PDF dan satu email
  let timerPdf = null;

  const idDariLink = (l) => { const m = String(l || "").match(/\/d\/([-\w]{10,})/); return m ? m[1] : ""; };
  const autoPdfAktif = () => $("autoPdf").checked;

  // Tanggal 16 ke atas masuk periode yang berakhir bulan depan; sebelum 16 masuk periode yang berakhir bulan ini.
  function periodeDariTanggal(kunci) {
    const [y, m, d] = kunci.split("-").map(Number);
    let ey = y, em = m;
    if (d >= 16) { em++; if (em === 13) { em = 1; ey++; } }
    return `${ey}-${pad(em)}`;
  }

  async function buatForm(opsi) {
    opsi = opsi && opsi.ym ? opsi : {};
    const otomatis = !!opsi.otomatis;
    const status = (t, j) => setStatus(t, j, otomatis ? "statusOtomatis" : "statusForm");
    const wadah = $(otomatis ? "hasilOtomatis" : "hasilForm");
    if (!urlScript()) { $("pengaturan").open = true; status("Isi alamat Web App di Pengaturan koneksi dulu.", "gagal"); return; }
    if (sedangForm) { status("PDF sedang dibuat, tunggu sebentar.", "gagal"); return; }
    const ym = opsi.ym || $("bulanForm").value;
    if (!/^\d{4}-\d{2}$/.test(ym)) { status("Pilih bulan periode dulu.", "gagal"); return; }
    if (typeof PDFLib === "undefined") { status("Pustaka PDF belum termuat. Periksa internet, lalu muat ulang halaman.", "gagal"); return; }

    sedangForm = true;
    const tombol = $("tombolForm");
    tombol.disabled = true;
    tombol.classList.add("memuat");
    tombol.textContent = "Membuat form...";
    wadah.textContent = "";
    if (urlPdf) { URL.revokeObjectURL(urlPdf); urlPdf = null; }
    if (otomatis) {
      $("bulanForm").value = ym;
      perbaruiPeriode();
      muatDaftar();
    }

    try {
      status(otomatis ? "Memperbarui PDF form lembur..." : "Mengambil data lembur dari Sheet...");
      const h = await panggil({ aksi: "dataForm", periode: ym });
      const periode = hitungPeriodeForm(ym);
      const baris = susunBaris(periode, h.entri);
      const jumlahSpl = baris.filter(Boolean).length;
      if (!jumlahSpl) throw new Error("Tidak ada data lembur pada periode " + periode.teks + ".");

      const total = baris.reduce((a, r) => a + (r ? r.fotoIds.length : 0), 0);
      let n = 0;
      for (const r of baris) {
        if (!r) continue;
        for (const id of r.fotoIds) {
          n++;
          if (cacheFoto.has(id)) { r.fotos.push(cacheFoto.get(id)); continue; }
          status(`Mengambil foto ${n} dari ${total}...`);
          try {
            const f = await panggil({ aksi: "foto", id });
            const bytes = dariBase64(f.data);
            cacheFoto.set(id, bytes);
            r.fotos.push(bytes);
          } catch (e) { /* foto yang gagal diambil dilewati */ }
        }
      }

      status("Menyusun PDF...");
      const bytes = await buatPdfLembur(PDFLib, {
        profil: h.profil, periode: periode, bulan: BULAN_PANJANG, baris: baris,
        catatan: h.catatan, catatanSpl: h.catatanSpl, fotoLebarCm: h.fotoLebarCm, fotoTinggiCm: h.fotoTinggiCm
      }, { biznet: dariBase64(ASET_LOGO.biznet), s3: dariBase64(ASET_LOGO.s3) });

      const nama = `Form Tunjangan Kerja ${periode.teks.replace(/\//g, "-")}.pdf`;
      const blob = new Blob([bytes], { type: "application/pdf" });
      urlPdf = URL.createObjectURL(blob);

      const tambah = (teks, href, unduh) => {
        const a = document.createElement("a");
        a.href = href; a.textContent = teks;
        if (unduh) a.download = nama; else { a.target = "_blank"; a.rel = "noopener"; }
        wadah.append(a);
        return a;
      };
      tambah("Buka PDF", urlPdf, false);
      tambah("Unduh PDF", urlPdf, true);
      try {
        const berkas = new File([blob], nama, { type: "application/pdf" });
        if (navigator.canShare && navigator.canShare({ files: [berkas] })) {
          const b = tambah("Bagikan PDF", "#", false);
          b.addEventListener("click", (ev) => { ev.preventDefault(); navigator.share({ files: [berkas], title: nama }).catch(() => {}); });
        }
      } catch (e) { /* perangkat tanpa fitur bagikan */ }

      const ringkas = `${periode.hari.length} baris tanggal dan ${jumlahSpl} Surat Perintah Lembur`;
      status(`Form siap: ${ringkas}. Menyimpan ke Drive...`, "ok");
      try {
        const up = await panggil({ aksi: "simpanPdf", nama: nama, periode: periode.teks, email: $("emailPdf").checked, data: keBase64Bytes(bytes) });
        if (typeof up.url === "string" && up.url.startsWith("https://")) tambah("Buka salinan di Drive", up.url, false);
        buatTombolCetak(wadah, { url: urlPdf, id: up.id, nama: nama, status: status });
        let email = "";
        if (up.emailKe) email = ` PDF juga dikirim ke email ${up.emailKe}.`;
        else if (up.emailGagal) email = ` Email PDF gagal terkirim (${up.emailGagal}).`;
        status(`${otomatis ? "PDF form lembur diperbarui" : "Form siap"}: ${ringkas}. Salinan tersimpan di Drive.${email}`, up.emailGagal ? "gagal" : "ok");
      } catch (e) {
        status(`Form siap: ${ringkas}. Salinan ke Drive gagal, gunakan Unduh PDF.`, "ok");
      }
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      status("Gagal: " + (masalah ? PESAN_KONEKSI : err.message), "gagal");
    } finally {
      sedangForm = false;
      tombol.disabled = false;
      tombol.classList.remove("memuat");
      tombol.textContent = "Buat PDF form lembur";
    }
  }

  // Dipanggil setelah foto disimpan, data diubah, atau data dihapus. Berjalan di latar belakang.
  function mintaPdfOtomatis() {
    if (!autoPdfAktif() || !urlScript()) return;
    Array.prototype.slice.call(arguments).forEach((k) => {
      if (/^\d{4}-\d{2}-\d{2}$/.test(k || "")) antrianPdf.add(periodeDariTanggal(k));
    });
    if (!antrianJalan) setStatus("PDF form lembur akan dibuat beberapa detik lagi...", "", "statusOtomatis");
    clearTimeout(timerPdf);
    timerPdf = setTimeout(jalankanAntrian, jedaPdfMs);
  }

  async function jalankanAntrian() {
    if (antrianJalan) return;
    antrianJalan = true;
    try {
      while (antrianPdf.size) {
        const ym = antrianPdf.values().next().value;
        antrianPdf.delete(ym);
        while (sedangForm) await new Promise((r) => setTimeout(r, 500));
        await buatForm({ ym: ym, otomatis: true });
      }
    } finally {
      antrianJalan = false;
    }
  }

  /* ---------- Data lembur: lihat, ubah, hapus ---------- */

  let daftarData = [];

  function tanggalDariKunci(k) {
    const [y, m, d] = k.split("-").map(Number);
    return new Date(y, m - 1, d);
  }

  function ringkasData(data) {
    const per = {};
    data.forEach((e) => {
      const p = per[e.tanggal] = per[e.tanggal] || { a: 1e9, b: 0 };
      p.a = Math.min(p.a, menit(e.mulai));
      p.b = Math.max(p.b, menit(e.selesai));
    });
    const hari = Object.keys(per);
    const total = hari.reduce((t, k) => t + Math.max(0, per[k].b - per[k].a), 0);
    return { jumlah: data.length, hari: hari.length, total: total };
  }

  function buatKartuData(e, i) {
    const li = document.createElement("li");
    li.style.animationDelay = `${Math.min(i, 8) * 50}ms`;
    const d = tanggalDariKunci(e.tanggal);
    const tgl = document.createElement("div");
    tgl.className = "tgl";
    tgl.textContent = `${HARI_FMT.format(d)}, ${TGL_FMT.format(d)}`;
    const jam = document.createElement("div");
    jam.className = "jam";
    jam.textContent = `${e.mulai} s/d ${e.selesai}  |  ${e.jadwal}`;
    const ket = document.createElement("div");
    ket.className = "ket-data";
    ket.textContent = e.keterangan || "(tanpa keterangan)";
    const lok = document.createElement("div");
    lok.className = "lok";
    lok.textContent = e.lokasi || "(lokasi kosong)";
    li.append(tgl, jam, ket, lok);

    const aksi = document.createElement("div");
    aksi.className = "aksi-data";
    const tombol = (teks, kelas, fn) => {
      const b = document.createElement("button");
      b.type = "button"; b.className = "mini" + (kelas ? " " + kelas : ""); b.textContent = teks;
      b.addEventListener("click", fn);
      aksi.append(b);
    };
    if (e.fotoId) {
      tombol("Foto", "", () => lihatFoto(e));
      tombol("Ubah", "", () => bukaEdit(e));
      tombol("Hapus", "bahaya", () => bukaHapus(e));
    }
    li.append(aksi);
    return li;
  }

  function gambarDaftar() {
    const ul = $("daftarData");
    ul.textContent = "";
    const r = ringkasData(daftarData);
    $("ringkasData").hidden = !daftarData.length;
    $("rDataJumlah").textContent = String(r.jumlah);
    $("rHari").textContent = String(r.hari);
    $("rJam").textContent = `${Math.floor(r.total / 60)}j ${pad(r.total % 60)}m`;
    if (!daftarData.length) { setStatus("Belum ada data lembur pada periode ini.", "", "statusDaftar"); return; }
    setStatus("", "", "statusDaftar");
    daftarData.forEach((e, i) => ul.append(buatKartuData(e, i)));
  }

  // "Tersimpan terakhir": 10 data terakhir langsung dari Sheet, lengkap dengan Foto, Ubah, dan Hapus
  let daftarTerakhir = [];

  function gambarTerakhir() {
    const ul = $("riwayat");
    ul.textContent = "";
    $("riwayatKosong").style.display = daftarTerakhir.length ? "none" : "block";
    daftarTerakhir.forEach((e, i) => ul.append(buatKartuData(e, i)));
  }

  async function muatTerakhir() {
    if (!urlScript()) { gambarRiwayat(); return; }
    const status = (t, j) => setStatus(t, j, "statusTerakhir");
    status("Memuat...");
    try {
      const h = await panggil({ aksi: "terakhir", jumlah: 10 });
      daftarTerakhir = h.entri;
      gambarTerakhir();
      status("");
    } catch (err) {
      gambarRiwayat();
      status("Menampilkan catatan di perangkat ini. Server: " + String(err.message).slice(0, 160), "gagal");
    }
  }

  async function muatDaftar() {
    const status = (t, j) => setStatus(t, j, "statusDaftar");
    if (!urlScript()) { status("Isi alamat Web App di Pengaturan koneksi untuk melihat data.", "gagal"); return; }
    const ym = $("bulanForm").value;
    if (!/^\d{4}-\d{2}$/.test(ym)) return;
    status("Memuat data...");
    try {
      const h = await panggil({ aksi: "dataForm", periode: ym });
      daftarData = h.entri.slice().sort((a, b) =>
        a.tanggal < b.tanggal ? -1 : a.tanggal > b.tanggal ? 1 : menit(a.selesai) - menit(b.selesai));
      gambarDaftar();
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      daftarData = [];
      $("daftarData").textContent = "";
      $("ringkasData").hidden = true;
      status("Gagal memuat data: " + (masalah ? PESAN_KONEKSI : err.message), "gagal");
    }
  }

  async function lihatFoto(e) {
    const dlg = $("dialogFoto");
    const d = tanggalDariKunci(e.tanggal);
    $("ketFoto").textContent = `${TGL_FMT.format(d)}: memuat foto...`;
    $("gambarFoto").removeAttribute("src");
    dlg.showModal();
    try {
      const f = await panggil({ aksi: "foto", id: e.fotoId });
      $("gambarFoto").src = "data:image/jpeg;base64," + f.data;
      $("ketFoto").textContent = `${TGL_FMT.format(d)}, ${e.lokasi || ""}`;
    } catch (err) {
      $("ketFoto").textContent = "Foto tidak bisa dimuat: " + err.message;
    }
  }

  let dataDiedit = null;

  // "TROUBLESHOOT FTTH 18182637 NAMA CUSTOMER" -> jenis, nomor tiket, nama customer
  function pecahKeterangan(k) {
    const t = String(k || "").trim();
    const m = t.match(/^(.*?)\s*\b(\d{4,})\b\s*(.*)$/);
    if (m) return { jenis: m[1].trim(), tiket: m[2], customer: m[3].trim() };
    return { jenis: t, tiket: "", customer: "" };
  }

  function keteranganEdit() {
    return [$("edJenis").value, $("edTiket").value, $("edCustomer").value]
      .map((x) => x.trim()).filter(Boolean).join(" ").toUpperCase();
  }

  function perbaruiPratinjauEdit() {
    const k = keteranganEdit();
    $("edPratinjau").textContent = k ? "Keterangan: " + k : "Keterangan masih kosong";
  }

  function bukaEdit(e) {
    dataDiedit = e;
    $("edTanggal").value = e.tanggal;
    $("edLokasi").value = e.lokasi;
    $("edJadwal").value = e.jadwal;
    $("edMulai").value = e.mulai;
    $("edSelesai").value = e.selesai;
    const pecah = pecahKeterangan(e.keterangan);
    $("edJenis").value = pecah.jenis || "TROUBLESHOOT FTTH";
    $("edTiket").value = pecah.tiket;
    $("edCustomer").value = pecah.customer;
    perbaruiPratinjauEdit();
    setStatus("", "", "statusEdit");
    $("dialogEdit").showModal();
  }

  async function simpanEdit() {
    const status = (t, j) => setStatus(t, j, "statusEdit");
    if (!dataDiedit) return;
    const tombol = $("simpanEdit");
    tombol.disabled = true;
    status("Menyimpan...");
    try {
      await panggil({
        aksi: "ubah", id: dataDiedit.fotoId,
        tanggal: $("edTanggal").value,
        lokasi: $("edLokasi").value.trim(),
        jadwal: $("edJadwal").value.trim(),
        mulai: $("edMulai").value.trim(),
        selesai: $("edSelesai").value.trim(),
        keterangan: keteranganEdit()
      });
      const tglLama = dataDiedit.tanggal, tglBaru = $("edTanggal").value;
      $("dialogEdit").close();
      dataDiedit = null;
      mintaPdfOtomatis(tglLama, tglBaru);
      muatTerakhir();
      await muatDaftar();
      setStatus("Data berhasil diperbarui.", "ok", "statusDaftar");
    } catch (err) {
      status("Gagal: " + err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  let dataDihapus = null;

  function bukaHapus(e) {
    dataDihapus = e;
    const d = tanggalDariKunci(e.tanggal);
    $("ketHapus").textContent = `${TGL_FMT.format(d)}: ${e.keterangan || e.lokasi || "(tanpa keterangan)"}`;
    setStatus("", "", "statusHapus");
    $("dialogHapus").showModal();
  }

  async function yakinHapus() {
    const status = (t, j) => setStatus(t, j, "statusHapus");
    if (!dataDihapus) return;
    const tombol = $("yakinHapus");
    tombol.disabled = true;
    status("Menghapus...");
    try {
      await panggil({ aksi: "hapus", id: dataDihapus.fotoId });
      const tglHapus = dataDihapus.tanggal;
      $("dialogHapus").close();
      dataDihapus = null;
      mintaPdfOtomatis(tglHapus);
      muatTerakhir();
      await muatDaftar();
      setStatus("Data dihapus dari Sheet dan Drive (foto masuk sampah Drive).", "ok", "statusDaftar");
    } catch (err) {
      status("Gagal: " + err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  /* ---------- Penyimpanan Drive dan Sheet ---------- */

  const GB = 1024 * 1024 * 1024, MB = 1024 * 1024;
  const angka = (n, d) => Number(n).toLocaleString("id-ID", { maximumFractionDigits: d === undefined ? 0 : d });
  const keadaan = (p) => (p >= 90 ? "kritis" : p >= 70 ? "waspada" : "aman");
  const LABEL_KEADAAN = { aman: "Aman", waspada: "Waspada", kritis: "Hampir penuh" };

  function ukuranTeks(b) {
    if (b >= GB) return angka(b / GB, 1) + " GB";
    if (b >= MB) return angka(b / MB, 1) + " MB";
    if (b >= 1024) return angka(b / 1024, 0) + " KB";
    return angka(b) + " B";
  }

  function buatMeter(judul, nilai, persen, catatan) {
    const k = keadaan(persen);
    const el = document.createElement("div");
    el.className = "meter " + k;
    const atas = document.createElement("div");
    atas.className = "meter-atas";
    const j = document.createElement("span");
    j.className = "meter-judul"; j.textContent = judul;
    const n = document.createElement("span");
    n.className = "meter-nilai"; n.textContent = nilai;
    atas.append(j, n);
    const bar = document.createElement("div");
    bar.className = "meter-bar";
    bar.setAttribute("role", "progressbar");
    bar.setAttribute("aria-label", judul);
    bar.setAttribute("aria-valuemin", "0");
    bar.setAttribute("aria-valuemax", "100");
    bar.setAttribute("aria-valuenow", String(Math.round(persen)));
    const isi = document.createElement("i");
    bar.append(isi);
    const cat = document.createElement("div");
    cat.className = "meter-cat";
    cat.textContent = `${catatan} (${LABEL_KEADAAN[k]}, terpakai ${angka(persen, 1)}%)`;
    el.append(atas, bar, cat);
    requestAnimationFrame(() => requestAnimationFrame(() => { isi.style.width = Math.max(persen, 1.5).toFixed(1) + "%"; }));
    return el;
  }

  function buatInfo(judul, baris) {
    const el = document.createElement("div");
    el.className = "info-simpan";
    const t = document.createElement("strong");
    t.textContent = judul;
    el.append(t);
    baris.forEach((b) => { const p = document.createElement("span"); p.textContent = b; el.append(p); });
    return el;
  }

  function gambarKapasitas(h, waktu) {
    const wadah = $("isiKapasitas");
    wadah.textContent = "";
    const peringatan = [];
    wadah.style.display = "grid";
    wadah.style.gap = "14px";

    // Google Drive (seluruh akun)
    const d = h.drive || {};
    if (d.batas > 0) {
      const p = (d.pakai / d.batas) * 100;
      wadah.append(buatMeter("Google Drive", `${ukuranTeks(d.pakai)} dari ${ukuranTeks(d.batas)}`, p, `Tersisa ${ukuranTeks(Math.max(0, d.batas - d.pakai))}`));
      if (p >= 80) peringatan.push({ p, teks: `Ruang Google Drive ${p >= 90 ? "hampir penuh" : "mulai menipis"} (${angka(p, 0)}%). Kosongkan sampah Drive atau hapus file yang tidak dipakai supaya foto baru tetap bisa disimpan.` });
    } else {
      wadah.append(buatInfo("Google Drive", [`Terpakai ${ukuranTeks(d.pakai || 0)}`, "Batas kapasitas tidak terbaca (bisa jadi tanpa batas untuk akun ini)."]));
    }

    // Folder foto dan PDF
    const f = h.foto || {}, pdf = h.pdf || {};
    const baris = [
      `${angka(f.jumlah || 0)} foto, sekitar ${ukuranTeks(f.ukuran || 0)}${f.perkiraan ? " (perkiraan)" : ""}`,
      `${angka(pdf.jumlah || 0)} PDF form lembur, sekitar ${ukuranTeks(pdf.ukuran || 0)}`
    ];
    if (d.batas > 0 && f.rata > 0) baris.push(`Sisa ruang cukup untuk sekitar ${angka(Math.floor(Math.max(0, d.batas - d.pakai) / f.rata))} foto lagi.`);
    wadah.append(buatInfo("Folder foto dan PDF", baris));

    // Google Sheet
    const sh = h.sheet || {};
    const ps = sh.batasSel > 0 ? (sh.sel / sh.batasSel) * 100 : 0;
    wadah.append(buatMeter("Google Sheet", `${angka(sh.sel)} dari ${angka(sh.batasSel)} sel`, ps, `Muat sekitar ${angka(sh.sisaData)} data lagi (sekarang ${angka(sh.barisData)} data)`));
    if (ps >= 80) peringatan.push({ p: ps, teks: `Google Sheet ${ps >= 90 ? "hampir mencapai" : "mendekati"} batas 10 juta sel (${angka(ps, 0)}%). Pindahkan data lama ke Sheet baru.` });

    if (typeof h.emailSisa === "number") wadah.append(buatInfo("Email cadangan", [`Sisa kuota kirim email hari ini: ${angka(h.emailSisa)}`]));

    $("waktuKapasitas").textContent = waktu ? "Diperbarui " + new Date(waktu).toLocaleString("id-ID") : "";

    // Peringatan di bagian atas halaman
    const banner = $("peringatan");
    if (peringatan.length) {
      peringatan.sort((a, b) => b.p - a.p);
      banner.textContent = peringatan.map((x) => x.teks).join(" ");
      banner.className = "peringatan" + (peringatan[0].p >= 90 ? " kritis" : "");
      banner.hidden = false;
    } else {
      banner.hidden = true;
    }
  }

  async function muatKapasitas(segar) {
    const tombol = $("muatKapasitas");
    if (!urlScript()) { $("isiKapasitas").textContent = "Isi alamat Web App di Pengaturan koneksi untuk melihat penyimpanan."; return; }
    tombol.disabled = true;
    tombol.textContent = "Memuat...";
    try {
      const h = await panggil({ aksi: "kapasitas", segar: !!segar });
      gambarKapasitas(h, h.waktu);
      simpan("kapasitas", JSON.stringify(h));
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      if (!$("isiKapasitas").children.length) $("isiKapasitas").textContent = "Gagal memuat: " + (masalah ? PESAN_KONEKSI : err.message);
    } finally {
      tombol.disabled = false;
      tombol.textContent = "Perbarui penyimpanan";
    }
  }

  /* ---------- Scan dokumen ---------- */

  const scan = { halaman: [], stream: null, target: null, sibuk: false };
  const SISI_SCAN = 2000;   // sisi terpanjang gambar mentah (px)

  const jepit = (v) => (v < 0 ? 0 : v > 1 ? 1 : v);

  function maksSepar(a, w, h, r) {
    const t = new Float32Array(a.length), o = new Float32Array(a.length);
    for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
      let m = -1;
      for (let k = Math.max(0, x - r); k <= Math.min(w - 1, x + r); k++) m = Math.max(m, a[y * w + k]);
      t[y * w + x] = m;
    }
    for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
      let m = -1;
      for (let k = Math.max(0, y - r); k <= Math.min(h - 1, y + r); k++) m = Math.max(m, t[k * w + x]);
      o[y * w + x] = m;
    }
    return o;
  }

  function kaburSepar(a, w, h, r) {
    const t = new Float32Array(a.length), o = new Float32Array(a.length);
    for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
      let j = 0, n = 0;
      for (let k = Math.max(0, x - r); k <= Math.min(w - 1, x + r); k++) { j += a[y * w + k]; n++; }
      t[y * w + x] = j / n;
    }
    for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
      let j = 0, n = 0;
      for (let k = Math.max(0, y - r); k <= Math.min(h - 1, y + r); k++) { j += t[k * w + x]; n++; }
      o[y * w + x] = j / n;
    }
    return o;
  }

  // Perkiraan warna kertas di setiap titik (peta kecil) supaya bayangan dan cahaya tidak merata bisa diratakan
  function petaLatar(gray, w, h) {
    const f = 8;
    const sw = Math.max(1, Math.ceil(w / f)), sh = Math.max(1, Math.ceil(h / f));
    const kecil = new Float32Array(sw * sh);
    for (let y = 0; y < sh; y++) for (let x = 0; x < sw; x++) {
      let j = 0, n = 0;
      const y1 = Math.min(h, y * f + f), x1 = Math.min(w, x * f + f);
      for (let yy = y * f; yy < y1; yy++) for (let xx = x * f; xx < x1; xx++) { j += gray[yy * w + xx]; n++; }
      kecil[y * sw + x] = j / n;
    }
    return { peta: kaburSepar(maksSepar(kecil, sw, sh, 3), sw, sh, 3), sw: sw, sh: sh, f: f };
  }

  // Memutar, mengecilkan, dan menerapkan tampilan (dokumen, hitamputih, asli)
  function prosesHalaman(sumber, rot, mode, sisiMaks, kotak) {
    if (kotak) sumber = luruskan(sumber, kotak, sisiMaks);
    const sk = Math.min(1, sisiMaks / Math.max(sumber.width, sumber.height));
    const rw = Math.max(1, Math.round(sumber.width * sk)), rh = Math.max(1, Math.round(sumber.height * sk));
    const tukar = rot % 180 !== 0;
    const c = document.createElement("canvas");
    c.width = tukar ? rh : rw;
    c.height = tukar ? rw : rh;
    const g = c.getContext("2d", { willReadFrequently: true });
    g.translate(c.width / 2, c.height / 2);
    g.rotate((rot * Math.PI) / 180);
    g.drawImage(sumber, -rw / 2, -rh / 2, rw, rh);
    if (mode === "asli") return c;

    const w = c.width, h = c.height;
    const img = g.getImageData(0, 0, w, h);
    const d = img.data;
    const gray = new Float32Array(w * h);
    for (let i = 0, j = 0; i < gray.length; i++, j += 4) gray[i] = (d[j] * 299 + d[j + 1] * 587 + d[j + 2] * 114) / 1000;
    const L = petaLatar(gray, w, h);
    for (let y = 0; y < h; y++) {
      const gy = Math.min(L.sh - 1, Math.max(0, y / L.f - 0.5));
      const y0 = Math.floor(gy), y1 = Math.min(L.sh - 1, y0 + 1), fy = gy - y0;
      for (let x = 0; x < w; x++) {
        const gx = Math.min(L.sw - 1, Math.max(0, x / L.f - 0.5));
        const x0 = Math.floor(gx), x1 = Math.min(L.sw - 1, x0 + 1), fx = gx - x0;
        const bg = (L.peta[y0 * L.sw + x0] * (1 - fx) + L.peta[y0 * L.sw + x1] * fx) * (1 - fy) +
                   (L.peta[y1 * L.sw + x0] * (1 - fx) + L.peta[y1 * L.sw + x1] * fx) * fy;
        const rasio = gray[y * w + x] / Math.max(bg, 1);
        let v;
        if (mode === "hitamputih") v = rasio < 0.78 ? 0 : 255;
        else { const t = jepit((rasio - 0.55) / 0.42); v = t * t * (3 - 2 * t) * 255; }
        const p = (y * w + x) * 4;
        d[p] = d[p + 1] = d[p + 2] = v;
        d[p + 3] = 255;
      }
    }
    g.putImageData(img, 0, 0);
    return c;
  }

  const tunda = () => new Promise((r) => setTimeout(r, 0));

  function perbaruiThumb(p) {
    p.thumb = prosesHalaman(p.orig, p.rot, $("filterScan").value, 300, p.kotak).toDataURL("image/jpeg", 0.75);
  }

  async function perbaruiSemuaThumb() {
    for (const p of scan.halaman) { perbaruiThumb(p); await tunda(); }
    gambarTumpukan();
  }

  function gambarTumpukan() {
    const ul = $("tumpukan");
    ul.textContent = "";
    const n = scan.halaman.length;
    $("tombolSimpanScan").disabled = !n || scan.sibuk;
    const badge = $("badgeHalaman");
    if (badge) {
      badge.hidden = !n;
      badge.textContent = n ? n + " hlm" : "";
    }
    $("ketTumpukan").textContent = n
      ? (scan.target ? "Akan ditambah ke dokumen yang dipilih" : "Geser untuk melihat · urutan kiri → kanan = PDF")
      : "Belum ada halaman · scan atau pilih dari galeri";
    scan.halaman.forEach((p, i) => {
      const li = document.createElement("li");
      // Tandai landscape bila hasil setelah rotasi lebih lebar
      const tukar = (p.rot || 0) % 180 !== 0;
      const w = p.orig ? p.orig.width : 0, h = p.orig ? p.orig.height : 0;
      const ls = tukar ? h > w : w > h;
      if (ls) li.classList.add("ls");
      const img = document.createElement("img");
      img.src = p.thumb; img.alt = "Halaman " + (i + 1);
      const no = document.createElement("div");
      no.className = "no";
      no.textContent = (i + 1) + (p.kotak ? " · potong" : "");
      const aksi = document.createElement("div");
      aksi.className = "aksi-hal";
      const tombol = (teks, kelas, fn, mati) => {
        const b = document.createElement("button");
        b.type = "button"; b.className = "mini" + (kelas ? " " + kelas : ""); b.textContent = teks;
        b.disabled = !!mati;
        b.addEventListener("click", fn);
        aksi.append(b);
      };
      tombol("←", "", () => { if (i > 0) { [scan.halaman[i - 1], scan.halaman[i]] = [scan.halaman[i], scan.halaman[i - 1]]; gambarTumpukan(); } }, i === 0);
      tombol("→", "", () => { if (i < n - 1) { [scan.halaman[i + 1], scan.halaman[i]] = [scan.halaman[i], scan.halaman[i + 1]]; gambarTumpukan(); } }, i === n - 1);
      tombol("↻", "", () => { p.rot = (p.rot + 90) % 360; perbaruiThumb(p); gambarTumpukan(); });
      tombol("✂", "", () => bukaPotong(p));
      tombol("✕", "bahaya", () => { scan.halaman.splice(i, 1); gambarTumpukan(); });
      li.append(img, no, aksi);
      ul.append(li);
    });
  }

  function tambahHalaman(kanvas) {
    const p = { orig: kanvas, rot: 0, thumb: "", kotak: null };
    if ($("potongOtomatis").checked) { try { p.kotak = deteksiDokumen(kanvas); } catch (e) { p.kotak = null; } }
    perbaruiThumb(p);
    scan.halaman.push(p);
    gambarTumpukan();
  }

  async function kanvasDariFile(file) {
    let bmp;
    try {
      bmp = await createImageBitmap(file, { imageOrientation: "from-image" });
    } catch (e) {
      bmp = await new Promise((res, rej) => {
        const img = new Image();
        img.onload = () => res(img);
        img.onerror = () => rej(new Error("Gambar tidak bisa dibaca."));
        img.src = URL.createObjectURL(file);
      });
    }
    const sk = Math.min(1, SISI_SCAN / Math.max(bmp.width, bmp.height));
    const c = document.createElement("canvas");
    c.width = Math.round(bmp.width * sk);
    c.height = Math.round(bmp.height * sk);
    c.getContext("2d").drawImage(bmp, 0, 0, c.width, c.height);
    if (bmp.close) bmp.close();
    return c;
  }

  async function dariGaleriScan(files) {
    const status = (t, j) => setStatus(t, j, "statusScan");
    for (const f of Array.from(files)) {
      if (!f.type.startsWith("image/")) continue;
      try { tambahHalaman(await kanvasDariFile(f)); await tunda(); }
      catch (e) { status("Satu gambar gagal dibaca.", "gagal"); }
    }
    $("galeriScan").value = "";
  }

  /* Kamera scan — ikut orientasi HP (portrait / landscape) */
  function orientasiLayar() {
    try {
      if (screen.orientation && screen.orientation.type) {
        return screen.orientation.type.indexOf("landscape") >= 0 ? "landscape" : "portrait";
      }
    } catch (e) { /* abaikan */ }
    return window.innerWidth > window.innerHeight ? "landscape" : "portrait";
  }

  function constraintKameraScan() {
    const ori = orientasiLayar();
    // Portrait: tinggi lebih besar; landscape: lebar lebih besar. Minta resolusi tinggi.
    const video = {
      facingMode: { ideal: "environment" },
      width: ori === "landscape" ? { ideal: 2560 } : { ideal: 1440 },
      height: ori === "landscape" ? { ideal: 1440 } : { ideal: 2560 }
    };
    return { video: video, audio: false };
  }

  function aturBingkaiPanduan() {
    const bingkai = $("bingkaiA4");
    const vf = $("kameraScan") && $("kameraScan").querySelector(".vf");
    if (!bingkai || !vf) return;
    const r = vf.getBoundingClientRect();
    const ori = orientasiLayar();
    // Rasio A4 ≈ 1 : 1.414. Sisakan margin agar mudah menempatkan dokumen.
    const margin = 0.1;
    let bw, bh;
    if (ori === "portrait") {
      bh = r.height * (1 - margin * 2);
      bw = bh / 1.414;
      if (bw > r.width * (1 - margin * 2)) {
        bw = r.width * (1 - margin * 2);
        bh = bw * 1.414;
      }
    } else {
      bw = r.width * (1 - margin * 2);
      bh = bw / 1.414;
      if (bh > r.height * (1 - margin * 2)) {
        bh = r.height * (1 - margin * 2);
        bw = bh * 1.414;
      }
    }
    bingkai.style.width = Math.round(bw) + "px";
    bingkai.style.height = Math.round(bh) + "px";
    const badge = $("badgeOri");
    if (badge) badge.textContent = ori === "landscape" ? "Landscape" : "Portrait";
  }

  async function bukaKameraScan() {
    if (!navigator.mediaDevices || !navigator.mediaDevices.getUserMedia) {
      setStatus("Kamera tidak didukung di browser ini. Pakai Dari galeri.", "gagal", "statusScan"); return;
    }
    try {
      scan.stream = await navigator.mediaDevices.getUserMedia(constraintKameraScan());
    } catch (e) {
      // Fallback tanpa constraint resolusi ketat
      try {
        scan.stream = await navigator.mediaDevices.getUserMedia({
          video: { facingMode: { ideal: "environment" } }, audio: false
        });
      } catch (e2) {
        setStatus("Kamera tidak bisa dibuka. Izinkan akses kamera di browser, atau pakai Dari galeri.", "gagal", "statusScan"); return;
      }
    }
    const v = $("videoScan");
    v.srcObject = scan.stream;
    try { await v.play(); } catch (e) { /* diputar otomatis */ }
    $("kameraScan").classList.add("aktif");
    document.body.style.overflow = "hidden";
    scan.senter = false;
    const btnSenter = $("senterScan");
    if (btnSenter) {
      btnSenter.classList.remove("nyala");
      const track = scan.stream.getVideoTracks()[0];
      const caps = track && track.getCapabilities ? track.getCapabilities() : {};
      btnSenter.hidden = !(caps && caps.torch);
    }
    perbaruiInfoScan();
    aturBingkaiPanduan();
    mulaiDeteksiLangsung();
    // Ikuti putaran HP saat kamera terbuka
    if (!scan._onOri) {
      scan._onOri = () => { aturBingkaiPanduan(); };
      try { screen.orientation && screen.orientation.addEventListener("change", scan._onOri); } catch (e) { /* abaikan */ }
      window.addEventListener("resize", scan._onOri);
    }
    $("ranaScan").focus();
  }

  function tutupKameraScan() {
    hentikanDeteksiLangsung();
    if (scan.stream) {
      try {
        const track = scan.stream.getVideoTracks()[0];
        if (track && scan.senter) track.applyConstraints({ advanced: [{ torch: false }] }).catch(() => {});
      } catch (e) { /* abaikan */ }
      scan.stream.getTracks().forEach((t) => t.stop());
      scan.stream = null;
    }
    $("videoScan").srcObject = null;
    $("kameraScan").classList.remove("aktif");
    document.body.style.overflow = "";
    scan.senter = false;
    if (scan._onOri) {
      try { screen.orientation && screen.orientation.removeEventListener("change", scan._onOri); } catch (e) { /* abaikan */ }
      window.removeEventListener("resize", scan._onOri);
      scan._onOri = null;
    }
  }

  async function toggleSenterScan() {
    if (!scan.stream) return;
    const track = scan.stream.getVideoTracks()[0];
    if (!track) return;
    const caps = track.getCapabilities ? track.getCapabilities() : {};
    if (!caps.torch) {
      setStatus("Senter tidak tersedia di kamera ini.", "gagal", "statusScan");
      return;
    }
    scan.senter = !scan.senter;
    try {
      await track.applyConstraints({ advanced: [{ torch: scan.senter }] });
      $("senterScan").classList.toggle("nyala", scan.senter);
    } catch (e) {
      scan.senter = false;
      $("senterScan").classList.remove("nyala");
    }
  }

  function perbaruiInfoScan() {
    const n = scan.halaman.length;
    $("infoScan").textContent = n ? n + " halaman siap" : "Siap scan";
  }

  async function ambilHalamanScan() {
    const v = $("videoScan");
    if (!v.videoWidth) return;
    // Ambil frame penuh — orientasi mengikuti stream kamera (portrait/landscape HP)
    const sk = Math.min(1, SISI_SCAN / Math.max(v.videoWidth, v.videoHeight));
    const c = document.createElement("canvas");
    c.width = Math.round(v.videoWidth * sk);
    c.height = Math.round(v.videoHeight * sk);
    c.getContext("2d").drawImage(v, 0, 0, c.width, c.height);
    const kilat = $("kilatScan");
    kilat.classList.remove("jalan"); void kilat.offsetWidth; kilat.classList.add("jalan");
    tambahHalaman(c);
    oto.s.siap = false;
    perbaruiInfoScan();
    // Reset progress stabil
    const bar = $("progressStabilBar");
    const wrap = $("progressStabil");
    if (bar) bar.style.width = "0%";
    if (wrap) { wrap.hidden = true; wrap.classList.remove("ok"); }
  }

  /* Menyusun dan menyimpan PDF — halaman ikut orientasi gambar (portrait / landscape) */
  async function susunPdfScan(pdfAwal) {
    const { PDFDocument } = PDFLib;
    const pdf = pdfAwal ? await PDFDocument.load(pdfAwal) : await PDFDocument.create();
    const mode = $("filterScan").value;
    let n = 0;
    for (const p of scan.halaman) {
      n++;
      setStatus(`Menyusun halaman ${n} dari ${scan.halaman.length}...`, "", "statusScan");
      await tunda();
      const c = prosesHalaman(p.orig, p.rot, mode, 2000, p.kotak);
      const blob = await new Promise((r) => c.toBlob(r, "image/jpeg", 0.88));
      const img = await pdf.embedJpg(new Uint8Array(await blob.arrayBuffer()));
      // A4 portrait atau landscape sesuai proporsi hasil scan
      const landscape = img.width > img.height;
      const pageW = landscape ? 841.89 : 595.28;
      const pageH = landscape ? 595.28 : 841.89;
      const halaman = pdf.addPage([pageW, pageH]);
      // Sedikit margin agar tidak mepet tepi
      const margin = 18;
      const sk = Math.min((pageW - margin * 2) / img.width, (pageH - margin * 2) / img.height);
      const w = img.width * sk, h = img.height * sk;
      halaman.drawImage(img, {
        x: (pageW - w) / 2,
        y: (pageH - h) / 2,
        width: w,
        height: h
      });
    }
    return pdf;
  }

  async function simpanTumpukan() {
    const status = (t, j) => setStatus(t, j, "statusScan");
    if (!scan.halaman.length || scan.sibuk) return;
    if (!urlScript()) { $("pengaturan").open = true; status("Isi alamat Web App di Pengaturan koneksi dulu.", "gagal"); return; }
    if (typeof PDFLib === "undefined") { status("Pustaka PDF belum termuat. Periksa internet, lalu muat ulang halaman.", "gagal"); return; }

    scan.sibuk = true;
    const tombol = $("tombolSimpanScan");
    tombol.disabled = true; tombol.classList.add("memuat"); tombol.textContent = "Menyimpan...";
    $("hasilScan").textContent = "";
    try {
      let awal = null;
      if (scan.target) {
        status("Mengambil dokumen yang akan ditambah...");
        awal = dariBase64((await panggil({ aksi: "ambilScan", id: scan.target.id })).data);
      }
      const pdf = await susunPdfScan(awal);
      const bytes = await pdf.save();
      const jumlah = pdf.getPageCount();
      status("Mengunggah ke Drive...");
      const nama = $("namaScan").value.trim() || ("Scan " + TGL_FMT.format(new Date()));
      const namaBerkas = (scan.target ? scan.target.nama : nama) + ".pdf";
      const up = scan.target
        ? await panggil({ aksi: "perbaruiScan", id: scan.target.id, halaman: jumlah, data: keBase64Bytes(bytes) })
        : await panggil({ aksi: "simpanScan", nama: nama, halaman: jumlah, data: keBase64Bytes(bytes) });

      const blob = new Blob([bytes], { type: "application/pdf" });
      const urlLokal = URL.createObjectURL(blob);
      const tambah = (teks, href, unduh) => {
        const a = document.createElement("a");
        a.href = href; a.textContent = teks;
        if (unduh) a.download = namaBerkas; else { a.target = "_blank"; a.rel = "noopener"; }
        $("hasilScan").append(a);
      };
      if (typeof up.url === "string" && up.url.startsWith("https://")) tambah("Buka PDF di Drive", up.url, false);
      tambah("Unduh PDF", urlLokal, true);
      buatTombolCetak($("hasilScan"), { url: urlLokal, id: up.id, nama: namaBerkas, status: status });

      status(`Tersimpan: ${jumlah} halaman di Drive dan Sheet.`, "ok");
      scan.halaman = [];
      batalTargetScan(true);
      $("namaScan").value = "";
      muatScan();
    } catch (err) {
      const masalah = err instanceof SyntaxError || (err instanceof TypeError && /fetch|network|load failed/i.test(err.message));
      status("Gagal: " + (masalah ? PESAN_KONEKSI : err.message) + " Tumpukan masih ada, coba lagi.", "gagal");
    } finally {
      scan.sibuk = false;
      tombol.classList.remove("memuat");
      tombol.textContent = "Simpan sebagai PDF";
      gambarTumpukan();
    }
  }

  /* Dokumen tersimpan: buka, tambah halaman, hapus */
  let daftarScan = [];
  let scanDihapus = null;

  function tetapkanTargetScan(e) {
    scan.target = e;
    $("targetScan").hidden = false;
    $("teksTargetScan").textContent = `Menambah halaman ke: ${e.nama} (${e.halaman} halaman)`;
    $("namaScan").value = e.nama;
    $("namaScan").disabled = true;
    gambarTumpukan();
    $("bagianScan").scrollIntoView({ behavior: "smooth", block: "start" });
  }

  function batalTargetScan(diam) {
    scan.target = null;
    $("targetScan").hidden = true;
    $("namaScan").disabled = false;
    if (!diam) $("namaScan").value = "";
    gambarTumpukan();
  }

  function gambarDaftarScan() {
    const ul = $("daftarScan");
    ul.textContent = "";
    pilihGabung = pilihGabung.filter((id) => daftarScan.some((x) => x.id === id));
    perbaruiTombolGabung();
    if (!daftarScan.length) { setStatus("Belum ada dokumen yang disimpan.", "", "statusDaftarScan"); return; }
    setStatus("", "", "statusDaftarScan");
    daftarScan.forEach((e, i) => {
      const li = document.createElement("li");
      li.style.animationDelay = `${Math.min(i, 8) * 50}ms`;
      const nama = document.createElement("div");
      nama.className = "tgl"; nama.textContent = e.nama || "(tanpa nama)";
      const info = document.createElement("div");
      info.className = "lok";
      info.textContent = `${e.halaman} halaman` + (e.waktu ? `, ${new Date(e.waktu).toLocaleString("id-ID")}` : "");
      li.append(nama, info);
      const cek = document.createElement("label");
      cek.className = "cek";
      const kotakCek = document.createElement("input");
      kotakCek.type = "checkbox";
      kotakCek.checked = pilihGabung.indexOf(e.id) >= 0;
      kotakCek.addEventListener("change", () => {
        if (kotakCek.checked) { if (pilihGabung.indexOf(e.id) < 0) pilihGabung.push(e.id); }
        else pilihGabung = pilihGabung.filter((x) => x !== e.id);
        perbaruiTombolGabung();
      });
      cek.append(kotakCek, document.createTextNode(" Pilih untuk digabung"));
      li.append(cek);
      const aksi = document.createElement("div");
      aksi.className = "aksi-data";
      const tombol = (teks, kelas, fn) => {
        const b = document.createElement("button");
        b.type = "button"; b.className = "mini" + (kelas ? " " + kelas : ""); b.textContent = teks;
        b.addEventListener("click", fn);
        aksi.append(b);
      };
      tombol("Buka", "", () => { if (/^https:\/\//.test(e.url)) window.open(e.url, "_blank", "noopener"); });
      tombol("Tambah halaman", "", () => tetapkanTargetScan(e));
      tombol("Cetak", "", () => cetakDokumenScan(e));
      tombol("Ke printer", "", () => kirimPrinterId(e.id, e.nama, (t, j) => setStatus(t, j, "statusDaftarScan")));
      tombol("Hapus", "bahaya", () => {
        scanDihapus = e;
        $("ketScanHapus").textContent = `${e.nama} (${e.halaman} halaman)`;
        setStatus("", "", "statusScanHapus");
        $("dialogScanHapus").showModal();
      });
      li.append(aksi);
      ul.append(li);
    });
  }

  async function muatScan() {
    if (!urlScript()) return;
    const status = (t, j) => setStatus(t, j, "statusDaftarScan");
    status("Memuat dokumen...");
    try {
      const h = await panggil({ aksi: "daftarScan" });
      daftarScan = h.entri;
      gambarDaftarScan();
    } catch (err) {
      $("daftarScan").textContent = "";
      status("Gagal memuat dokumen: " + err.message, "gagal");
    }
  }

  async function yakinHapusScan() {
    const status = (t, j) => setStatus(t, j, "statusScanHapus");
    if (!scanDihapus) return;
    const tombol = $("yakinHapusScan");
    tombol.disabled = true;
    status("Menghapus...");
    try {
      await panggil({ aksi: "hapusScan", id: scanDihapus.id });
      if (scan.target && scan.target.id === scanDihapus.id) batalTargetScan(false);
      $("dialogScanHapus").close();
      scanDihapus = null;
      await muatScan();
      setStatus("Dokumen dihapus dari Sheet dan Drive (PDF masuk sampah Drive).", "ok", "statusDaftarScan");
    } catch (err) {
      status("Gagal: " + err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  /* ---------- Deteksi dokumen dan luruskan perspektif ---------- */

  function ambangOtsu(hist, total) {
    let jumlah = 0;
    for (let i = 0; i < 256; i++) jumlah += i * hist[i];
    let jb = 0, wb = 0, maks = 0, ambang = 128;
    for (let t = 0; t < 256; t++) {
      wb += hist[t];
      if (!wb) continue;
      const wf = total - wb;
      if (!wf) break;
      jb += t * hist[t];
      const mb = jb / wb, mf = (jumlah - jb) / wf;
      const varAntar = wb * wf * (mb - mf) * (mb - mf);
      if (varAntar > maks) { maks = varAntar; ambang = t; }
    }
    return ambang;
  }

  function luasPoligon(q) {
    let a = 0;
    for (let i = 0; i < q.length; i++) { const j = (i + 1) % q.length; a += q[i].x * q[j].y - q[j].x * q[i].y; }
    return Math.abs(a) / 2;
  }

  function cembung(q) {
    let tanda = 0;
    for (let i = 0; i < 4; i++) {
      const a = q[i], b = q[(i + 1) % 4], c = q[(i + 2) % 4];
      const z = (b.x - a.x) * (c.y - b.y) - (b.y - a.y) * (c.x - b.x);
      if (Math.abs(z) < 1e-6) return false;
      const s = z > 0 ? 1 : -1;
      if (tanda && s !== tanda) return false;
      tanda = s;
    }
    return true;
  }

  // Mencari lembaran (kertas) terbesar di gambar. Mengembalikan 4 titik [kiri-atas, kanan-atas, kanan-bawah, kiri-bawah]
  // dalam koordinat kanvas asli, atau null bila tidak yakin.
  function deteksiDokumen(kanvas) {
    const maks = 320;
    const sk = Math.min(1, maks / Math.max(kanvas.width, kanvas.height));
    const w = Math.max(16, Math.round(kanvas.width * sk)), h = Math.max(16, Math.round(kanvas.height * sk));
    const c = document.createElement("canvas");
    c.width = w; c.height = h;
    const g = c.getContext("2d", { willReadFrequently: true });
    g.drawImage(kanvas, 0, 0, w, h);
    const d = g.getImageData(0, 0, w, h).data;
    let gray = new Float32Array(w * h);
    for (let i = 0, j = 0; i < gray.length; i++, j += 4) gray[i] = (d[j] * 299 + d[j + 1] * 587 + d[j + 2] * 114) / 1000;
    gray = kaburSepar(gray, w, h, 2);

    const hist = new Array(256).fill(0);
    for (let i = 0; i < gray.length; i++) hist[Math.max(0, Math.min(255, gray[i] | 0))]++;
    const T = ambangOtsu(hist, w * h);
    const total = w * h;

    // Kertas biasanya berwarna netral (kroma rendah). Berguna bila sebagian kertas gelap oleh bayangan.
    const kroma = new Float32Array(total);
    const histK = new Array(256).fill(0);
    for (let i = 0, j = 0; i < total; i++, j += 4) {
      const mx = Math.max(d[j], d[j + 1], d[j + 2]), mn = Math.min(d[j], d[j + 1], d[j + 2]);
      kroma[i] = mx - mn;
      histK[Math.min(255, kroma[i] | 0)]++;
    }
    const Tk = ambangOtsu(histK, total);

    // Segmentasi kandidat; setiap kandidat dicari komponen terbesar yang bentuknya seperti segi empat
    const kandidat = [
      (i) => gray[i] > T,
      (i) => gray[i] <= T,
      (i) => gray[i] > T * 0.8,
      (i) => gray[i] > T * 0.65,
      (i) => kroma[i] <= Tk && gray[i] > T * 0.45
    ];
    let terbaik = null;
    for (const fungsi of kandidat) {
      const mask = new Uint8Array(total);
      for (let i = 0; i < total; i++) mask[i] = fungsi(i) ? 1 : 0;
      const dilihat = new Uint8Array(total);
      const tumpuk = new Int32Array(total);
      for (let awal = 0; awal < total; awal++) {
        if (!mask[awal] || dilihat[awal]) continue;
        let sp = 0, luas = 0;
        tumpuk[sp++] = awal; dilihat[awal] = 1;
        let x0 = w, x1 = 0, y0 = h, y1 = 0;
        let tl = null, br = null, tr = null, bl = null;
        let sMin = 1e9, sMaks = -1e9, dMin = 1e9, dMaks = -1e9;
        while (sp) {
          const idx = tumpuk[--sp];
          const y = (idx / w) | 0, x = idx - y * w;
          luas++;
          if (x < x0) x0 = x; if (x > x1) x1 = x; if (y < y0) y0 = y; if (y > y1) y1 = y;
          const s = x + y, df = x - y;
          if (s < sMin) { sMin = s; tl = { x, y }; }
          if (s > sMaks) { sMaks = s; br = { x, y }; }
          if (df > dMaks) { dMaks = df; tr = { x, y }; }
          if (df < dMin) { dMin = df; bl = { x, y }; }
          if (x > 0 && mask[idx - 1] && !dilihat[idx - 1]) { dilihat[idx - 1] = 1; tumpuk[sp++] = idx - 1; }
          if (x < w - 1 && mask[idx + 1] && !dilihat[idx + 1]) { dilihat[idx + 1] = 1; tumpuk[sp++] = idx + 1; }
          if (y > 0 && mask[idx - w] && !dilihat[idx - w]) { dilihat[idx - w] = 1; tumpuk[sp++] = idx - w; }
          if (y < h - 1 && mask[idx + w] && !dilihat[idx + w]) { dilihat[idx + w] = 1; tumpuk[sp++] = idx + w; }
        }
        if (luas < total * 0.12) continue;
        // komponen yang menempel ke tiga sisi bingkai atau lebih kemungkinan latar, bukan kertas
        const sisi = (x0 <= 1 ? 1 : 0) + (x1 >= w - 2 ? 1 : 0) + (y0 <= 1 ? 1 : 0) + (y1 >= h - 2 ? 1 : 0);
        if (sisi >= 3) continue;
        const q = [tl, tr, br, bl];
        const luasQ = luasPoligon(q);
        if (luasQ < total * 0.12 || luasQ > total * 0.97) continue;
        if (!cembung(q)) continue;
        const isi = luas / luasQ;
        if (isi < 0.8) continue;                            // bentuknya jauh dari segi empat
        const sisiMin = Math.min(...[0, 1, 2, 3].map((i) => Math.hypot(q[i].x - q[(i + 1) % 4].x, q[i].y - q[(i + 1) % 4].y)));
        if (sisiMin < Math.max(w, h) * 0.1) continue;
        const skor = luasQ * isi * isi;                     // utamakan yang besar dan benar-benar penuh
        if (!terbaik || skor > terbaik.skor) terbaik = { q: q, luas: luasQ, skor: skor };
      }
    }
    if (!terbaik) return null;
    return terbaik.q.map((p) => ({ x: (p.x + 0.5) / sk, y: (p.y + 0.5) / sk }));
  }

  // Koefisien homografi yang memetakan titik dst -> src (masing-masing 4 titik)
  function homografi(dst, src) {
    const A = [], b = [];
    for (let i = 0; i < 4; i++) {
      const x = dst[i].x, y = dst[i].y, u = src[i].x, v = src[i].y;
      A.push([x, y, 1, 0, 0, 0, -x * u, -y * u]); b.push(u);
      A.push([0, 0, 0, x, y, 1, -x * v, -y * v]); b.push(v);
    }
    for (let i = 0; i < 8; i++) {
      let p = i;
      for (let r = i + 1; r < 8; r++) if (Math.abs(A[r][i]) > Math.abs(A[p][i])) p = r;
      [A[i], A[p]] = [A[p], A[i]]; [b[i], b[p]] = [b[p], b[i]];
      const pv = A[i][i] || 1e-12;
      for (let r = i + 1; r < 8; r++) {
        const f = A[r][i] / pv;
        for (let c = i; c < 8; c++) A[r][c] -= f * A[i][c];
        b[r] -= f * b[i];
      }
    }
    const hsl = new Array(8).fill(0);
    for (let i = 7; i >= 0; i--) {
      let s = b[i];
      for (let c = i + 1; c < 8; c++) s -= A[i][c] * hsl[c];
      hsl[i] = s / (A[i][i] || 1e-12);
    }
    return hsl;
  }

  // Memotong dan meluruskan perspektif: mengubah segi empat k menjadi persegi panjang
  function luruskan(sumber, k, sisiMaks) {
    const [tl, tr, br, bl] = k;
    const jarak = (a, b) => Math.hypot(a.x - b.x, a.y - b.y);
    let W = Math.max(jarak(tl, tr), jarak(bl, br)), H = Math.max(jarak(tl, bl), jarak(tr, br));
    const A4 = 1.4142;
    const rasio = Math.max(W, H) / Math.max(1, Math.min(W, H));
    if (Math.abs(rasio - A4) / A4 < 0.1) { if (H >= W) W = H / A4; else H = W / A4; }   // hampir A4: pakai rasio A4 tepat
    const sk = Math.min(1, sisiMaks / Math.max(W, H));
    W = Math.max(8, Math.round(W * sk)); H = Math.max(8, Math.round(H * sk));

    const hsl = homografi([{ x: 0, y: 0 }, { x: W, y: 0 }, { x: W, y: H }, { x: 0, y: H }], [tl, tr, br, bl]);
    const sw = sumber.width, sh = sumber.height;
    const src = sumber.getContext("2d", { willReadFrequently: true }).getImageData(0, 0, sw, sh).data;
    const out = document.createElement("canvas");
    out.width = W; out.height = H;
    const go = out.getContext("2d");
    const img = go.createImageData(W, H);
    const o = img.data;
    for (let y = 0; y < H; y++) {
      for (let x = 0; x < W; x++) {
        const pen = hsl[6] * x + hsl[7] * y + 1;
        let sx = (hsl[0] * x + hsl[1] * y + hsl[2]) / pen;
        let sy = (hsl[3] * x + hsl[4] * y + hsl[5]) / pen;
        sx = Math.min(sw - 1.001, Math.max(0, sx)); sy = Math.min(sh - 1.001, Math.max(0, sy));
        const x0 = sx | 0, y0 = sy | 0, fx = sx - x0, fy = sy - y0;
        const i00 = (y0 * sw + x0) * 4, i10 = i00 + 4, i01 = i00 + sw * 4, i11 = i01 + 4;
        const p = (y * W + x) * 4;
        for (let c = 0; c < 3; c++) {
          const a = src[i00 + c] * (1 - fx) + src[i10 + c] * fx;
          const b = src[i01 + c] * (1 - fx) + src[i11 + c] * fx;
          o[p + c] = a * (1 - fy) + b * fy;
        }
        o[p + 3] = 255;
      }
    }
    go.putImageData(img, 0, 0);
    return out;
  }

  /* ---------- Atur sudut potong (manual) ---------- */

  const potong = { p: null, k: null, skala: 1, seret: -1 };

  function kotakBawaan(w, h) {
    const mx = w * 0.08, my = h * 0.08;
    return [{ x: mx, y: my }, { x: w - mx, y: my }, { x: w - mx, y: h - my }, { x: mx, y: h - my }];
  }

  function gambarPotong() {
    const cv = $("kanvasPotong"), g = cv.getContext("2d");
    g.clearRect(0, 0, cv.width, cv.height);
    g.drawImage(potong.p.orig, 0, 0, cv.width, cv.height);
    const k = potong.k.map((t) => ({ x: t.x * potong.skala, y: t.y * potong.skala }));
    g.fillStyle = "rgba(0, 0, 0, 0.5)";
    g.beginPath();
    g.rect(0, 0, cv.width, cv.height);
    g.moveTo(k[0].x, k[0].y);
    for (let i = 1; i < 4; i++) g.lineTo(k[i].x, k[i].y);
    g.closePath();
    g.fill("evenodd");
    g.strokeStyle = "#38bde0";
    g.lineWidth = 2.5;
    g.beginPath();
    g.moveTo(k[0].x, k[0].y);
    for (let i = 1; i < 4; i++) g.lineTo(k[i].x, k[i].y);
    g.closePath();
    g.stroke();
    k.forEach((t) => {
      g.beginPath();
      g.arc(t.x, t.y, 13, 0, Math.PI * 2);
      g.fillStyle = "rgba(255, 255, 255, 0.9)";
      g.fill();
      g.strokeStyle = "#0a7ea4";
      g.lineWidth = 3;
      g.stroke();
    });
  }

  function bukaPotong(p) {
    potong.p = p;
    potong.k = (p.kotak || deteksiDokumen(p.orig) || kotakBawaan(p.orig.width, p.orig.height)).map((t) => ({ x: t.x, y: t.y }));
    const cv = $("kanvasPotong");
    const lebarMaks = 360, tinggiMaks = 460;
    potong.skala = Math.min(lebarMaks / p.orig.width, tinggiMaks / p.orig.height);
    cv.width = Math.round(p.orig.width * potong.skala);
    cv.height = Math.round(p.orig.height * potong.skala);
    gambarPotong();
    $("dialogPotong").showModal();
  }

  function titikPotong(e) {
    const cv = $("kanvasPotong"), r = cv.getBoundingClientRect();
    return { x: ((e.clientX - r.left) * cv.width) / r.width / potong.skala, y: ((e.clientY - r.top) * cv.height) / r.height / potong.skala, px: cv.width / r.width };
  }

  function mulaiSeretPotong(e) {
    const t = titikPotong(e);
    let terdekat = -1, jarakMin = 34 * t.px / potong.skala;
    potong.k.forEach((k, i) => { const j = Math.hypot(k.x - t.x, k.y - t.y); if (j < jarakMin) { jarakMin = j; terdekat = i; } });
    potong.seret = terdekat;
    if (terdekat >= 0) { $("kanvasPotong").setPointerCapture(e.pointerId); e.preventDefault(); }
  }

  function seretPotong(e) {
    if (potong.seret < 0) return;
    const t = titikPotong(e);
    potong.k[potong.seret] = { x: Math.max(0, Math.min(potong.p.orig.width, t.x)), y: Math.max(0, Math.min(potong.p.orig.height, t.y)) };
    gambarPotong();
    e.preventDefault();
  }

  function terapkanPotong() {
    if (luasPoligon(potong.k) < potong.p.orig.width * potong.p.orig.height * 0.02) { return; }
    potong.p.kotak = potong.k.map((t) => ({ x: t.x, y: t.y }));
    perbaruiThumb(potong.p);
    gambarTumpukan();
    $("dialogPotong").close();
  }

  /* ---------- Deteksi langsung di kamera dan ambil otomatis ---------- */

  const oto = { timer: null, kecil: null, s: { terakhir: null, stabilSejak: 0, siap: true, hilangSejak: 0 } };

  // Keputusan ambil otomatis: dokumen terlihat, diam ~1 detik, lalu ambil.
  function putuskanAmbil(s, q, t, w, h) {
    if (q && luasPoligon(q) < w * h * 0.18) q = null;
    if (!q) {
      if (!s.hilangSejak) s.hilangSejak = t;
      if (t - s.hilangSejak > 700) s.siap = true;
      s.terakhir = null; s.stabilSejak = 0;
      return false;
    }
    s.hilangSejak = 0;
    if (s.terakhir) {
      let geser = 0;
      for (let i = 0; i < 4; i++) geser = Math.max(geser, Math.hypot(q[i].x - s.terakhir[i].x, q[i].y - s.terakhir[i].y));
      geser /= Math.max(w, h);
      if (geser > 0.022) s.stabilSejak = t;
      if (geser > 0.1) s.siap = true;
    } else {
      s.stabilSejak = t;
    }
    s.terakhir = q;
    if (s.siap && t - s.stabilSejak >= 1000) { s.siap = false; return true; }
    return false;
  }

  function gambarLapis(q, w, h, stabil) {
    const v = $("videoScan"), cv = $("lapisScan");
    const r = v.getBoundingClientRect();
    if (cv.width !== Math.round(r.width) || cv.height !== Math.round(r.height)) {
      cv.width = Math.round(r.width); cv.height = Math.round(r.height);
    }
    const g = cv.getContext("2d");
    g.clearRect(0, 0, cv.width, cv.height);
    // object-fit: cover → skala ke sisi terpanjang
    const sk = Math.max(r.width / w, r.height / h);
    const ox = (r.width - w * sk) / 2, oy = (r.height - h * sk) / 2;
    if (!q) return;
    g.beginPath();
    q.forEach((t, i) => {
      const x = ox + t.x * sk, y = oy + t.y * sk;
      if (i) g.lineTo(x, y); else g.moveTo(x, y);
    });
    g.closePath();
    g.fillStyle = stabil ? "rgba(91, 227, 161, 0.2)" : "rgba(255, 193, 94, 0.18)";
    g.fill();
    g.lineWidth = 3;
    g.strokeStyle = stabil ? "#5be3a1" : "#ffc15e";
    g.stroke();
  }

  function langkahDeteksi() {
    const v = $("videoScan");
    if (!v.videoWidth || scan.sibuk || document.hidden) return;
    const sk = 240 / Math.max(v.videoWidth, v.videoHeight);
    const w = Math.round(v.videoWidth * sk), h = Math.round(v.videoHeight * sk);
    if (!oto.kecil) oto.kecil = document.createElement("canvas");
    oto.kecil.width = w; oto.kecil.height = h;
    oto.kecil.getContext("2d", { willReadFrequently: true }).drawImage(v, 0, 0, w, h);
    let q = null;
    try { q = deteksiDokumen(oto.kecil); } catch (e) { q = null; }
    const otomatis = $("autoAmbil").checked;
    const t = Date.now();
    const ambil = otomatis ? putuskanAmbil(oto.s, q, t, w, h) : false;
    const stabil = !!q && !!oto.s.terakhir && t - oto.s.stabilSejak > 400;
    gambarLapis(q, w, h, stabil);

    // Progress bar stabilisasi + bingkai panduan
    const wrap = $("progressStabil");
    const bar = $("progressStabilBar");
    const panduan = $("panduanDok");
    if (panduan) panduan.classList.toggle("stabil", stabil && !!q);
    if (otomatis && q && oto.s.siap && oto.s.stabilSejak) {
      const pct = Math.min(100, Math.round(((t - oto.s.stabilSejak) / 1000) * 100));
      if (wrap) { wrap.hidden = false; wrap.classList.toggle("ok", pct >= 100); }
      if (bar) bar.style.width = pct + "%";
    } else if (wrap) {
      wrap.hidden = true;
      if (bar) bar.style.width = "0%";
    }

    $("petunjukScan").textContent = !q
      ? "Masukkan dokumen ke dalam bingkai"
      : ambil ? "Halaman diambil ✓"
      : otomatis
        ? (oto.s.siap ? "Tahan diam sebentar..." : "Ganti halaman untuk scan berikutnya")
        : "Dokumen terdeteksi — ketuk tombol putih";
    if (ambil) ambilHalamanScan();
  }

  function mulaiDeteksiLangsung() {
    oto.s = { terakhir: null, stabilSejak: 0, siap: true, hilangSejak: 0 };
    clearInterval(oto.timer);
    oto.timer = setInterval(langkahDeteksi, 300);
  }

  function hentikanDeteksiLangsung() {
    clearInterval(oto.timer);
    oto.timer = null;
    const cv = $("lapisScan");
    if (cv) cv.getContext("2d").clearRect(0, 0, cv.width, cv.height);
  }

  /* ---------- Gabungkan dokumen tersimpan ---------- */

  let pilihGabung = [];

  function perbaruiTombolGabung() {
    const t = $("tombolGabung");
    t.disabled = pilihGabung.length < 2;
    t.textContent = `Gabungkan yang dipilih (${pilihGabung.length})`;
    $("aksiGabung").hidden = !daftarScan.length;
  }

  function bukaGabung() {
    const ol = $("urutGabung");
    ol.textContent = "";
    pilihGabung.forEach((id) => {
      const e = daftarScan.find((x) => x.id === id);
      const li = document.createElement("li");
      li.textContent = e ? `${e.nama} (${e.halaman} halaman)` : id;
      ol.append(li);
    });
    $("namaGabung").value = "Gabungan " + TGL_FMT.format(new Date());
    $("hapusAsalGabung").checked = false;
    setStatus("", "", "statusGabung");
    $("dialogGabung").showModal();
  }

  async function jalankanGabung() {
    const status = (t, j) => setStatus(t, j, "statusGabung");
    if (pilihGabung.length < 2) return;
    if (typeof PDFLib === "undefined") { status("Pustaka PDF belum termuat. Muat ulang halaman.", "gagal"); return; }
    const tombol = $("yakinGabung");
    tombol.disabled = true;
    try {
      const { PDFDocument } = PDFLib;
      const hasil = await PDFDocument.create();
      let n = 0;
      for (const id of pilihGabung) {
        n++;
        status(`Mengambil dokumen ${n} dari ${pilihGabung.length}...`);
        const sumber = await PDFDocument.load(dariBase64((await panggil({ aksi: "ambilScan", id })).data));
        const halaman = await hasil.copyPages(sumber, sumber.getPageIndices());
        halaman.forEach((h) => hasil.addPage(h));
      }
      status("Mengunggah hasil gabungan...");
      const bytes = await hasil.save();
      const nama = $("namaGabung").value.trim() || "Gabungan";
      await panggil({ aksi: "simpanScan", nama: nama, halaman: hasil.getPageCount(), data: keBase64Bytes(bytes) });
      if ($("hapusAsalGabung").checked) {
        for (const id of pilihGabung) await panggil({ aksi: "hapusScan", id });
      }
      const jumlah = hasil.getPageCount();
      pilihGabung = [];
      $("dialogGabung").close();
      await muatScan();
      setStatus(`Dokumen digabung: ${jumlah} halaman.`, "ok", "statusDaftarScan");
    } catch (err) {
      status("Gagal: " + err.message, "gagal");
    } finally {
      tombol.disabled = false;
    }
  }

  /* ---------- Cetak dan kirim ke printer ---------- */

  const LAYAR_SENTUH = navigator.maxTouchPoints > 0;

  function cetakLokal(url, status) {
    // Di HP: buka PDF lalu cetak lewat menu Chrome. Di komputer: langsung membuka dialog cetak.
    if (LAYAR_SENTUH) {
      window.open(url, "_blank");
      status("PDF dibuka di tab baru. Untuk mencetak: ketuk menu di Chrome, pilih Bagikan lalu Cetak (atau tombol cetak di penampil PDF).", "");
      return;
    }
    try {
      const f = document.createElement("iframe");
      f.style.cssText = "position:fixed;right:0;bottom:0;width:0;height:0;border:0";
      f.src = url;
      f.onload = () => {
        try { f.contentWindow.focus(); f.contentWindow.print(); } catch (e) { window.open(url, "_blank"); }
        setTimeout(() => f.remove(), 60000);
      };
      document.body.append(f);
    } catch (e) {
      window.open(url, "_blank");
    }
  }

  async function kirimPrinterId(id, nama, status, data) {
    status("Mengirim ke printer...", "");
    try {
      const h = await panggil(id ? { aksi: "kirimPrinter", id } : { aksi: "kirimPrinter", nama: nama, data: data });
      status(`Terkirim ke printer (${h.ke}). Dokumen akan dicetak sebentar lagi.`, "ok");
    } catch (err) {
      status("Gagal kirim ke printer: " + err.message, "gagal");
    }
  }

  async function cetakDokumenScan(e) {
    const status = (t, j) => setStatus(t, j, "statusDaftarScan");
    status("Menyiapkan dokumen...", "");
    try {
      const bytes = dariBase64((await panggil({ aksi: "ambilScan", id: e.id })).data);
      cetakLokal(URL.createObjectURL(new Blob([bytes], { type: "application/pdf" })), status);
    } catch (err) {
      status("Gagal: " + err.message, "gagal");
    }
  }

  // Tombol Cetak dan Kirim ke printer di bawah hasil PDF. o: { url, id, nama, status }
  function buatTombolCetak(wadah, o) {
    const tombol = (teks, fn) => {
      const b = document.createElement("button");
      b.type = "button"; b.className = "mini"; b.textContent = teks;
      b.addEventListener("click", fn);
      wadah.append(b);
    };
    tombol("Cetak", () => cetakLokal(o.url, o.status));
    tombol("Kirim ke printer", () => {
      if (o.id) kirimPrinterId(o.id, o.nama, o.status);
      else o.status("PDF belum tersimpan di Drive, jadi belum bisa dikirim ke printer.", "gagal");
    });
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
  document.addEventListener("keydown", (e) => {
    if (e.key !== "Escape") return;
    if ($("kamera").classList.contains("aktif")) tutupKamera();
    if ($("kameraScan").classList.contains("aktif")) tutupKameraScan();
  });
  window.addEventListener("pagehide", () => { tutupKamera(); tutupKameraScan(); });
  $("tesKoneksi").addEventListener("click", tesKoneksi);
  $("tombolForm").addEventListener("click", () => buatForm());
  $("autoPdf").checked = ambil("autoPdf") !== "0";
  $("autoPdf").addEventListener("change", () => simpan("autoPdf", $("autoPdf").checked ? "1" : "0"));
  $("emailPdf").checked = ambil("emailPdf") !== "0";
  $("emailPdf").addEventListener("change", () => simpan("emailPdf", $("emailPdf").checked ? "1" : "0"));
  $("muatData").addEventListener("click", muatDaftar);
  $("mulaiScan").addEventListener("click", bukaKameraScan);
  $("ranaScan").addEventListener("click", ambilHalamanScan);
  $("selesaiScan").addEventListener("click", tutupKameraScan);
  $("senterScan").addEventListener("click", toggleSenterScan);
  $("galeriScan").addEventListener("change", (e) => dariGaleriScan(e.target.files));
  $("filterScan").addEventListener("change", perbaruiSemuaThumb);
  $("tombolSimpanScan").addEventListener("click", simpanTumpukan);
  $("batalTargetScan").addEventListener("click", () => batalTargetScan(false));
  $("muatScan").addEventListener("click", muatScan);
  $("kanvasPotong").addEventListener("pointerdown", mulaiSeretPotong);
  $("kanvasPotong").addEventListener("pointermove", seretPotong);
  ["pointerup", "pointercancel"].forEach((n) => $("kanvasPotong").addEventListener(n, () => { potong.seret = -1; }));
  $("batalPotong").addEventListener("click", () => $("dialogPotong").close());
  $("terapkanPotong").addEventListener("click", terapkanPotong);
  $("tanpaPotong").addEventListener("click", () => { potong.p.kotak = null; perbaruiThumb(potong.p); gambarTumpukan(); $("dialogPotong").close(); });
  $("deteksiUlangPotong").addEventListener("click", () => {
    const k = deteksiDokumen(potong.p.orig);
    potong.k = (k || kotakBawaan(potong.p.orig.width, potong.p.orig.height)).map((t) => ({ x: t.x, y: t.y }));
    gambarPotong();
  });
  $("tombolGabung").addEventListener("click", bukaGabung);
  $("batalGabung").addEventListener("click", () => $("dialogGabung").close());
  $("yakinGabung").addEventListener("click", jalankanGabung);
  $("batalScanHapus").addEventListener("click", () => $("dialogScanHapus").close());
  $("yakinHapusScan").addEventListener("click", yakinHapusScan);
  $("muatTerakhir").addEventListener("click", muatTerakhir);
  ["edJenis", "edTiket", "edCustomer"].forEach((id) => $(id).addEventListener("input", perbaruiPratinjauEdit));
  $("muatKapasitas").addEventListener("click", () => muatKapasitas(true));
  $("muatAkun").addEventListener("click", muatDaftarAkun);
  $("bulanForm").addEventListener("change", muatDaftar);
  $("batalEdit").addEventListener("click", () => $("dialogEdit").close());
  $("simpanEdit").addEventListener("click", simpanEdit);
  $("batalHapus").addEventListener("click", () => $("dialogHapus").close());
  $("yakinHapus").addEventListener("click", yakinHapus);
  $("tutupFoto").addEventListener("click", () => $("dialogFoto").close());
  $("bulanForm").addEventListener("input", perbaruiPeriode);
  $("simpanPengaturan").addEventListener("click", () => {
    simpan("urlScript", $("urlScript").value.trim());
    const nomor = parseInt($("indeks").value, 10);
    if (!isNaN(nomor) && nomor >= 1) simpan("indeksFoto", String(nomor));
    $("pengaturan").open = false;
    setStatus("Pengaturan tersimpan.", "ok");
  });
  $("urlScript").value = ambil("urlScript") || CONFIG.SCRIPT_URL;
  $("indeks").value = String(ambilIndeks());
  perbaruiHari();
  gambarRiwayat();
  perbaruiKeterangan();
  $("bulanForm").value = bulanFormDefault();
  perbaruiPeriode();

  // Pendengar gerbang: login, daftar, profil, keluar (dipasang selalu; hanya berjalan setelah dipakai)
  $("tabMasuk").addEventListener("click", () => gantiTabAuth(true));
  $("tabDaftar").addEventListener("click", () => gantiTabAuth(false));
  $("formMasuk").addEventListener("submit", prosesMasuk);
  $("formDaftar").addEventListener("submit", prosesDaftar);
  $("simpanUrlGerbang").addEventListener("click", () => {
    simpan("urlScript", $("urlScriptGerbang").value.trim());
    $("urlScript").value = $("urlScriptGerbang").value.trim();
    $("pengaturanGerbang").open = false;
  });
  $("keluarAkun").addEventListener("click", keluarAkun);
  $("ubahProfil").addEventListener("click", bukaDialogProfil);
  $("batalProfil").addEventListener("click", () => $("dialogProfil").close());
  $("simpanProfil").addEventListener("click", simpanProfilBaru);

  // Data yang perlu akun aktif baru dimuat setelah login berhasil (lihat mulaiApp, dipanggil dari tampilkanApp()).
  function mulaiApp() {
    perbaruiJam();
    setInterval(perbaruiJam, 30000);
    muatDaftar();
    muatTerakhir();
    muatScan();
    try { const kk = JSON.parse(ambil("kapasitas") || "null"); if (kk) gambarKapasitas(kk, kk.waktu); } catch (e) { /* abaikan */ }
    muatKapasitas(false);
  }

  mulaiSplash();
</script>
<script>
/* Pembuat PDF Form Tunjangan Kerja + Surat Perintah Lembur (meniru template Word).
 * Dipakai di browser (PDFLib dari cdnjs) dan di Node untuk pengujian. */
async function buatPdfLembur(PDFLib, d, aset) {
  const { PDFDocument, StandardFonts, rgb } = PDFLib;
  const pdf = await PDFDocument.create();
  pdf.setTitle('Form Tunjangan Kerja ' + d.periode.teks);
  pdf.setAuthor(d.profil.nama);

  const F = await pdf.embedFont(StandardFonts.Helvetica);
  const FB = await pdf.embedFont(StandardFonts.HelveticaBold);
  const TB = await pdf.embedFont(StandardFonts.TimesRomanBold);
  const logoBiznet = await pdf.embedJpg(aset.biznet);
  const logo3s = await pdf.embedJpg(aset.s3);

  const PW = 595.28, PH = 841.89;
  const HITAM = rgb(0, 0, 0);
  const BIRU = rgb(0.851, 0.886, 0.953);
  const TEBAL = 0.7;

  const bersih = (t) => String(t == null ? '' : t).replace(/[^\x20-\x7E\xA0-\xFF]/g, '?');

  function bungkus(font, str, size, lebar) {
    const kata = bersih(str).split(/\s+/).filter(Boolean);
    const out = [];
    let cur = '';
    kata.forEach((k) => {
      const uji = cur ? cur + ' ' + k : k;
      if (!cur || font.widthOfTextAtSize(uji, size) <= lebar) cur = uji;
      else { out.push(cur); cur = k; }
    });
    if (cur) out.push(cur);
    return out;
  }

  function pas(font, str, lebar, tinggi, sizeMaks, sizeMin, satu) {
    if (satu) {
      for (let s = sizeMaks; s >= sizeMin - 1e-6; s -= 0.25) {
        if (font.widthOfTextAtSize(bersih(str), s) <= lebar + 0.01) return { size: s, lines: [bersih(str)] };
      }
    }
    for (let s = sizeMaks; s >= sizeMin - 1e-6; s -= 0.25) {
      const lines = bungkus(font, str, s, lebar);
      const lebarMaks = Math.max.apply(null, lines.map((l) => font.widthOfTextAtSize(l, s)).concat([0]));
      if (lines.length * s * 1.12 <= tinggi && lebarMaks <= lebar + 0.01) return { size: s, lines };
    }
    const s = sizeMin;
    const maks = Math.max(1, Math.floor(tinggi / (s * 1.12)));
    return { size: s, lines: bungkus(font, str, s, lebar).slice(0, maks) };
  }

  function halaman() {
    const p = pdf.addPage([PW, PH]);
    const Y = (t) => PH - t;
    const api = {
      p,
      garis(x1, y1, x2, y2, tb) {
        p.drawLine({ start: { x: x1, y: Y(y1) }, end: { x: x2, y: Y(y2) }, thickness: tb || TEBAL, color: HITAM });
      },
      kotak(x, y, w, h, isi) {
        p.drawRectangle({ x: x, y: Y(y + h), width: w, height: h, borderColor: HITAM, borderWidth: TEBAL, color: isi });
      },
      // yBase = garis dasar teks (koordinat dari atas)
      teks(str, x, yBase, size, font, rata, warna) {
        const t = bersih(str);
        const w = font.widthOfTextAtSize(t, size);
        const xx = rata === 'c' ? x - w / 2 : rata === 'r' ? x - w : x;
        p.drawText(t, { x: xx, y: Y(yBase), size: size, font: font, color: warna || HITAM });
        return w;
      },
      // teks di dalam sel, otomatis mengecil/membungkus, rata tengah vertikal
      sel(x, y, w, h, str, opsi) {
        opsi = opsi || {};
        if (!str) return;
        const font = opsi.font || F;
        const pad = opsi.pad === undefined ? 1.5 : opsi.pad;
        const hasil = pas(font, str, w - 4, h - pad, opsi.size || 7, opsi.min || 4, opsi.satu);
        const tinggiBlok = hasil.lines.length * hasil.size * 1.12;
        let yb = y + (h - tinggiBlok) / 2 + hasil.size * 0.9;
        hasil.lines.forEach((l) => {
          const rata = opsi.rata || 'c';
          const xx = rata === 'c' ? x + w / 2 : x + 2;
          api.teks(l, xx, yb, hasil.size, font, rata);
          yb += hasil.size * 1.12;
        });
      },
      logo(x1, y1, x2, y2) {
        // Ukuran dan posisi sama dengan template
        p.drawImage(logo3s, { x: x1, y: Y(y1 + 30.2), width: 35.5, height: 30.2 });
        p.drawImage(logo3s === null ? logoBiznet : logoBiznet, { x: x2, y: Y(y2 + 18.9), width: 63.1, height: 18.9 });
      }
    };
    return api;
  }

  const P = d.profil;
  const hari = d.periode.hari;
  const tglTeks = (t) => t.d + ' ' + d.bulan[t.m - 1] + ' ' + t.y;

  /* ================= Halaman 1: Form Tunjangan Kerja ================= */
  const g = halaman();
  g.logo(425.3, 72.2, 471.1, 78.4);
  g.teks('FORM TUNJANGAN KERJA', 296.2, 72.4, 7.5, F, 'c');

  // Identitas
  const infoBaris = [['Nama Lengkap:', P.nama], ['Posisi :', P.posisi], ['Lokasi :', P.kantor], ['NIK Biznet :', P.nik]];
  infoBaris.forEach((b, i) => {
    const y = 82.0 + i * 13.75;
    g.kotak(51.3, y, 88.45, 13.75);
    g.kotak(139.75, y, 171.95, 13.75);
    g.sel(51.3, y, 88.45, 13.75, b[0], { size: 7 });
    g.sel(139.75, y, 171.95, 13.75, b[1], { size: 7, rata: 'l', font: FB });
  });

  g.teks('Periode : ' + d.periode.teks, 283.3, 148.4, 7, F, 'c');

  // Tabel utama
  const X = [51.3, 73.4, 139.8, 202.35, 269.35, 311.85, 351.25, 401.8, 451.75, 540.0];
  const yA = 153.4, yB = 167.2, yC = 180.9, RH = 13.75;
  const span = (c0, c1, y0, y1, str) => {
    g.kotak(X[c0], y0, X[c1 + 1] - X[c0], y1 - y0, BIRU);
    g.sel(X[c0], y0, X[c1 + 1] - X[c0], y1 - y0, str, { size: 7, satu: true });
  };
  span(0, 0, yA, yC, 'No');
  span(1, 1, yA, yC, 'Tanggal');
  span(2, 2, yA, yC, 'Lokasi');
  span(3, 3, yA, yC, 'Jadwal kerja');
  span(4, 5, yA, yB, 'Jam Lembur');
  span(4, 4, yB, yC, 'Mulai');
  span(5, 5, yB, yC, 'Selesai');
  span(6, 6, yA, yC, 'Paraf Karyawan');
  span(7, 7, yA, yC, 'Paraf User');
  span(8, 8, yA, yC, 'Keterangan Kegiatan Kerja');

  // Baris dibuat lebih tinggi bila keterangan panjang atau ada beberapa kegiatan di tanggal yang sama
  function tinggiUntuk(r) {
    if (!r) return RH;
    const teks = r.keterangan.join(' / ');
    const lebar = X[9] - X[8] - 4;
    for (let h = RH; h <= RH * 3 + 0.01; h += RH / 4) {
      for (let sz = 6.5; sz >= 5.25 - 1e-6; sz -= 0.25) {
        if (bungkus(F, teks, sz, lebar).length * sz * 1.12 <= h - 0.75) return h;
      }
    }
    return RH * 3;
  }
  let tinggi = hari.map((h, i) => tinggiUntuk(d.baris[i]));
  let tambahan = tinggi.reduce((a, h) => a + (h - RH), 0);
  if (tambahan > 60) { tinggi = hari.map(() => RH); tambahan = 0; }

  let yBaris = yC;
  hari.forEach((h, i) => {
    const y = yBaris, rh = tinggi[i];
    for (let c = 0; c < 9; c++) g.kotak(X[c], y, X[c + 1] - X[c], rh);
    const r = d.baris[i];
    g.sel(X[0], y, X[1] - X[0], rh, String(i + 1), { size: 7, satu: true });
    g.sel(X[1], y, X[2] - X[1], rh, tglTeks(h), { size: 7, satu: true });
    if (r) {
      g.sel(X[2], y, X[3] - X[2], rh, r.lokasi, { size: 7, min: 4.5 });
      g.sel(X[3], y, X[4] - X[3], rh, r.jadwal, { size: 7, satu: true });
      g.sel(X[4], y, X[5] - X[4], rh, r.mulai, { size: 7, satu: true });
      g.sel(X[5], y, X[6] - X[5], rh, r.selesai, { size: 7, satu: true });
      g.sel(X[8], y, X[9] - X[8], rh, r.keterangan.join(' / '), { size: 6.5, min: 3.75, rata: 'l', pad: 0.75 });
    }
    yBaris += rh;
  });

  // Catatan
  const T = tambahan;
  g.teks('Keterangan :', 75.0, 629.6 + T, 7, FB, 'l');
  d.catatan.forEach((t, i) => g.teks((i + 1) + '. ' + t, 75.0, 638.4 + T + i * 8.7, 7, F, 'l'));

  // Tanda tangan. Bagian atasan sengaja dikosongkan untuk ditandatangani sendiri.
  const akhir = 'Tanggal: ' + tglTeks(d.periode.akhir);
  g.teks('Karyawan yang membuat absensi,', 193.0, 698.0 + T, 7, F, 'c');
  g.teks('( ' + P.nama + ' )', 193.0, 741.8 + T, 7, FB, 'c');
  g.teks(akhir, 193.0, 752.7 + T, 7, F, 'c');
  g.teks('Mengetahui atasan,', 471.0, 698.0 + T, 7, F, 'c');
  g.teks('( ' + P.atasan + ' )', 471.0, 741.8 + T, 7, FB, 'c');
  g.teks(akhir, 471.0, 752.7 + T, 7, F, 'c');

  /* ================= Halaman berikutnya: Surat Perintah Lembur ================= */
  const CM = 28.3465;
  const fotoW = d.fotoLebarCm * CM, fotoH = d.fotoTinggiCm * CM;
  const judulKata = (s) => String(s).toLowerCase().replace(/(^|\s)\S/g, (c) => c.toUpperCase());

  for (let i = 0; i < hari.length; i++) {
    const r = d.baris[i];
    if (!r) continue;
    const s = halaman();
    s.logo(428.2, 71.0, 473.7, 77.5);

    const bx0 = 31.4, bx1 = 527.7, by0 = 188.8;
    const S = 7; // ukuran huruf isi
    s.teks('Surat Perintah Lembur', 279.5, 205.4, 11.5, TB, 'c');
    const jw = TB.widthOfTextAtSize('Surat Perintah Lembur', 11.5);
    s.garis(279.5 - jw / 2, 207.2, 279.5 + jw / 2, 207.2, 0.8);

    const LX = 33.8, KX = 131.5, VX = 136.4, VR = bx1 - 1.5;
    const garisIsi = (yb) => s.garis(VX, yb + 1.8, VR, yb + 1.8, 0.6);
    const baris = (label, nilai, yb, tebal) => {
      s.teks(label, LX, yb, S, F, 'l');
      s.teks(':', KX, yb, S, F, 'l');
      if (nilai) s.teks(nilai, VX + 3, yb, S, tebal ? FB : F, 'l');
      garisIsi(yb);
    };

    // "Dengan ini menginstruksikan kepada" (dua baris, nilai kosong seperti template)
    s.teks('Dengan ini menginstruksikan', LX, 218.6, S, F, 'l');
    s.teks('kepada', LX, 226.4, S, F, 'l');
    s.teks(':', KX, 226.4, S, F, 'l');
    garisIsi(226.4);
    baris('Nama', P.nama, 237.4, true);
    baris('Jabatan', P.posisi, 247.6);
    baris('Hari / Tanggal', tglTeks(hari[i]), 257.8);
    baris('Waktu', r.mulai + '  s/d  ' + r.selesai, 268.0);

    // Keperluan lembur (bisa lebih dari satu baris)
    let yb = 278.2;
    const ket = r.keterangan.length ? r.keterangan : [''];
    s.teks('Keperluan Lembur', LX, yb, S, F, 'l');
    s.teks(':', KX, yb, S, F, 'l');
    ket.forEach((k, idx) => {
      const hasil = pas(F, k, VR - VX - 6, 9, S, 5);
      s.teks(hasil.lines[0] || '', VX + 3, yb, hasil.size, F, 'l');
      garisIsi(yb);
      if (idx < ket.length - 1) yb += 9;
    });

    yb += 17;
    s.teks('Demikian Surat Perintah Lembur (SPL) ini dibuat untuk dijalankan dengan baik.', LX, yb, S, F, 'l');
    yb += 14;
    s.teks(P.kota + ', ' + tglTeks(hari[i]), LX, yb, S, F, 'l');
    yb += 8.6;
    s.teks('Mengetahui / Menyetujui', LX, yb, S, F, 'l');

    // Ruang tanda tangan atasan (dikosongkan), garis, lalu nama
    yb += 44;
    s.garis(LX - 2, yb, 150, yb, 0.8);
    yb += 8.6;
    s.teks(judulKata(P.atasan), LX, yb, S, F, 'l');

    const by1 = yb + 5;
    s.kotak(bx0, by0, bx1 - bx0, by1 - by0);

    // Keterangan di bawah kotak
    s.teks('Keterangan', 31.8, by1 + 13, 6, F, 'l');
    s.teks(':', KX, by1 + 13, 6, F, 'l');
    s.teks('1. ' + d.catatanSpl, VX, by1 + 13, 6, F, 'l');

    // Foto bukti: lebar x tinggi sesuai pengaturan, tanpa gepeng
    let fx = 31.8, fy = by1 + 30;
    for (let k = 0; k < r.fotos.length; k++) {
      if (k > 0 && k % 3 === 0) { fx = 31.8; fy += fotoH + 10; }
      let img;
      try { img = await pdf.embedJpg(r.fotos[k]); } catch (e) { img = null; }
      if (img) {
        const sk = Math.min(fotoW / img.width, fotoH / img.height);
        const w = img.width * sk, h = img.height * sk;
        s.p.drawImage(img, { x: fx, y: PH - (fy + h), width: w, height: h });
      } else {
        s.teks('[foto tidak dapat dibaca]', fx, fy + 10, 7, F, 'l');
      }
      fx += fotoW + 10;
    }
  }

  return pdf.save();
}

  // Logo dari template Word (dipakai di setiap halaman PDF)
  const ASET_LOGO = {
    biznet: "/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCABpAVEDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD9U6KKKAGAClPTim8EelfKn7Xf7W9v8F9PufDXhiWK88cXUZxgeZFpcR/5aSesn9yPv+Qfehh6mLqezp7mU6ipq8z134u/Hnwb8D9Blv8AxRq4tpdheDTrciW8uP8ArnH/AF+7Xxn43/4KE+OfiFcPpvw+0KDwtZDiTVtST7RcJ/uD/Vp/5Er5Qddd+Kfi+4vdYvp9S1S/k8ye9uP3lfRvwo+AWv8AjiKKx0Cx8rToPv6jcDy7c/QV+k4Th/B4Gl9ZxzPz/NuIKkKn1PLvfqHG6/8AEDxtr0ckeu+M9a1f7RH5ckUl5JHHJHJ/yz8uP93XnV9FHFH5caRxR1+iPhP9hPwrZPFP4i1G+1yVB+8toz9nt5PyzJ/5Ers2/Y5+Ecln9nfwjEY/v5+13HmZ/wB/zK2/1lyzC/u8NSPNw+Q5nif3uMqH5maB8dviD8P5LeTQvF2rWUdv+6jtvtHmW/7v/pnJ+7r76/Zd/bNt/jPZrpniO1h0vxFE3ll4ZMwXDj0/uH2rzb9o79gHSLPw5qviLwBdT2V1aQ+e+i3D+ZFJHHy4jk/1nT/np5lfLHwbtf7G0u51KP8Ad3Nxcfu5f+uf+ZKXsMv4hpOpS0qHpZjj6/D9BTqH7LB8Kp7Gl24z715z8C/Gj+P/AIZ6Jqs7iS7eLZO4/wCeiHYf1FejZ5Ar8uqwdCo6ctz7rDV4YmhCvDqSDpS0UVmdYUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUh6UtITgUAeR/tG/GGL4J/C3UPECRpPqTMLTT7d8eXJcv8A6sOfTq30zX5IalLd+I9YvdS1KeS51G8kkuLi5l/5aSSV9V/t8ePD4t+LNr4cg3/Z9At9kn/XxJ+8/wDRfl1896B4cn13WLLTbSPzbm8uI7eOP/ppJX63w9gKeFwbxNX7Z+a51m3+0eypn0F+yJ+zwfHEv9ranbumkn55nP8Ay8H/AJ5/Sv0K0Lw/YeHdLgsNOto7S1gGEiiTAFYnw08EWvw/8HaZo9qiIIYwGx/E/c11ueDjtX5/m2ZVcwxD/kR9Jk2VU8HT9rNfvJiipCtB6Vg+LPFem+CdAv8AWdYukstOtIzJJNI+ABXjJXdkfQSmqauzjf2gviLp/wAN/hpqt9d/vLi4gks7WAdZZHQ4FfmVZCCwt4oII/Kjj/dx10vxt+OF98ZfGT6pdJ9msov3dnZeZ5nlx/8AxytP9nj4SXfxt8dxWP7yPRbPE+p3P/TP/nn/ANdJP/jlfrmT4SGR4KeJxO7PxTPa1TiHGU8Nh/4Z9xfsoaRPpHwU0Pzyxe733Y8yPYQkkhKcfTFe0beWqlp1jbaVZwWtpEkUEKCOONOir2/lV8nHNflFev8AWK86ndn7Fg8P9Uw9PD/yIcOlLRRWB3hRRRQA0Y9KPwr85v2jf+ClniXwJ8TtZ8L+B9D0ia00e5ks7i+1YST/AGiSP/WeX5cseyvLP+Hq/wAXv+gT4S/8F9x/8kV7NPJsZUp+0S0M+dH62fhR+Ffkn/w9W+L3/QJ8H/8AgvuP/kiul8Mf8FY/GVuIx4h8G6NqX7z95/Zkstt+7/7aeZWn9hY3sHOj9R+KUdK8O/Z4/at8EftF2Ug8PXD2Wr28fm3ejX/7u5iHA34z88fT94OPnT1r25+FrxJ06lKfJUVjQdx6UcV+ZnxP/wCCpPivRviHqOneFPDeiyeHdPv5LYy35le4vI45MeYOY/K8z/rnJX3V8CfivB8cPhR4d8bWtq9jFqkBL20vzGKSOSSOQf8AfcZ/Kuqvgq+Hgp1Opnzo9LopBS1xmgUUUlAC0UUUAFFFFABRRRQAUUUlAC0UUUAIRQBWJ4n8U6T4N0O51nXdRtdJ0q0j8y4vLyXy44x6lzXPfDX4x+CPi3aXFx4Q8Safr0dphbj7HMC9ufSROqfc70vZ/bA7wnFAOa8b/aA+Iep+BtFtodFjMmp3vlxR7F/efvL20s/3cnlyCN997G+fLk/1f3DTPgH8Vr74g2slreRRyzQaZaail4Zi8kkctxeW/wC8/dR/vM2Tyf6uP/W7PLj8utOT3OcD2iiiis7gIORUU3QmnA/LXOePNfbwv4Q1vWEi+0SadYT3Plf39kZfH6VVNXdjGrU9nTcz8rPiHqf/AAlnj/xFrIeOWLUNQuLiOX/pn5ldv+zBoP8Aanxy8Kx+T9ojjn+0Z9PLjrz+O1r3D9kS38j43aUf+ne4/wDRdfu2NX1fK5qn/IfzvhMX9ZzWHP8A8/D9EEHFOxQOgoNfhB/RqEHNfDX/AAUW+JN1Ynw94Ktw0UFwh1S8K/8ALTny44//AEZ+Pl19yjivz0/4KW+FtRTxR4V8TRQebp7WcllLJH/yzkjk8z/2p/5Dkr3sjVN4+n7XY8TOf9zmfJP2+v1u/Z5+Flr8J/hbpmixCOS8dPtF9cJ/y1uH5kP51+NP9qV+rf7IX7Rtj8a/AVvZX+oQJ4u02COO9tiPLln44uBH6Scn5M9fpX2vFXtKlCn7P+GfPcPYenQmfR9LRRX5YfehRRRQAUh6UtIelAH4EfH7/kunxB/7GC9/9KZK+zf2Uf2Avhz8bvgN4Z8Z+IL3xDbapqYuPtEdlexxx5juJI/+eX/TOvjL4/f8l0+IP/YwXv8A6UyV+sv/AATu5/Y98BfXUP8A04XNfe5vXqUMHSVJ2OamcF/w6p+EP/QW8W/+B9v/API9eC/tJ/8ABNpfhp4G1bxb4J8Qz6raaXHJe3mmamn7z7PH+8kkjkj/AOeeP+edfqRxXhf7TX7R3hv4A+ANTvtQ1K0k12e2kTTNJEv7+5l/5Z/uyc+Xn779B+VfOYTMceqiVOo2a8iPxj+GfxG1b4VePNF8WaFPJbajpdxHcR/vP3cn/PSOT/pnJX79eH9WXXdCsNR8vyvtdvHP5fdN4zX8/ngLwVqvxD8ZaN4Y0e1e81DU7uO3RI+g/wCmtf0B6Bpy6Bomn6cj+Ylnbx22/wBkTGf0r1uIvZ89P+fqZ0z4/wDiP/wTE+H/AI58a6j4gstd1Lw3FfyefJptkkckaSfxlN44zX1B8LPhtpPwi8B6P4N0KOePStLj8uJppPMeTLGR3c+ru7k/WvyL/ao/aK+IOsftE+LxH4o1LSLbQNYuNPsLbTbuS3jgjt7jy4/+2n7vzK/UD9mH4lav8Vv2bfCPiq/hSTXriweKTe//AB8TwSSReZ/208vzP+B15eNw+IhQp1KlS6Zoe1fhSYr8PPHP7Qfx90XxbrFnrnjHxfo+pxXD+fYie4txHv6fu/8AlnHWN/w0z8af+iieMP8AwaXFaU8jq1FdVEHOj93Pwo/Cvwfl/ae+M0X+s+JPiyP/ALilxXb/AAM/ag+Mk/xj8FwL418Qa79o1S2t5NNvruS5juI3l2P+7/3OadTIcRTp+1c1YPaI/arqPSg/nXxl/wAFLfjH4h+Gnwj8P6d4b1GbSrrXdSME9/bSbJFhjjLmMH/pplBXyR+yV+2xrvweg8ZJ4o1278QaUNIkudL07UriSTzNQ8yPy4o5P+Wf7uSTzP8ArnXHQynEYig8RTDnR+wY96jEoPcV+GHxU/ao+Kfxi1+TVdR8SanY23mf6Ppuk3Elvb28f/bP/wBqVzPhf47/ABF8Havb6jo3jbXra8g/1Y/tCSSP/v3J+7kr0qfD9V07+0Vw5z9+s+1KcEV8t/sP/tVXX7SPgy+h1uCO38V6GIo78xACO6STPl3A/wCeedkn7uvoPxl4y0jwD4X1HxDrt9Hp2k6fB9ouLmX/AJZx185UoVKdT2U9zQ6HGKh8wH0r8hv2hf8Agop49+J2sXFj4Iv7jwR4UjfEZt/3d7cf9NJJf+Wf/XOP/wAiV4xYp8atU8OS+JLRPH99oUcckv8Aa1t9skt/Lj/1n7z/AFde9DIajp89WooGfOfvNgUcCvxM+Bv7cfxQ+Cl9HHJrVx4p0H/lpourSeZ/37k/1kdfrV8IfjLo3xw+G1n4y8M5ltbhH/0eX5JIJ04eKT3zXDi8tr4P+JsHOfM//BVzWbqw+B/h+zgnaOC/1yOOeMD74SOST+lfNX/BLq6ki/aWuY0keKOTQ7jzIz/y0/eR14l8dvjN8R/iP4r1rT/HGsak4tNRlP8AYlw/lW1pKn7sxxx/8s/LrhPB3jfxD8P9Y/tbw3rV/wCHtR8vy/tOm3HlyeXX12HwE3l/sDLn/eH7+eJvC+n+K7NYb2OcMjCSO4t55Le4jPqkkZDp+GKZ4W8HaX4OsXt9OtmiWeU3E0ks73Es8nH7ySSQl3fjuTX48fAv9pb416r8XvCFnY+NfEPiB7jU4ov7NvbyS4juInk/eeZHJ6R1+1Ofavjcbgp4N+yqM25ySiiivN5UVcZ2FcV8YP8AklXjD/sEXn/ol67XsK5H4n2M+pfDzxJaWqebcz6bcRxxr/G5jIH9K3ofxV6o5cZ/u1T0Z+Y8drXs/wCylF5Xxr0r/rncf+i68qjir179luLyvjNpP/XO4/8ARdfvOb/8iip6H8pZHX/4WaH/AF8PvmikHSlr8BP64G9q83+NvwktPi/4IvNFuX+zzsPMtrkdYJOxr0k9KQgYq6dSdGoqkDmr0IYim6dQ/G34jfBefwf4jvNK1ixfTdQg5Bi/5af9NI64/TtF13wRrFlrPh7UnttRs5PMt7mP93JHX69fFj4L+Hfi9ojWusWwS8jH+j6hCMTwH1Br8/vjH8CfEHwf1PZqMIutJkkdLPUo/wDVyD/pp/zzev1zKs6w2aU/Y4n4z8gzLB5nkdT2uHnz0z6a/Zk/bS0/4pGHw/40SDw54v8ANEVuCfLt7/jH7sn/AJaf9M/9z1r6vxk1+LN3ZF84r7d/ZN/avbxIbPwX4yus61nyLDVLhxm9P/POT/pr05/5af8AXT7/AM1n3Dzwv+0Yb+GfSZFxPDGWoYjSZ9l0UgPApa+FP0QKQ9KWkPSgD8CP2g/+S6/EH/sOXv8A6USVg6T4t8WaXp8cGm61rVtZR/6uOyuJI463vj9/yXT4g/8AYwXv/pTJX6yf8E7gP+GQfAfH/QQ/9OFxX6PjMZ9TwdKfszmp0z8iv+E38df9DD4i/wDAy4rmNSlu7q8knv5J5bmSTzJJLn/WSV/RX5Iz0rjvF/wo8G/EG0ng8SeGNJ1qGcYkF7ZxyOf+B15FLiGFN60l/XyH7M/Mv9gP9oL4T/B+/ubPxVpMmj+JtQHlnxZJJ59uY/3n7rZ1tv8AlmMjzN/WTy6/Vu0uotRtknt3S4t5E3pLG+9Hr8QP2v8A4J2nwE+OWs+GNJEg0GSOO90/zZPMk8uT/ln/AN/PMjr9Cv8AgmX8SdW8a/s/yadqsklyfDuoSabbzyyeZIbfy45I4/8AtmJPL/Css1wkKtNZhT2ZcP5D80P2j/8Ak4f4pf8AY0ap/wClslfrL/wT7/5NA+H3+5ef+ltxX5NftH/8nD/FL/saNU/9LZK/WX/gn3/yaB8Pv9y8/wDS24rqzb/kX4b+ugQ+M+h/LGelc/478caF8NPCuoeJPEl7DpujWEfmXFzL0FaOs61aaBpd3qV/OlrY2sTzz3En3I0Tkk1+PX7av7YE/wC0d4kTSdGSSy8EaRcebaRy/u5LyT/n4k9P+mdfOYDBVMZU5FsDOM/ap/aU1b9pT4l3Opb7u28M2cnl6RpMn/LCP/npJH/z0kr7x/YS/Yrg+Eul2fjvxhb7/G17b77eymi/5BMb9v8Arv8A+iwfLrz/AP4J7fsZRQ29j8U/HOmPJO/7zQNOv0+4na7eP1/55/8Afz/nnj9F+lermWPhCH1PDP8AdocIHwH/AMFcP+RI+H3/AGELj/0XHXxf+yL8FI/j18ddG8OX8ckugReZqOseV/z7x/8AxyTy4/3f/PSvtD/grh/yJHw+/wCwhcf+i468b/4JRHH7Q+vf9ivcf+llnXo4WpUpZO6lPzM/+Xh+oPhjwJ4e8G6WNO0PQ7HSLEDb9nsrdI0/IV+d3/BT34AeH/Bul+GPiB4c0uy0Zri9Olahb2UXl/aJHjkkjk2Dj/lnJ/5Dr9NM5r45/wCCpP8AybRb/wDYwWn/AKBLXzmW4ipTxlN36mk9j42/4Jqazd6Z+1VpMFpNst9Q0+8t7weX/rI/L8z/ANGRx17d/wAFXPizew3fhj4c2NyIrWSL+2NUSP8AjHmeXbiT2/dyV4P/AME5Bn9rTwt/17Xv/pPJXW/8FU/+TktM/wCxatv/AEouK+oqU4VM5gZ/8uy7/wAE1v2dNG+JfinVvHXiS3S/0vQJI7ey02ePzEkvH6ySe8f/ALU/6Z1+qscMUMaRokccaD5Er8Rvgh8Nvjx428MXE/wvl1qTRoLjyp4tJ1iO2jjk/wCufmR16N/wz9+2F/c8Y/8AhSR//JFc2Z4T6xiHKpiEKnM9b/4Kc/s46Npmh2fxP8P2sGm3X2lNP1i2t4/LjuPMP7u4/wCug/1X/bQf8864j/gln8U7/Q/irq3gR5PM0fXLP7ZFHK+fKubfvGP+mkf/AKL/AOmdcL4g/Zc/ar8Wad9h1rRvEur2PmeZ9nvtcjki/wC/f2ivV/2JP2Mvih4B+PWk+L/F2iHw7peiJO+J7iOWWeSW3ki2R+XJ0/efpWtR0KeX1MPUq876B/y8PR/+CsGj2Mfwq8K30drBHeSa2I5Lny/3jx/Z5f8AlpXzb/wTQ0Gx179o2W01Kyg1G3/sO4k8u4jEkf8ArI/WvqD/AIK0f8kb8I/9h8f+k8tfNv8AwS8/5Obk/wCwHef+jI6jCN/2PUYf8vD9W9J8G+HtCn+0aboenadcH5PMtbSOJ/zAroKKK+Kbb3OkKKKKQCDpVe5G+Bx14NWB0qGQZ4prRmNVXi0fmNqOlSaZqV1YyGOWS2kkt5P+2dd18ApWi+MHhnb086XP/furvxy8FT+Hfivrcbpm3vJPtcGO0cn/ANs8yq/wnifR/iH4duk+/wDbI4z/ANtP3dfvNSvTxWU86/59/ofyNQwtTB8Q+zf2Kn6n39H92n0yL/Vin1+Cn9fLZBRRSGgY0HNY/iHw7Y+KNJuNO1G1jvLOdNksUg61rqwbpSg5FNP2eqMalNVVyTPym+N3wvf4TePtR0MSSSWx/wBItJJE++j15cZLjT72O7tJ5La5t5PMjlik8uSOSvuL9vzw5BJa+GNZjSOOcyyWj/JmST+OMfhiT/v5XxLexc9K/dcor/2jl1OdU/nPNqP9lZpUp0z9S/2dfievxi+Fmla5O8B1LBt7+ODkR3CHkfjw/wDwOvVx8uK+KP8AgnDqFy+leOrB5nNjb3NtcRxn/lnJIj+Z/wCi0r7XxxX41muHWExlSlDoz92yXFTxmAp1Kg+kPSlpDXnHuH4EfH7/AJLp8Qf+xgvf/SmSvv79jP8Aa5+Evws/Zu8I+GPFXi+HStd083nn2xs7iQxeZeXEkf8Aq4/7jivIv2nf+CfnxM1P4teI/EXgnTIPEmjaxeSXiRR3kdvcQeZ+8kjcyScjzK8jP/BP74+Dr8Pp/wDwaWf/AMkV+g1Xgsww1OnVq2sYan6U/wDDf/wE/wCig2//AIL7z/41XG+Nv+CmXwa8PWlyNJ1DU/E9yiZjSws3jjc/9dJdlfA4/wCCf3x+P/NPp/8AwaWf/wAkVv6R/wAE2fjjqkEc8+i6Zpn/AEyvdUj8z/yHXmrLsrpu861yeeZ4n8avixqvxw+J+teMtVt47W41CSP/AEaP/V28ccflxx/+Q6/UH/gmd8N9R8Dfs+f2lqUE1lc+IdQl1GO1uI9hEGPLjkx/00CeZ+NcH8Af+CYej+Btc07X/iLrFv4qvLORbmPRbG3JsxIhx+9dx+/H+r+Ty4+hzvr70iiSKPYiCNPSsM1zKnUprDYf+GjSELH4KftH8/tD/FL/ALGjVP8A0tkr9Zv2AP3X7IHgLf8A887z/wBLbivir9or9gL4q638dfE2qeF9Kg1/R9f1STVE1A3KW5t/tEpeSOSOWTJEe88x9f8AyHX318IPgtc/DD9m7TPh1HeL/aMGkzwS3gHyJcz75JCn+x5kj/gBV5liaVXB4elB7bjgfA37ev7Z138SdZ1D4d+Db5R4NtH8vUNRs5B/xM5PTzBx9nj/APIlcb+w/wDCf4f6v4utvGfxL8XeEtJ0LS5PMs9E1fWLeOS8uP8AnpJHJJ/q4/8App/rKoa3/wAE7vjxo9/Ja2/hC31iL/n5sdUt/L/8iSRyVnf8O/fj5/0T1/8AwaWf/wAkV69N4KOD9hQq8jIP1m/4aW+EA/5qh4L/APCgs/8A45VrQvjl8OfFmq2+laJ4/wDC+ratP/qLKx1i3uZZP+2ccnNfkf8A8O/fj/8A9E+k/wDBpZ//ACRXX/Cj/gn98cD8QdEu77Qx4Rt7S7juX1aTULeSS38uT/ln5ckn7yvDqZXg4Qv9ZTNOc+gf+Ct//IkfD/8A7CFx/wCi468c/wCCUn/JxWv/APYr3P8A6WWdfXf7e37PGvftCfC/Srbwp5Fxr+j3n2lLW6n8vz4vLPmR/wC/xHXk/wDwTz/ZK8ffBfx3rvi7xpYpoZl0yTS7fTvtEdw775YpDITG5A/1daU8TSWU1KLeov8Al4foD0NfHf8AwVFP/GNFuP8AqO2n/oElfYnpXg37ZXwR1H49/A/UfDmhi3Otpc295ZG4fy4xJHJ3/wC2byV8/g6kKeIp1J9zQ/Nz/gnD/wAnbeFf+va9/wDSaSvpP/gqf8FdT17RNA+I2mWwuxpEbWGp+UP3kcMh/dSf7gcuP+2lYv7C/wCxZ8Sfhp8ZIPG3jXTY/DdnplvJFb28lxHcSXbyR+WT+7kPl4Ffodq2jWPiXS7rTtSs4L7T7qPyp7a5iEkciH+B0P1r3Mbj1DH/AFmkZwh7lj8gv2D/ANqm0/Z+8Y3uk+JHeLwZrfl/aJUjMn2O4j+5ccf8s8Z8w/8AXOv1n8OfETwr4u0e31bRfEml6nptwN8dzbXcbxyD65r8/P2gP+CXN/a38mq/Cm+jurOT/WaDqs5jdP8ArnJ/y0/7aV8oeI/2SvjL4Uv/ALDffDTxLLceX5n/ABLdPkvY/wDv5b+ZHXVXo4LNH7eFT2bMv4Z+n/7QX7c3w9+Bukz29pqlp4z8VRSeV/Ymm33KYfEhlkAcR7O45fjpW1+yZ+1dp37U+ga1eQaK+gappNxHHc6abj7RiOTPlyeZ5cfXy5BjH/LOvz8+HH/BNb4veML+3OvWNp4M0nzI/MuNRuI7mXy/+mUUf/tTy6/S/wDZ8/Z68Mfs4+DW0Lw4ksrXEn2i+vbh8y3cuOZDXm4yhgMNS9nSqc8zSHP1Pn3/AIKuaNNqHwK8P30f+ostcjEn/bSKSP8ArXxP+wz8XdC+DH7QOnaz4kn+zaVeWcmnve5xHb+Z/wAtJP8Av3X62fG/4QaN8ePhtqvg7XPMitb/AOeO4iP7y3lQ/JInuP61+VHif/gnN8cND1iS0sPDcHiC3j/1d7ZahbxRyfhJJHXp5VicNPB1MJiHYcz9WtC+Ofw38V6vbaVonxB8LavqtwMwWVlrNtcTyf7iJJmvQia/Ib4Kf8E+vjK/xL8N3mu6MnhLTbC9try4vp7uCX/VyeZ+7jik/wBZX67AYFfPY6hQw9T2dKpzlwJN1FGfaivOsMdRRSGmB4N+0j4EOsWVpr8A+ez+SdPWOvBbGw8qSN6+5b6wh1C3kt7hEkt5E2OjjqK+Z/HPgCfwdq8iRxySadJ/qJPSvuclzP8AdPB1D8o4myL/AGj+0KR9IaJfJq2kWl3H9yaNHH4itQ8A15n8FteF54eGnSSh7ix+X6p2r0w9DXx+Ih7Oo4M/R8BX+sYanPyHDpQelAPFLXMegRKfQYppPHPSmyPkfeAFeJfGr9ofS/h5a3Gm6Y8eo6+I/ktozlIfeT/4jrXTQwlTGVFTpq55eOzDD5dQdfETseF/tw+M4tY8YaT4etseVptu9xPKJP8AlpJ0j2fSP/yJXyndxbX57V1/iK/u9X1a8v7+T7Re3EkklxL/AM9JKh8G/DzWfif4nt9D0O1+03E/+sl/5Z28f/PSSv3XB0KeU4L2dV/AfzZicVUzzM51KX22fU3/AAT18NXuneGPE+uzp5Vrql5HBbAdZBF5mZPp+8x9UevsXtXIfDfwJp3w18Gaf4d0tHFpZx+WHkPzv/fc/nXXEnBr8RzLFfXMXUxHc/o/KsJ9SwdOg+g+ikpa889gKKKKAExS0UUAFFFFACYpaKKACiiigBMUtFFABSUtFABRRRQAmKKWigApMUtFABSYpaKACkxS0UAFFFFABRRRQAUUUUAFUNS0u31S0ktLuOO5t5P9ZHJV1+lOovbUTSaszzBfhreeH9V/tHw/cgEjBtrg5H5128V+8Wm/aLyGS2dPvxp+9I/74rSoPSt5VpVvjOKjhoYe/IcHffFzQ7CTY8d1n/rga5DWv2krW0j/ANA0ue4k9J38qvRtZr5M8W/8hW9/6+JK+nynL8NiZWqRPzrPc7x2Dv7KY3x/8dPF3iOCSH7d/ZtuP9ZHp3yf+RK8di0bUtZuPLsLC7vpJJPL/dx+Z+8r0jwT/wAlB0f/AK7/APtOvrbwz/qj/vV9pisVDI4ezw1Nan5RhqNfiPFXxlZnyZ4I/ZL8X+M5IJ9Y8vw5p7nfiT95cbPTZ/8AHK+tvhd8IfDvwn0h7PRLURySY8+7k/eTzn1kOOa7SD/VU+Poa/N80znF47WrLTsfv2ScOYHKqaq0I+93ZZHSlpB0pa8U+sCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAP/2Q==",
    s3: "/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT/2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT/wAARCACoALwDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD9U6hp4wKztX1SDRbC4u7h/Lt4I/MkNMiUuWPNIvVLmvC2/a9+GsUhRtdYFP8AphJ/hR/w198Mv+hgb/vxJ/hXbHAYuX/LqX3Hm/2pg/5z3TNGa8L/AOGvfhh/0MA/78Sf4Uf8Ne/DD/oYB/34k/wq/wCz8X/z6l9wf2pg/wCc90zRmvC/+Gvfhh/0MA/78Sf4Uf8ADXvwx/6GAf8AfiT/AAo/s7F/8+pfcH9qYP8AnPdM0Zrwr/hr34Zf9DCv/fiT/Cj/AIa9+GP/AEMI/wC/En+FH9m43/nzL7if7WwX/Pw9wqavGPDX7Tfw/wDFut2+k6brL3N9cSeXHGIJK9di/ex1xVaVShLlqRsd1DE08RHmpu5aopgIpTWN7bnR6DqhqvLLivN/HX7QXgb4f+ZHqesQfaY/+Xa3/eSVtTpVa2lKNzmqYqjR/iyseoUV8ia/+39odrJs0rw5f33/AE0kfyqwf+HgWoY3/wDCHJ5f/X4K9SOUYx/FFL5nlSzzBr4W38j7Zor4/wBF/wCCgWjyy7NV8OXdr/00t5/Mr2XwL+0j4C8eeXHY6zHHeyf8u1z+7krCrl2Lo/FD7tTopZthK3wy+89horPhu45x+7/eVZiIxmvPa5Xyvc9SM1OPPHVE9FFFIsYMEVjeKNLj1nQ720kk8qO4j8vzK1u4rD8ZadNqnhzUbS1OLme3kjj/ABq4q8rGNZWpu+p8ky/sS+GJbmST/hOf3m//AJ5x/wDxymf8MQeGP+h8/wDIcf8A8crz+X9j34oSXEshMf7yT/n8pI/2Ofih62//AIGV9/CK5b/XbfM/MJxkp8v1Z/eeg/8ADD/hf/oev/Icf/xyj/hh/wAL/wDQ9f8AkOP/AOOV5/8A8McfFD/ph/4GUf8ADHHxQ/6Yf+BlX/3O/iLkl/0DP7zv/wDhhvwv/wBDz/5Dj/8AjlL/AMMP+F/+h6/8hx//AByvP/8Ahjj4of8ATD/wMqP/AIY4+KP/AEw/8DKP+50Vnt9Wkei/8MP+F/8Aoff/ACHH/wDHKfH+wl4evo5PJ8ZSXPl/88reP/45Xj/iz9mP4h+DtBvdY1Joo7Ozj8yQfaK9U/YOne4n8TmSSSX93/y0rKvKtTo+2pYlyRtQjRqV/YVaPL53/wCAeSfBjRo/Dn7R+laTHJ5sdnqHl+Z/z0r9NrdMoDX5v+Af+Tr7b/sMSV+kS/6ofSvHz981WL7o97h1WhJdgc5rl/GPjjSvBGi3Oq6tfR2ttGOslaut6vb6Lp099dOkVtBHvkkkr89PiR43139pv4oR6Fovmf2dHJ5dvH/yz8v/AJ6V5eX4T6y+ao7QXU9bMsb9VXJTV59ja+I/7SPjf42a3/wj3giC4sbKT93/AKN/x83H/wAbq/oP7Keh+GLD+2Pid4mSz/5aSWccvzj/ALada6jxR4t8Ofsl+FU0Lw/BHfeLriP9/cSV5v4O+C/jf9oG9fxR4s1KSx0U/vPtNz/zz/6Zx19SoxhH2tP3Kb2e7fy6HxUpyqS9lUfPUXxLZL59TqZfjF8DPh+fI0Lwd/bc8f8Ay8SRf/HKj/4bF8N/cj+GFr9m/wC2f/xurV1dfAP4Q/6J9kk8XajH/rP+WlVf+Go/hv8A6iP4aQ/Zv+ucVXClGe1KcvV2/UU5uEeZ1Ir01CP45fBPx5J9n8QeBv7I8z/l5ji/1f8A20jpNU/Zc8JfEGzk1X4Y+Jo5Jf8AWfYriXIqzD4i+AXxUPkXmlv4XvJP+WmPKNc142/Z+8UfCCWPxP4E1aTU9Kj/AHkclt/rI6S5IvljJwn2eq+8EpVI+0aU4+Wj+4PB3xz+Iv7POuR6F4ot7u/02P8Ad+Xc/wDtOSvtj4d/ErRviPoVvquj3UcttJ/yz/5aJXy94A+JXh79pTQ5fCHjK3gtvEUcf+j3n/PSvM9E1nxD+yZ8V/sl2ZJNJlk/eR/8s7iP/npXFicJDERlHl5aq/E9HBY+eElFyfNTf4H6RRy5qaue8MeIrTxVo9lqVjIkttcR+ZHIK2T1r4+UXCXLI+9jUjOCnHZju4rA8bXV1YeGNSns95uY7eSSOulqrcxebRF8suYqpHnjyn5wy/Hf41GeTZdaljzP+fOov+F7/G3/AJ+tS/8AAOv0a/sy3/54R/8Afuj+zLf/AJ4R/wDfuvo45tQjHl+rxPkJZHVlLm9tL7z85v8AhfHxt/5+9S/8A6P+F8fG7/n71L/wDr9FfsFvj/UR/wDfusPxjr2leC/D95qupeRb2VvH5hJrSGZ0KkuSOHXN2MamTzpR9pKvLl73Pz51P9pX4t6N5f2/Wbu28z/nrb+XXp37PPjz4sfF7xXH5/iGePQbf95eSeXH/wB+68t1/VNd/af+LEVvYJ5dtJJ+7j/5Z28dfRvxI8b6F+yt8Mbfw3oWyTXriP8Ad/8APT/rpJXu41UHThQpUoqpLdW2PBwcqqlPEVK0nTWz7mL+2B8d4NL0+TwTpT/ab64j/wBMk/55x0fskeEZvht4I1rxX4hk+w2V3HmPzP8AnnXmX7OHwRu/iz4kl8WeJPMl0q3k8ySSX/l4kq7+1D8bX8ZapH4J8L/8gq3k8uT7N/y0krl9lHl+pUdl8Uu3yNXXlf63WWr+GPf5nMfCK/j8R/tP2V/YJJJbSahJJ/2zr9J4pf3VfO/7LXwEj+GmgR6rqUIk168Tef8ApnH6V9ER18/m2JhiK0VD7J9XkeGqUaEp1Fa581fttfEWTwv8P4tJtJPLudTk8r/tnXnv7P2mWvwc+C+qfEC+jj/tG8jzB5lYf7dN+998TNFsP+WcdvW9+1Dc/wDCOfADwZo0H7qO48sSf9+693D0lHDUaK2qbnzuNqueLrVHvD8Tz74BfDuf4+fEfUfEviR5JdKs5PtFx5n/AC0k/wCedaXxw+MmrfFDxZH4B8ECSLRY5PsccVt/y8f/AGuu3+HG/wCH/wCx1rGs2n7u9vI5D5n/AF0k8usr9hLwbBf6xr3iS7j8y4t/Lt7et6lWnzVcU17tPSPZfI4qNKTVPCrSVT4u7+Z3vwm/Yl0HRbOO88W/8TfUX/5dv+WcdezR/AbwHDafZ/8AhGNP8v8A65138dSV8fWx+Jrv3qj+TP0Gjl2GoR5Y04/NHzF8UP2KvC/iS0kn8Oj+w9R/g8r/AFb14P8AC/4n+IfgF44k8J+KPMl0aSTy5I5f/RkdfohIg/jTNfJP7cHw5k1nS9O13TbCS51GOTy5PKj8yTy69fL8fKt/s1d+5+P3nz+aZXGh/tmGjaXbp9x5b+0n8NE+H3iDTvG3heTytPu5PtEflf8ALOSu/wDiRa2n7QH7O9t4rjjQ6zpMeZPb/npV+y0bU/G/7JUlpqVhcf2jp8X7uOWP95+7qj+x3pep/wDCIeLtD1XTbi2tpD+7+0x+X/yzr0vaP2aq396D+9f8MeP7H33Ts+WX4Gn+w18RZL/QNR8MXcnmy6fJ5lv/ANc6+tBLkV8C/sq6BrvhP45yx3Gm3lrZSRyR+bJb/u6++K+ezynD6xek9GfT5M6n1VQqbovUUUV459KNwKjqaopOtAtShfXcdhbyTzv5caV+fn7Snxov/jT4wj8L+HvMl0q3k8uOOP8A5eJK+gf21vFupeGPhfFBps/2Y39x9mkkj/55151+yJ8KtN0bwvJ8QNRR765PmfZ7aOPzPLr6jLaVPC4f67UV5HxGaYipicT9Sp6ROm8HeHdD/ZN+FMms6r5dz4hu4+Y/+ekn/POvnvwB4N8Q/tSfFC41K+nk+zeZ5l5c/wDLOOP/AJ51F+0D4i8Z/ETxPJqWq6Dq1jpMcnl2cdzbyRxxx10/7Pv7T9j8KtHj0LUtCj+xeZ+8vbb/AFn/AG0r6GGHqvDzxELSrS89j52VWnHExo1Fy0V+J6T+0n8XtO+FPhS3+H3hA/Zrjy/LcRf8so6yv2RP2fpL6ePxp4ht8/8APnFJ/wCjK5r4sfAW1+INpeeOfAGqvr8Fz/pE9lJJ+8T6Vp/s0ftNXfhO/t/Cfix5PsfmeXb3Mn/Lv/0zkrklCX1FxwetR/FfdnVTq06mN5q38NfD5H3Nbjy4qsgYFVra5jlgSSP95Gas58we1fn7uump+mRfNT02Pg39u7THsfHmg6mI/wB3Jb/62t39oqH/AITH9nTwrrsH72O08syV6l+2N8NX8b/DiS7tI/NvdM/0iOvH/wBmTxbYfET4f6r8NNak/wBIEf7jzPSvu8PU58HRrR1dPdH53jaTp4ytCeiqdexpfBnPxK/ZS13w3B/x+WYkj8v/AMiVzH7Dfju38L+LNV8MX7/Zzfn915v/AD0j/wCWdcj8N/FupfswfF+903WYJP7Okk+z3Ef/AEz/AOWckddv8c/gTJqtzH8Rfhu/223uP9Ikisf9Ykn/AD0jredOnHno1HanU2a1+/scVGrL93Wp61IdHofdcUtSV8O/C/8AbefQbePTfG9hJcyW/wC7+223+s/7aR17JbftpfDKSP59Vntv+utvJXyk8sxMfhg38j7ennOElG85pP1PfutUr2LzvkevL9F/aa+G+vv5UHiizik/6eD5X/oyvRtO1mw1m38+xu4LmP8A56RyeZXn1MPXo62aO6OKoYmPLCSfroOjtY/9X5f7upIrSOL/AFcdXUOBTxyKx/m956nXye7GVloU4tPjhk/dx1d8upqKrmk/idyowjH4VYKKKKRYVFJ1qWopOtAHyr+3sP8Ai3ml/wDX5Xzx8OP2rfE/w18M22h6bYWFzZ243x/aY5PMr9GdY8M6br8Qj1Kxgvo0/guI/MrMPwu8Lnp4b0z/AMA4/wDCvo8HmVGjh/YVqfMvU+NxuU1qmI9vQnb5HxhpH7eGsLceXrHhzTr23/5afZpikn611/8Awjvwi/acspTpCx+G/FI/gMflSiT3j/5aV7z4v/Z58B+LrOSG68OWcbyf8tbeMRyJXxl8b/2eda+BGqReIdCu7i50aOTzI7iP/WW9eph62CxUuTDt05+tzxsVhcXhNcQueHe1jEil8ZfssePtk++O2/55/wDLteR13Hxv8C6T8SvCNv8AEvwikcUv/L/bx/wSV3PhvWLD9q34QXumar5Y8VaXH5kcn/tSvMv2XvFr+EvHd74J1r/kHan5lvJFL/z0rv5pT9pOWlSHRdUebOEVKnD/AJdy69j2v9jL43SeLdEk8L6tPnUdP/1cn/PSOvqqP/V1+Zf7/wCAn7Q8fl/u7a3vP/JeSv0m025jutPinj/1bx+ZXzOb4aNOpGrS0Uj7LIMVOtSlRqvVEl9aR3dvJHInmRvXwB8ffg5rPwO8bx+M/C++PTvtHmRyRf8ALvJ/00r9Caydb0Kz1/T7ixvoEurW4GySOTvXDgsbPCS7rsd+ZYL61HR2fc+R4NV8G/tbeFIrHUnj0TxtZx/JJ6f/AGuvLYLz4pfstau8EtvJLosknEf+ss3/AMK774xfscatoOoSa78Pp5JDH+8+w+Z5ckf/AFzrmPDn7VHjDwTEdC8e6Gdas0/dyJeR+XLX1tOMakX9SalGW6f6dj4qrF0Zf7bFxfdG8/xx+DnxSh3+NvC50jUX/wBZcomf/IkdV/8AhEv2Zpfn/wCEkvo/+mfmSf8AxurH9vfs4/EEGS+sZ/C19J/rPL8yL/0X+7pn/Cqv2d5f9X43uIvM/wCnj/7XTShTVp+1j6amUoS5uZKmxg/Z6+EXjYf8Ur8QY47n/lnHcSRyf/G657Vvgn8V/gdcHUvDepXGp2Uf7zzNOk/9GR1vXP7JHhvxPBLP4C8ewX0n/PvcyRy/+RI65mx8cfFf9mrVI7TWUnvtJ/553P7y3k/65yU4yqVPdjPmfZqxNZU/iqxaXdM9V+Dv7bMdzcRaN45g+wXn+r/tGPp/20r6203U4NVt47iCeO5t5Pnjkjr431rwT4O/ai8Mya54Y8vSfFsEfmT2/wDf+tct+zx8ctV+EHi3/hDPFjyRaV5nl/vf+XeT/wCN15OKy+GJhOVGPLNfZ7nu4LNKmH5I1pXi+vY/QGPrUtULK7juoo5I5PMjkq2cNzmvlWnHSR9ynzLmiPzRVcsqbeelMNxGQeetKzHdaeZbpaqG4jJH7yntcR45NPlfYXNHuTAjPShiKi+0p61NxipdmPVFWeES4rD8ZeFrTxdoF/pV8nmW13H5ZFdDVe4ljp05qlPnjpIxxFP2tN056xPzg+CF9d/Cv9oc6Lv/AHf2ySyk/wCmkdWP2iNMPgX9oWHULX90ks8d6aqalL/b37WEklh/0GK6L9tKWO6+L+mwR/6yO3jjr9LS9pi4PZuN2fk7d6M10UrIk/bS0uL+2PDPiCP/AJf7PFfYPwF1g678JvDF2/32s4818nfthhIfCPgGCT/WJaf0FfTH7LsL2vwR8MJJ1+zV4OY65fTk9/8Ahz3sqvHMKkY7HsPGKi8uoWnjIAzUn2hAOtfJWfRH3/NG12xskbkVzfir4d6B4wt/I1rSrS+j/wCmkddJ9pj/AOelO8+M/wAYqlKdN80bownGnVXK7M+ftd/Yl+HurPvggu9NP/TtPiuXuf2BPCx/1es6hF+CV9V0snWvUhm2Np/DVfzPNlk2Be1NI+BvH37HXiv4cn+2fCGtSXv2f955cf7u4rV+EPx7g8dmTwN8SLeO5Mn+jx3FzH1k/wCmlfbUkPm/8s6+H/22PhfB4X1jTvGGkx/ZvtEnl3Hlf89P+elexgsYsdKNGvpJ/aX+R85mWXywMZVqDvFfZf8AmcL468O6z+y78TrfUtJnkOmySeZAP+ekf/POvQP2kvCdj8SvhzpfxL0aP/SBH/pflelaXjXy/iz+yrZ67OnmajpnPmVH+yRdJ4x+D/i/wpdfvYo0k2f9tI69J1JQSxC+KEuV+Z4/s1Uk6L2lHmXkei/sdfFGTxt4AGm3cnm6hpH7r/rpHX0Vur8/P2LdUk0H4x6lpP8AyzuI5I/+/dfoD5tfMZvQVLENR6n2mR4qVTD2l0Mbxsl3L4U1NNPkeK8NvJ5Ukf8AfxXxt+zP8bvFGp/FC58PeJdZnvo5I5I4/M/5ZyV9x3UCyQqma/OT4++F7v4L/G+PWrGN47a4uPtlvXXk0KOJVahUWr2ZyZ3KvQlGvB2ijotX+NPjP4a/HeTTdW1qeXRI7z/Vy/8APOuw/av8ZeN/Buqad4h8Pa1dx6BqEf8Ayz/1cclZv7Q3hKD4x+ANJ+Inh795cRR/6XHFVb4D/FTQ/ih4Jk+GfjaRPM/1dpcSd69v6vB06eLULqGkl1+4+ceLqRlUw0p+9P4X0+8+hv2ePjbY/FnwjbSSXEf9swR+XeRV7DHLX5seOfhP46/Z68Uf2tosk8tlH/q9Stv+ef8A00rvPCn7ees6bbpb61oUF9In/LSOTy5K83E5O8TP2mBaafRux7OEz2GHp8mOTT8tT7rkrx79ob40WHwp8I3MjTCTVLiPy7S2Hc187eKP29NavraSDRdCgsZJP+WssnmVwXg/4V+Pv2ivE/8Aa2tSXEVl/wAtNRvf9X5f/TOpwuSyw8/aY5qK8ncrG519ap+zwKv66HR/sh+DZ9e8cXvjPVv+PLT/ADJPNk/5aSVzurXT/HL9pP8AcfvbaS88uP8A65x16J8dPiVo3wq8Ep8NvBMn+keX5d3cxjp/9so/Z08GwfCXwJqPxF8Qx+VJ9n/0OOSvek5w5sY42UlyxXV/I+ZVNSlHDJ+9GXNJ9F8zk/2w9dTXviVp2hWv72Owt47f/tpX3F8LdGHh34eaFpv/AD72cYr4J+B/hy7+N3x3/ta7jklto7j7bcS/+06/R22j8q3x6V8/nMo0oUsLfVbn0mRRlUqVMTb3ejPjj9r34meLPh98QNKj0nVp7HTbi3/1cVbX7RfxB8SaN8H/AApruhalPay3Hl/aJIv+udXf26fAb694Pstdt4/Mk0+T95/1zrl/hVdQfHf9na98ISSRy6zpkeI//adbYenSlQoV1G6W5x4urXp4mvRctXsdH4T+IXiHxj+yhqOrWmpSSeI7SOT/AEn/AJafu5Kr/sY/GPVvHF5rWk+IdWkvr2Py7i38z/nnXlH7LfxFj+HXjDVfBHiT/RtPv5Ps483/AJZyVT+KPw+8Q/s3fEyPxR4e8yTRZJPMt5Y/9X/1zkrpnhKS9rh5L3p/D2+856ONrKNPEp3jD4l1+4/RWOWpK8F+Ev7V/hTx3aRx313HpGq/8tLW5kr2D/hKNJNt5/8AaVp5X/PT7RXyFbDVaDtOL+Wp95Qx1HEx5oSXz0Np+tfJP7eXiO0h8JaTpG+OS8nuPMr034pftP8Ag34fWMn+nx6lqH8FtbfvDXyV4b0LxJ+1T8T/AO1r+OSLSY5P3kv/ACzjj/5517eVYSVGaxWJVor7/uPnc2xsa0JYXD6yf3feeneF/wDikv2NdRe7/dG7ik8uqH7Dsf2Hw/4y1WT/AI90T/69YX7VPxFtLo6V8O/Db+Zb2nlxyeV/z0rrtRjj/Z7/AGZpbB5PL13Wo/8AV+8lezKDnRVO3vTle3b+keDFxjVdS/uxja/c84/ZQi/tT9oeW7j/ANXH9okr9Eh0r41/YO8CSRQar4nnTmX/AEe3k9q+y6+fzyrF4m0dbH0+QUpLD3loJKvQV5D+0P8AB23+LPg2W3jT/iY2/wC8t5a9hqOSL93XkUa08PUjUpu1j3sVh44qk6M9j83fgf8AF6/+CXiy98NeJIJP7Gkk8u8tpf8AlnXX/Gf9mo38X/CZ/Dd/7S064/0j7Nbf6yP/AK517p+0D+zJp3xVtpNS07Fjr8Y+SUf8tP8ArpXyV4b8efEX9mXX/wCzZ4J4rb/lpZXsfmRyf9c6++o4mGOl9awztUfxRezPzPE4d4H/AGbEp+zXwyS1R0Pw4/a18R+CYP7G8UWH9t6fH+72XH+tjrvpfir+z54yzPrXh4WNzJ/rP9D/APjdPj+MfwY+NEOzxdo0eiap/wA/Bj/9qR0wfst/CXxGPP0bx75UftcRyVlV+rXftacqb8tS6brtfuZRn66Cf8LV/Z98Hf6Xo3h4XtxH9z/Q/wD45XDfEX9rXxJ40gOjeF7E6LZy/u447c/6TJXc/wDDLnwl8OxefrPxANxH73kcdPHxe+DHwXgH/CIaUNb1T+C4A/8Aasn/ALToh9XbXsYSqPz0Iqe1X8aSh6anP/B39mqS1j/4S/4kv/ZunW/+kfZrmT95J/10rlPjh8Xr/wCNPiSy8L+GreT+xbeTy7e2i/5aVleKPiN8Qv2mvEEem2kEklt5n7uysv8AVx/9dK+tP2dv2YLD4U2qanqWy+16Qf6wf6uOta+Jjg/9pxLvUXwxWyNMNh6uO/2bDK1N/FJ7s3/2dPgvb/CXwXHbyRxyarcfvLiWvYoiPLIxTYoqkr4HEVpYmpKrPdn6PhsPHC0Y0aey/EwPFGhW3ijRLzTLuPzLe5j8t6/PfUrXxB+yl8X/AD4I5JdNkk/d/wDPO4jr9JvL4zXBfFH4S6F8VdAk03VYM5/1dxH/AKyOSvSy7GRwzlTq6wfTseVmWAlioRq09Jr8T5k+Kvwm0n9oLQI/HXw9eP8AtXy/MuLL/np/9srk/h7+0pd+E4H8GfEnSpNR06L/AEeT7RH+8g/+OVla34E+Iv7K3iT+1tJeS60X/n5j/eRyR/8ATSu1g+M/wr+ONpHa+P8ARhoms4/5CCcY/wC2tfUOTdLkiuemvhfVf5nxkkoVvaS9yo/iXR/5BcfAD4V/FNhdeCvFiaTcSf8ALo0vH5VW/wCGJPFH+rj8ZWn2f/tpSS/sf6F4iIuvBPj20uY/+Wcckkco/wDIdVf+GMviB5fl/wDCWWP2f/rvLU068afw1resbjdLnjZwv6SsaVt+zX8O/h1/p3jvxjBeyR/8uUcvl/8A2ysrx3+0zbx6aPCnwv0n7DZv+7+0xR/vJP8ArnVy2/Y0sNH/ANL8ZeObS3j/AOmX/wAckq4vxQ+D/wACIJE8I2I8R67H+7+2vz/5Epc6qS9or1Jell92xGtOPs5rkj63f3jPg78GLT4aWcnxB+JE/wBmlj/0i3trn/WCT/45Xn+v6x4g/at+LdtYWEckWmxyeXH/AM87eP8A56VdttL+JP7WOvxzz+ZbaJHJ/rP9Xbx19n/B34L6H8JfD8djpsfm3En+vuZP9ZJWFbFwwkZVZSvUey7HZgsFUx3LGnG1Nbt9TpPAng2w8B+GLLRrBPLtrOPyxXUeVUUcVSV8TNyqS5pM/RKVONKPLEmpr9KdULypig1IniyOtc54t8AaJ470+Sw17TrfUrc9pY66j7UlR/ao6qE5wfMnZ+RnUhGpHkkk15o+TPG37AWjapI8/h7WbjSM/wDLtc/6RHXl2pfsF+OrSX/RNS0m5j/56eZJHX6CebHUfmxy17VPOsZT+0n6o+dr8PYOvtdejPz/ANN/YP8AHd1cf6XqWk2P/bSSSvUfBX7AWh6fJHP4k1yfV5P+fe3Tyoq+r/Nj9qsRypL0oq51jKn2kvRFYfIMFQ3TfqzmPCXw60HwHp8dhoOm2+m247RR10Kxgd8VP5sdHmx14s5zm+aTu/M96FGnTjyRVl5Egpah+0x/3xS+bHUmw481XEdTebHUX2qOlZNWY7tbFTUNPi1C3eG4RJI5PvxyV4b4+/Y18DeMGluLSCTQLxx/rdO4j/799K99+1R/89Kk82umliK1HSErLsefXwVDEe9OOvc+GdW/YH8UaZJ5mheK7SSP/prHJbyf+Q6yv+GR/i//AKv/AISFPL/7CElfe8vl1H+7r1IZviI9vuPKqZDhpfC2j4b0/wDYP8V6vOZdd8T2sYH/ADz8yeT9a9j8AfsT+CPCTxXF+LjxBcJ/z/f6v/v3X0NFLHSfao6xrZnia3xO3pob0cmw1Lpf1KGmaPbaXbpBaQx29vH9yOKPZitDZhR82KT7VHUn2mOvJbctZu7PajBRjyJaeRKOlLUIljkqagshrwr9ou51aGTQf3+rWvhiST/iaXOif8fP/TOvdpOteafFHwx4vvL/AE7VvCWpwR3NnxJpt7/x7zx0AeLxeI5NG+HXiu48L+N7vW9Oj+z/AGeK9k/02z/eV0cf9p/F/wAUataXWu3+h+GPD9vHHcRabJ5clxceX5kn7z/nnSXHwN8V+LbfxPqOsyaTY6rq8cdvHbWX+rj8uSt/V/hf4r8KeID4g8GXdjLc3ltHHqmnaj/q7iSP/lpQBwekeO49H0Lx5o2h+Pn8QWcWlyXOn/aZP9Nt/wDtp/y0qP4XfF7WbD9njVU1a+kufFmn/wChRyyf6ySST/Vyf+RK2v8AhQfjPXvFmreIdav9MiudQ0O40qOyso/3dv5lWI/2adS/4TjwpqX9pQRaTZ2dvHqll/z8XFv/AKuSgDG8CfEbXfC/7K9zqWralJqfif7RJp1vc3Mn+suJJPLjrt/2aPE2qppeteD/ABFqT6xr3hu88uS+l/5eLeT95HJWLF+zddazaeHNG12e3uvDthqF5qF5bRyf8fEkn+rrqfDXwMt/h/8AFaPxD4XSGx0W70+S01S2eTmSQH93JQBzX7Qd1qEXjLRU1a+13TfBH2eT7Rc6BxJ9o/6af9M6wrHxlq1h4OttJ8N+MP7cj1jVPsWn6lc/vLizj/6aV6j8Q/DnjqPxRb654Tv7S5i+z/Z7jSdR/wBVJ/00rjNN/Z51rVNM1bUtSv7PTPE95eR3tv8A2bH/AKPbyR0AVvG3gTV/g3oH/CX6L4r1rU7jT5I5NQttWuPtEd5H/wAtP+uddZ8JvFN94j+JHj1Li4kkso/sclvbS/8ALPzI6xL74e/Ej4jG20fxhdaRY6FHJHJeHTfM8288upJvh/8AETwn8Q/Ees+FP7Bm03Vfs4jivnkSSPy46AN/wLrN/dfGTx7YXF3JLY2cdv8AZ4v+edeS+KPFHiy/0/xPHBf6nLp1v4k+z3kum/vLm3s/+mdd5c+A/iNoPiSTxRoUmiy6jqlvHHqljc+Z5fmR/wDLSOksvg74v0Xw39v03XYIvFcmoSajcR/8u1x5n/LOgDjPC+s2ljofjifwn47v9T0630O4k/s3V5PMvbO48uT95XuPw7v7/VPhHoN95n2rUrjS45PMk/5aSeXXmv8AwqDxf4x1fWte8Q/2Tpt7caHcaNZ22m/9NP8AlpJJXrPhLwrPo3w40nw7PceXdW+nx2ck8f8Az08vBoA+YPDeqSebZvrXjfXvD3xA+2f6RbatJ5enSfvP9XH/AMs6l1vxRpt18WPGlp4l8YeKdM+x3EcdvbaJJ+78vy/+uddvqfwy+Jfifw/F4P1q70K+0lJYx/bkgP2ySOOT/nn/AM9KvW3w2+Ivgzxp4m1Lw0mg32narJHIP7Skk8yPy4/LoA4vx9qmm2Gr/DXTZfG+u6Z4Z1C3vJJb2S88u4k/55+ZVbTNZ1O/1DxXpPgnxnfeJdK0+wjvPttzJ5klvcf88/Mr1Z/hhrni7xf4L1/xRBpEkmkR3EdxbRjfH+8/1fl1r6J8Jo9A+J+o69aR2llpOoaf9nktoo/L/eUAchr/AMQb/wAeaf8AD7TdFu5La91SSO4vJY/9ZHHH/rK4GXxH4n1TwBZTyX+tS6NH4gubfVLnSf3lzHbR/wCrr074U/A6+8CeO9f1e+v47qykzFpcQ/5d45KpWXwg8b+E9Cjfw9rVpFqtvqlxefZpP+Pe4jk/5ZyUAWPgFdWM2t6smheMJ/EGg+XH5djq0nmXlnJXu1eNfDn4d+JE8f33jTxQNNsr2Syjs47HTP8AV/8AXSSvaBHgUAPqGSLNFFAC+VR5VFFAB5UdHlUUUAHlUeVRRQAeVR5VFFAB5VHlUUUAHlUeVRRQAeVSUUUAL5VHlUUUAHlUeVRRQAeVR5VFFAB5VS0UUAf/2Q=="
  };
</script>
</body>
</html>
