# Customer Churn Analysis 📉

*A SQLite + Python (pandas, numpy, matplotlib, seaborn) exploratory data analysis project investigating why customers cancel their subscriptions.*


---

### Overview
This project analyzes a subscription-based business's **customer churn** using data stored in a SQLite database (`customer_churn.db`). The analysis combines three tables — customers, subscriptions, and support interactions — to understand churn patterns, identify at-risk customer segments, and quantify revenue impact.

### Dataset
The SQLite database contains three tables:

| Table | Description |
|---|---|
| `db_customer` | Customer demographics: ID, name, country, state, gender, date of birth, interests |
| `db_subscription` | Subscription details: start/renewal/cancellation dates, plan type, contract type, monthly charges, CLTV, churn score |
| `db_support` | Support interactions: complaint dates, escalations, CSAT score, comments |

### What's inside the notebook
- Loading and joining data directly from SQLite using `sqlite3` and `pandas.read_sql`
- Data cleaning and feature engineering (e.g. deriving a `churn_flag` from cancellation dates, counting complaints per customer)
- **Churn rate** calculation, overall and by plan type
- **Revenue at risk** estimation from churned customers
- Correlation analysis between escalations, churn score, and churn
- Visualizations: churn trend over time, churn rate by state, correlation heatmaps, pairplots, and categorical comparisons (plan type, contract type, gender)
- Pivot tables summarizing churn and revenue by plan type

### Tech Stack
- Python 3
- SQLite (`sqlite3`)
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

### Project Structure
```
customer-churn-analysis/
├── churn_analysis.ipynb     # Main analysis notebook
├── customer_churn.db        # SQLite database (if included)
├── requirements.txt         # Python dependencies
├── README.md                # This file (English-Turkish)
```

### How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/customer-churn-analysis.git
   cd customer-churn-analysis
   ```
2. (Optional) Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook churn_analysis.ipynb
   ```

> **Note:** Make sure `customer_churn.db` is in the same folder as the notebook, since the code connects to it using a relative path.



# Müşteri Kayıp (Churn) Analizi 📉

*Müşterilerin abonelikleri neden iptal ettiğini inceleyen, SQLite ve Python (pandas, numpy, matplotlib, seaborn) kullanılarak yapılmış keşifsel veri analizi projesi.*
---

### Genel Bakış
Bu proje, bir abonelik tabanlı işletmenin **müşteri kaybını (churn)** SQLite veritabanında (`customer_churn.db`) saklanan verileri kullanarak analiz eder. Analiz; müşteri, abonelik ve destek etkileşimi olmak üzere üç tabloyu bir araya getirerek churn (kayıp) örüntülerini incelemeyi, risk altındaki müşteri segmentlerini belirlemeyi ve gelir kaybını sayısallaştırmayı amaçlar.

### Veri Seti
SQLite veritabanı üç tablo içerir:

| Tablo | Açıklama |
|---|---|
| `db_customer` | Müşteri demografik bilgileri: ID, isim, ülke, eyalet/il, cinsiyet, doğum tarihi, ilgi alanları |
| `db_subscription` | Abonelik bilgileri: başlangıç/yenileme/iptal tarihleri, plan türü, sözleşme türü, aylık ücret, CLTV, churn skoru |
| `db_support` | Destek etkileşimleri: şikayet tarihleri, eskalasyonlar, CSAT skoru, yorumlar |

### Notebook İçeriği
- `sqlite3` ve `pandas.read_sql` kullanılarak verinin doğrudan SQLite'tan yüklenmesi ve birleştirilmesi
- Veri temizleme ve özellik türetme (örn. iptal tarihinden `churn_flag` oluşturma, müşteri başına şikayet sayısı hesaplama)
- Genel ve plan türüne göre **churn oranı** hesaplaması
- Kaybedilen müşterilerden kaynaklanan **risk altındaki gelir** tahmini
- Eskalasyonlar, churn skoru ve churn arasındaki korelasyon analizi
- Görselleştirmeler: zaman içinde churn trendi, eyalete göre churn oranı, korelasyon ısı haritaları, pairplot'lar ve kategorik karşılaştırmalar (plan türü, sözleşme türü, cinsiyet)
- Plan türüne göre churn ve gelir özetleyen pivot tablolar

### Kullanılan Teknolojiler
- Python 3
- SQLite (`sqlite3`)
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

### Proje Yapısı
```
customer-churn-analysis/
├── churn_analysis.ipynb     # Ana analiz notebook'u
├── customer_churn.db        # SQLite veritabanı (dahil edildiyse)
├── requirements.txt         # Python bağımlılıkları
├── README.md                # İngilizce-Türkçe dosya
```

### Nasıl Çalıştırılır
1. Repoyu klonlayın:
   ```bash
   git clone https://github.com/<kullanici-adiniz>/customer-churn-analysis.git
   cd customer-churn-analysis
   ```
2. (Opsiyonel) Sanal ortam oluşturun:
   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```
3. Gerekli paketleri kurun:
   ```bash
   pip install -r requirements.txt
   ```
4. Jupyter'ı başlatıp notebook'u açın:
   ```bash
   jupyter notebook churn_analysis.ipynb
   ```

> **Not:** Notebook, `customer_churn.db` dosyasına göreli (relative) bir yol ile bağlandığı için veritabanı dosyasının notebook ile aynı klasörde olduğundan emin olun.

