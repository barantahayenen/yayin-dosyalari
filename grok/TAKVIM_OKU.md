# Grokbot: paylaşım takvimi nasıl okunur

Adres (her zaman güncel): https://raw.githubusercontent.com/barantahayenen/yayin-dosyalari/main/grok/takvim.json
İnsan okunur tablo: https://raw.githubusercontent.com/barantahayenen/yayin-dosyalari/main/grok/takvim.md

Her kayıt:
- `id` — tekil kimlik (ör. sahabilim-015, sahabilim-gm-20261124)
- `hesap` — Instagram hesabı (sahabilim, …)
- `tur` — mac (tek maç analizi) · gunun-maclari (toplu) · veri-dosyasi
- `baslik` — içerik başlığı
- `zaman_tsi` / `zaman_utc` — planlanan paylaşım zamanı (TSİ = UTC+3)
- `mac_saati_tsi` / `mac_saati_utc` — (varsa) maçın başlama saati
- `durum` — planlandi · paylasildi · iptal · ertelendi
- `link`, `medya` — paylaşıldıktan sonra Instagram bağlantısı ve medya kimliği
- `paylasildi` — gerçek paylaşım zamanı (TSİ)
- `not` — iptal/erteleme nedeni vb.

Kural: `durum=paylasildi` olana kadar gönderi yok sayılır. Zamanı geçmiş ama `planlandi` kalan kayıt = gecikme/iptal ihtimali; takvim birkaç dakika içinde güncellenir.
