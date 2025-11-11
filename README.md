# 💸 Investasi Titip Modal Bot

Sistem investasi berbasis **Telegram Bot + Dashboard Web** untuk memudahkan investor menitipkan modal dan admin memantau transaksi.  
Dibuat dengan Node.js, Express, dan integrasi API Telegram.

---

## 🚀 Fitur Utama
✅ Login & Registrasi user (Nama, Email, Nomor Telepon)  
✅ Dashboard investasi seperti tampilan di foto (UI biru modern)  
✅ Admin menerima notifikasi transaksi lewat bot Telegram  
✅ Sistem Top-Up & Konfirmasi Investasi  
✅ Backend siap deploy 24 jam di Render  

---

## 🧩 Instalasi di Lokal

### 1️⃣ Clone atau download repo
```bash
git clone https://github.com/<USERNAME>/investasi-titipmodal.git
cd investasi-titipmodal
```

### 2️⃣ Install dependencies
```bash
npm install
```

### 3️⃣ Buat file `.env`
Isi dengan konfigurasi berikut:
```
BOT_TOKEN=8125211356:AAENry5bVESxsWix2YZn16nliGdW-CDrZAg
ADMIN_CHAT_ID=7793991218
PORT=10000
```

### 4️⃣ Jalankan di lokal
```bash
npm start
```

Lalu buka browser:
```
http://localhost:10000
```

---

## ☁️ Deploy ke Render (Gratis)

1. Login ke [Render.com](https://render.com)
2. Klik **“New +” → Web Service**
3. Pilih repo `investasi-titipmodal`
4. Isi:
   - **Build command:** `npm install`
   - **Start command:** `npm start`
5. Tambahkan environment variable:
   ```
   BOT_TOKEN=... (token bot Telegram kamu)
   ADMIN_CHAT_ID=... (chat ID admin)
   PORT=10000
   ```
6. Klik **Create Web Service**

Tunggu 1-2 menit hingga status berubah jadi ✅ *Live*

Render akan memberi URL seperti:
```
https://investasi-titipmodal.onrender.com
```

---

## 🤖 Setup Telegram Bot
1. Buka Telegram, cari **@BotFather**
2. Ketik `/newbot` dan ikuti instruksi untuk membuat bot
3. Salin **Bot Token**
4. Ubah `BOT_TOKEN` di `.env` dengan token kamu
5. Dapatkan Chat ID kamu di Telegram (bisa lewat [@userinfobot](https://t.me/userinfobot))
6. Masukkan Chat ID ke variabel `ADMIN_CHAT_ID`

---

## 🧠 Teknologi yang Digunakan
- Node.js (Express)
- Telegram Bot API
- HTML + CSS (Frontend Dashboard)
- Render (Hosting 24 jam)

---

## 🧑‍💻 Pengembang
**Bayu & GPT-5 Developer Partner**  
Project open-source: silakan fork & kembangkan 💙
