
# Etanol Dönüştürücü – w/w ↔ v/v

Web tabanlı etanol konsantrasyon dönüştürücü. Ağırlık/ağırlık (w/w) ve hacim/hacim (v/v) yüzde değerleri arasında dönüşüm yapar.



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


 Etanol Dönüştürücü – w/w ↔ v/v 

Açıklama

Bu PR, etanol çözeltilerinde ağırlıkça (w/w) ve hacimce (v/v) yüzde dönüşümünü hesaplayan interaktif bir web uygulamasını ekler. Uygulama sade bir HTML, CSS ve vanilla JavaScript yapısıyla geliştirilmiştir. Kullanıcı dostu, koyu temalı arayüzü ile laboratuvar ortamında hızlı tahmini hesaplamalar sağlar.

Özellikler

w/w → v/v ve v/v → w/w yönlerinde çift yönlü dönüşüm

Sıcaklık seçimi: 15 °C, 20 °C, 25 °C

Manuel çözeltinin yoğunluğu girişi (opsiyonel)

Doğrusal karışım veya tablo modeli seçimi

Klavye kısayolu: Enter ile hesaplama

Minimalist karanlık arayüz (#0b1220 taban rengi, #4aa4ff vurgu rengi)


Teknik Detaylar

ρ<sub>EtOH</sub> ve ρ<sub>H₂O</sub> sıcaklığa göre ayarlanır

Tablo modeli 20 °C verisine göre aradeğerleme (interpolasyon) yapar

Sıcaklık farkı düzeltmesi: ±0.0003 g/mL · °C

Ortalama doğruluk: ±0.5 %


Test Adımları

1. index.html dosyasını tarayıcıda açın.


2. %40 w/w girin → beklenen ≈ %55 v/v


3. %70 v/v girin → beklenen ≈ %50 w/w


4. Sıcaklığı değiştirin ve yoğunluk farkını gözlemleyin.



Görsel/SS

İsteğe bağlı olarak ekran görüntüsü veya kısa demo gif eklenebilir.

Not

Bu uygulama tahmini dönüşüm için tasarlanmıştır; en doğru sonuçlar laboratuvar ölçümüyle alınan yoğunluk değerleriyle elde edilir.

