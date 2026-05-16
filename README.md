<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

#  Re-Life — Bütünleşik Hayvan Barınağı ve Bağış Yönetim Platformu

> **"Kırıkları gizlemiyoruz; onları teknoloji ve şeffaflıkla, altın damarlar gibi parlatarak onarıyoruz."**

Re-Life; geleneksel hayvan barınağı yönetim sistemlerindeki şeffaflık, güven ve takip edilebilirlik sorunlarını çözmek amacıyla **Kintsugi** felsefesinden ilham alınarak geliştirilmiş, modern, güvenli ve **multi-tenant** mimariye sahip bütünleşik bir platformdur.

---

## 🌟 Projenin Vizyonu ve Kintsugi Felsefesi
Geleneksel barınak platformları, hayvanların geçmişteki travmalarını veya sistemin eksikliklerini saklama eğilimindedir. Re-Life ise bu yaklaşımı tamamen reddeder:
* **Çatlakların Tespiti:** Sokaktaki sahipsiz dostlarımızın yaşadığı fiziksel, duygusal veya sistemsel travmalar birer "hasar haritası" (Fracture Map) olarak sisteme işlenir.
* **Altın Dokunuş (Restorasyon):** Bağışçılar, bu hasar haritasındaki belirli parçaları (fragments) şeffaf bir şekilde fonlar. Fonlanan her parça, yazılım ve şeffaflık (Altın) ile onarılır.
* **Görsel Kanıt:** Hayvanların "Before & After" (Önce / Sonra) durumları, kronolojik olarak "Recovery Updates" (İyileşme Raporları) aracılığıyla bağışçıya sunulur.

---

## 🛠️ Teknik Mimari ve Teknolojiler

Re-Life, **Teknik Derinlik**, **Siber Dayanıklılık** ve **Yüksek UX Performansı** yönergelerine tam uyumlu modern bir teknoloji yığınıyla inşa edilmiştir:

* **Backend:** PHP 8.4+ & Laravel 11.5+ (Kurumsal, kararlı ve güvenli çekirdek mimari)
* **Frontend:** Laravel Livewire (Sayfa yenilemeden çalışan, SPA hızında dinamik kullanıcı deneyimi)
* **Veritabanı:** PostgreSQL / MySQL (İlişkisel, optimize edilmiş vaka ve bağış şeması)
* **Güvenlik:** Rol Bazlı Erişim Kontrolü (RBAC) ve Gelişmiş Middleware katmanları

---

## 🚀 Öne Çıkan Özellikler

### 1. Parçalı Fonlama ve Canlı Takip (Fractional Funding)
Bağışçılar ucu açık yardımlar yapmak yerine, bir hayvanın tedavi, kedi/köpek sosyalleşmesi, aşı veya ameliyat gibi spesifik bir iyileşme parçasına (fragment) destek olur. Bağış tamamlandığında sistem otomatik olarak dijital bir **Teşekkür Belgesi** (Certificate of Restoration) üretir.

### 2. Gelişmiş Rol ve Yetki Yönetimi (RBAC)
Siber dayanıklılık ve veri güvenliği kapsamında, sistemdeki tüm aksiyonlar sıkı bir yetki kontrolünden geçer:
* **Superadmin:** Sistem genelindeki barınakların onaylanması, global finansal akışın denetlenmesi.
* **Barınak Yöneticisi:** Barınak personeli atamaları, yerel ihtiyaç haritalarının yönetimi.
* **Saha Personeli / Gönüllü:** Hayvan kayıtlarının girilmesi, "Recovery Journal" (İyileşme Günlüğü) notlarının ve fotoğraflarının güncellenmesi.
* **Bağışçı / Kullanıcı:** Akıllı eşleşme motorunu (Matching Engine) kullanarak evine en uygun dostu bulma ve şeffaf bağış yapma.

### 3. Oyunlaştırma (Gamification Engine)
Bağışçı bağlılığını ve topluluk içi etkileşimi artırmak amacıyla tasarlanmış rozet (Badge) motoru ve liderlik tablosu (Leaderboard). Yapılan dijital restorasyonların kalibresine göre kullanıcılar profil rozetleri kazanır.

---

## 📊 Veritabanı ve Akış Şeması Özet dökümü

```text
 [Kullanıcı/Bağışçı] ----> (Bağış Yap / Parça Seç) ----> [İhtiyaç / Vaka Tablosu]
          |                                                       |
          |                                                       v
 [RBAC Middleware] <--- (Güncelleme / Fotoğraf Ekle) <--- [Barınak Personeli]
          |
          v
 [Şeffaf Rapor / Recovery Update] ----> (Otomatik Bildirim) ----> [Bağışçı]


# 📦 Kurulum ve Çalıştırma

Projeyi yerel geliştirme ortamınızda sorunsuz şekilde çalıştırmak için aşağıdaki adımları takip edin.

---

# 1. Ön Gereksinimler

Sisteminizde aşağıdaki teknolojilerin kurulu olduğundan emin olun:

- PHP >= 8.2
- Composer
- Node.js & NPM
- MySQL / PostgreSQL / SQLite

---

# 🚀 Adım Adım Kurulum

## 1. Projeyi Klonlayın

```bash
git clone https://github.com/kullanici-adi/Re-Life.git
cd Re-Life
```

---

## 2. Backend Bağımlılıklarını Kurun

Laravel ve PHP paketlerini yükleyin:

```bash
composer install
```

---

## 3. Frontend Bağımlılıklarını Kurun

Node paketlerini yükleyin ve frontend dosyalarını derleyin:

```bash
npm install
npm run build
```

> Geliştirme sürecinde canlı değişiklikleri görmek için:

```bash
npm run dev
```

---

## 4. .env Dosyasını Oluşturun

```bash
cp .env.example .env
```

---

## 5. Uygulama Anahtarını Oluşturun

```bash
php artisan key:generate
```

---

## 6. Veritabanı Bağlantısını Yapılandırın

`.env` dosyasını açın ve kendi veritabanı bilgilerinizi girin.

Örnek MySQL yapılandırması:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=relife_db
DB_USERNAME=root
DB_PASSWORD=
```

> Migration işlemlerinden önce `relife_db` adında boş bir veritabanı oluşturmayı unutmayın.

---

## 7. Migration ve Seeder İşlemlerini Çalıştırın

```bash
php artisan migrate --seed
```

Bu işlem sonunda:

- Barınak verileri
- Örnek hayvan kayıtları
- Recovery Journal verileri
- Test kullanıcıları
- RBAC rol yetkilendirmeleri

otomatik olarak sisteme yüklenecektir.

---

## 8. Storage Link Oluşturun

```bash
php artisan storage:link
```

Bu işlem yüklenen görsellerin ve dosyaların tarayıcı üzerinden görüntülenmesini sağlar.

---

# ▶️ Uygulamayı Çalıştırma

Laravel geliştirme sunucusunu başlatın:

```bash
php artisan serve
```

Ardından aşağıdaki adres üzerinden projeye erişebilirsiniz:

```txt
http://127.0.0.1:8000
```

---


# 👥 Proje Ekibi

- Fatma Bedia Erdem 
- Onur Şahin 
- Ahmet Selim Çiftçi 
