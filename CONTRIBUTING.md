# 🤝 Katkıda Bulunma Rehberi

Projeye katkıda bulunmak istediğiniz için teşekkür ederiz! Bu rehber, katkı sürecini kolaylaştırmak için hazırlanmıştır.

## 📋 İçindekiler

- [Davranış Kuralları](#davranış-kuralları)
- [Nasıl Katkıda Bulunabilirim?](#nasıl-katkıda-bulunabilirim)
- [Geliştirme Süreci](#geliştirme-süreci)
- [Kod Standartları](#kod-standartları)
- [Commit Mesajları](#commit-mesajları)

---

## 🤝 Davranış Kuralları

Bu proje herkese açıktır ve saygılı bir topluluk ortamı sağlamayı amaçlar.

### Beklentilerimiz:
- ✅ Saygılı ve yapıcı iletişim
- ✅ Farklı görüşlere açık olma
- ✅ Eleştirileri yapıcı bir şekilde kabul etme
- ✅ Topluluğun iyiliğini ön planda tutma

### Kabul Edilemez Davranışlar:
- ❌ Hakaret veya aşağılayıcı yorumlar
- ❌ Kişisel saldırılar
- ❌ Spam veya reklam
- ❌ Telif hakkı ihlali

---

## 🚀 Nasıl Katkıda Bulunabilirim?

### 1. Hata Bildirimi (Bug Report)

Bir hata bulduysanız:

1. [Issues](https://github.com/devnanotek/ders/issues) sayfasına gidin
2. "New Issue" butonuna tıklayın
3. Hatayı detaylı açıklayın:
   - Ne olması gerekiyordu?
   - Ne oldu?
   - Hangi tarayıcı/cihaz?
   - Ekran görüntüsü (varsa)

### 2. Özellik Önerisi (Feature Request)

Yeni bir özellik öneriyorsanız:

1. Önce Issues'da benzer bir öneri olup olmadığını kontrol edin
2. Yeni issue açın ve şunları belirtin:
   - Özelliğin ne işe yarayacağı
   - Nasıl çalışması gerektiği
   - Neden faydalı olacağı

### 3. Kod Katkısı (Pull Request)

Kod katkısında bulunmak için:

1. Repository'yi **fork** edin
2. Yeni bir **branch** oluşturun
3. Değişikliklerinizi yapın
4. **Commit** edin
5. **Push** edin
6. **Pull Request** açın

---

## 💻 Geliştirme Süreci

### Adım 1: Fork ve Clone

```bash
# Fork ettikten sonra:
git clone https://github.com/sizin-kullaniciadi/ders.git
cd ders
```

### Adım 2: Branch Oluştur

```bash
git checkout -b feature/yeni-ozellik
# veya
git checkout -b fix/hata-duzeltmesi
```

### Adım 3: Değişiklikleri Yap

- Kodunuzu yazın
- Test edin
- HTML validator'dan geçirin ([W3C Validator](https://validator.w3.org/))

### Adım 4: Commit

```bash
git add .
git commit -m "feat: Yeni özellik eklendi"
```

### Adım 5: Push ve PR

```bash
git push origin feature/yeni-ozellik
```

GitHub'da Pull Request açın.

---

## 📝 Kod Standartları

### HTML Standartları

```html
<!-- İYİ ✅ -->
<div class="container">
    <h1>Başlık</h1>
    <p>Paragraf metni</p>
</div>

<!-- KÖTÜ ❌ -->
<div class="container"><h1>Başlık</h1><p>Paragraf</p></div>
```

**Kurallar:**
- Semantic HTML kullanın
- Alt attribute her img için zorunlu
- ARIA labels kullanın
- Girintileme: Tab (4 boşluk)

### CSS Standartları

```css
/* İYİ ✅ */
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}

/* KÖTÜ ❌ */
.container{display:flex;justify-content:center;align-items:center}
```

**Kurallar:**
- Class isimleri kebab-case: `.main-header`
- Tek satır CSS kullanmayın (okunabilirlik için)
- Renk kodları büyük harf: `#FF0000` yerine `#ff0000`

### JavaScript Standartları

```javascript
// İYİ ✅
function copyCode(button) {
    const codeBlock = button.closest('.code-container');
    // ...
}

// KÖTÜ ❌
function copyCode(button){const codeBlock=button.closest('.code-container');}
```

**Kurallar:**
- camelCase kullanın
- Noktalı virgül kullanın
- Modern ES6+ syntax
- Yorumlar Türkçe olabilir

---

## 💬 Commit Mesajları

### Format

```
<tip>: <kısa açıklama>

<detaylı açıklama> (opsiyonel)
```

### Commit Tipleri

- `feat`: Yeni özellik
- `fix`: Hata düzeltme
- `docs`: Dokümantasyon
- `style`: CSS/tasarım değişiklikleri
- `refactor`: Kod iyileştirme
- `test`: Test ekleme
- `chore`: Genel işler

### Örnekler

```bash
# İYİ ✅
git commit -m "feat: Karanlık mod eklendi"
git commit -m "fix: Mobilde menü düzeltildi"
git commit -m "docs: README güncellendi"

# KÖTÜ ❌
git commit -m "değişiklikler"
git commit -m "bug fix"
```

---

## 🧪 Test Etme

Pull Request açmadan önce:

1. **Tarayıcı Uyumluluğu**: Chrome, Firefox, Safari, Edge
2. **Responsive Test**: Mobil, tablet, masaüstü
3. **HTML Validation**: [W3C Validator](https://validator.w3.org/)
4. **Erişilebilirlik**: ARIA attributes kontrol
5. **Performans**: Sayfanın hızlı yüklendiğinden emin olun

---

## 📚 Ders İçeriği Eklemek

Yeni bir ders eklemek istiyorsanız:

1. Mevcut yapıyı takip edin
2. Interaktif örnekler ekleyin
3. Kod ve çıktı sekmelerini kullanın
4. Syntax highlighting ekleyin
5. Responsive olduğundan emin olun

### Şablon

```html
<article class="question-card">
    <div class="question-header">
        <span class="question-number">Soru X</span>
        <span>Soru başlığı</span>
    </div>
    
    <ul class="nav nav-tabs">
        <!-- Sekmeler -->
    </ul>
    
    <div class="tab-content">
        <!-- İçerik -->
    </div>
</article>
```

---

## 🎨 Tasarım Kuralları

- **Renk Paleti**: Mevcut gradient'ları (#667eea, #764ba2) kullanın
- **Tipografi**: Poppins font ailesini tercih edin
- **İkonlar**: Bootstrap Icons kullanın
- **Spacing**: Consistent margin/padding
- **Animasyonlar**: Smooth transitions (0.3s)

---

## ❓ Sorular?

- 💬 [GitHub Discussions](https://github.com/devnanotek/ders/discussions)
- 🐛 [Issues](https://github.com/devnanotek/ders/issues)
- 🐙 [GitHub Profile](https://github.com/devnanotek)

---

## 🙏 Teşekkürler!

Her katkı, projeyi daha iyi hale getirir. Zaman ayırdığınız için teşekkür ederiz!

**Happy Coding! 💻✨**

