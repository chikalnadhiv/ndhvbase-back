# PWA Setup - Ndhvbase

## ✅ Fitur yang Sudah Diimplementasikan

### 1. **Logo & Favicon**
- ✅ Logo ndhvbase telah digunakan sebagai favicon dan icon aplikasi
- ✅ Icon tersedia dalam berbagai ukuran: 32x32, 72x72, 96x96, 128x128, 144x144, 152x152, 180x180, 192x192, 384x384, 512x512
- ✅ Icon disimpan di `/public/icons/`

### 2. **PWA (Progressive Web App)**
- ✅ Aplikasi dapat diinstall di handphone dan desktop
- ✅ Manifest.json sudah dikonfigurasi
- ✅ Service Worker otomatis di-generate oleh next-pwa
- ✅ Offline support
- ✅ Install prompt otomatis muncul setelah 3 detik

### 3. **Metadata**
- ✅ SEO-friendly metadata
- ✅ Open Graph tags untuk social media sharing
- ✅ Twitter Card support
- ✅ Apple Web App support
- ✅ Theme color untuk dark/light mode

## 📱 Cara Install di Handphone

### Android (Chrome/Edge):
1. Buka website di Chrome atau Edge
2. Tunggu beberapa detik, akan muncul prompt "Install Ndhvbase App"
3. Klik "Install Now" atau
4. Tap menu (⋮) → "Install app" atau "Add to Home screen"
5. Aplikasi akan muncul di home screen

### iOS (Safari):
1. Buka website di Safari
2. Tap tombol Share (kotak dengan panah ke atas)
3. Scroll ke bawah dan tap "Add to Home Screen"
4. Tap "Add"
5. Aplikasi akan muncul di home screen

### Desktop (Chrome/Edge):
1. Buka website di Chrome atau Edge
2. Klik icon install di address bar (sebelah kanan)
3. Atau klik menu (⋮) → "Install Ndhvbase"
4. Aplikasi akan terbuka sebagai standalone app

## 🔧 Generate Icons Ulang

Jika ingin mengganti logo atau regenerate icons:

```bash
# Edit logo di /public/assets/ndhvlogo.jpeg
# Kemudian jalankan:
node scripts/generate-icons.js
```

## 🚀 Build untuk Production

```bash
npm run build
npm start
```

Service worker hanya aktif di production mode. Di development mode, PWA dinonaktifkan untuk mempermudah development.

## 📝 File-file Penting

- `/public/manifest.json` - PWA manifest
- `/public/icons/` - Icon dalam berbagai ukuran
- `/scripts/generate-icons.js` - Script untuk generate icons
- `/components/InstallPrompt.tsx` - Komponen install prompt
- `/app/layout.tsx` - Metadata dan PWA setup
- `/next.config.ts` - Konfigurasi next-pwa

## 🎨 Customization

### Mengubah Warna Theme:
Edit di `/public/manifest.json`:
```json
{
  "theme_color": "#5e6ad2",
  "background_color": "#000000"
}
```

### Mengubah Nama Aplikasi:
Edit di `/public/manifest.json`:
```json
{
  "name": "Ndhvbase - Premium Web Development",
  "short_name": "Ndhvbase"
}
```

## ✨ Features

- 📱 Installable di semua platform (Android, iOS, Desktop)
- 🔄 Offline support dengan service worker
- 🎨 Custom install prompt dengan UI yang menarik
- 🌓 Dark/Light mode support
- ⚡ Fast loading dengan caching strategy
- 🔔 Install prompt yang user-friendly (muncul setelah 3 detik)
- 💾 Remember user preference (jika dismiss, tidak muncul lagi selama 7 hari)
