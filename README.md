## 📊 Diabetes Prediction Model

Bu proje, Pima Indian kadınları üzerine yapılan bir diyabet araştırmasına ait veri setiyle, bireylerin diyabet hastası olup olmadığını tahmin etmeye yönelik bir makine öğrenmesi modeli geliştirmeyi amaçlar. Modeli eğitmeden önce kapsamlı bir veri analizi ve özellik mühendisliği süreci gerçekleştirilmiştir.

---

## 📁 Veri Seti Hakkında

Veri seti, ABD’deki Ulusal Diyabet-Sindirim-Böbrek Hastalıkları Enstitüleri tarafından toplanmıştır. Arizona Eyaleti’nin Phoenix şehrinde yaşayan, 21 yaş ve üzerindeki Pima Indian kadınlarına ait bilgiler içermektedir.

- **Toplam Gözlem Sayısı**: 768  
- **Bağımsız Değişkenler**: 8  
- **Hedef Değişken**: `Outcome` (1: Diyabet Pozitif, 0: Negatif)

### 🔍 Değişkenler

| Değişken                  | Açıklama                                                                 |
|---------------------------|--------------------------------------------------------------------------|
| `Pregnancies`             | Hamilelik sayısı                                                        |
| `Glucose`                 | Glikoz değeri                                                           |
| `BloodPressure`           | Kan basıncı (Diastolic - Küçük Tansiyon)                                |
| `SkinThickness`           | Cilt kalınlığı                                                          |
| `Insulin`                 | İnsülin düzeyi                                                          |
| `BMI`                     | Beden kitle indeksi                                                     |
| `DiabetesPedigreeFunction`| Aile geçmişine göre diyabet olasılığı                                    |
| `Age`                     | Yaş                                                                     |
| `Outcome`                 | Hedef değişken – Diyabet hastalığı (1: Pozitif, 0: Negatif)             |

---

## 🛠 Kullanılan Teknolojiler ve Kütüphaneler

Bu projede kullanılan başlıca teknolojiler ve kütüphaneler şunlardır:

- **Python**: Veri analizi, modelleme ve görselleştirme işlemleri için tercih edilen ana programlama dili.

- **pandas**: Veri setini yüklemek, temizlemek ve dönüştürmek için kullanıldı. Özellikle (`DataFrame`) yapısı sayesinde, verilerin kolayca işlenmesini ve manipüle edilmesini sağladı.

- **numpy**: Matematiksel hesaplamalar, özellikle veri setindeki sayısal özelliklerin işlenmesi ve işlemlerinin hızlandırılması amacıyla kullanıldı. Model için gereken matematiksel işlemleri hızlı ve verimli bir şekilde gerçekleştirdi.

- **matplotlib** ve **seaborn**: Veri görselleştirmeleri oluşturmak için kullanıldı. `matplotlib`, temel grafiklerin çizilmesinde; `seaborn`, daha estetik ve anlaşılır dağılım grafikleri ve ısı haritaları gibi görselleştirmelerin oluşturulmasında tercih edildi.

- **scikit-learn**: Makine öğrenmesi modellemesi için kullanıldı. Modelin eğitilmesi ve değerlendirilmesi süreçlerinde, özellikle:
  - **RandomForestClassifier**: Diyabet tahmin modelinin oluşturulmasında, karar ağaçlarının bir araya getirilerek güçlü bir sınıflandırma modeli sağlamak için kullanıldı.
  - **StandardScaler**: Modelin eğitim verisinin özelliklerini standartlaştırarak, farklı ölçeklere sahip verilerin model üzerinde daha sağlıklı bir şekilde öğrenilmesini sağladı.
  - **LabelEncoder**: Kategorik değişkenlerin sayısal verilere dönüştürülmesi için kullanıldı, böylece model veriyi doğru şekilde işleyebildi.



---

## 📌 Proje Adımları

### 1. Keşifçi Veri Analizi (Exploratory Data Analysis)

- Veri setinin yapısı incelendi.
- Değişken türleri ayrıştırıldı (sayısal & kategorik).
- Değişkenlerin dağılımları, aykırı değerler ve eksik veri kontrol edildi.
- Hedef değişken (`Outcome`) ile ilişkiler incelendi.

### 2. Veri Ön İşleme

- Ayırıcı nitelikteki eksik değerler belirlendi ve uygun şekilde dönüştürüldü.
- Aykırı değerlerin etkisi incelendi.
- Numerik değişkenler için `StandardScaler` ile standartlaştırma yapıldı.

### 3. Özellik Mühendisliği (Feature Engineering)

- Yeni değişkenler üretildi (örneğin yaş ve BMI grupları).
- `Pregnancies`, `Age`, `Glucose` gibi değişkenlerin etkileşimleri kontrol edildi.
- Gerekirse kategorik dönüşümler ve feature encoding işlemleri yapıldı.

### 4. Modelleme ve Değerlendirme

- `RandomForestClassifier` algoritması kullanıldı.
- `train_test_split` ile veri ayrılarak model eğitildi.
- Performans metrikleri: Accuracy, Precision, Recall, F1 Score, ROC-AUC
- Modelin doğruluğu ve genellenebilirliği test edildi.

---

