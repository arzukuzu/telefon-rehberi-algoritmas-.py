#  JSON Tabanlı Konsol Telefon Rehberi (Python)

Bu proje; kişi ekleme, silme, listeleme ve isimle arama işlemlerini gerçekleştiren, verileri **JSON** formatında kalıcı olarak saklayan modüler bir Python konsol uygulamasıdır.

---

##  Temel Özellikler

- **Kalıcı Veri Depolama (Data Persistence):** Kişi kayıtları `rehber.json` dosyası üzerinde saklanır; program kapansa dahi veriler kaybolmaz.
- **Hata Yönetimi (Error Handling):** `FileNotFoundError` ve `json.JSONDecodeError` durumları kontrol edilerek dosyanın bulunamaması veya bozuk olması halinde uygulamanın çökmesi engellenir.
- **Akıllı Arama (Substring Search):** İsim ve soyisim üzerinde büyük/küçük harf duyarsız (`case-insensitive`) ve metin/parça eşleşmesiyle arama yapılabilir.
- **Güvenli ve Etkileşimli Silme:** Aranan isimle eşleşen tüm kayıtlar numaralandırılarak gösterilir; kullanıcı doğru numarayı seçerek kaydı silebilir veya işlemi iptal edebilir.
- **Türkçe Karakter Desteği:** JSON işlemlerinde `utf-8` ve `ensure_ascii=False` kullanılarak karakter bozulmaları önlenir.

---

##  Desteklenen İşlemler

| No | İşlem | Açıklama |
| :---: | :--- | :--- |
| **1** | **Ekle** | Yeni bir kişi kaydını (ad, soyad, telefon) rehbere ekler ve kaydeder. |
| **2** | **Sil** | İsme göre eşleşen kayıtları listeler, seçilen numaradaki kişiyi rehberden siler. |
| **3** | **Listele** | Rehberdeki tüm kişileri sıralı ve numaralandırılmış olarak görüntüler. |
| **4** | **Ara** | İsim veya harf grubuna göre rehberde arama yapar. |
| **5** | **Çıkış** | Konsol uygulamasını sonlandırır. |

---

##  Kurulum ve Çalıştırma

Projeyi yerel makinenizde veya terminalinizde çalıştırmak için:

```bash
python main.py
```

> **Not:** İlk çalıştırmada `rehber.json` dosyası mevcut değilse otomatik olarak oluşturulacaktır.

---

##  Örnek Konsol Çıktısı

```text
1-Ekle
2-Sil
3-Listele
4-Ara
5-Çıkış 
Seçiminiz : 1
isim: Ahmet
soyad: Yılmaz
numara: 05551234567
Kişi eklendi.

1-Ekle
2-Sil
3-Listele
4-Ara
5-Çıkış 
Seçiminiz : 3
1. Ahmet Yılmaz 05551234567
```

---

##  Kullanılan Teknolojiler & Kütüphaneler

- **Dil:** Python 3.x
- **Kütüphaneler:** `json` (Python Standart Kütüphanesi)
- **Yapılar:** Dosya Yönetimi (`with open`), Hata Yönetimi (`try-except`), Koleksiyonlar (`list`, `dict`), Numaralandırma (`enumerate`)

---

