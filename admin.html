<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Yönetici Paneli - Kurye İzin Yönetimi</title>
<style>
  :root {
    --primary: #1e293b;
    --accent: #0f766e;
    --bg: #f8fafc;
    --card-bg: #ffffff;
    --border: #e2e8f0;
    --danger: #ef4444;
  }
  * { box-sizing: border-box; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; margin: 0; padding: 0; }
  body { background: var(--bg); color: #334155; padding: 20px; }
  .container { max-width: 1100px; margin: 0 auto; }
  .header { background: var(--primary); color: white; padding: 20px 24px; border-radius: 12px; margin-bottom: 24px; display: flex; justify-content: space-between; align-items: center; }
  .header h1 { font-size: 20px; font-weight: 700; }
  
  .tabs { display: flex; gap: 10px; margin-bottom: 20px; border-bottom: 2px solid var(--border); padding-bottom: 10px; }
  .tab-btn { background: none; border: none; padding: 10px 18px; font-weight: 600; font-size: 14px; cursor: pointer; color: #64748b; border-radius: 8px; }
  .tab-btn.active { background: var(--accent); color: white; }

  .tab-content { display: none; background: var(--card-bg); padding: 20px; border-radius: 12px; border: 1px solid var(--border); box-shadow: 0 1px 3px rgba(0,0,0,0.05); }
  .tab-content.active { display: block; }

  table { width: 100%; border-collapse: collapse; margin-top: 10px; font-size: 14px; }
  th, td { text-align: left; padding: 12px; border-bottom: 1px solid var(--border); }
  th { background: #f1f5f9; font-weight: 600; }

  input[type="number"], select { padding: 6px 10px; border: 1px solid var(--border); border-radius: 6px; font-size: 13px; width: 100%; }
  
  .btn-sm { padding: 6px 12px; border-radius: 6px; border: none; font-weight: 600; cursor: pointer; font-size: 12px; }
  .btn-danger { background: var(--danger); color: white; }
  .btn-success { background: var(--accent); color: white; }
  .btn-refresh { background: #475569; color: white; }

  .grid-form { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 10px; margin-bottom: 15px; }
  .form-group { display: flex; flex-direction: column; gap: 4px; }
  .form-group label { font-size: 12px; font-weight: 600; }
</style>
</head>
<body>

<div class="container">
  <div class="header">
    <h1>Yönetici Kontrol Paneli</h1>
    <button class="btn-sm btn-refresh" onclick="loadAllData()">Verileri Yenile 🔄</button>
  </div>

  <div class="tabs">
    <button class="tab-btn active" onclick="switchTab('tab-submissions')">Seçim Yapan Kuryeler</button>
    <button class="tab-btn" onclick="switchTab('tab-limits')">Bölge Kontenjanları</button>
    <button class="tab-btn" onclick="switchTab('tab-fixed')">Sabit İzin Tanımlama</button>
  </div>

  <!-- SEKMELİ 1: SEÇİM YAPAN KURYELER VE SİLME -->
  <div id="tab-submissions" class="tab-content active">
    <h3>Mevcut İzin Talepleri</h3>
    <table id="submissionsTable">
      <thead>
        <tr>
          <th>Bölge</th>
          <th>Ad Soyad</th>
          <th>Telefon</th>
          <th>Seçilen İzin Günü</th>
          <th>Talep Tarihi</th>
          <th>İşlem</th>
        </tr>
      </thead>
      <tbody><!-- Dinamik Yüklenecek --></tbody>
    </table>
  </div>

  <!-- SEKMELİ 2: BÖLGE KONTENJANLARI BELİRLEME -->
  <div id="tab-limits" class="tab-content">
    <h3>Bölge İzin Günleri Kontenjan Ayarları</h3>
    <p style="font-size: 13px; color: #64748b; margin-bottom: 15px;">Aşağıdan bölge seçip günlere özel günlük izin kontenjan limitlerini güncelleyebilirsiniz.</p>
    
    <div style="max-width: 300px; margin-bottom: 15px;">
      <label style="font-size: 13px; font-weight: 600;">Bölge Seçiniz:</label>
      <select id="regionSelect" onchange="populateLimitForm()"></select>
    </div>

    <div class="grid-form">
      <div class="form-group"><label>Pazartesi</label><input type="number" id="limit_Pazartesi" min="0"></div>
      <div class="form-group"><label>Salı</label><input type="number" id="limit_Salı" min="0"></div>
      <div class="form-group"><label>Çarşamba</label><input type="number" id="limit_Çarşamba" min="0"></div>
      <div class="form-group"><label>Perşembe</label><input type="number" id="limit_Perşembe" min="0"></div>
      <div class="form-group"><label>Cuma</label><input type="number" id="limit_Cuma" min="0"></div>
      <div class="form-group"><label>Cumartesi</label><input type="number" id="limit_Cumartesi" min="0"></div>
      <div class="form-group"><label>Pazar</label><input type="number" id="limit_Pazar" min="0"></div>
    </div>
    <button class="btn-sm btn-success" onclick="saveLimits()">Kontenjanları Kaydet</button>
  </div>

  <!-- SEKMELİ 3: SABİT İZİN GÜNÜ GİRME -->
  <div id="tab-fixed" class="tab-content">
    <h3>Kuryelere Sabit İzin Günü Tanımlama</h3>
    <p style="font-size: 13px; color: #64748b; margin-bottom: 15px;">Sabit gün atanan kuryeler sisteme girdiklerinde gün seçemezler, doğrudan kendilerine atanan günü görürler.</p>
    <table id="usersTable">
      <thead>
        <tr>
          <th>Telefon</th>
          <th>Ad Soyad</th>
          <th>Bölge</th>
          <th>Sabit İzin Günü</th>
          <th>İşlem</th>
        </tr>
      </thead>
      <tbody><!-- Dinamik Yüklenecek --></tbody>
    </table>
  </div>
</div>

<script>
  const SCRIPT_URL = "https://script.google.com/macros/s/AKfycbwbf4rDR7ICIHXENQzcPnz2X2A0B9w6DSTRgEgTRIeyWZuxngdmepQMTMXo0WzxW-806Q/exec";

  let adminData = { users: [], submissions: [], settings: [] };

  window.onload = loadAllData;

  function switchTab(tabId) {
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
    event.target.classList.add('active');
    document.getElementById(tabId).classList.add('active');
  }

  async function loadAllData() {
    try {
      const res = await fetch(`${SCRIPT_URL}?action=getAdminData`);
      adminData = await res.json();
      
      renderSubmissions();
      renderLimitsSelect();
      renderUsers();
    } catch (e) {
      alert("Veriler çekilirken hata oluştu!");
    }
  }

  // 1. TALEPLERİ LİSTELEME VE SİLME
  function renderSubmissions() {
    const tbody = document.querySelector('#submissionsTable tbody');
    tbody.innerHTML = '';

    adminData.submissions.forEach(row => {
      const tr = document.createElement('tr');
      tr.innerHTML = `
        <td><b>${row[0]}</b></td>
        <td>${row[1]}</td>
        <td>${row[2]}</td>
        <td><span style="color: #0f766e; font-weight:700;">${row[3]}</span></td>
        <td>${row[4]}</td>
        <td><button class="btn-sm btn-danger" onclick="deleteSubmission('${row[2]}')">Talebi Sil</button></td>
      `;
      tbody.appendChild(tr);
    });
  }

  async function deleteSubmission(phone) {
    if (!confirm(`${phone} numaralı kuryenin izin talebini silmek istediğinize emin misiniz?`)) return;

    const res = await fetch(SCRIPT_URL, {
      method: 'POST',
      headers: { 'Content-Type': 'text/plain' },
      body: JSON.stringify({ action: 'deleteSubmission', phone: phone })
    });
    const result = await res.json();
    alert(result.message || "İşlem tamamlandı");
    loadAllData();
  }

  // 2. KONTENJAN LİMİTLERİ DÜZENLEME
  function renderLimitsSelect() {
    const select = document.getElementById('regionSelect');
    select.innerHTML = '';
    
    adminData.settings.forEach(s => {
      const opt = document.createElement('option');
      opt.value = s[0];
      opt.innerText = s[0];
      select.appendChild(opt);
    });
    populateLimitForm();
  }

  function populateLimitForm() {
    const selectedRegion = document.getElementById('regionSelect').value;
    const regionData = adminData.settings.find(s => s[0] === selectedRegion);

    if (regionData) {
      const days = ["Pazartesi", "Salı", "Çarşamba", "Perşembe", "Cuma", "Cumartesi", "Pazar"];
      days.forEach((day, idx) => {
        document.getElementById(`limit_${day}`).value = regionData[idx + 1] || 0;
      });
    }
  }

  async function saveLimits() {
    const region = document.getElementById('regionSelect').value;
    const days = ["Pazartesi", "Salı", "Çarşamba", "Perşembe", "Cuma", "Cumartesi", "Pazar"];
    
    const payload = { action: 'updateLimits', region: region };
    days.forEach(day => {
      payload[day] = Number(document.getElementById(`limit_${day}`).value) || 0;
    });

    const res = await fetch(SCRIPT_URL, {
      method: 'POST',
      headers: { 'Content-Type': 'text/plain' },
      body: JSON.stringify(payload)
    });
    const result = await res.json();
    alert(result.message || "Kontenjanlar güncellendi");
    loadAllData();
  }

  // 3. SABİT İZİN GÜNÜ DÜZENLEME
  function renderUsers() {
    const tbody = document.querySelector('#usersTable tbody');
    tbody.innerHTML = '';

    const days = ["Yok", "Pazartesi", "Salı", "Çarşamba", "Perşembe", "Cuma", "Cumartesi", "Pazar"];

    adminData.users.forEach(user => {
      const currentFixed = user[3] || "Yok";
      
      let optionsHtml = days.map(d => `<option value="${d === 'Yok' ? '' : d}" ${currentFixed === d ? 'selected' : ''}>${d}</option>`).join('');

      const tr = document.createElement('tr');
      tr.innerHTML = `
        <td>${user[0]}</td>
        <td><b>${user[1]}</b></td>
        <td>${user[2]}</td>
        <td>
          <select id="fixed_select_${user[0]}">
            ${optionsHtml}
          </select>
        </td>
        <td><button class="btn-sm btn-success" onclick="saveFixedDay('${user[0]}')">Güncelle</button></td>
      `;
      tbody.appendChild(tr);
    });
  }

  async function saveFixedDay(phone) {
    const fixedVal = document.getElementById(`fixed_select_${phone}`).value;

    const res = await fetch(SCRIPT_URL, {
      method: 'POST',
      headers: { 'Content-Type': 'text/plain' },
      body: JSON.stringify({ action: 'updateFixedDay', phone: phone, fixedDay: fixedVal })
    });
    const result = await res.json();
    alert(result.message || "Güncellendi");
    loadAllData();
  }
</script>

</body>
</html>
