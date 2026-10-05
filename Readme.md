# GMT 458 - Web GIS: Personal Web Page

Bu proje, GMT 458 Web GIS dersi Assignment 1 (Kişisel Web Sayfası) kapsamında hazırlanmıştır. Projede HTML, CSS, OpenLayers ve Leaflet teknolojileri kullanılmıştır.

## Yapay Zeka (AI) Kullanımı

Bu projeyi geliştirirken yapay zekadan (Gemini) destek aldım. Yapay zekadan öğrendiğim spesifik konular ve çözdüğüm sorunlar şunlardır:

* **Harita Altlığı (Basemap) Sorunları:** Leaflet'te standart OpenStreetMap sunucularından kaynaklanan '403 Access Blocked' hatasının nedenini ve bunu çözmek için API anahtarı gerektirmeyen Esri (ArcGIS) altlıklarına nasıl geçiş yapacağımı öğrendim.
* **Issue 1 (Zoom Threshold):** Leaflet haritasında işaretçilerin sadece belirli bir yakınlaştırma seviyesinden sonra görünmesi için `leafletMap.on('zoomend', ...)` fonksiyonunu ve `getZoom()` metodunu nasıl kullanacağımı öğrendim.
* **Issue 2 (WrapX):** OpenLayers haritası uzaklaştırıldığında dünyanın yatay düzlemde kendini tekrar etmesini (yan yana dizilmesini) engellemek için kaynak ayarlarında `wrapX: false` parametresinin kullanımını öğrendim.
* **CSS Animasyonları:** Sayfanın `@keyframes` animasyonlarının mantığını kavradım.

**Toplam Yapay Zeka Kullanım Süresi:**
Projeyi planlamak, hataları (debug) çözmek ve kod yapılarını öğrenmek dahil olmak üzere yapay zeka ile tahmini olarak toplam **2.5 saat** çalıştım.