# NPC Bot - Discord AI NPC Sistemi

Bu bot, Discord sunucunuzda gerçekçi NPC'ler oluşturmanızı ve onlarla etkileşim kurmanızı sağlar. Her NPC'nin kendine özgü kişiliği, görevi ve hafızası vardır. **Artık NPC'ler tamamen bağımsız, gerçek üyeler gibi davranabilir!**

## 🆕 Tamamen Bağımsız NPC Sistemi

- 🤖 **Kendi Kararlarını Verir**: NPC'ler ne yapacağına kendisi karar verir
- 👥 **Otomatik Üye Etkileşimi**: NPC'ler kendileri üyelerle konuşur
- 🎭 **Dinamik Davranış**: Kendi hedefleri, duyguları ve stratejileri var
- ⏰ **Gerçek Zamanlı Roleplay**: Sürekli aktif ve etkileşimli
- 🧠 **Gelişmiş AI**: Her eylem için ayrı karar verir

## Özellikler

- 🤖 **AI Destekli NPC'ler**: Google Gemini AI ile gelişmiş etkileşim
- 🧠 **Hafıza Sistemi**: NPC'ler her kullanıcıyı hatırlar
- 🎭 **Kişilik Sistemi**: Her NPC'nin kendine özgü karakteri
- 🇹🇷 **Tamamen Türkçe**: Tüm etkileşimler Türkçe
- 💰 **Ekonomi Entegrasyonu**: NPC'ler para alıp verebilir
- 🔄 **Global Hafıza**: NPC'ler başkalarından öğrendiklerini hatırlar
- 🎯 **Hedef Sistemi**: NPC'lerin kendi hedefleri var
- 😊 **Duygu Sistemi**: NPC'lerin duygusal durumları var

## Kurulum

### 1. Gereksinimler
- Node.js (v16 veya üzeri)
- Google Gemini AI API anahtarı

### 2. API Anahtarı Alma
1. [Google AI Studio](https://makersuite.google.com/app/apikey) adresine gidin
2. Ücretsiz hesap oluşturun
3. API anahtarı alın

### 3. Bot Kurulumu
```bash
# Bağımlılıkları yükleyin
npm install

# .env dosyası oluşturun
echo "DISCORD_TOKEN=your_bot_token_here" > .env
echo "GEMINI_API_KEY=your_gemini_api_key_here" >> .env

# Botu başlatın
npm start
```

## Komutlar

### 📊 Ekonomi Komutları
- `.cüzdan` - Bakiye görüntüle
- `.satın-al <npc_ismi>` - NPC'den ürün satın al
- `.para-ver @kullanıcı <miktar>` - Para ver (Yönetici)
- `.para-al @kullanıcı <miktar>` - Para al (Yönetici)

### 🤖 NPC Yönetimi
- `.npc-ekle` - Yeni NPC oluştur (Yönetici)
- `.npc-liste` - Mevcut NPC'leri listele
- `.npc-sil <isim>` - NPC sil (Yönetici)

### 📜 NPC Bilgi Yönetimi
- `.bilgi-gör <npc_ismi>` - NPC bilgilerini görüntüle
- `.bilgi-ekle <npc_ismi> <bilgi>` - Bilgi ekle (Yönetici)
- `.bilgi-duzenle <npc_ismi> <yeni_bilgi>` - Bilgiyi değiştir (Yönetici)
- `.bilgi-sil <npc_ismi>` - Bilgiyi sil (Yönetici)

### 🎭 Bağımsız Roleplay Komutları
- `.npc-bağımsız-başlat <npc_ismi>` - NPC'yi bağımsız modda başlat (Yönetici)
- `.npc-bağımsız-durdur <npc_ismi>` - NPC'yi bağımsız modda durdur (Yönetici)
- `.npc-durum <npc_ismi>` - NPC'nin mevcut durumunu görüntüle
- `.npc-hedef-ayarla <npc_ismi> <tip> <hedef>` - NPC hedefi ayarla (Yönetici)
- `.npc-duygu-ayarla <npc_ismi> <duygu> <değer>` - NPC duygusu ayarla (Yönetici)

### 📺 Kanal Yönetimi
- `.npc-kanal-ekle <npc_ismi> <kanal_id>` - Kanal ekle (Yönetici)
- `.npc-kanal-sil <npc_ismi> <kanal_id>` - Kanal sil (Yönetici)
- `.npc-kanallar <npc_ismi>` - NPC kanallarını görüntüle

### ⚙️ Davranış Ayarları
- `.npc-zaman-ayarla <npc_ismi> <dakika>` - Mesaj aralığını ayarla (Yönetici)

### 💬 Sohbet
- `.<npc_ismi> <mesaj>` - NPC ile konuş

## 🎭 Tamamen Bağımsız NPC Örnekleri

### Kral NPC'si Kurulumu
```
.npc-hedef-ayarla Kral primary "Krallığımı güçlendirmek ve halkımı korumak"
.npc-hedef-ayarla Kral immediate "Sarayda önemli kararlar almak"
.npc-hedef-ayarla Kral longterm "Komşu krallıklarla ittifak kurmak"
.npc-duygu-ayarla Kral trust 30
.npc-duygu-ayarla Kral curiosity 70
.npc-kanal-ekle Kral 1234567890123456789
.npc-zaman-ayarla Kral 15
.npc-bağımsız-başlat Kral
```

### Tüccar NPC'si Kurulumu
```
.npc-hedef-ayarla Tüccar primary "Ticaret yaparak zengin olmak"
.npc-hedef-ayarla Tüccar immediate "Yeni mallar satmak"
.npc-duygu-ayarla Tüccar happiness 80
.npc-duygu-ayarla Tüccar trust 60
.npc-kanal-ekle Tüccar 1234567890123456789
.npc-zaman-ayarla Tüccar 10
.npc-bağımsız-başlat Tüccar
```

### Demirci NPC'si Kurulumu
```
.npc-hedef-ayarla Demirci primary "En iyi silahları yapmak"
.npc-hedef-ayarla Demirci immediate "Yeni kılıç siparişi almak"
.npc-duygu-ayarla Demirci anger 20
.npc-duygu-ayarla Demirci happiness 60
.npc-kanal-ekle Demirci 1234567890123456789
.npc-zaman-ayarla Demirci 20
.npc-bağımsız-başlat Demirci
```

## 🤖 NPC Davranış Türleri

NPC'ler şu eylemleri kendi başlarına gerçekleştirebilir:

1. **idle** - Hiçbir şey yapma, sadece bekle
2. **wander** - Kanallarda dolaş, rastgele mesaj gönder
3. **work** - İşini yap (rolüne göre)
4. **socialize** - Üyelerle etkileşime geç
5. **explore** - Yeni şeyler keşfet
6. **rest** - Dinlen, enerji topla
7. **pursue_goal** - Hedefini takip et

## 🎯 Hedef Sistemi

Her NPC'nin üç tür hedefi olabilir:
- **Primary**: Ana hayat hedefi
- **Immediate**: Acil hedef
- **Longterm**: Uzun vadeli hedefler listesi

## 😊 Duygu Sistemi

NPC'lerin 5 temel duygusu vardır (0-100 arası):
- **Happiness**: Mutluluk seviyesi
- **Anger**: Öfke seviyesi
- **Fear**: Korku seviyesi
- **Trust**: Güven seviyesi
- **Curiosity**: Merak seviyesi

## Dosya Yapısı

```
npcbot/
├── index.js                    # Ana bot dosyası
├── package.json                # Bağımlılıklar
├── .env                       # Bot token'ı ve API anahtarları
├── data/
│   ├── npcs.json              # NPC verileri
│   ├── memories.json          # Hafıza verileri
│   ├── identities.json        # Kimlik verileri
│   ├── global_memories.json   # Global hafıza
│   ├── npc_behaviors.json     # NPC davranış şablonları
│   ├── npc_schedules.json     # NPC zamanlayıcıları
│   ├── npc_channels.json      # NPC kanal listeleri
│   ├── npc_states.json        # NPC durumları
│   ├── npc_goals.json         # NPC hedefleri
│   ├── npc_emotions.json      # NPC duyguları
│   └── npc_relationships.json # NPC ilişkileri
└── README.md                  # Bu dosya
```

## Özellik Detayları

### 🧠 Hafıza Sistemi
- Her NPC, her kullanıcı ile olan konuşmaları hatırlar
- Son 5000 mesaj saklanır
- Global hafıza ile başkalarından öğrendiklerini hatırlar
- Kimlik doğrulama sistemi ile sahtekarlığı önler

### 🎭 Kişilik Sistemi
- NPC'ler verilen kişilik özelliklerine göre davranır
- Tutarlı karakter sergiler
- Rolünü asla bozmaz
- Duygusal tepkiler verir

### 🤖 Tamamen Bağımsız Roleplay
- NPC'ler kendi kararlarını verir
- Üyelerle otomatik etkileşime geçer
- Hedeflerine göre davranır
- Duygusal durumlarına göre tepki verir
- Gerçek zamanlı roleplay yapar

### 💰 Ekonomi Sistemi
- NPC'ler para alıp verebilir
- Ürün satışı yapabilir
- Kullanıcı bakiyelerini kontrol eder
- Otomatik para transferi

## Sorun Giderme

### Bot Çalışmıyor
1. Google Gemini API anahtarının doğru olduğunu kontrol edin
2. Discord token'ının doğru olduğunu kontrol edin
3. Gerekli izinlerin verildiğinden emin olun

### AI Cevap Vermiyor
1. API anahtarının geçerli olduğunu kontrol edin
2. API kullanım limitini kontrol edin
3. İnternet bağlantınızı kontrol edin

### NPC'ler Bağımsız Davranmıyor
1. Bağımsız modun başlatıldığını kontrol edin
2. Kanal ID'lerinin doğru olduğunu kontrol edin
3. Hedeflerin ve duyguların ayarlandığını kontrol edin

## Lisans

MIT License - Ücretsiz kullanım ve dağıtım. 