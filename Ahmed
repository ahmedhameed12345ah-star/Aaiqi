<!DOCTYPE html>

<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>منشئ الجداول</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&family=Tajawal:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0e1a;
    --surface: #111827;
    --card: #1a2235;
    --accent: #4f9cf9;
    --accent2: #a78bfa;
    --gold: #f59e0b;
    --text: #e2e8f0;
    --muted: #64748b;
    --border: #1e3a5f;
    --success: #10b981;
    --danger: #ef4444;
  }

- { margin: 0; padding: 0; box-sizing: border-box; }

body {
font-family: ‘Cairo’, sans-serif;
background: var(–bg);
color: var(–text);
min-height: 100vh;
padding: 20px;
background-image:
radial-gradient(ellipse at 20% 20%, rgba(79,156,249,0.08) 0%, transparent 50%),
radial-gradient(ellipse at 80% 80%, rgba(167,139,250,0.08) 0%, transparent 50%);
}

.container {
max-width: 900px;
margin: 0 auto;
}

header {
text-align: center;
margin-bottom: 40px;
padding-top: 20px;
}

header h1 {
font-family: ‘Tajawal’, sans-serif;
font-size: 2.8rem;
font-weight: 900;
background: linear-gradient(135deg, var(–accent), var(–accent2));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
margin-bottom: 8px;
}

header p {
color: var(–muted);
font-size: 1rem;
}

.panel {
background: var(–card);
border: 1px solid var(–border);
border-radius: 16px;
padding: 28px;
margin-bottom: 24px;
}

.panel-title {
font-size: 1.1rem;
font-weight: 700;
color: var(–accent);
margin-bottom: 20px;
display: flex;
align-items: center;
gap: 8px;
}

.panel-title::before {
content: ‘’;
display: block;
width: 4px;
height: 20px;
background: linear-gradient(var(–accent), var(–accent2));
border-radius: 2px;
}

/* Input area */
.input-row {
display: flex;
gap: 12px;
margin-bottom: 12px;
}

input[type=“text”] {
flex: 1;
background: var(–surface);
border: 1px solid var(–border);
border-radius: 10px;
padding: 12px 16px;
color: var(–text);
font-family: ‘Cairo’, sans-serif;
font-size: 1rem;
outline: none;
transition: border-color 0.2s, box-shadow 0.2s;
}

input[type=“text”]:focus {
border-color: var(–accent);
box-shadow: 0 0 0 3px rgba(79,156,249,0.15);
}

input[type=“text”]::placeholder { color: var(–muted); }

.btn {
border: none;
border-radius: 10px;
padding: 12px 22px;
font-family: ‘Cairo’, sans-serif;
font-size: 0.95rem;
font-weight: 700;
cursor: pointer;
transition: all 0.2s;
display: inline-flex;
align-items: center;
gap: 6px;
}

.btn-primary {
background: linear-gradient(135deg, var(–accent), #3b82f6);
color: #fff;
}

.btn-primary:hover { opacity: 0.9; transform: translateY(-1px); }

.btn-danger {
background: rgba(239,68,68,0.15);
color: var(–danger);
border: 1px solid rgba(239,68,68,0.3);
}

.btn-danger:hover { background: rgba(239,68,68,0.25); }

.btn-sm { padding: 6px 14px; font-size: 0.85rem; }

/* Names list */
.names-grid {
display: flex;
flex-wrap: wrap;
gap: 8px;
min-height: 48px;
padding: 12px;
background: var(–surface);
border-radius: 10px;
border: 1px dashed var(–border);
}

.name-tag {
background: linear-gradient(135deg, rgba(79,156,249,0.2), rgba(167,139,250,0.2));
border: 1px solid rgba(79,156,249,0.3);
border-radius: 20px;
padding: 4px 14px;
font-size: 0.9rem;
display: flex;
align-items: center;
gap: 8px;
animation: popIn 0.2s ease;
}

@keyframes popIn {
from { transform: scale(0.8); opacity: 0; }
to { transform: scale(1); opacity: 1; }
}

.name-tag button {
background: none;
border: none;
color: var(–muted);
cursor: pointer;
font-size: 0.8rem;
line-height: 1;
transition: color 0.15s;
padding: 0;
}

.name-tag button:hover { color: var(–danger); }

.empty-hint {
color: var(–muted);
font-size: 0.9rem;
margin: auto;
}

/* Column builder */
.cols-row {
display: flex;
gap: 10px;
flex-wrap: wrap;
margin-bottom: 12px;
}

.col-tag {
background: rgba(167,139,250,0.15);
border: 1px solid rgba(167,139,250,0.3);
border-radius: 8px;
padding: 6px 14px;
font-size: 0.88rem;
display: flex;
align-items: center;
gap: 8px;
}

.col-tag button {
background: none; border: none;
color: var(–muted); cursor: pointer;
font-size: 0.8rem; padding: 0;
transition: color 0.15s;
}

.col-tag button:hover { color: var(–danger); }

/* Preview table */
.table-wrap {
overflow-x: auto;
border-radius: 10px;
border: 1px solid var(–border);
}

table {
width: 100%;
border-collapse: collapse;
font-size: 0.92rem;
}

thead th {
background: linear-gradient(135deg, rgba(79,156,249,0.2), rgba(167,139,250,0.2));
color: var(–accent);
font-weight: 700;
padding: 12px 16px;
text-align: right;
border-bottom: 2px solid var(–border);
white-space: nowrap;
}

tbody tr {
border-bottom: 1px solid rgba(255,255,255,0.05);
transition: background 0.15s;
}

tbody tr:hover { background: rgba(79,156,249,0.05); }

tbody tr:last-child { border-bottom: none; }

td {
padding: 10px 16px;
color: var(–text);
}

td:first-child { color: var(–muted); font-size: 0.85rem; }

/* Export buttons */
.export-row {
display: flex;
gap: 12px;
flex-wrap: wrap;
}

.btn-excel {
background: linear-gradient(135deg, #16a34a, #15803d);
color: #fff;
}

.btn-excel:hover { opacity: 0.9; transform: translateY(-1px); }

.btn-word {
background: linear-gradient(135deg, #2563eb, #1d4ed8);
color: #fff;
}

.btn-word:hover { opacity: 0.9; transform: translateY(-1px); }

.btn-csv {
background: rgba(245,158,11,0.15);
color: var(–gold);
border: 1px solid rgba(245,158,11,0.3);
}

.btn-csv:hover { background: rgba(245,158,11,0.25); }

.toast {
position: fixed;
bottom: 24px;
left: 50%;
transform: translateX(-50%) translateY(80px);
background: var(–success);
color: #fff;
padding: 12px 24px;
border-radius: 10px;
font-weight: 700;
font-size: 0.95rem;
transition: transform 0.3s ease;
z-index: 999;
pointer-events: none;
}

.toast.show { transform: translateX(-50%) translateY(0); }

.counter {
color: var(–muted);
font-size: 0.85rem;
margin-top: 8px;
}

.divider {
height: 1px;
background: var(–border);
margin: 20px 0;
}

.no-names-msg {
text-align: center;
color: var(–muted);
padding: 30px;
font-size: 0.95rem;
}
</style>

</head>
<body>
<div class="container">
  <header>
    <h1>📋 منشئ الجداول</h1>
    <p>أضف الأسماء، حدد الأعمدة، وصدّر جدولك بنقرة واحدة</p>
  </header>

  <!-- Step 1: Add Names -->

  <div class="panel">
    <div class="panel-title">الخطوة ١ — أضف الأسماء</div>
    <div class="input-row">
      <input type="text" id="nameInput" placeholder="اكتب الاسم هنا..." autocomplete="off">
      <button class="btn btn-primary" onclick="addName()">➕ إضافة</button>
      <button class="btn btn-danger btn-sm" onclick="clearNames()">🗑 مسح الكل</button>
    </div>
    <div class="names-grid" id="namesGrid">
      <span class="empty-hint">لا توجد أسماء بعد...</span>
    </div>
    <div class="counter" id="counter"></div>
  </div>

  <!-- Step 2: Columns -->

  <div class="panel">
    <div class="panel-title">الخطوة ٢ — حدد أعمدة الجدول</div>
    <div class="input-row">
      <input type="text" id="colInput" placeholder="اسم العمود (مثال: الحضور، الدرجة...)">
      <button class="btn btn-primary" onclick="addColumn()">➕ عمود</button>
    </div>
    <div class="cols-row" id="colsRow">
      <span class="empty-hint" style="font-size:0.85rem;color:var(--muted)">لا توجد أعمدة إضافية</span>
    </div>
    <p style="font-size:0.82rem;color:var(--muted);margin-top:8px">💡 عمود "الاسم" والرقم يُضافان تلقائياً</p>
  </div>

  <!-- Step 3: Preview -->

  <div class="panel">
    <div class="panel-title">الخطوة ٣ — معاينة الجدول</div>
    <div id="previewArea">
      <div class="no-names-msg">أضف أسماء لمعاينة الجدول 👆</div>
    </div>
  </div>

  <!-- Step 4: Export -->

  <div class="panel">
    <div class="panel-title">الخطوة ٤ — تصدير</div>
    <div class="export-row">
      <button class="btn btn-excel" onclick="exportExcel()">📊 تصدير Excel</button>
      <button class="btn btn-word" onclick="exportWord()">📄 تصدير Word</button>
      <button class="btn btn-csv" onclick="exportCSV()">📁 تصدير CSV</button>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
  let names = [];
  let columns = [];

  const nameInput = document.getElementById('nameInput');
  const colInput = document.getElementById('colInput');

  nameInput.addEventListener('keydown', e => { if (e.key === 'Enter') addName(); });
  colInput.addEventListener('keydown', e => { if (e.key === 'Enter') addColumn(); });

  function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 2500);
  }

  function addName() {
    const val = nameInput.value.trim();
    if (!val) return;
    names.push(val);
    nameInput.value = '';
    nameInput.focus();
    renderNames();
    renderPreview();
  }

  function removeName(i) {
    names.splice(i, 1);
    renderNames();
    renderPreview();
  }

  function clearNames() {
    names = [];
    renderNames();
    renderPreview();
  }

  function renderNames() {
    const grid = document.getElementById('namesGrid');
    const counter = document.getElementById('counter');
    if (names.length === 0) {
      grid.innerHTML = '<span class="empty-hint">لا توجد أسماء بعد...</span>';
      counter.textContent = '';
      return;
    }
    grid.innerHTML = names.map((n, i) =>
      `<div class="name-tag">${n}<button onclick="removeName(${i})" title="حذف">✕</button></div>`
    ).join('');
    counter.textContent = `إجمالي الأسماء: ${names.length}`;
  }

  function addColumn() {
    const val = colInput.value.trim();
    if (!val) return;
    columns.push(val);
    colInput.value = '';
    colInput.focus();
    renderColumns();
    renderPreview();
  }

  function removeColumn(i) {
    columns.splice(i, 1);
    renderColumns();
    renderPreview();
  }

  function renderColumns() {
    const row = document.getElementById('colsRow');
    if (columns.length === 0) {
      row.innerHTML = '<span class="empty-hint" style="font-size:0.85rem;color:var(--muted)">لا توجد أعمدة إضافية</span>';
      return;
    }
    row.innerHTML = columns.map((c, i) =>
      `<div class="col-tag">${c}<button onclick="removeColumn(${i})">✕</button></div>`
    ).join('');
  }

  function renderPreview() {
    const area = document.getElementById('previewArea');
    if (names.length === 0) {
      area.innerHTML = '<div class="no-names-msg">أضف أسماء لمعاينة الجدول 👆</div>';
      return;
    }
    const allCols = ['الاسم', ...columns];
    const rows = names.map((n, i) => {
      const cells = allCols.map((c, ci) => `<td>${ci === 0 ? n : ''}</td>`).join('');
      return `<tr><td>${i + 1}</td>${cells}</tr>`;
    }).join('');
    area.innerHTML = `
      <div class="table-wrap">
        <table>
          <thead>
            <tr>
              <th>#</th>
              ${allCols.map(c => `<th>${c}</th>`).join('')}
            </tr>
          </thead>
          <tbody>${rows}</tbody>
        </table>
      </div>`;
  }

  // ── Export Excel (using SheetJS via CDN) ──────────────────────────────────
  function exportExcel() {
    if (names.length === 0) { showToast('⚠️ أضف أسماء أولاً!'); return; }
    const script = document.createElement('script');
    script.src = 'https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js';
    script.onload = () => {
      const allCols = ['#', 'الاسم', ...columns];
      const data = [allCols, ...names.map((n, i) => [i + 1, n, ...columns.map(() => '')])];
      const ws = XLSX.utils.aoa_to_sheet(data);

      // Style column widths
      ws['!cols'] = allCols.map((c, i) => ({ wch: i === 0 ? 5 : Math.max(c.length * 2, 15) }));

      const wb = XLSX.utils.book_new();
      XLSX.utils.book_append_sheet(wb, ws, 'الجدول');
      XLSX.writeFile(wb, 'جدول_الأسماء.xlsx');
      showToast('✅ تم تصدير Excel بنجاح!');
    };
    document.head.appendChild(script);
  }

  // ── Export CSV ────────────────────────────────────────────────────────────
  function exportCSV() {
    if (names.length === 0) { showToast('⚠️ أضف أسماء أولاً!'); return; }
    const allCols = ['#', 'الاسم', ...columns];
    const rows = [allCols, ...names.map((n, i) => [i + 1, n, ...columns.map(() => '')])];
    const csv = rows.map(r => r.map(c => `"${c}"`).join(',')).join('\n');
    const bom = '\uFEFF'; // UTF-8 BOM for Arabic support in Excel
    const blob = new Blob([bom + csv], { type: 'text/csv;charset=utf-8;' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a'); a.href = url; a.download = 'جدول_الأسماء.csv';
    a.click(); URL.revokeObjectURL(url);
    showToast('✅ تم تصدير CSV بنجاح!');
  }

  // ── Export Word (HTML → .doc trick, opens in Word) ───────────────────────
  function exportWord() {
    if (names.length === 0) { showToast('⚠️ أضف أسماء أولاً!'); return; }
    const allCols = ['#', 'الاسم', ...columns];
    const headerRow = allCols.map(c =>
      `<th style="background:#1e40af;color:#fff;padding:10px 14px;border:1px solid #93c5fd;font-family:Arial,sans-serif;">${c}</th>`
    ).join('');
    const bodyRows = names.map((n, i) => {
      const cells = allCols.map((c, ci) => {
        const val = ci === 0 ? i + 1 : ci === 1 ? n : '';
        return `<td style="padding:9px 14px;border:1px solid #ddd;font-family:Arial,sans-serif;">${val}</td>`;
      }).join('');
      return `<tr style="background:${i % 2 === 0 ? '#f0f7ff' : '#fff'}">${cells}</tr>`;
    }).join('');

    const html = `
      <html xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:w="urn:schemas-microsoft-com:office:word" xmlns="http://www.w3.org/TR/REC-html40">
      <head><meta charset="utf-8"><title>جدول الأسماء</title>
      <style>
        body { font-family: Arial, sans-serif; direction: rtl; }
        h2 { color: #1e40af; margin-bottom: 16px; }
        table { border-collapse: collapse; width: 100%; }
      </style></head>

```
  <body>
    <h2>📋 جدول الأسماء</h2>
    <p style="color:#555;margin-bottom:12px;">إجمالي الأسماء: ${names.length}</p>
    <table>
      <thead><tr>${headerRow}</tr></thead>
      <tbody>${bodyRows}</tbody>
    </table>
  </body></html>`;

const blob = new Blob(['\uFEFF' + html], { type: 'application/msword;charset=utf-8' });
const url = URL.createObjectURL(blob);
const a = document.createElement('a'); a.href = url; a.download = 'جدول_الأسماء.doc';
a.click(); URL.revokeObjectURL(url);
showToast('✅ تم تصدير Word بنجاح!');
```

}
</script>

</body>
</html>
