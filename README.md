# Mall_Customers-LogisticRegression-DecisionTreeC
Müşteri Cinsiyet Tahmin Analizi
Bu proje, müşterilerin yaş, yıllık gelir ve harcama puanına dayalı olarak cinsiyetlerini tahmin etmek için Lojistik Regresyon ve Karar Ağacı sınıflandırma modellerini kullanır. Kullanılan veri kümesi, alışveriş merkezi müşterilerinin demografik ve harcama verilerini içeren Mall_Customers.csv dosyasıdır.

İçindekiler
Veri Kümesine Genel Bakış
Veri Ön İşleme
Model Uygulaması
Performans Değerlendirmesi
Bağımlılıklar
Projeyi Çalıştırma
Veri Kümesine Genel Bakış
Veri kümesi, aşağıdaki sütunları içeren 200 kayıttan oluşur:

CustomerID: Her müşteriye atanan benzersiz kimlik (modelleme için kullanılmamıştır).
Gender: Müşterinin cinsiyeti (Erkek/Kadın).
Age: Müşterinin yaşı.
Annual Income (k$): Müşterinin yıllık geliri (bin dolar cinsinden).
Spending Score (1-100): Müşterinin harcama davranışına dayalı olarak atanmış puan.
Veri Ön İşleme
Kategorik Değişkenlerin Kodlanması:

Gender sütunu, LabelEncoder kullanılarak sayısal değerlere dönüştürülür:
Male: 1
Female: 0
Özellik Seçimi:

Modelleme için kullanılan özellikler:
Age
Annual Income (k$)
Spending Score (1-100)
Hedef değişken: Gender
Eğitim-Test Ayrımı:

Veri kümesi, train_test_split kullanılarak eğitim (%90) ve test (%10) setlerine ayrılmıştır.
Standardizasyon:

Özellikler, değerleri normalleştirmek ve model performansını artırmak için StandardScaler kullanılarak ölçeklendirilmiştir.

Classification report:

            precision    recall  f1-score   support

         0       0.50      0.80      0.62        10
         1       0.50      0.20      0.29        10

  accuracy                           0.50        20
 macro avg       0.50      0.50      0.45        20

weighted avg       0.50      0.50      0.45        20


### Decision Tree Results
- **Accuracy**: 65%
- Classification report:

          precision    recall  f1-score   support

       0       0.59      1.00      0.74        10
       1       1.00      0.30      0.46        10

accuracy                           0.65        20

macro avg       0.79      0.65      0.60        20
weighted avg       0.79      0.65      0.60        20


### Heatmaps
- Confusion matrices for both models are visualized using heatmaps.

---

## Dependencies

- Python 3.9+
- Required libraries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

---

## How to Run the Project

1. Clone the repository:
 ```bash
 git clone <repository-url>
 cd <repository-folder>

Install dependencies:

pip install -r requirements.txt

Place the Mall_Customers.csv file in the working directory.

Run the script:

python main.py

View results, including classification reports and heatmaps, in the terminal and plots displayed during execution.
