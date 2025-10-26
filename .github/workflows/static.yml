<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>WEBSITE INPUT BARANG ABADI CENTER</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="icon" href="data:;base64,iVBORw0KGgo=">
  <style>
    body {
      background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
    }
    select option[value="R22"] { background-color: #86efac; }
    select option[value="R32"] { background-color: #93c5fd; }
    select option[value="R410"] { background-color: #f9a8d4; }
  </style>
</head>
<body class="text-gray-800 font-inter">
  <div class="max-w-6xl mx-auto p-6">
    <header class="mb-6 text-center">
      <h1 class="text-4xl font-bold text-indigo-800 mb-2">WEBSITE INPUT BARANG ABADI CENTER</h1>
      <p class="text-sm text-gray-700">Aplikasi modern untuk menyimpan dan mengelola data barang Anda.</p>
    </header>

    <section class="grid grid-cols-1 lg:grid-cols-3 gap-6">
      <!-- Form -->
      <div class="bg-white rounded-2xl shadow-lg p-6 border border-gray-200 hover:shadow-2xl transition-all duration-300">
        <h2 class="text-xl font-semibold mb-4 text-indigo-700 flex items-center gap-2">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-5 w-5 text-indigo-500' fill='none' viewBox='0 0 24 24' stroke='currentColor'>
            <path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M12 4v16m8-8H4'/>
          </svg>
          Form Input Barang
        </h2>
        <form id="formBarang" class="space-y-4">
          <input type="hidden" id="editingId" />

          <div>
            <label class="text-sm font-medium">Kode Barang</label>
            <input id="kode" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="KD001" />
          </div>

          <div>
            <label class="text-sm font-medium">Nama Barang</label>
            <input id="nama" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="Contoh: AC LG" required />
          </div>

          <div>
            <label class="text-sm font-medium">Ruangan</label>
            <input id="ruangan" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="Contoh: Ruang Server / Kantor Depan" required />
          </div>

          <div class="grid grid-cols-2 gap-3">
            <div>
              <label class="text-sm font-medium">Harga (Rp)</label>
              <input id="harga" type="number" min="0" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="0" required />
            </div>
            <div>
              <label class="text-sm font-medium">Jumlah</label>
              <input id="jumlah" type="number" min="0" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="0" required />
            </div>
          </div>

          <div>
            <label class="text-sm font-medium">Kondisi Barang</label>
            <select id="kondisi" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" required>
              <option value="">-- Pilih Kondisi --</option>
              <option value="Bagus">Bagus</option>
              <option value="Sedang">Sedang</option>
              <option value="Tidak Bagus">Tidak Bagus</option>
              <option value="Tidak Bagus">Rusak</option>
            </select>
          </div>

          <div>
            <label class="text-sm font-medium">Status Barang</label>
            <select id="status" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" required>
              <option value="">-- Pilih Status --</option>
              <option value="Sedang diperbaiki">Sedang diperbaiki</option>
              <option value="Menunggu Sparepart">Menunggu Sparepart</option>
              <option value="Sudah Oke">Sudah Oke</option>
            </select>
          </div>

          <div>
            <label class="text-sm font-medium">Isi FREON</label>
            <select id="freon" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" required>
              <option value="">-- Pilih Jenis FREON --</option>
              <option value="R22">R22 (Warna Hijau)</option>
              <option value="R32">R32 (Warna Biru)</option>
              <option value="R410">R410 (Warna Pink)</option>
            </select>
          </div>

          <div>
            <label class="text-sm font-medium">Deskripsi (opsional)</label>
            <textarea id="deskripsi" rows="2" class="w-full mt-1 rounded-lg border-gray-300 focus:ring-2 focus:ring-indigo-400 shadow-sm p-2" placeholder="Deskripsi singkat..."></textarea>
          </div>

          <div class="flex gap-2 pt-2">
            <button type="submit" id="btnSimpan" class="flex-1 py-2 bg-indigo-600 hover:bg-indigo-700 text-white rounded-lg shadow transition">Simpan</button>
            <button type="button" id="btnReset" class="flex-1 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg transition">Reset</button>
          </div>
        </form>
      </div>

      <div class="lg:col-span-2 space-y-4">
        <div class="flex items-center gap-3">
          <input id="search" placeholder="Cari kode / nama / ruangan..." class="flex-1 rounded-lg border-gray-300 shadow-sm p-2 focus:ring-2 focus:ring-indigo-400" />
          <button id="btnClearAll" class="px-3 py-2 bg-red-600 hover:bg-red-700 text-white rounded-lg shadow transition">Hapus Semua</button>
        </div>

        <div class="bg-white rounded-2xl shadow-lg p-4 border border-gray-200 overflow-auto">
          <table class="w-full table-auto text-sm" id="tableBarang">
            <thead class="text-left text-indigo-700 border-b">
              <tr>
                <th class="p-2">#</th>
                <th class="p-2">Kode</th>
                <th class="p-2">Nama</th>
                <th class="p-2">Ruangan</th>
                <th class="p-2">Kondisi</th>
                <th class="p-2">Status</th>
                <th class="p-2">FREON</th>
                <th class="p-2">Harga (Rp)</th>
                <th class="p-2">Jumlah</th>
                <th class="p-2">Total (Rp)</th>
                <th class="p-2">Aksi</th>
              </tr>
            </thead>
            <tbody id="tbodyBarang" class="divide-y divide-gray-100"></tbody>
          </table>
          <div id="emptyState" class="text-center text-gray-500 py-6">Belum ada data barang. Tambah data melalui form di kiri.</div>
        </div>
      </div>
    </section>
  </div>

  <script>
    /* 🟢 TAMBAHAN LOGIN CHECK & USER-SPECIFIC STORAGE */
    const activeUser = JSON.parse(localStorage.getItem('activeUser') || 'null');
    if (!activeUser) {
      window.location.href = 'halaman_login.html';
    }

    // Key data disimpan berdasarkan username login
    const LS_KEY = `barang_abadi_${activeUser.username}`;

    // Tombol logout otomatis muncul
    window.addEventListener('DOMContentLoaded', () => {
      const logoutBtn = document.createElement('button');
      logoutBtn.textContent = `Logout (${activeUser.username})`;
      logoutBtn.className = 'fixed top-4 right-4 bg-red-600 text-white px-4 py-2 rounded-lg shadow hover:bg-red-700';
      logoutBtn.onclick = () => {
        if (confirm('Yakin ingin keluar?')) {
          localStorage.removeItem('activeUser');
          window.location.href = 'halaman_login.html';
        }
      };
      document.body.appendChild(logoutBtn);
    });
    /* 🟢 END TAMBAHAN */
    
    const fields = ['kode','nama','ruangan','harga','jumlah','kondisi','status','freon','deskripsi'];

    function uid() { return Date.now().toString(36) + Math.random().toString(36).slice(2,7); }
    function loadData(){ try { return JSON.parse(localStorage.getItem(LS_KEY) || '[]'); } catch(e){ return []; } }
    function saveData(list){ localStorage.setItem(LS_KEY, JSON.stringify(list)); }

    let data = loadData();
    const form = document.getElementById('formBarang');
    const tbody = document.getElementById('tbodyBarang');
    const emptyState = document.getElementById('emptyState');
    const searchEl = document.getElementById('search');
    const btnClearAll = document.getElementById('btnClearAll');
    const editingId = document.getElementById('editingId');
    const btnSimpan = document.getElementById('btnSimpan');
    const btnReset = document.getElementById('btnReset');

    function render(){
      tbody.innerHTML = '';
      const q = searchEl.value.trim().toLowerCase();
      const list = data.filter(d => !q || Object.values(d).some(v => String(v).toLowerCase().includes(q)));
      if(!list.length){ emptyState.style.display='block'; return; }
      emptyState.style.display='none';
      list.forEach((item,i)=>{
        const tr = document.createElement('tr');
        tr.className = i%2?'bg-gray-50':'';
        tr.innerHTML = `
          <td class='p-2'>${i+1}</td>
          <td class='p-2'>${item.kode}</td>
          <td class='p-2'>${item.nama}</td>
          <td class='p-2'>${item.ruangan}</td>
          <td class='p-2'>${item.kondisi}</td>
          <td class='p-2'>${item.status}</td>
          <td class='p-2 font-semibold text-${item.freon==='R22'?'green':item.freon==='R32'?'blue':'pink'}-600'>${item.freon}</td>
          <td class='p-2'>${item.harga.toLocaleString('id-ID')}</td>
          <td class='p-2'>${item.jumlah}</td>
          <td class='p-2'>${(item.harga*item.jumlah).toLocaleString('id-ID')}</td>
          <td class='p-2 space-x-1'>
            <button data-id='${item.id}' class='editBtn px-2 py-1 bg-yellow-500 text-white rounded text-xs hover:bg-yellow-600'>Edit</button>
            <button data-id='${item.id}' class='deleteBtn px-2 py-1 bg-red-500 text-white rounded text-xs hover:bg-red-600'>Hapus</button>
          </td>`;
        tbody.appendChild(tr);
      });
      document.querySelectorAll('.deleteBtn').forEach(btn=>btn.onclick=del);
      document.querySelectorAll('.editBtn').forEach(btn=>btn.onclick=edit);
    }

    form.onsubmit = e => {
      e.preventDefault();
      const obj = {};
      fields.forEach(f => obj[f] = document.getElementById(f).value);
      obj.harga = Number(obj.harga||0);
      obj.jumlah = Number(obj.jumlah||0);

      if(editingId.value){ // mode edit
        const idx = data.findIndex(x=>x.id===editingId.value);
        if(idx>-1){ data[idx] = {...data[idx], ...obj}; }
        editingId.value = '';
        btnSimpan.textContent = 'Simpan';
      } else { // mode tambah baru
        obj.id = uid();
        obj.created = Date.now();
        data.push(obj);
      }
      saveData(data);
      form.reset();
      render();
    }

    function del(e){
      if(!confirm('Hapus data ini?')) return;
      const id = e.currentTarget.dataset.id;
      data = data.filter(x=>x.id!==id);
      saveData(data);
      render();
    }

    function edit(e){
      const id = e.currentTarget.dataset.id;
      const item = data.find(x=>x.id===id);
      if(!item) return;
      fields.forEach(f => document.getElementById(f).value = item[f]);
      editingId.value = id;
      btnSimpan.textContent = 'Update';
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    btnReset.onclick = ()=>{ form.reset(); editingId.value=''; btnSimpan.textContent='Simpan'; };
    searchEl.oninput = render;
    btnClearAll.onclick = ()=>{ if(confirm('Hapus semua data?')){ data=[]; saveData(data); render(); } };

    render();
  </script>
</body>
</html>
