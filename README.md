# Kalp Hastalığı Tahmini (Heart Disease Prediction)

## Proje Açıklaması
Bu proje, Kaggle'da bulunan Heart_Disease_Prediction.csv veri setini kullanarak **Makine Öğrenmesi** yöntemleriyle bireylerin kalp hastalığı riskini tahmin etmeyi amaçlamaktadır.

Çalışma; **Keşifçi Veri Analizi (EDA)**, temel modelleme, hiperparametre optimizasyonu ve model yorumlama adımlarını içermektedir. Projenin ana hedefi, yüksek doğruluk oranına sahip, aynı zamanda yorumlanabilir bir sınıflandırma modeli geliştirmektir.

## Veri Seti
Projede kullanılan *Heart_Disease_Prediction.csv* veri seti, çeşitli sağlık parametrelerini içermektedir. Temel olarak incelenen özellikler şunlardır:
* `Age` (Yaş)
* `Sex` (Cinsiyet)
* `ChestPainType` (Göğüs Ağrısı Tipi)
* `BP` (Dinlenme Kan Basıncı)
* `Cholesterol` (Kolesterol Seviyesi)
* `FBS over 120` (Açlık kan şekeri)
* `EKG results` (Dinlenme EKG sonucu)
* `MaxHR` (Maksimum kalp atış hızı)
* `ExerciseAngina` (Egzersizle tetiklenen anjina (0 veya 1))
* `ST depression` (ST segmenti depresyonu)
* `Slope of ST` (ST segmentinin eğimi)
* `Number of vessels fluro` (Floroskopi ile tespit edilen tıkanmış damar sayısı)
* `Thallium` (Talium stres testi sonucu)
*  Kalp Hastalığı (`HeartDisease`) hedef değişken.

## Uygulanan Metodoloji ve Adımlar

Proje, titiz bir veri bilimi süreci izlenerek aşağıdaki aşamalarla tamamlanmıştır:

1.  **Veri Hazırlığı ve Keşifçi Veri Analizi (EDA):**
    * Veri setindeki kayıp ve aykırı değerlerin incelenmesi.
    * Özellik dağılımlarının ve hedef değişken ile ilişkilerinin görselleştirilmesi (**Matplotlib** ve **Seaborn**).
    * Veri seti temizliği ve ön işleme adımları.

2.  **Temel Modelleme:**
    * Sınıflandırma için başlangıç modeli olarak **Lojistik Regresyon** kullanılmıştır.

3.  **Gelişmiş Modelleme ve Optimizasyon:**
    * Modelin genelleme yeteneğini artırmak için **Stratified K-Fold** çapraz doğrulama yöntemi kullanılmıştır.
    * Model performansını maksimize etmek amacıyla **Grid Search** yöntemi ile hiperparametre optimizasyonu yapılmıştır.

4.  **Model Yorumlama:**
    * Elde edilen nihai modelin performansı **(Model Doğruluk (Accuracy) Skoru, ROC AUC Skoru, Confusion Matrix Değeri, precision, recall, f1-score vb. metrikler)** değerlendirilmiştir.
    * En iyi parametrelerle yeniden eğitilmiş modelin **Katsayı Analizi** ile hangi özelliklerin (yaş, kolesterol, göğüs ağrısı vb.) kalp hastalığı tahmini üzerindeki etkisinin en yüksek olduğu yorumlanmıştır.

## Kullanılan Teknolojiler
* **Python**
* **Jupyter Notebook:** (Ana çalışma dosyası: `heart-disease-prediction.ipynb`)
* **Pandas:** Veri işleme ve analizi için temel kütüphane.
* **Numpy:** Sayısal işlemler ve dizilerle çalışmak için.
* **Scikit-learn (sklearn):** Makine öğrenmesi modeli oluşturmak ve değerlendirmek için.
* **Matplotlib & Seaborn:** Veri görselleştirme için.

## Kurulum ve Çalıştırma

Bu projeyi kendi bilgisayarınızda çalıştırmak için şu adımları takip edebilirsiniz:

1.  Gerekli kütüphaneleri yükle:
    `pip install pandas numpy matplotlib seaborn plotly`
2.  Proje klasörüne git ve Jupyter Notebook'u başlat:
    `jupyter notebook`
3.  Tarayıcında açılan ekrandan `heart-disease-prediction.ipynb` dosyasını açıp çalıştırabilirsiniz.

### Kaggle Proje Linki:https://www.kaggle.com/code/mehmetren/heart-disease-prediction
