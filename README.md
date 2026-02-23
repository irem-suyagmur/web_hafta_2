# 📦 BEUShareBox

BEUShareBox, sınıf içi ürün paylaşımı ve topluluk etkileşimi için geliştirilmiş modern bir web uygulamasıdır. Kullanıcılar ürünlerini paylaşabilir, beğenebilir ve yorum yapabilir.

## 🌟 Özellikler

- **Ürün Paylaşımı**: Başlık, açıklama, fiyat ve kategori bilgileriyle ürün ekleme
- **Kategoriler**: Elektronik, Moda, Kitaplar, Ev & Bahçe, Spor ve Diğer
- **Arama Fonksiyonu**: Ürünleri başlık ve açıklamalarında arama
- **Filtreleme**: Kategoriye göre ürün filtreleme
- **Beğeni Sistemi**: Ürünleri beğenme/beğenmeme
- **Yorum Sistemi**: Ürünlere yorum ekleme
- **İstatistikler**: Toplam ürün ve beğeni sayısı
- **LocalStorage**: Veriler tarayıcıda kalıcı olarak saklanır
- **Responsive Tasarım**: Mobil ve masaüstü uyumlu arayüz

## 🚀 Kurulum

### Gereksinimler

- Modern bir web tarayıcısı (Chrome, Firefox, Safari, Edge)
- Herhangi bir sunucu veya ek yazılım gerektirmez

### Kullanım

1. Projeyi bilgisayarınıza indirin:
```bash
git clone [repository-url]
```

2. Proje klasörüne gidin:
```bash
cd "uygulama 2"
```

3. `index.html` dosyasını bir web tarayıcısında açın:
   - Dosyaya çift tıklayın, veya
   - Sağ tıklayıp "Birlikte Aç" > "Tarayıcı" seçin

## 📁 Proje Yapısı

```
uygulama 2/
│
├── index.html          # Ana HTML dosyası
├── style.css           # Stil ve tasarım dosyası
├── app.js              # JavaScript mantık ve fonksiyonlar
└── README.md           # Proje dokümantasyonu
```

## 💻 Teknolojiler

- **HTML5**: Yapısal içerik
- **CSS3**: Modern tasarım ve animasyonlar
  - CSS Variables (Custom Properties)
  - Flexbox & Grid Layout
  - Responsive Media Queries
  - Animasyonlar ve Geçişler
- **Vanilla JavaScript (ES6+)**: 
  - LocalStorage API
  - DOM Manipulation
  - Event Handling
  - Array Methods (filter, map, reduce)

## 🎯 Kullanım Kılavuzu

### Ürün Ekleme

1. "Add New Product" formunu doldurun
2. Ürün başlığı (zorunlu)
3. Ürün açıklaması (zorunlu, max 500 karakter)
4. Fiyat (zorunlu, $ cinsinden)
5. Kategori seçin (zorunlu)
6. "Add Product" butonuna tıklayın

### Ürün Arama ve Filtreleme

- **Arama**: Arama kutusuna yazarak ürünleri başlık ve açıklamalarında arayın
- **Kategori Filtresi**: Dropdown menüden kategori seçerek filtreleyin
- Her iki filtre de aynı anda çalışır

### Ürünlerle Etkileşim

- **Beğeni**: ❤️ ikonuna tıklayarak ürünü beğenin/beğeniyi kaldırın
- **Yorum**: Yorum kutusuna yazıp "Add Comment" ile yorum ekleyin
- **Silme**: 🗑️ ikonuna tıklayarak ürünü silin

## 🎨 Tasarım Özellikleri

- **Modern UI**: Gradient renkler ve gölge efektleri
- **Smooth Transitions**: Yumuşak geçiş animasyonları
- **Color Scheme**:
  - Primary: Pink (#ec4899)
  - Accent: Amber (#f59e0b)
  - Success: Green (#10b981)
  - Danger: Red (#ef4444)

## 🔧 Özelleştirme

### Renkleri Değiştirme

`style.css` dosyasındaki CSS değişkenlerini düzenleyin:

```css
:root {
    --primary-color: #ec4899;
    --accent-color: #f59e0b;
    /* Diğer renkler... */
}
```

### Yeni Kategori Ekleme

`index.html` dosyasında kategori select elementine yeni option ekleyin:

```html
<select id="productCategory" required>
    <option value="yeni-kategori">Yeni Kategori</option>
</select>
```

## 📊 Veri Yönetimi

Tüm veriler tarayıcınızın LocalStorage'ında saklanır:

- **Anahtar**: `beusharebox_products`
- **Format**: JSON array
- **Temizleme**: Tarayıcı verilerini temizlediğinizde silinir

### Verileri Yedekleme

Tarayıcı konsolunda şu komutu çalıştırın:
```javascript
console.log(localStorage.getItem('beusharebox_products'));
```

## 🐛 Bilinen Sınırlamalar

- Veriler yalnızca yerel tarayıcıda saklanır (backend yok)
- Kullanıcı yönetimi yoktur (herkes aynı verileri görür)
- Resim yükleme desteği yoktur
- Maksimum LocalStorage kapasitesi: ~5-10MB

## 🚀 Gelecek Geliştirmeler

- [ ] Kullanıcı kimlik doğrulama sistemi
- [ ] Ürün görseli yükleme
- [ ] Sıralama seçenekleri (fiyat, tarih, beğeni)
- [ ] Dışa aktarma/İçe aktarma özelliği
- [ ] Dark mode desteği
- [ ] Backend entegrasyonu

## 👨‍💻 Geliştirici Notları

### Kod Yapısı

**app.js** ana fonksiyonlar:
- `renderProducts()`: Ürünleri DOM'a render eder
- `handleAddProduct()`: Yeni ürün ekleme
- `handleLike()`: Beğeni sistemini yönetir
- `handleAddComment()`: Yorum ekleme
- `handleDelete()`: Ürün silme
- `handleSearch()`: Arama fonksiyonu
- `handleFilter()`: Kategori filtreleme

### LocalStorage Yapısı

```javascript
{
  "id": "unique-id",
  "title": "Product Title",
  "description": "Product Description",
  "price": 99.99,
  "category": "electronics",
  "likes": 5,
  "comments": [
    {
      "id": "comment-id",
      "text": "Great product!",
      "createdAt": "2026-02-23T..."
    }
  ],
  "createdAt": "2026-02-23T..."
}
```

## 📝 Lisans

Bu proje eğitim amaçlı geliştirilmiştir.

## 🤝 Katkıda Bulunma

1. Projeyi fork edin
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branch'inizi push edin (`git push origin feature/AmazingFeature`)
5. Pull Request oluşturun

## 📧 İletişim

Proje Hakkında Sorularınız için: [contact-info]

---

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın!
