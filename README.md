<h1 style="color:#2E86C1;text-align:center;">Tur Yönetim Sistemi 🚐</h1>

<p align="center">
  <img src="public/logo.jpg" alt="Proje Logosu" width="200"/>
</p>

## <span style="color:#ff6347">Genel Bakış</span>

Tur Yönetim Sistemi, tur firmalarının rezervasyon, müşteri, şoför, otel ve program yönetimini kolaylaştırmak için tasarlanmış bir web uygulamasıdır. **Node.js** ve **Express** kullanılarak hazırlanmış API yapısı ile, veritabanı olarak **MySQL** kullanılmaktadır.

Bu projede kullanıcılar; tur programları oluşturabilir, otel ve oda bilgilerini girebilir, müşterilerin rezervasyon ve şikayet kayıtlarını tutabilir ve araç-şoför atamalarını gerçekleştirebilir.

## <span style="color:#ff6347">Kurulum</span>

1. Depoyu klonlayın:
   ```bash
   git clone <repo-url>
   cd Tur-Yonetim-Sistemi-Projesi
   ```
2. Bağımlılıkları yükleyin:
   ```bash
   npm install
   ```
3. `db/mysql_connect.js` dosyasında MySQL bağlantı ayarlarınızı güncelleyin.
4. Veritabanında gerekli tabloların bulunduğundan emin olun.

## <span style="color:#ff6347">Çalıştırma</span>

Projeyi geliştirme modunda başlatmak için:
```bash
npm start
```
Uygulama varsayılan olarak **3000** portunda çalışacaktır. Tarayıcıdan `http://localhost:3000` adresine giderek arayüze erişebilirsiniz.

## <span style="color:#ff6347">Proje Yapısı</span>

- **app.js**: Express sunucusunun ana dosyası.
- **routers/**: API uç noktalarını tanımlayan yönlendiriciler.
- **controllers/**: İş mantığını ve veritabanı işlemlerini içeren kontrolörler.
- **public/**: Statik dosyalar (resimler, CSS) ve istemci tarafı scriptleri.
- Çeşitli HTML dosyaları: Uygulamanın arayüz sayfaları.

## <span style="color:#ff6347">API Uç Noktalarından Örnekler</span>

`routers/routes.js` içinde tanımlı bazı uç noktalar şunlardır:
```javascript
router.post("/registerSofor", registerSofor);        // Şoför ekleme
router.post("/registerProgram", registerProgram);    // Program ekleme
router.post("/registerOtel", registerOtel);          // Otel ekleme
router.get("/getSoforler", getSoforler);             // Şoförleri listeleme
router.get("/getProgramlar", getProgramlar);         // Programları listeleme
router.post("/registerArabalar", registerArabalar);  // Araç ekleme
router.delete("/deleteAraba/:plaka", deleteAraba);   // Araç silme
```
Daha fazla uç nokta detayını ilgili dosyada bulabilirsiniz.

## <span style="color:#ff6347">Ekran Görselleri</span>

Aşağıdaki resimler `public/` klasöründe yer almakta olup arayüzde kullanılmaktadır:
ER Diyagramı
  <img width="887" height="563" alt="image" src="https://github.com/user-attachments/assets/dadce7df-0494-446f-9584-a91514982acf" />
- ![Sumela](public/sumela.jpg)
- ![Uzungöl](public/uzungol.jpg)

## <span style="color:#ff6347">Testler</span>

Projede tanımlı bir test komutu bulunmamaktadır. `npm test` çalıştırıldığında aşağıdaki çıktıyı alırsınız:
```
npm ERR! Missing script: "test"
```

## <span style="color:#ff6347">Katkıda Bulunma</span>

Pull request göndermeden önce lütfen kod stiline ve proje yapısına uygun hareket ediniz. Her türlü katkıya açığız! 🙌

## <span style="color:#ff6347">Lisans</span>

Bu proje örnek amaçlıdır ve belirli bir lisans belirtmemiştir.
