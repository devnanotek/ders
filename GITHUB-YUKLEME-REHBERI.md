# 🚀 GitHub'a Yükleme Rehberi

Bu dokuman, projenizi GitHub'a yüklemek için adım adım talimatlar içerir.

## 📋 Ön Hazırlık

### 1. README.md Dosyasını Özelleştirin

`README.md` dosyasını açın ve şu yerleri değiştirin:

```markdown
# Değiştirilmesi gerekenler:

✅ TAMAMLANDI! Tüm linkler devnanotek olarak güncellendi.

Repository URL: https://github.com/devnanotek/ders
GitHub Pages: https://devnanotek.github.io/ders/
```

### 2. Git Kurulumu Kontrolü

Terminal/CMD'de kontrol edin:

```bash
git --version
```

Eğer yüklü değilse: [Git İndirin](https://git-scm.com/downloads)

---

## 🎯 Adım Adım GitHub'a Yükleme

### ADIM 1: GitHub'da Repository Oluşturun

1. [GitHub](https://github.com) hesabınıza giriş yapın
2. Sağ üst köşeden **"+"** → **"New repository"**
3. Repository ayarları:
   - **Repository name**: `ders`
   - **Description**: 
     ```
     Mardin Artuklu Üniversitesi Bilgisayar Programcılığı dersi notları ve interaktif soru çözümleri
     ```
   - **Public** seçin (herkesin görmesi için)
   - **Add a README file** → ✅ **İŞARETLEMEYİN** (zaten var)
   - **Add .gitignore** → ✅ **İŞARETLEMEYİN** (zaten var)
   - **Choose a license** → **MIT License** seçin
4. **Create repository** butonuna tıklayın

### ADIM 2: Projenizi Git'e Hazırlayın

Terminal/CMD'yi açın ve proje klasörüne gidin:

```bash
# Windows için:
cd C:\Users\NANOTEK\Desktop\ders

# Git'i başlatın
git init
```

### ADIM 3: Dosyaları Git'e Ekleyin

```bash
# Tüm dosyaları ekle
git add .

# İlk commit
git commit -m "feat: İlk commit - Ders notları projesi eklendi"
```

### ADIM 4: GitHub Repository'ye Bağlayın

GitHub'da oluşturduğunuz repository sayfasında gösterilen komutu kopyalayın:

```bash
# devnanotek repository'si için
git remote add origin https://github.com/devnanotek/ders.git

# Ana branch'i main olarak ayarlayın
git branch -M main

# GitHub'a yükleyin
git push -u origin main
```

### ADIM 5: GitHub'da Kontrol Edin

1. GitHub repository sayfanızı yenileyin
2. Tüm dosyaların yüklendiğini kontrol edin
3. README.md'nin düzgün görüntülendiğinden emin olun

---

## 🌐 GitHub Pages ile Canlı Yayına Alma (Opsiyonel)

Projenizi canlı bir website olarak yayınlamak için:

### ADIM 1: GitHub Pages Aktifleştirin

1. Repository sayfanızda **Settings** sekmesine gidin
2. Sol menüden **Pages** seçin
3. **Source** bölümünden:
   - Branch: **main** seçin
   - Folder: **/ (root)** seçin
4. **Save** butonuna tıklayın

### ADIM 2: Yayına Alındığında

- 1-2 dakika içinde siteniz hazır olacak
- URL: `https://devnanotek.github.io/ders/`
- Bu URL README.md'de zaten güncellendi! ✅

### ADIM 3: README.md Güncellendi ✅

Demo linki zaten güncellenmiş durumda:

```markdown
[Demo](https://devnanotek.github.io/ders/)
```

Tüm linkler devnanotek olarak düzenlendi!

---

## 🏷️ Repository Ayarları

### Topics (Etiketler) Ekleyin

1. Repository ana sayfasında **⚙️ (Settings)** yanındaki **About** → ⚙️ ikonuna tıklayın
2. **Topics** bölümüne şunları ekleyin:
   ```
   education, html-css-javascript, turkish, university, 
   programming, web-design, student-project, open-source, 
   study-notes, interactive, mardin-artuklu
   ```
3. **Website** bölümüne GitHub Pages URL'nizi ekleyin:
   ```
   https://devnanotek.github.io/ders/
   ```
4. **Save changes**

### Description Zaten Eklenmiş ✅

About kısmında:
```
Bilgisayar Programlama Bölümü ( web tasarım ve programlama temelleri dersleri)
```

---

## 📸 Ekran Görüntüleri Eklemek (Opsiyonel)

### ADIM 1: Klasör Oluşturun

```bash
mkdir screenshots
```

### ADIM 2: Ekran Görüntülerini Alın

1. Ana sayfanın ekran görüntüsünü alın → `anasayfa.png`
2. Programlama sayfasının → `programlama.png`
3. Web Tasarım sayfasının → `web-tasarim.png`

### ADIM 3: Klasöre Kaydedin

Screenshots'ları `screenshots/` klasörüne kaydedin.

### ADIM 4: README.md'ye Ekleyin

```markdown
### Ekran Görüntüleri

<div align="center">
  <img src="screenshots/anasayfa.png" alt="Ana Sayfa" width="800"/>
  <br>
  <img src="screenshots/programlama.png" alt="Programlama" width="800"/>
  <br>
  <img src="screenshots/web-tasarim.png" alt="Web Tasarım" width="800"/>
</div>
```

### ADIM 5: GitHub'a Yükleyin

```bash
git add screenshots/
git add README.md
git commit -m "docs: Ekran görüntüleri eklendi"
git push
```

---

## 🔄 Güncelleme Yapmak

İleride değişiklik yaptığınızda:

```bash
# Değişiklikleri kaydet
git add .

# Commit mesajı yaz
git commit -m "fix: Mobil görünüm düzeltildi"

# GitHub'a gönder
git push
```

---

## ⚠️ Sık Karşılaşılan Sorunlar

### Sorun 1: "Permission denied"

**Çözüm**: SSH key oluşturun veya HTTPS kullanın

```bash
# HTTPS kullanarak yeniden deneyin
git remote set-url origin https://github.com/devnanotek/ders.git
```

### Sorun 2: "Updates were rejected"

**Çözüm**: Önce GitHub'daki değişiklikleri çekin

```bash
git pull origin main --rebase
git push
```

### Sorun 3: Türkçe karakter sorunu

**Çözüm**: Git'te encoding ayarını yapın

```bash
git config --global core.quotepath false
```

---

## 📱 Mobil Uygulama ile Yönetmek

GitHub mobil uygulaması ile repository'nizi takip edebilirsiniz:

- 📱 [GitHub Mobile - iOS](https://apps.apple.com/app/github/id1477376905)
- 📱 [GitHub Mobile - Android](https://play.google.com/store/apps/details?id=com.github.android)

---

## ✅ Kontrol Listesi

Yüklemeden önce kontrol edin:

- [x] README.md'de kullanıcı adı değiştirildi ✅
- [x] Email adresi güncellendi ✅
- [ ] LICENSE dosyası mevcut
- [ ] .gitignore dosyası mevcut
- [ ] Tüm HTML dosyaları çalışıyor
- [ ] Responsive tasarım test edildi
- [ ] Türkçe karakterler düzgün görünüyor

---

## 🎯 Başarı!

Projeniz artık GitHub'da! 🎉

### Şimdi ne yapabilirsiniz?

1. **Paylaşın**: Arkadaşlarınıza linki gönderin
2. **Geliştirin**: Yeni özellikler ekleyin
3. **Katkı Alın**: Pull request'leri kabul edin
4. **İstatistikleri İzleyin**: Star ve fork sayılarını takip edin

---

## 📞 Yardım

Sorun yaşarsanız:

1. [GitHub Docs](https://docs.github.com/tr)
2. [Git Dokümantasyonu](https://git-scm.com/doc)
3. Google'da "git [sorun]" araması yapın

---

**Başarılar! 🚀**

Hazırlayan: İslam ERGÜN  
Tarih: 14 Kasım 2024

