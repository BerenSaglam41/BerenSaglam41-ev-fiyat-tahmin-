# Ev Fiyat Tahmin Sistemi

## Proje Hakkında
Bu proje, **Akbank Makine Öğrenmesi Bootcamp** kapsamında geliştirilmiş gözetimli öğrenme tabanlı bir ev fiyat tahmin sistemidir. Çeşitli makine öğrenmesi algoritmaları kullanılarak ev özelliklerine dayalı fiyat tahmini yapılmaktadır.

## Veri Seti
- **Kaynak**: [Kaggle - House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)  
- **Hedef**: Ev Fiyatı

## Gerçek Hayatta Kullanımı
- **Emlak Değerleme**: Gayrimenkul ekspertizi için otomatik fiyat tahmini  
- **Yatırım Analizi**: Emlak yatırım kararlarında destek  
- **Kredi Değerlendirme**: Bankalar için teminat olarak gösterilen evleri değerleme  
- **Pazar Analizi**: Emlak piyasası trend analizi

## Kullanılan Algoritmalar
- Linear Regression  
- Ridge Regression  
- Lasso Regression *(Satırı çalıştırmadım çok uzun sürüyor)*  
- ElasticNet  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- K-Nearest Neighbours (KNN)  
- Support Vector Machine (SVM)

## Proje Adımları

### 1. Kütüphaneler ve Veri Yükleme

### 2. Veri Ön İşleme
- Tarih formatı düzenleme  
- Yeni değişken türetme (ör: `house_age`, `sqft_per_room`)  
- Kategorik dönüşümler  
- Outlier (aykırı değer) analizi

### 3. Veri Görselleştirme
- Dağılım grafikleri  
- Korelasyon matrisi  
- Lokasyon bazlı analizler

### 4. Modelleme
#### Özellik Ölçeklendirme  
#### Model Eğitimi  
#### Model Karşılaştırma
- MAE, MSE, RMSE, R²  
- Cross-validation R²  
- Eğitim süreleri

### 5. Hiperparametre Optimizasyonu
- En iyi model: Gradient Boosting  
- `RandomizedSearchCV` ile parametre optimizasyonu  
- Final sonuçların karşılaştırması

### 6. Sonuç ve Test Aşaması

## Metrikler
Bu projede, **Gradient Boosting** regresyon modeli kullanarak bir hedef değişkeni tahmin etmeye çalıştım. Çünkü **Random Forest** kullandığımda optimizasyon yaparken bir düşüş olduğunu fark ettim ve sonra ikisini karşılaştırıp Gradient Boosting kullanmam gerektiğini anladım. Çünkü Random Forest'ta optimizasyon sırasında tahmin değerleri düşerken, bunun aksine Gradient Boosting'te bu değerler artıyor. Normalde ikisini karşılaştırıp orada da yüksek değeri alacaktım ama bu yaklaşık 7 dakika sürüyor. Bu yüzden doğrudan Gradient Boosting'i `best_model` olarak seçtim. Bunu da kodun içinde belirttim. Sonuç olarak, hiperparametre optimizasyonu ile modeli daha doğru ve kararlı hale getirebildim. Bu da, gerçek dünya uygulamalarında daha güvenilir tahminler yapılabileceği anlamına geliyor.

## Sonuç ve Gelecek Çalışmalar
Bu proje benim için çok güzel bir deneyim oldu. Öğrendiğim şeyleri uygulama fırsatı buldum ve bundan sonra daha iyi hale getirmek için birkaç fikrim var:

- **Gerçek Zamanlı ve Dinamik Veri Toplama**: Şu anki veri seti statik ve önceden hazırlanmış. Gelecekte, gerçek zamanlı veri akışını entegre ederek modelin güncel ve dinamik verilerle beslenmesini istiyorum. Bu, modelin adaptasyon kabiliyetini artırır ve daha güncel tahminler yapılmasını sağlar.

- **Daha İyi Modeller ve Teknolojiler**: Makine öğrenmesi ve yapay zeka alanında sürekli yeni şeyler çıkıyor. İleride daha gelişmiş modeller deneyip performansı artırmak isterim. Ayrıca sonuçların neden böyle çıktığını daha iyi anlatabilmek de önemli.

- **Kariyerim İçin**: Bu proje benim yapay zeka ve veri bilimi alanında ilerlememi sağladı. Gelecekte bu alanda daha çok şey öğrenip, bu tür projelerde çalışmak ve kendimi geliştirmek istiyorum.

## Linkler
- [Veri Seti - Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)  
- [Proje Not Defteri - Kaggle](https://www.kaggle.com/code/mustafaberen/house-regressions)
