<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
  <title>Pengumuman Kelulusan Tunas Gurindam Corps Akt 7 2025/2026</title>
  <style>
    /* Gradien biru dominan */
    body, html {
      margin: 0; padding: 0; height: 100%;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #3b82f6, #1e40af);
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      text-align: center;
      overflow-x: hidden;
    }
    /* Container umum */
    .container {
      background: rgba(255 255 255 / 0.1);
      border-radius: 16px;
      padding: 2.5rem 3rem;
      max-width: 600px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.3);
      width: 90%;
      position: relative;
    }
    /* Logo bulat */
    .logo-circle {
      width: 120px;
      height: 120px;
      background: white;
      border-radius: 50%;
      margin: 0 auto 1.5rem auto;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 0 15px rgba(255 255 255 / 0.7);
      user-select: none;
    }
    /* Logo gambar */
    .logo-image {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
    }
    h1 {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 2rem;
      line-height: 1.3;
      user-select: none;
    }
    /* Tombol */
    button {
      background-color: #2563eb;
      border: none;
      color: white;
      padding: 0.75rem 2rem;
      font-size: 1.1rem;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 700;
      transition: background-color 0.3s ease;
      box-shadow: 0 4px 12px rgba(37, 99, 235, 0.6);
    }
    button:hover {
      background-color: #1e40af;
      box-shadow: 0 6px 18px rgba(30, 64, 175, 0.8);
    }
    /* Halaman cek kelulusan */
    #check-page {
      display: none;
      background: white;
      color: #1e40af;
      padding: 2rem 2.5rem;
      border-radius: 16px;
      max-width: 600px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.3);
      width: 90%;
      text-align: left;
      position: relative;
    }
    #check-page h2 {
      text-align: center;
      margin-bottom: 1.5rem;
      font-weight: 800;
      font-size: 1.8rem;
      user-select: none;
    }
    label {
      font-weight: 600;
      display: block;
      margin-bottom: 0.5rem;
      user-select: none;
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 0.6rem 0.8rem;
      font-size: 1rem;
      border-radius: 8px;
      border: 2px solid #3b82f6;
      margin-bottom: 1.2rem;
      box-sizing: border-box;
      transition: border-color 0.3s ease;
    }
    input[type="text"]:focus, input[type="password"]:focus {
      outline: none;
      border-color: #1e40af;
      box-shadow: 0 0 8px #1e40af;
    }
    #check-btn, #back-btn, #admin-logout-btn {
      width: 100%;
      margin-top: 0.5rem;
    }
    #result {
      margin-top: 1.5rem;
      font-weight: 700;
      font-size: 1.2rem;
      min-height: 3rem;
      user-select: text;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    #admin-list {
      margin-top: 1.5rem;
      max-height: 300px;
      overflow-y: auto;
      border-top: 2px solid #3b82f6;
      padding-top: 1rem;
    }
    #admin-list ul {
      list-style: none;
      padding-left: 0;
      color: #1e40af;
      font-weight: 600;
    }
    #admin-list li {
      padding: 0.3rem 0;
      border-bottom: 1px solid #cbd5e1;
      user-select: text;
    }
    /* Admin login form */
    #admin-login {
      display: none;
      margin-top: 1rem;
    }
    #admin-login label {
      margin-top: 0.5rem;
    }
    /* Responsive */
    @media (max-width: 480px) {
      .container, #check-page {
        padding: 1.5rem 1.8rem;
      }
      .logo-circle {
        width: 90px;
        height: 90px;
      }
      .logo-text {
        font-size: 2.2rem;
      }
      h1, #check-page h2 {
        font-size: 1.4rem;
      }
    }
/* Styles for result display */
    .result-passed {
      color: #22c55e;
      font-size: 1.6rem;
      font-weight: 800;
      animation: fadeInUp 1s ease-out, glow 2s ease-in-out infinite alternate;
      text-align: center;
      margin: 1.5rem 0;
      background: linear-gradient(135deg, rgba(34, 197, 94, 0.1), rgba(34, 197, 94, 0.05));
      padding: 1.5rem 2rem;
      border-radius: 15px;
      border: 2px solid #22c55e;
      box-shadow: 0 8px 25px rgba(34, 197, 94, 0.3);
      position: relative;
      overflow: hidden;
    }
    .result-passed::before {
      content: '🎉';
      font-size: 2rem;
      position: absolute;
      top: 10px;
      left: 20px;
      animation: bounce 1s ease-in-out;
    }
    .result-passed::after {
      content: '✅';
      font-size: 2rem;
      position: absolute;
      top: 10px;
      right: 20px;
      animation: bounce 1s ease-in-out 0.2s;
    }

    .result-not-found {
      color: #ef4444;
      font-size: 1.4rem;
      font-weight: 700;
      animation: fadeIn 0.8s ease-in, shake 0.5s ease-in-out 0.8s;
      text-align: center;
      margin: 1.5rem 0;
      background: linear-gradient(135deg, rgba(239, 68, 68, 0.1), rgba(239, 68, 68, 0.05));
      padding: 1.5rem 2rem;
      border-radius: 15px;
      border: 2px solid #ef4444;
      box-shadow: 0 8px 25px rgba(239, 68, 68, 0.3);
      position: relative;
    }
    .result-not-found::before {
      content: '❌';
      font-size: 2rem;
      position: absolute;
      top: 10px;
      left: 20px;
    }

    .result-admin {
      color: #f59e0b;
      font-size: 1.4rem;
      font-weight: 700;
      animation: fadeIn 0.8s ease-in, pulse 2s ease-in-out infinite;
      text-align: center;
      margin: 1.5rem 0;
      background: linear-gradient(135deg, rgba(245, 158, 11, 0.1), rgba(245, 158, 11, 0.05));
      padding: 1.5rem 2rem;
      border-radius: 15px;
      border: 2px solid #f59e0b;
      box-shadow: 0 8px 25px rgba(245, 158, 11, 0.3);
      position: relative;
    }
    .result-admin::before {
      content: '🔐';
      font-size: 2rem;
      position: absolute;
      top: 10px;
      left: 20px;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes glow {
      from { box-shadow: 0 8px 25px rgba(34, 197, 94, 0.3); }
      to { box-shadow: 0 8px 25px rgba(34, 197, 94, 0.6), 0 0 30px rgba(34, 197, 94, 0.4); }
    }
    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
      40% { transform: translateY(-10px); }
      60% { transform: translateY(-5px); }
    }
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      10%, 30%, 50%, 70%, 90% { transform: translateX(-5px); }
      20%, 40%, 60%, 80% { transform: translateX(5px); }
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    /* Music Control Styles */
    #music-control {
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 1000;
    }

    #music-btn {
      background: rgba(255, 255, 255, 0.95);
      border: 2px solid #4f46e5;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
      color: #4f46e5;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
      transition: all 0.3s ease;
      backdrop-filter: blur(10px);
    }

    #music-btn:hover {
      transform: scale(1.1);
      box-shadow: 0 6px 20px rgba(79, 70, 229, 0.4);
      background: rgba(255, 255, 255, 1);
    }

    #music-btn.playing {
      background: linear-gradient(135deg, #22c55e, #16a34a);
      color: white;
      border-color: #16a34a;
      animation: pulse 2s infinite;
    }

    #music-btn.muted {
      background: linear-gradient(135deg, #ef4444, #dc2626);
      color: white;
      border-color: #dc2626;
    }

    /* Mobile responsive for music control */
    @media (max-width: 768px) {
      #music-control {
        top: 15px;
        right: 15px;
      }

      #music-btn {
        width: 45px;
        height: 45px;
        font-size: 16px;
      }
    }

    @media (max-width: 480px) {
      #music-control {
        top: 10px;
        right: 10px;
      }

      #music-btn {
        width: 40px;
        height: 40px;
        font-size: 14px;
      }
    }
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      10%, 30%, 50%, 70%, 90% { transform: translateX(-5px); }
      20%, 40%, 60%, 80% { transform: translateX(5px); }
    }
    /* Glowing black text */
    .glowing-gold {
      color: #000000;
      text-shadow: 0 0 10px #000000, 0 0 20px #000000, 0 0 30px #000000;
      animation: glow-black 2s ease-in-out infinite alternate;
      font-weight: bold;
    }

    /* Detail link styling */
    .detail-link {
      transition: all 0.3s ease;
    }

    .detail-link:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(79, 70, 229, 0.4) !important;
    }
    @keyframes glow-black {
      from { text-shadow: 0 0 10px #000000, 0 0 20px #000000, 0 0 30px #000000; }
      to { text-shadow: 0 0 20px #000000, 0 0 30px #000000, 0 0 40px #000000, 0 0 50px #000000; }
    }
    @keyframes glow-gold {
      from { text-shadow: 0 0 10px #ffd700, 0 0 20px #ffd700, 0 0 30px #ffd700; }
      to { text-shadow: 0 0 20px #ffd700, 0 0 30px #ffd700, 0 0 40px #ffd700, 0 0 50px #ffd700; }
    }
    /* Styles for admin table */
    #student-table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 1rem;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    #student-table th, #student-table td {
      padding: 0.75rem;
      border: 1px solid #3b82f6;
      text-align: left;
      font-weight: 600;
    }
    #student-table th {
      background: linear-gradient(135deg, #1e40af, #3b82f6);
      color: white;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }
    #student-table tr:nth-child(even) {
      background-color: rgba(59, 130, 246, 0.05);
    }
    #student-table tr:hover {
      background-color: rgba(59, 130, 246, 0.1);
      transition: background-color 0.3s ease;
    }
    #student-table td:first-child {
      font-weight: 700;
      color: #1e40af;
    }
  </style>
</head>
<body>
 <!-- Background Music -->
 <audio id="bg-music" loop preload="auto">
   <source src="[Royalty Free] Awarding Background Music for Nomination Show and Ceremony Opening.mp3" type="audio/mpeg">
   Your browser does not support the audio element.
 </audio>

 <!-- Music Control Button -->
 <div id="music-control" style="position: fixed; top: 20px; right: 20px; z-index: 1000;">
   <button id="music-btn" style="background: rgba(255,255,255,0.9); border: 2px solid #4f46e5; border-radius: 50%; width: 50px; height: 50px; cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 18px; color: #4f46e5; box-shadow: 0 4px 12px rgba(0,0,0,0.2); transition: all 0.3s ease;">
     🔊
   </button>
 </div>

 <!-- Halaman Sambutan -->
 <div class="container" id="welcome-page" role="main" aria-label="Halaman sambutan pengumuman kelulusan">
    <div class="logo-circle" aria-hidden="true">
      <img src="242104513_266398215333645_4612524844173446882_n.jpg" alt="Logo TGC" class="logo-image" aria-label="Logo Tunas Gurindam Corps" />
    </div>
    <h1>PENGUMUMAN KELULUSAN ANGGOTA TUNAS GURINDAM CORPS AKT 7 2025/2026</h1>
    <div id="countdown" style="font-size: 1.2rem; color: #3b82f6; margin: 1rem 0; text-align: center;"></div>
    <button id="enter-btn" aria-describedby="desc-enter">Masuk ke Pengumuman</button>
    <p id="desc-enter" style="font-size:0.9rem; margin-top:0.8rem; user-select:none;">Klik tombol untuk melanjutkan ke halaman cek kelulusan</p>
  </div>

  <!-- Halaman Cek Kelulusan -->
  <section id="check-page" role="main" aria-label="Halaman cek kelulusan">
    <h2>Pengumuman Kelulusan</h2>
    <p id="current-time" style="font-size: 0.9rem; color: #3b82f6; margin-bottom: 1rem;"></p>

    <form id="check-form" autocomplete="off" aria-describedby="desc-check">
      <label for="name-input">Masukkan Nama Lengkap atau ID Peserta:</label>
      <input type="text" id="name-input" name="name" placeholder="" aria-required="true" />

      <button type="submit" id="check-btn">Cek Kelulusan</button>
      <button type="button" id="back-btn" style="background-color:#1e40af; margin-top: 1rem;">Kembali ke Sambutan</button>
    </form>

    <div id="result" role="alert" aria-live="polite"></div>

  </section>

  <script>
    // Fungsi untuk menyimpan data siswa ke localStorage
    function saveStudentsToStorage() {
      localStorage.setItem('tunasGurindamStudents', JSON.stringify(students));
    }

    // Fungsi untuk memuat data siswa dari localStorage
    function loadStudentsFromStorage() {
      const saved = localStorage.getItem('tunasGurindamStudents');
      if (saved) {
        const parsed = JSON.parse(saved);
        // Update students object dengan data dari localStorage
        Object.keys(students).forEach(key => delete students[key]);
        Object.assign(students, parsed);
      } else {
        // Jika belum ada data di localStorage, simpan data awal
        saveStudentsToStorage();
      }
    }

    // Data siswa awal
    let students = {
      "TGC00001": { nama: "AHMAD", status: "LULUS" },
      "TGC00002": { nama: "SITI", status: "LULUS" },
      "TGC00003": { nama: "BUDI", status: "TIDAK LULUS" },
      "TGC00004": { nama: "RINA", status: "LULUS" },
      "TGC00005": { nama: "DENI", status: "LULUS" },
      "TGC00006": { nama: "LINA", status: "TIDAK LULUS" },
      "TGC00007": { nama: "BAIM", status: "LULUS" },
      "TGC00008": { nama: "FARAH", status: "LULUS" },
      "TGC00009": { nama: "GILANG", status: "TIDAK LULUS" },
      "TGC00010": { nama: "HANA", status: "LULUS" },
      "TGC00011": { nama: "DONI", status: "TIDAK LULUS" },
      "TGC00012": { nama: "SARI", status: "TIDAK LULUS" },
      "TGC00013": { nama: "REZA", status: "LULUS" },
      "TGC00014": { nama: "NOVA", status: "TIDAK LULUS" },
      "TGC00015": { nama: "ANDI", status: "LULUS" }
    };

    // Muat data dari localStorage saat halaman dimuat
    loadStudentsFromStorage();

    // Waktu pengumuman dibuka: 8 September 2025 pukul 21:55 WIB (UTC+7)
    // WIB = UTC+7, jadi 21:55 WIB = 14:55 UTC
    function getWaktuPengumuman() {
      const saved = localStorage.getItem('tunasGurindamReleaseDate');
      if (saved) {
        return new Date(saved);
      }
      return new Date(Date.UTC(2025, 8, 8, 14, 55, 0)); // bulan 8 = September (0-based)
    }
    const releaseDate = getWaktuPengumuman();

    // Elemen DOM
    const welcomePage = document.getElementById('welcome-page');
    const checkPage = document.getElementById('check-page');
    const enterBtn = document.getElementById('enter-btn');
    const backBtn = document.getElementById('back-btn');
    const checkForm = document.getElementById('check-form');
    const nameInput = document.getElementById('name-input');
    const nameLabel = document.querySelector('label[for="name-input"]');
    const resultDiv = document.getElementById('result');
    const currentTimeDiv = document.getElementById('current-time');
    const countdownDiv = document.getElementById('countdown');

    // Fungsi untuk update tanggal dan waktu
    function updateCurrentTime() {
      const now = new Date();
      const options = { timeZone: 'Asia/Jakarta', year: 'numeric', month: 'long', day: 'numeric', hour: '2-digit', minute: '2-digit', second: '2-digit' };
      const formatted = now.toLocaleString('id-ID', options) + ' WIB';
      currentTimeDiv.textContent = 'Tanggal dan Waktu: ' + formatted;
    }

    // Fungsi untuk countdown
    function updateCountdown() {
      const now = new Date().getTime();
      const distance = releaseDate.getTime() - now;
      if (distance > 0) {
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);
        countdownDiv.innerHTML = `
          <table style="color: white; margin: 0 auto; font-size: 1.2rem; border-collapse: collapse;">
            <tr>
              <td style="padding: 0.5rem; text-align: center;">Hari</td>
              <td style="padding: 0.5rem; text-align: center;">:</td>
              <td style="padding: 0.5rem; text-align: center; font-weight: bold;">${days}</td>
              <td style="padding: 0.5rem; text-align: center;">|</td>
              <td style="padding: 0.5rem; text-align: center;">Jam</td>
              <td style="padding: 0.5rem; text-align: center;">:</td>
              <td style="padding: 0.5rem; text-align: center; font-weight: bold;">${hours}</td>
              <td style="padding: 0.5rem; text-align: center;">|</td>
              <td style="padding: 0.5rem; text-align: center;">Menit</td>
              <td style="padding: 0.5rem; text-align: center;">:</td>
              <td style="padding: 0.5rem; text-align: center; font-weight: bold;">${minutes}</td>
              <td style="padding: 0.5rem; text-align: center;">|</td>
              <td style="padding: 0.5rem; text-align: center;">Detik</td>
              <td style="padding: 0.5rem; text-align: center;">:</td>
              <td style="padding: 0.5rem; text-align: center; font-weight: bold;">${seconds}</td>
            </tr>
          </table>
        `;
        enterBtn.disabled = true;
        enterBtn.style.opacity = '0.5';
      } else {
        countdownDiv.innerHTML = '<span class="glowing-gold" style="font-size: 1.5rem; font-weight: bold; text-transform: uppercase; letter-spacing: 2px;">Pengumuman Sudah Dimulai!</span>';
        enterBtn.disabled = false;
        enterBtn.style.opacity = '1';
      }
    }

    // Update waktu setiap detik
    setInterval(updateCurrentTime, 1000);
    updateCurrentTime(); // Update awal

    // Update countdown setiap detik
    setInterval(updateCountdown, 1000);
    updateCountdown(); // Update awal

    // Check for URL parameters and auto-search
    function checkURLParameters() {
      const urlParams = new URLSearchParams(window.location.search);
      const studentName = urlParams.get('name');
      const studentId = urlParams.get('id');

      if (studentName || studentId) {
        // Wait a moment for page to load, then auto-search
        setTimeout(() => {
          const searchInput = document.getElementById('name-input');
          if (studentName) {
            searchInput.value = decodeURIComponent(studentName);
          } else if (studentId) {
            // Find student by ID and fill name
            for (const key in students) {
              if (key === studentId) {
                searchInput.value = students[key].nama;
                break;
              }
            }
          }

          // Auto-submit the search
          if (searchInput.value) {
            const form = document.getElementById('check-form');
            form.dispatchEvent(new Event('submit'));
          }
        }, 500);
      }
    }

    // Cek akses waktu
    function isAccessAllowed() {
      const now = new Date();
      return now >= releaseDate;
    }

    // Data admin
    const adminCredentials = [
      { user: 'ADMIN', pass: 'ADMIN' },
      { user: 'ADMIN', pass: 'TUNASGURINDAM' },
      { user: 'OKA', pass: 'OKAJB123' },
      { user: 'PENDY SETIAWANSYAH', pass: 'TUNASGURINDAM' },
      { user: 'DIGO BRAMALDO TAKBIRANTO', pass: 'TUNASGURINDAM' },
      { user: 'ROBY SAHPUTRA', pass: 'TUNASGURINDAM' },
      { user: 'OGGY ARLIANSYAH', pass: 'TUNASGURINDAM' }
    ];


    // Tampilkan halaman cek kelulusan dan sembunyikan sambutan
    enterBtn.addEventListener('click', () => {
      if (isAccessAllowed()) {
        alert('Selamat datang di halaman pengumuman kelulusan!');
        welcomePage.style.display = 'none';
        checkPage.style.display = 'block';
        nameInput.focus();
      } else {
        const now = new Date().getTime();
        const distance = releaseDate.getTime() - now;
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);
        alert(`Pengumuman kelulusan belum dimulai. Sisa waktu: ${days} hari ${hours} jam ${minutes} menit ${seconds} detik. Harap tunggu hingga pukul 21.55 WIB tanggal 8 September 2025.`);
      }
    });

    // Kembali ke halaman sambutan
    backBtn.addEventListener('click', () => {
      checkPage.style.display = 'none';
      welcomePage.style.display = 'block';
      resetCheckPage();
    });


    // Reset halaman cek kelulusan
    function resetCheckPage() {
      resultDiv.innerHTML = '';
      nameInput.value = '';
      nameInput.disabled = false;
      nameInput.style.display = 'block';
      nameLabel.style.display = 'block';
      checkForm.querySelector('#check-btn').textContent = 'Cek Kelulusan';
    }



    // Submit form cek kelulusan
    checkForm.addEventListener('submit', e => {
      e.preventDefault();
      if (!isAccessAllowed()) {
        alert('Pengumuman kelulusan belum dimulai. Harap dicek sesuai waktu yang telah ditentukan pada pukul 21.55 WIB tanggal 8 September 2025.');
        return;
      }

      const inputName = nameInput.value.trim();
      if (!inputName) {
        resultDiv.innerHTML = '<div class="result-not-found">Mohon masukkan nama siswa.</div>';
        return;
      }

      // Cari siswa berdasarkan nama atau ID
      let found = null;
      let foundKey = null;
      for (const key in students) {
        if (students.hasOwnProperty(key)) {
          const s = students[key];
          // Cek berdasarkan nama lengkap
          if (s.nama.toLowerCase() === inputName.toLowerCase()) {
            found = s;
            foundKey = key;
            break;
          }
          // Cek berdasarkan ID peserta
          if (key.toLowerCase() === inputName.toLowerCase()) {
            found = s;
            foundKey = key;
            break;
          }
        }
      }
      if (found) {
        if (found.status === 'TIDAK LULUS') {
          // Show result in red styling for TIDAK LULUS students
          resultDiv.innerHTML = `
            <div class="result-not-found">
              <h3>💪 ${found.nama}</h3>
              <p>ID Peserta: <strong>${foundKey}</strong></p>
              <p>Anda telah mengikuti proses seleksi Tunas Gurindam Corps Angkatan 7 2025/2026.</p>
              <p>Status Anda: <strong>TIDAK LULUS</strong></p>
              <p>Jangan berkecil hati! Kegagalan adalah bagian dari perjalanan menuju kesuksesan. Teruslah belajar, berkembang, dan persiapkan diri untuk kesempatan berikutnya.</p>
              <p>Kami yakin Anda akan berhasil! 💪</p>
            </div>
          `;
        } else {
          // Redirect to individual detail page for LULUS students
          const studentName = encodeURIComponent(found.nama);
          window.location.href = `student-detail.html?name=${studentName}`;
        }
      } else {
        resultDiv.innerHTML = '<div class="result-not-found">Maaf, nama lengkap atau ID peserta tidak ditemukan. Pastikan penulisan sudah benar (contoh: BAIM atau TGC00007).</div>';
      }
    });


    // Optional: Enter key triggers submit
    nameInput.addEventListener('keydown', e => {
      if (e.key === 'Enter') {
        e.preventDefault();
        checkForm.dispatchEvent(new Event('submit'));
      }
    });

    // Music Control Functionality
    const bgMusic = document.getElementById('bg-music');
    const musicBtn = document.getElementById('music-btn');
    let musicPlaying = false;
    let autoplayAttempted = false;

    // Function to update music button state
    function updateMusicButton() {
      if (musicPlaying) {
        musicBtn.textContent = '🔊';
        musicBtn.className = 'playing';
        musicBtn.title = 'Musik sedang dimainkan - Klik untuk pause';
      } else {
        musicBtn.textContent = '🔇';
        musicBtn.className = 'muted';
        musicBtn.title = 'Musik paused - Klik untuk play';
      }
    }

    // Function to play music
    function playMusic() {
      const playPromise = bgMusic.play();
      if (playPromise !== undefined) {
        playPromise.then(() => {
          musicPlaying = true;
          updateMusicButton();
          console.log('Music started playing');
        }).catch(error => {
          console.log('Autoplay blocked:', error);
          musicPlaying = false;
          updateMusicButton();
          // Show message to user about autoplay being blocked
          if (!autoplayAttempted) {
            setTimeout(() => {
              alert('Musik tidak dapat dimainkan otomatis. Klik tombol musik 🔊 untuk memulai musik latar.');
            }, 1000);
          }
        });
      }
      autoplayAttempted = true;
    }

    // Function to pause music
    function pauseMusic() {
      bgMusic.pause();
      musicPlaying = false;
      updateMusicButton();
      console.log('Music paused');
    }

    // Try to autoplay music when page loads
    document.addEventListener('DOMContentLoaded', () => {
      // Small delay to ensure audio element is ready
      setTimeout(() => {
        playMusic();
      }, 500);
    });

    // Music button click handler
    musicBtn.addEventListener('click', () => {
      if (musicPlaying) {
        pauseMusic();
      } else {
        playMusic();
      }
    });

    // Handle music end (loop)
    bgMusic.addEventListener('ended', () => {
      console.log('Music ended, restarting...');
      playMusic();
    });

    // Handle page visibility change (pause when tab is hidden)
    document.addEventListener('visibilitychange', () => {
      if (document.hidden && musicPlaying) {
        pauseMusic();
      } else if (!document.hidden && !musicPlaying) {
        // Optionally resume when tab becomes visible
        // playMusic();
      }
    });

    // Initialize button state
    updateMusicButton();

    // Click anywhere to play music (first interaction)
    let clickToPlayEnabled = true;
    document.addEventListener('click', function firstClickToPlay(event) {
      // Don't trigger if clicking on music control button
      if (event.target.closest('#music-control')) {
        return;
      }

      // Don't trigger if music is already playing
      if (musicPlaying) {
        return;
      }

      // Don't trigger if we've already handled the first click
      if (!clickToPlayEnabled) {
        return;
      }

      console.log('First click detected - attempting to play music');
      clickToPlayEnabled = false;

      // Remove this event listener after first use
      document.removeEventListener('click', firstClickToPlay);

      // Attempt to play music
      playMusic();
    });
  </script>
</body>
</html>
