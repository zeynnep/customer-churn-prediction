
# 🛒 Müşteri Kayıp (Churn) Tahmini ve Davranışsal Analiz

Bu proje, bir e-ticaret platformundaki müşterilerin gelecek 6 ay içindeki terk etme (churn) olasılıklarını tahmin etmek amacıyla geliştirilmiş uçtan uca bir makine öğrenmesi ürünüdür. Proje, sadece istatistiksel teoride kalmayıp, **Python** kullanılarak canlıya alınabilir bir modelleme mimarisine dönüştürülmüş ve doğrudan iş zekasına yönelik stratejik çıktılar üretmiştir.

## 🚀 Projenin İş Değeri ve Hedefleri
* **CRISP-DM Metodolojisi:** Veriyi anlama aşamasından, modelin canlıya alınabilir stratejiler üretmesine kadar tüm veri madenciliği süreçleri pratik bir yaklaşımla ele alınmıştır.
* **Erken Müdahale Sistemi:** %60'ın üzerinde churn riski taşıyan müşteriler tespit edilerek, kişiselleştirilmiş pazarlama kampanyaları için hazır bir hedef kitle oluşturulmuştur.
* **Kök Neden Analizi:** Kurulan modellerin "kara kutu" (black-box) olmasını engellemek için **SHAP** kullanılmış, churn üzerinde en çok etkisi olan faktörler şeffaf bir şekilde açıklanmıştır.

## 🛠️ Kullanılan Teknolojiler ve Geliştirme Yaklaşımı
* **Dil:** Python
* **Makine Öğrenmesi:** LightGBM (Gradient Boosting Framework)
* **Açıklanabilir Yapay Zeka (XAI):** SHAP (SHapley Additive exPlanations)
* **Model Doğrulama:** 5-Fold Stratified Cross-Validation
* **Veri Sızıntısı (Data Leakage) Kontrolü:** Klasik rastgele veri ayırma (train/test split) yerine gerçek dünya senaryosuna en uygun olan **Zamana Dayalı Ayrım (Temporal Split)** uygulanmıştır. (Eğitim: İlk 18 ay, Test: Son 6 ay)

## 📊 Öne Çıkan Analiz Sonuçları ve Çıktılar

SHAP analizleri sonucunda belirlenen en önemli faktörler ışığında şu stratejik aksiyonlar geliştirilmiştir:
1. >%60 riskli müşterilere özel "geri kazanım" (win-back) kampanyalarının düzenlenmesi.
2. Son 3 ayda harcama frekansı düşen müşterilere erken müdahale e-postaları gönderilmesi.

## 📁 Proje Klasör Yapısı

```text
├── data/
│   ├── Year 2009-2010.csv    # Veri setinin ilk kısmı (Boyut sınırından dolayı Github'da yoktur, kaynak linki aşağıdadır)
│   └── Year 2010-2011.csv    # Veri setinin ikinci kısmı
├── notebooks/
│   └── crisp_dm_churn_analizi_v2.ipynb  # Uçtan uca veri işleme, LightGBM modellemesi ve SHAP analizleri
├── docs/
│   └── proje_posteri.pdf     # 3.'lük getiren proje sunum posteri
├── README.md
└── requirements.txt          # Proje bağımlılıkları ve Python kütüphaneleri
