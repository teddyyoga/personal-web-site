# GMT 458 - Web GIS: Personal Web Page 🌍

Bu proje, Geomatik Mühendisliği **GMT 458 Web GIS** dersi *Assignment 1 (Kişisel Web Sayfası)* kapsamında hazırlanmıştır. Projede modern web standartlarına uygun olarak HTML5, CSS3, JavaScript, OpenLayers ve Leaflet teknolojileri kullanılmıştır.

## 🚀 Proje Özellikleri

- **Akıllı Navigasyon:** Sayfalar arası geçişlerde geleneksel linkler yerine `window.history` API kullanılarak tarayıcı mantığında çalışan ikon tabanlı akıllı menü (Glassmorphism tasarımı ile).
- **Çift Harita Altyapısı (OSM Tabanlı):** 
  - **OpenLayers:** Türkiye genelini kapsayan makro bakış açısı ve iller arası buton kontrollü uçuş (fly-to) animasyonları.
  - **Leaflet:** Sadece Ankara sınırları içine hapsedilmiş (Bounding Box / Kamera Kilidi), özel ikonlar (mezuniyet kepi, bina, şehir yıldızı vb.) ve popup içerikleri barındıran mikro detay haritası.
- **İnteraktif Tasarım:** CSS `transition` ve `transform` özellikleriyle zenginleştirilmiş dinamik yetenek ve teknoloji kartları.

## 🤖 Yapay Zeka (AI) Kullanımı

Bu projeyi geliştirirken yapay zekadan (Gemini) aktif olarak destek aldım. Proje sürecinde yapay zekadan öğrendiğim spesifik konular ve çözdüğüm sorunlar şunlardır:

- **Harita Altlığı (Basemap) Sorunları:** Leaflet'te standart OpenStreetMap sunucularından kaynaklanan '403 Access Blocked' hatasının yerel dosya (`file://`) kullanımından kaynaklandığını; bu sorunu çözmek için VS Code "Live Server" eklentisiyle (veya Python http.server ile) nasıl yerel sunucu başlatacağımı öğrendim.
- **Kamera Kilidi (Bounding Box):** Leaflet üzerinde kullanıcının haritada kaybolmasını engellemek için `maxBounds` ve `minZoom` parametreleriyle kamerayı sadece Ankara sınırlarına nasıl hapsedeceğimi kavradım.
- **Issue 1 (Zoom Threshold):** Leaflet haritasında işaretçilerin sadece belirli bir yakınlaştırma seviyesinden sonra görünmesi için `leafletMap.on('zoomend', ...)` fonksiyonunu ve `getZoom()` metodunu nasıl kullanacağımı öğrendim.
- **Issue 2 (WrapX):** OpenLayers haritası uzaklaştırıldığında dünyanın yatay düzlemde kendini tekrar etmesini engellemek için kaynak ayarlarında `wrapX: false` parametresinin kullanımını öğrendim.
- **UI/UX Geliştirmeleri:** Sayfanın `@keyframes` animasyonlarının mantığını, z-index çakışmalarını nasıl yöneteceğimi ve modern grid/flexbox yapılarını öğrendim.

**Toplam Yapay Zeka Kullanım Süresi:**
Projeyi planlamak, modern tasarımı inşa etmek, hataları (debug) çözmek ve yeni kod yapılarını öğrenmek dahil olmak üzere yapay zeka ile tahmini olarak toplam **10 saat** çalıştım.

## 💻 Kurulum ve Yerel Kullanım

OpenStreetMap'in katı güvenlik politikaları nedeniyle, harita altlıklarının sorunsuz çalışması için projenin bir yerel sunucu üzerinden çalıştırılması gerekmektedir:
1. VS Code üzerinden projeyi açın.
2. **Live Server** eklentisini kurun ve `maps.html` veya `index.html` dosyasındayken "Go Live" butonuna basın (veya terminalde `python -m http.server` komutunu çalıştırın).
3. Tarayıcınızda açılan `localhost` adresi üzerinden projeyi tam performanslı olarak görüntüleyin.

---
*Geliştirici:* **Oğuz Meriç**