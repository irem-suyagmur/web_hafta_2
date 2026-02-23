# BEUShareBox 📦

[cite_start]BEUShareBox, kullanıcıların keşfettikleri veya sahip oldukları ürünleri toplulukla paylaşabilecekleri bir mini sosyal medya platformudur[cite: 7]. [cite_start]Bitlis Eren Üniversitesi Bilgisayar Mühendisliği Bölümü "Web Tabanlı Programlama" dersi sınıf içi uygulaması olarak, tek sayfalık web uygulaması (SPA) mantığıyla geliştirilmiştir[cite: 2, 3, 5, 20].

## 🚀 Özellikler

[cite_start]Bu proje, sınıf içi etkinlik kapsamında istenen tüm temel gereksinimleri (10 tam puanlık) eksiksiz olarak karşılamaktadır[cite: 21, 22]:

* [cite_start]**Ürün Paylaşımı:** Kullanıcılar ürün başlığı, açıklaması, fiyatı ve kategorisi ile yeni ürün kartları oluşturabilir [cite: 137-141].
* [cite_start]**Etkileşim (Beğeni & Yorum):** Her ürün kartında bağımsız çalışan beğeni (❤️) sayacı ve o ürüne özel yorum ekleme/görüntüleme alanı bulunur[cite: 155, 156].
* [cite_start]**Gelişmiş Arama ve Filtreleme:** Kategori bazlı filtreleme yapılabilir ve arama çubuğu ile ürün başlıkları/açıklamaları içinde anlık arama gerçekleştirilebilir[cite: 157, 158].
* [cite_start]**Güvenli Silme:** Ürünler, yanlışlıkla silinmeleri önlemek amacıyla onay penceresi (`confirm()`) aracılığıyla kaldırılır[cite: 159].
* [cite_start]**Veri Kalıcılığı:** Tüm veriler (ürünler, beğeniler, yorumlar) tarayıcının `localStorage` (yerel hafıza) alanında tutulur, sayfa yenilendiğinde veriler kaybolmaz[cite: 160].
* [cite_start]**Dinamik İstatistikler:** Sayfa üst kısmında platformdaki toplam ürün ve toplam beğeni sayıları anlık olarak hesaplanıp gösterilir[cite: 165, 166].

## 🛠️ Kullanılan Teknolojiler

[cite_start]Projede hiçbir harici kütüphane veya framework (React, Vue, Bootstrap, Tailwind vb.) kullanılmamıştır[cite: 90, 113]. [cite_start]Tamamen saf (Vanilla) web teknolojileri kullanılarak modüler bir mimariyle inşa edilmiştir[cite: 112, 114, 172]:

* [cite_start]**HTML5:** Semantik (`<header>`, `<main>`, `<section>`, `<article>`) etiket yapısı ve form doğrulamaları[cite: 135, 136, 142, 143].
* [cite_start]**CSS3:** Mobil uyumlu (responsive) tasarım için CSS Grid/Flexbox yapıları, özel CSS değişkenleri (custom properties) ve temiz bir kullanıcı arayüzü[cite: 147, 148, 152].
* [cite_start]**Vanilla JavaScript:** DOM manipülasyonu, dizi (array) metotları (`filter`, `reduce`), Event Delegation (olay delegasyonu) ve localStorage yönetimi[cite: 157, 161, 267, 276].

## 📂 Kurulum ve Kullanım

Proje tarayıcı üzerinde çalıştığı için herhangi bir sunucu kurulumu veya derleyici (build tool) gerektirmez.

1.  [cite_start]Dosyaları (`index.html`, `style.css`, `app.js`) aynı klasörde toplayın [cite: 85, 190-192].
2.  `index.html` dosyasını tercih ettiğiniz bir modern web tarayıcısında (Chrome, Firefox, Safari vb.) açın.
3.  Formu kullanarak ilk ürününüzü ekleyin ve platformu test edin!

## 📁 Dosya Yapısı

```text
OgrenciNo_BEUShareBox/
│
├── index.html    # Sayfanın temel iskeleti, form ve arayüz yapısı
├── style.css     # Doğa renklerinden ilham alan renk paleti ve responsive tasarım kuralları
└── app.js        # Ürün işleme, filtreleme ve localStorage gibi tüm mantıksal süreçler
