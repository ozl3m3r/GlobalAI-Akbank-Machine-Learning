# GlobalAI-Akbank-Machine-Learning

# ❤️ Heart Disease Prediction - Akbank Machine Learning Bootcamp

Bu proje, **2020 CDC Behavioral Risk Factor Surveillance System (BRFSS)** veri seti kullanılarak, bireylerin kalp hastalığı risklerini tahmin etmeyi amaçlamaktadır. Çalışma, **Akbank Machine Learning Bootcamp** kapsamında gerçekleştirilmiştir.

## 📌 Veri Seti Hakkında

- **Kaynak:** https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease
- **Kapsam:** 319.795 birey, 18 değişken.
- **Hedef Değişken:** `HeartDisease` (0: Hayır, 1: Evet)
- 
## 🧠 Kullanılan Yöntemler ve Süreç

- **Veri Ön İşleme:** Kategorik değişkenler kodlanmış, sayısal veriler standartlaştırılmıştır.
- **Özellik Mühendisliği:** Yeni değişkenler (örneğin `BMI_Category`, `UnhealthyScore`, `RiskyLifestyle`) türetilerek model performansı artırılmaya çalışılmıştır.
- **Modelleme:** Üç farklı makine öğrenmesi algoritması ile modeller kurulmuştur:
  - Random Forest
  - XGBoost
  - LightGBM
- **Dengesiz Veri Problemi:** `class_weight='balanced'` ve `scale_pos_weight` gibi parametrelerle ele alınmıştır.

---

## 📊 Metrikler

Aşağıda modellerin test verisinde gösterdiği performans karşılaştırmaları yer almaktadır:

| Model         | Accuracy | Recall | F1 Score |
|---------------|----------|--------|----------|
| Random Forest | 0.85     | 0.78   | 0.81     |
| XGBoost       | 0.86     | 0.80   | 0.83     |
| LightGBM      | 0.87     | 0.82   | 0.84     |

> ⚠️ Not: Recall değerine özellikle odaklanılmıştır çünkü kalp hastalığı gibi kritik bir durumda **pozitif sınıfın (hastalığın) doğru yakalanması** hayati öneme sahiptir.

---

## 🚀 Sonuç ve Gelecek Çalışmalar

Modelimiz kalp hastalığı tahmini konusunda oldukça başarılı sonuçlar vermektedir. Ancak geliştirilebilecek bazı yönler şunlardır:

- **Gerçek zamanlı veri akışı:** CDC verisi her yıl güncelleniyor. Bu nedenle veri pipeline'ı dinamik hale getirilebilir.
- **Web tabanlı kullanıcı arayüzü:** Kullanıcıların kendi bilgilerini girerek tahmin alabilecekleri bir web uygulaması geliştirilebilir (Flask, Streamlit vb.).
- **Model açıklanabilirliği:** SHAP veya LIME gibi yöntemlerle modelin kararlarını açıklayan interaktif görsellikler eklenebilir.
- **Derin öğrenme modelleri:** Geniş veri kümesi için derin öğrenme tabanlı modeller (MLP, TabNet) denenebilir.


---

## 🔗 Linkler

- 📁 [Kaggle Notebook - Akbank ML Bootcamp](https://www.kaggle.com/code/ozl3m3r/akbank-machine-learning-bootcamp)

---

