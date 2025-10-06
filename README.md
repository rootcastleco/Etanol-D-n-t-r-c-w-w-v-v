# Etanol Dönüştürücü – w/w ↔ v/v

Web tabanlı etanol konsantrasyon dönüştürücü. Ağırlık/ağırlık (w/w) ve hacim/hacim (v/v) yüzde değerleri arasında dönüşüm yapar.

## Özellikler

- ✨ Çift yönlü dönüşüm: w/w → v/v ve v/v → w/w
- 🎯 Hassas hesaplama: 20°C sıcaklıkta etanol ve su yoğunlukları kullanılır
- 🚀 Anlık sonuçlar: Değer girerken otomatik hesaplama
- 📱 Responsive tasarım: Mobil ve masaüstü uyumlu
- 🎨 Modern ve kullanıcı dostu arayüz

## Kullanım

1. `index.html` dosyasını bir web tarayıcısında açın
2. Bildiğiniz değeri (w/w veya v/v) girin
3. Diğer birim otomatik olarak hesaplanacaktır

### Örnek Dönüşümler

- 50% w/w = 55.90% v/v
- 70% v/v = 64.80% w/w
- 95% v/v = 93.03% w/w

## Teknik Detaylar

Dönüştürücü, sulu etanol çözeltileri için aşağıdaki parametreleri kullanır:

- **Etanol yoğunluğu (20°C)**: 0.789 g/mL
- **Su yoğunluğu (20°C)**: 1.0 g/mL

### Formüller

**w/w'den v/v'ye:**
```
ρ_çözelti = 1 / (w/w/ρ_etanol + (1-w/w)/ρ_su)
v/v = (w/w × ρ_çözelti) / ρ_etanol
```

**v/v'den w/w'ye:**
```
m_etanol = v/v × ρ_etanol
m_su = (1-v/v) × ρ_su
w/w = m_etanol / (m_etanol + m_su)
```

## Ekran Görüntüleri

### Başlangıç Ekranı
![Etanol Dönüştürücü](https://github.com/user-attachments/assets/08b57445-57de-4df2-951a-60197b58956c)

### Dönüşüm Örneği
![Çalışan Dönüştürücü](https://github.com/user-attachments/assets/159077d9-9b6f-470b-9a6f-40debf1781af)

## Lisans

Bu proje açık kaynaklıdır ve herkes tarafından kullanılabilir.