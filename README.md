# WastTry Admin System

Minecraft **1.21.11** için hazırlanmış, **OP gerektirmeyen** kapsamlı Türkçe Skript admin ve sunucu yönetim sistemi. Admin araçlarının yanında takım, home, pazar ve bounty sistemleri de içerir.

## 📺 YouTube

Minecraft içerikleri, PvP videoları ve WastTry projeleri için YouTube kanalım:

**WastTry** — [YouTube Kanalı](https://youtube.com/@wasttry)


## ✨ Özellikler

- 🛡️ OP gerektirmeyen admin sistemi
- 👤 Oyuncu takip ve inceleme sistemi
- 👻 Admin görünmezlik modu
- 📦 Oyuncu envanteri görüntüleme
- 📦 Oyuncunun Ender Sandığını görüntüleme
- 📋 Oyuncu bilgilerini görüntüleme
- ⚠️ Oyuncuya admin uyarısı gönderme
- 🔇 Oyuncu susturma sistemi
- 👥 Takım oluşturma, takım daveti, takım rengi ve takım sohbeti
- 🏠 GUI tabanlı Home sistemi
- 🛒 Pazar sistemi: eşyanı koy, karşılığında maden iste
- 🎯 Bounty sistemi: oyuncunun üzerine maden ödülü koy
- 🔧 Bakım modu
- 📝 Sunucu güncellemeleri sistemi
- 🟢 Nametag üzerinde takım ismi, TAB listesinde sade oyuncu adı
- 🔒 Bakım modunda oyuncu whitelist sistemi

## 📋 Gereksinimler

- **Minecraft:** 1.21.11
- **Skript:** 2.16.2
- **OP:** Gerekmez

Takım sistemi vanilla `team` komutlarını kullanır. Sunucuda başka bir takım veya nametag eklentisi varsa çakışabilir.

## 📥 Kurulum

1. `WastTry-AdminSystem.sk` dosyasını indirin.
2. Sunucunuzdaki `plugins/Skript/scripts/` klasörüne atın.
3. Sunucuyu başlatın veya `/sk reload WastTry-AdminSystem` komutunu kullanın.
4. Admin isimlerini kendi sunucunuza göre düzenleyin (aşağıdaki **Yapılandırma** bölümüne bakın).

Aynı komutları tanımlayan eski script dosyaları varsa kaldırın, aksi halde komutlar çakışır.

## 🛡️ Admin Komutları

| Komut | Açıklama |
|---|---|
| `/admin` | Admin modunu açar |
| `/adminleave` | Admin modundan çıkar |
| `/adminuyarı <oyuncu>` | Oyuncuya admin uyarısı gönderir |
| `/env <oyuncu>` | Oyuncunun envanterini görüntüler |
| `/ender <oyuncu>` | Oyuncunun Ender Sandığını görüntüler |
| `/bilgi <oyuncu>` | Oyuncu bilgilerini gösterir |
| `/mute <oyuncu>` | Oyuncuyu susturur |
| `/unmute <oyuncu>` | Susturmayı kaldırır |

### Admin modu

- `/admin` ile spectator moduna geçilir ve admin diğer oyunculardan gizlenir.
- İzlenecek oyuncunun ismi chat'e yazılır, admin o oyuncuya ışınlanır.
- Admin, izlediği oyuncudan en fazla **10 blok** uzaklaşabilir. Uzaklaşırsa geri çekilir.
- `/adminleave` ile eski konuma, eski oyun moduna dönülür.

### Diğer admin notları

- `/env` ve `/ender` sadece **görüntüleme** modundadır, eşyalar alınamaz veya taşınamaz.
- Susturulan oyuncu chat kullanamaz, adminler susturmadan etkilenmez.
- `/adminuyarı` komutunda KGAMEOVER için **5 dakika** bekleme süresi vardır.

## 👥 Takım Sistemi

| Komut | Açıklama |
|---|---|
| `/takım` | Takım menüsünü açar (`/takim` de çalışır) |
| `/takımkabul` | Gelen takım davetini kabul eder (`/takimkabul` de çalışır) |

- Takım oluşturma, takım adı (2-8 karakter) ve takım rengi değiştirme
- Menüden oyuncu davet etme ve takımdan ayrılma
- Takım sohbeti (takım adı ve rengiyle)
- Nametag üzerinde takım ismi, TAB listesinde sadece oyuncu adı
- Takım içi vuruş (friendly fire) açıktır
- Maksimum **5 oyuncu**

## 🏠 Home Sistemi

Her oyuncu **tek bir home** kullanabilir. Tüm işlemler GUI üzerinden yapılır.

- `/home` menüsünden home oluşturma, güncelleme, ışınlanma, bilgi ve silme
- `/sethome`, `/delhome` ve `/homelist` komutları sistem tarafından **engellenir**, oyuncuya `/home` menüsünü kullanması söylenir

## 🛒 Pazar Sistemi

| Komut | Açıklama |
|---|---|
| `/pazar` | Pazar menüsünü açar (`/market` de çalışır) |

- Sayfalı ilan listesi, başkalarının ilanları görünür
- **Eşya Sat:** eşyayı ortadaki slota bırak veya **Elindeki Eşyayı Koy** butonunu kullan
- Karşılığında maden seç: **Zümrüt, Elmas, Altın, Demir, Netherite, Netherite Hurdası**
- ➕ ve ➖ butonlarıyla karışık fiyat belirlenir, örneğin "Zümrüt 5 + Elmas 16"
- Her maden için en fazla 64
- Oyuncu başına en fazla **10 ilan**
- **İlanlarım:** kendi ilanını kaldırıp eşyanı geri alırsın
- **Kazançlarım:** satıştan gelen madenler çevrimdışıyken de birikir, menüden alınır
- Yeni ilan konunca herkese chatte duyuru gider ve ses çalar

## 🎯 Bounty Sistemi

| Komut | Açıklama |
|---|---|
| `/bounty` | Bounty menüsünü açar |

- Aktif bounty'ler oyuncuların skinli kafalarıyla listelenir
- **Bounty Koy:** çevrimiçi bir oyuncuyu seç, ödül olarak koyacağın madenleri seç
- Seçtiğin madenler **envanterinden alınır**, ödül koyduğun madenlerin aynısıdır
- Hedefi **öldüren oyuncu** ödülün tamamını alır
- Hedef kendi kendine ölürse (düşme, lav, canavar vb.) ödül **yerinde kalır**
- Oyuncu çıkış yapsa da ödül durur
- Aynı oyuncuya birden fazla kişi ödül koyabilir, ödüller birikir
- Koyduğun ödülü **5 dakika içinde** `/bounty` ► **Ödüllerim** menüsünden geri alabilirsin
- Kendi üzerine ödül koyamazsın
- Ödül konunca ve alınınca herkese chatte duyuru gider

## 🔧 Bakım Sistemi

Sunucuyu bakım moduna alabilir ve yalnızca whitelist'teki oyuncuların giriş yapmasını sağlayabilirsiniz. Bu komutları sadece **WastTry** kullanabilir.

| Komut | Açıklama |
|---|---|
| `/bakım` | Whitelist'i açar, bakım moduna geçer (`/bakim`) |
| `/bakımçıkar` | Whitelist'i kapatır, bakım modundan çıkar (`/bakimcikar`) |
| `/bakımoyuncuekle` | Komutu yazdıktan sonra whitelist'e eklenecek oyuncunun adını chat'e yazarsınız, iptal için `iptal` yazın (`/bakimoyuncuekle`) |

## 📝 Güncellemeler

Sunucudaki son değişiklikleri oyunculara göstermek için:

`/songuncellemeler`

Menü `/home` ekranındaki turuncu **Son Güncellemeler** butonundan da açılır.

## ⚙️ Yapılandırma

Admin isimleri, scriptin başındaki `isAdmin` fonksiyonunda tanımlıdır. Kendi sunucunuza göre bu isimleri değiştirin veya yenilerini ekleyin:

```skript
function isAdmin(p: player) :: boolean:
    if {_p}'s name is "WastTry":
        return true
    if {_p}'s name is "KGAMEOVER":
        return true
    return false
```

Bakım komutları ise yalnızca `WastTry` adını kontrol eder. Bunları değiştirmek için `/bakım`, `/bakımçıkar` ve `/bakımoyuncuekle` komutlarındaki `player's name is not "WastTry"` satırlarını düzenleyin.

Diğer ayarlar:

- Takım üye sınırı: takım kodundaki `5` değerleri
- Oyuncu başına pazar ilan sınırı: dosyadaki `options` bölümünde `maxilan`

## ⚠️ Notlar

- Bounty ve pazar verileri Skript değişkenlerinde saklanır.
- Skript sürümüne göre `tablist name` ve `skull of` ifadeleri farklı çalışabilir. Reload sırasında hata alırsanız konsol çıktısını issue olarak paylaşın.
