# OCR Masking with Python 🖼️🔒

Bu projede, bir görsel içerisindeki yazılar OCR (Optik Karakter Tanıma) yöntemiyle tanımlanır ve her kelimenin yalnızca ilk 3 harfi açık bırakılarak geri kalanı yıldız (`*`) karakteriyle maskelenir.

---

## 📌 1. Giriş (Introduction)

Görsellerde yer alan metinlerin işlenmesi, birçok güvenlik ve gizlilik uygulamasında kritik öneme sahiptir. Bu proje, temel OCR teknikleri kullanılarak bir görseldeki yazıyı algılamayı ve veri gizliliği sağlamak amacıyla yalnızca kelimenin ilk üç harfini gösterip geri kalanını maskelemeyi hedefler.

---

## ⚙️ 2. Yöntem (Method)

- **Dil:** Python 3
- **Kütüphaneler:** `pytesseract`, `opencv-python`, `Pillow`
- **OCR Motoru:** [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- **İşlem Aşamaları:**
  1. Görsel dosyası OpenCV ile yüklenir.
  2. `pytesseract` kullanılarak Türkçe metin OCR ile çıkarılır.
  3. Her kelimenin ilk 3 harfi korunur, kalan harfler `*` ile maskelenir.
  4. Konsola hem orijinal hem maskelenmiş metin yazdırılır.

> Türkçe karakterlerin doğru tanınması için Tesseract'a `tur.traineddata` dil dosyası eklenmelidir.

---

## 🧪 3. Sonuçlar (Results)

Örnek giriş görsel (`BERAT.png`) metni:  

`BERAT`

Maskelenmiş:

`BER**`

---

## 💬 4. Değerlendirme (Discussion)

Bu proje, temel OCR uygulamalarını basit bir metin maskeleme tekniğiyle birleştirerek güvenlik odaklı mini bir metin işleme aracı sunmaktadır. Geliştirme alanları şunlardır:

- Maskelenmiş metni tekrar görsele yazma (OpenCV ile)
- Web tabanlı arayüz (Streamlit/Gradio)
- PDF, belge gibi daha karmaşık veri türleri için destek
- Kutucuklarla OCR görselleştirmesi

---

## 🚀 Nasıl Çalıştırılır? (Quickstart)

1. `tesseract-ocr` kur: [Windows için link](https://github.com/UB-Mannheim/tesseract/wiki)
2. `tur.traineddata` dosyasını `tessdata/` klasörüne koy
3. Gerekli Python kütüphanelerini yükle:
   ```bash
   pip install pytesseract opencv-python pillow
   ```

---

## Gereksinimler
Python 3.8+

Tesseract OCR yüklü ve tesseract.exe yolu ayarlanmış

Türkçe dil desteği için tur.traineddata

---

## Hazırlayan
**Berat Çalık**

Ankara Üniversitesi - Yapay Zeka ve Veri Mühendisliği

