# Çöl Operasyonu – FPS

Oyun ve kaynak kodu tek dosyadadır: [`index.html`](index.html). Three.js, harita ve silah modelleri dosyanın içine gömülüdür. Kurulum, derleme veya CDN bağlantısı gerekmez.

**Çalıştırma:** `index.html` dosyasını WebGL destekli bir tarayıcıda açıp **Başla**'ya basın. Telefonlarda dosya önizlemesi yerine tarayıcıdan bir web adresi açmak daha güvenilir olabilir. Statik sunucuyla açmak için depo kökünde `python3 -m http.server 8080` komutunu çalıştırın ve tarayıcıdan `http://localhost:8080` adresine gidin. Arena’da canlı önizleme de kullanılabilir.

| İşlem | Fare ve klavye | Dokunmatik |
| --- | --- | --- |
| Hareket / bakış | WASD / fare (Pointer Lock) veya yön tuşları | Sol joystick / sağ alanı sürükle |
| Koş / zıpla | Shift / Boşluk | Koş tuşunu basılı tut / Zıpla |
| Ateş / şarjör | Sol tık / R | Ateş / Şarjör |
| Dürbün (Hayalet) | Sağ tık | Dürbün |
| Envanter / silah seçimi | E / 1–5 ve 8 | Envanter / silah kartı |
| Duraklat | Esc | Duraklat düğmesi |
| Tam ekran | Başla / F / Tam ekran düğmesi | Başla / Tam ekran düğmesi |

- Dar ekranlarda ve dokunmatik cihazlarda dokunmatik düzen otomatik seçilir. Hibrit cihazlarda menüden kontrol türünü değiştirebilirsiniz.
- **Başla** tarayıcıdan tam ekran ister. Tarayıcı, cihaz veya önizleme buna izin vermezse oyun pencere içinde devam eder. Tarayıcılar sayfa açılır açılmaz kendiliğinden tam ekrana geçilmesini engeller.
- Fare kilidi reddedilirse masaüstünde otomatik olarak kilitsiz kamera kullanılır. İmleci oyun alanında hareket ettirin veya yön tuşlarını kullanın; oyun web kamerası izni istemez. Fare kilidi açıkken kamera tepki vermezse **M** ile kilitsiz moda geçebilirsiniz.
- Dokunmatik düzen dikey ve yatay oynanabilir; dikeyde daha geniş görüş için yatay çevirme önerisi gösterilir.
- Mobil grafik profili piksel oranını 1,15 ile, çizim arabelleğini yaklaşık 1 milyon pikselle ve görüş mesafesini 95 birimle sınırlar. Gölge haritaları kapalıdır; mobilde açılan WebGL bağlamında kenar yumuşatma da kapalıdır. Masaüstünde statik, 1024 × 1024 harita gölgeleri kullanılır. Donanım ve tarayıcıya göre performans değişir.

Harita ve silah modelleri paylaşılan HTML’den alınmıştır. Silah modelleri: **Rifles – LeyamaTk**. Gömülü motor ve yardımcı kütüphanelerin lisansları HTML dosyasındadır.

Oyun tek kişiliktir. Takım arkadaşı yoktur; rakip askerlerin kask ve teçhizatı, ayrıca birinci şahıs el ve kol modelleri korunur.

## Oyun içi mağaza

- Masaüstünde **B**, mobilde **Mağaza** düğmesiyle açılır. Başlangıç bakiyesi **$300**; elenen her rakip **+$150** kazandırır. Tutarlar oyun içi ABD dolarıdır, gerçek ödeme yapılmaz.
- **Bandaj** **$120** karşılığında +30 can, **McDonald’s Menü** **$280** karşılığında +60 can verir. Satın alınan ürünler çantada saklanır. Canın eksikken mağazadan **Kullan**'a basabilir veya **6** (bandaj) / **7** (menü) tuşlarını kullanabilirsin. Can, ürünün birinci şahıs animasyonu tamamlandığında yenilenir.
- Promosyon kutusuna **`OSMAN100`** yazmak **$100.000** ekler. Kod tarayıcı kaydı başına bir kez kullanılabilir. Tarayıcı yerel depolamaya izin verirse bakiye, ürünler ve kodun kullanım durumu saklanır. Gerçek para kullanılmaz.
- **M4A4 ($1.000):** Yeni 3B otomatik tüfek mağazada bir kez satın alınır ve kalıcı olarak açılır. Mağazada **Kuşan**, silah envanteri veya **8** tuşuyla seçebilirsin. M4A1 envanterde kalır.
