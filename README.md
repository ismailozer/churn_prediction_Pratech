# 🛒 E-Ticaret Müşteri Kayıp (Churn) Tahmini (GÖREV 7)

Bu proje, bir e-ticaret platformundaki müşteri davranışlarını analiz ederek, platformu terk etme (churn) riski olan müşterileri tahmin eden uçtan uca bir Makine Öğrenmesi pipeline'ı içerir. **Pratech Teknik Değerlendirme** süreci kapsamında hazırlanmıştır.

## 🚀 Öne Çıkan Özellikler
- **İş Zekası Odaklı Özellik Mühendisliği:** Müşteri şikayet oranı, pasiflik riski ve indirim duyarlılığı gibi yeni metrikler üretilmiştir.
- **Dengesiz Veri Yönetimi:** Azınlık sınıfı (Churn) SMOTE algoritması kullanılarak dengelenmiştir.
- **Pipeline Mimarisi:** Veri ön işleme ve modelleme adımları, veri sızıntısını (data leakage) önlemek adına Scikit-learn Pipeline yapısı ile kurgulanmıştır.
- **Model Performansı:** LightGBM ve Random Forest modelleri kıyaslanmış; yüksek Recall (Duyarlılık) değerine odaklanılarak müşteri kaybı minimize edilmiştir.

## 📊 Sonuçlar
- **En İyi Model:** LightGBM
- **F1-Score:** ~0.91
- **ROC-AUC:** 0.99
- **Odak Metrik:** Recall (Müşteri kaybını yakalama başarısı önceliklendirilmiştir.)

## 🛠️ Kurulum ve Çalıştırma
1. Bu depoyu klonlayın: `git clone <repo-linki>`
2. Sanal ortam oluşturun ve aktif edin: `python -m venv venv`
3. Gerekli kütüphaneleri yükleyin: `pip install -r requirements.txt`
4. `churn_prediction.ipynb` dosyasını çalıştırın.

## 📁 Dosya Yapısı
- `churn_prediction.ipynb`: Tüm analiz ve modelleme süreçlerini içeren Jupyter Notebook.
- `ecommerce_customer_features.csv`: Müşteri özellikleri veri seti.
- `ecommerce_customer_targets.csv`: Hedef değişken (churn) veri seti.
- `requirements.txt`: Gerekli kütüphaneler listesi.