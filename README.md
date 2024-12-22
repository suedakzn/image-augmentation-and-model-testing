# Image Augmentation and Model Testing

## Proje Açıklaması
Bu proje, veri artırma (image augmentation) tekniklerini ve farklı test setleri üzerinde bir modelin başarımını incelemeyi hedeflemektedir. 
Proje kapsamında model eğitimi, manipüle edilmiş test setleri ile modelin doğruluğunun değerlendirilmesi ve renk sabitliği (white balance) uygulanmış test seti sonuçlarının karşılaştırılması yapılmıştır.

## Veri Seti
- **Kullanılan Veri Seti:** ImageNet veri setinden alınan bir alt veri kümesi.
- **Sınıf Sayısı:** 10 farklı sınıf.
- **Veri Sayısı:** Her sınıftan 650 görüntü (toplamda 6500 görüntü).

## Kullanılan Kütüphaneler
Projede aşağıdaki Python kütüphaneleri kullanılmıştır:

- `TensorFlow/Keras`: Model eğitimi ve değerlendirmesi
- `NumPy`: Veri işlemleri
- `Matplotlib`: Grafik çizimi ve sonuçların görselleştirilmesi
- `OpenCV`: Görüntü işleme işlemleri
- `Pandas`: Veri düzenleme ve analiz

## Proje Adımları

### 1. Veri Ön İşleme
- Görüntülerin normalize edilmesi ve boyutlarının 128x128 olarak ayarlanması.
- Eğitim ve test setlerinin oluşturulması.

### 2. Model Eğitimi
- **Model Yapısı:** Derin öğrenme modeli (CNN tabanlı) kullanıldı.
- **Parametreler:**
  - Epoch sayısı: 10
  - Batch boyutu: 32
  - Optimizasyon: Adam Optimizer
- Eğitim doğruluğu ve kayıp grafikleri oluşturuldu.

### 3. Test Setinin Değerlendirilmesi
- Orijinal test setiyle modelin doğruluğu hesaplandı. Sonuç:
  - **Doğruluk:** %61.95

### 4. Veri Artırma (Augmentation)
- Görüntü manipülasyonu işlemleri:
  - Parlaklık değişiklikleri (brightness manipulation)
  - Renk sabitliği (white balance) uygulanması

### 5. Manipüle Edilmiş Test Setleri ile Model Değerlendirme
- Manipüle edilmiş test setiyle model doğruluğu hesaplandı. Sonuç:
  - **Manipüle edilmiş test doğruluğu:** %10.41

### 6. Renk Sabitliği (White Balance) ile Model Değerlendirme
- Renk sabitliği algoritması (Gray World) uygulanmış test setiyle model doğruluğu hesaplandı. Sonuç:
  - **Renk sabitliği uygulanmış test doğruluğu:** %10.38

### 7. Sonuçların Karşılaştırılması
- Orijinal, manipüle edilmiş ve renk sabitliği uygulanmış test setlerinin doğruluk oranları grafikle görselleştirildi.

| Test Seti                          | Doğruluk (%) |
|------------------------------------|--------------|
| Orijinal Test Seti                | 61.95        |
| Manipüle Edilmiş Test Seti        | 10.41        |
| Renk Sabitliği Uygulanmış Test Seti | 10.38         |

### 8. Raporlama ve İyileştirme Önerileri
Sonuçlar, manipüle edilmiş ve renk sabitliği uygulanmış test setlerinde doğruluğun düşük olduğunu göstermektedir. İyileştirme önerileri:
- **Veri artırma tekniklerinin çeşitlendirilmesi:** Daha fazla veri manipülasyonu (döndürme, yakınlaştırma vb.).
- **Model karmaşıklığının artırılması:** Daha derin bir ağ yapısı veya farklı model mimarilerinin kullanılması.
- **Daha büyük ve dengeli veri setleri:** Eğitim ve test setlerindeki veri çeşitliliğinin artırılması.

## Projeyi Çalıştırma
1. Bu repo içerisindeki notebook dosyasını (`.ipynb`) indirin.
2. Gerekli kütüphaneleri kurun:
   ```bash
   pip install tensorflow numpy matplotlib opencv-python
   ```
3. Notebook'u çalıştırarak adımları takip edin ve sonuçları analiz edin.

## Sonuç
Bu proje, görüntü manipülasyonu ve model test süreçlerini kapsamlı bir şekilde ele almıştır. Sonuçların düşük olması, özellikle veri çeşitliliği ve model karmaşıklığının iyileştirilmesi gerektiğini göstermektedir. Bu öneriler doğrultusunda, gelecekte daha yüksek doğruluk oranlarına ulaşılması hedeflenebilir.

---
**Not:** Projeyle ilgili daha fazla bilgi için [Kaggle notebook](https://www.kaggle.com/code/suedakazan/image-augmentation-and-model-testing) sayfasını ziyaret edebilirsiniz.
