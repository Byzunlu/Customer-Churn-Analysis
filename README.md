# Customer Churn Analysis 📉

*A SQLite + Python (pandas, numpy, matplotlib, seaborn) exploratory data analysis project investigating why customers cancel their subscriptions.*

🇹🇷 Bu dosyanın Türkçe versiyonu için: [README.tr.md](README.tr.md)

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
├── README.md                # This file (English)
└── README.tr.md             # Turkish version
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

### Notes
- If your database contains real customer data (names, personal info), consider **not** uploading it publicly, or anonymizing it first.

### License
This project is open source and available under the [MIT License](LICENSE).
