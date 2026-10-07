# WastTry Admin System

Minecraft **1.21.11** için hazırlanmış, **OP gerektirmeyen** kapsamlı Türkçe Skript admin ve sunucu yönetim sistemi.

## ✨ Özellikler

- 🛡️ OP gerektirmeyen admin sistemi
- 👤 Oyuncu takip ve inceleme sistemi
- 👻 Admin görünmezlik modu
- 📦 Oyuncu envanteri görüntüleme
- 📦 Oyuncunun Ender Sandığını görüntüleme
- 📋 Oyuncu bilgilerini görüntüleme
- ⚠️ Oyuncuya admin uyarısı gönderme
- 🔇 Oyuncu susturma sistemi
- 👥 Takım oluşturma ve takım daveti
- 💬 Takım sohbeti
- 🏠 GUI tabanlı Home sistemi
- 🔧 Bakım modu
- 📝 Sunucu güncellemeleri sistemi
- 🟢 TAB üzerinde admin ve takım bilgileri
- 🔒 Bakım modunda oyuncu whitelist sistemi

## 📋 Gereksinimler

- **Minecraft:** 1.21.11
- **Skript:** 2.16.2
- **OP:** Gerekmez

## 📥 Kurulum

1. `WastTry-AdminSystem.sk` dosyasını indirin.
2. Sunucunuzdaki `plugins/Skript/scripts/` klasörüne atın.
3. Sunucuyu başlatın veya `/sk reload WastTry-AdminSystem` komutunu kullanın.
4. Skript içerisindeki admin ayarlarını kendi sunucunuza göre düzenleyin.

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

## 👥 Takım Sistemi

- Takım oluşturma
- Takıma oyuncu davet etme
- Takım davetini kabul etme
- Takım sohbeti
- TAB üzerinde takım bilgileri
- Maksimum **5 oyuncu**

## 🏠 Home Sistemi

GUI üzerinden kolayca home oluşturabilir ve kullanabilirsiniz.

- `/home`
- `/sethome`
- `/delhome`
- `/homelist`

Eski home komutları sistem tarafından engellenebilir.

## 🔧 Bakım Sistemi

Sunucuyu bakım moduna alabilir ve yalnızca izin verilen oyuncuların giriş yapmasını sağlayabilirsiniz.

Bakım komutları:

- `/bakım`
- `/bakımçıkar`
- `/bakımoyuncuekle <oyuncu>`

## 📝 Güncellemeler

Sunucudaki son değişiklikleri oyunculara göstermek için:

`/songuncellemeler`

## ⚙️ Yapılandırma

Admin isimleri ve diğer temel ayarlar Skript dosyasının üst kısmındaki yapılandırma bölümünden değiştirilebilir.

Örnek:

```text
ADMINLER
- WastTry
- KGAMEOVER
