# Eksperimen Machine Learning - Mohammad Fajar Ma'shum

## 📊 Project Overview

Proyek ini merupakan bagian dari submission **Machine Learning System and MLOps** yang menggunakan dataset Titanic untuk memprediksi kelangsungan hidup penumpang.

## 🎯 Objective

Melakukan eksperimen dan preprocessing data untuk membangun model machine learning yang dapat memprediksi apakah seorang penumpang Titanic selamat atau tidak berdasarkan fitur-fitur seperti usia, jenis kelamin, kelas tiket, dll.

## 📁 Repository Structure

```
Eksperimen_SML_Mohammad-Fajar-Mashum/
├── README.md
├── titanic_raw.csv                                    # Dataset asli
└── preprocessing/
    ├── Eksperimen_Mohammad-Fajar-Mashum.ipynb        # Notebook eksperimen
    ├── titanic_preprocessing.csv                      # Data hasil preprocessing
    └── titanic_target.csv                             # Target variable
```

## 📚 Dataset Information

**Dataset**: Titanic - Machine Learning from Disaster  
**Source**: Kaggle  
**Total Samples**: 418 rows  
**Features**: 12 columns

### Features Description:
- `PassengerId`: ID unik penumpang
- `Survived`: Status kelangsungan hidup (0 = Tidak selamat, 1 = Selamat) **[TARGET]**
- `Pclass`: Kelas tiket (1, 2, 3)
- `Name`: Nama penumpang
- `Sex`: Jenis kelamin (male, female)
- `Age`: Usia dalam tahun
- `SibSp`: Jumlah saudara kandung/pasangan di kapal
- `Parch`: Jumlah orang tua/anak di kapal
- `Ticket`: Nomor tiket
- `Fare`: Harga tiket
- `Cabin`: Nomor kabin
- `Embarked`: Pelabuhan keberangkatan (C, Q, S)

## 🔬 Experimentation Process

### 1. Data Loading
- Load dataset menggunakan pandas
- Explorasi struktur data awal

### 2. Exploratory Data Analysis (EDA)
- ✅ Missing values analysis
- ✅ Target variable distribution
- ✅ Numerical features analysis
- ✅ Categorical features analysis
- ✅ Correlation analysis
- ✅ Survival analysis by features

### 3. Data Preprocessing
- ✅ Handle missing values (Age, Fare, Embarked)
- ✅ Feature engineering:
  - `FamilySize` = SibSp + Parch + 1
  - `IsAlone` = (FamilySize == 1)
  - `AgeGroup` = Age binning
  - `FareBin` = Fare binning
- ✅ Drop unnecessary columns (PassengerId, Name, Ticket, Cabin)
- ✅ Encode categorical variables (Label Encoding)
- ✅ Feature scaling (StandardScaler)
- ✅ Train-test split (80:20)

## 🛠️ Technologies Used

- **Python 3.12.7**
- **pandas**: Data manipulation
- **numpy**: Numerical computing
- **matplotlib & seaborn**: Data visualization
- **scikit-learn**: Machine learning & preprocessing

## 📈 Key Findings

- **Survival Rate**: ~38% penumpang selamat
- **Gender Impact**: Perempuan memiliki tingkat keselamatan lebih tinggi
- **Class Impact**: Penumpang kelas 1 memiliki tingkat keselamatan lebih tinggi
- **Missing Data**: Cabin (77%), Age (20%), Embarked (<1%)

## 🚀 How to Run

1. Clone repository:
```bash
git clone https://github.com/YOUR_USERNAME/Eksperimen_SML_Mohammad-Fajar-Mashum.git
cd Eksperimen_SML_Mohammad-Fajar-Mashum
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Run Jupyter Notebook:
```bash
cd preprocessing
jupyter notebook Eksperimen_Mohammad-Fajar-Mashum.ipynb
```

4. Run all cells in the notebook

## 📝 Next Steps

- [ ] Build machine learning model with MLflow
- [ ] Create CI/CD workflow with GitHub Actions
- [ ] Implement monitoring and logging system

## 👤 Author

**Mohammad Fajar Ma'shum**  
Submission: Machine Learning System and MLOps

## 📄 License

This project is created for educational purposes.

---

⭐ **Status**: Kriteria 1 - Basic ✅ Completed
