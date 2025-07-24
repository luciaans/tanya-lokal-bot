# 💖 TanyaLokal - Asisten Pintar Offline

**"Asisten pintar, selalu siap — bahkan tanpa internet."**

TanyaLokal adalah aplikasi web chat AI yang berjalan secara lokal menggunakan Ollama. Dirancang khusus untuk memberikan jawaban informatif dalam bahasa Indonesia tentang berbagai topik kehidupan sehari-hari seperti kesehatan, pendidikan, teknologi, dan kuliner.

## ✨ Fitur

- 🤖 **AI Chat Interface** - Interface chat yang modern dan responsif
- 🌐 **Offline First** - Bekerja tanpa koneksi internet (setelah setup)
- 🇮🇩 **Bahasa Indonesia** - Dioptimalkan untuk percakapan dalam bahasa Indonesia
- 💡 **Saran Pertanyaan** - Tombol saran untuk memulai percakapan
- 📱 **Responsive Design** - Tampil sempurna di desktop dan mobile
- 🎨 **Modern UI** - Desain gradien pink yang menarik dengan animasi halus
- ⚡ **Real-time Status** - Indikator status koneksi Ollama

## 🚀 Quick Start

### Prasyarat

1. **Ollama** - Pastikan Ollama sudah terinstall di sistem Anda
   ```bash
   # Install Ollama (Linux/macOS)
   curl -fsSL https://ollama.ai/install.sh | sh
   
   # Windows: Download dari https://ollama.com/download
   ```

2. **Model AI** - Download model Mistral
   ```bash
   ollama pull mistral:latest
   ```

### Instalasi

1. Clone repository ini:
   ```bash
   git clone https://github.com/username/tanyalokal.git
   cd tanyalokal
   ```

2. Jalankan Ollama server:
   ```bash
   ollama serve
   ```

3. Buka file `index.html` di browser Anda atau gunakan web server lokal:
   ```bash
   # Menggunakan Python
   python -m http.server 8000
   
   # Menggunakan Node.js
   npx serve .
   
   # Atau buka langsung file index.html di browser
   ```

4. Akses aplikasi di `http://localhost:8000` (jika menggunakan web server)

## 🛠️ Konfigurasi

### Mengubah Model AI

Edit variabel `MODEL_NAME` di file HTML:

```javascript
const MODEL_NAME = 'mistral:latest'; // Ganti dengan model pilihan Anda
```

Model yang direkomendasikan:
- `mistral:latest` (default)
- `llama2:latest`
- `codellama:latest`
- `qwen:latest`

### Mengubah URL Ollama

Jika Ollama berjalan di port atau host yang berbeda:

```javascript
const OLLAMA_API_URL = 'http://localhost:11434/api/generate'; // Sesuaikan URL
```

## 📖 Cara Penggunaan

1. **Mulai Percakapan** - Ketik pertanyaan di kolom input atau klik salah satu tombol saran
2. **Topik yang Didukung**:
   - 🌧️ Cuaca dan alam
   - 🏃‍♀️ Kesehatan dan olahraga
   - 🤖 Teknologi dan AI
   - 📚 Pendidikan dan belajar
   - 🍳 Kuliner dan resep
   - Dan topik umum lainnya

3. **Indikator Status**:
   - 🟢 Hijau: Ollama terhubung dengan baik
   - 🟡 Kuning: Koneksi bermasalah
   - 🔴 Merah: Tidak dapat terhubung ke Ollama

## 🔧 Troubleshooting

### Ollama Tidak Terhubung

1. Pastikan Ollama service berjalan:
   ```bash
   ollama serve
   ```

2. Cek apakah port 11434 terbuka:
   ```bash
   curl http://localhost:11434/api/tags
   ```

3. Restart Ollama jika diperlukan

### Model Tidak Tersedia

```bash
# List model yang tersedia
ollama list

# Download model yang diperlukan
ollama pull mistral:latest
```

### CORS Error

Jika mengalami CORS error, jalankan aplikasi melalui web server lokal, jangan buka file HTML secara langsung.

## 🎨 Kustomisasi

### Mengubah Tema Warna

Edit variabel CSS di bagian `:root` untuk mengubah skema warna:

```css
:root {
  --primary-color: #ff6b9d;
  --secondary-color: #c44569;
  --background-gradient: linear-gradient(180deg, #ffe6ec 0%, #fff4f6 100%);
}
```

### Menambah Pertanyaan Saran

Tambahkan tombol saran baru di bagian HTML:

```html
<div class="suggestion-btn" onclick="sendSuggestion('Pertanyaan baru')">
  🆕 Topik Baru
</div>
```

## 📱 Kompatibilitas

- ✅ Chrome/Chromium 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan:

1. Fork repository ini
2. Buat branch untuk fitur baru (`git checkout -b feature/fitur-baru`)
3. Commit perubahan (`git commit -am 'Tambah fitur baru'`)
4. Push ke branch (`git push origin feature/fitur-baru`)
5. Buat Pull Request

---

**Made by Lucians**
