## 🧠 Customer Segmentation Tool

A machine learning-based tool that segments customers using RFM analysis and KMeans clustering. Built with Streamlit for an interactive UI, this app helps businesses understand customer behavior and target groups effectively.

---

### 📌 Problem Statement

E-commerce platforms often struggle to tailor their marketing efforts to different customer types. This project solves that by grouping customers into segments based on their purchasing behavior, using Recency, Frequency, and Monetary (RFM) features.

---

### 📊 Dataset

* Source: [Kaggle – E-Commerce Customer Data](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
* Contains over 400,000 transactions from a UK-based online retailer between 2010–2011.

---

### 🛠️ Tech Stack

* **Language**: Python
* **Data Handling**: Pandas, NumPy
* **ML Model**: Scikit-Learn (KMeans Clustering)
* **Visualization**: Plotly, Seaborn
* **UI**: Streamlit
* **Other Tools**: Jupyter Notebook, Anaconda

---

### 🔍 Approach

#### 📌 Step 1: Data Preprocessing

* Handled missing values
* Removed canceled (negative quantity) transactions
* Filtered for United Kingdom-based customers

#### 📌 Step 2: RFM Feature Engineering

* **Recency** = days since last purchase
* **Frequency** = number of purchases
* **Monetary** = total money spent

#### 📌 Step 3: Clustering with KMeans

* Scaled the RFM data using `StandardScaler`
* Used Elbow Method to find optimal number of clusters
* Applied **KMeans** to group customers into segments

#### 📌 Step 4: Streamlit UI

* User selects Recency, Frequency, and Monetary values using sliders
* Predicts customer segment instantly based on trained model
* Displays interpretation of cluster (e.g., High-value, At-risk, etc.)

---

### 💡 Features

* RFM-based clustering using KMeans
* Interactive sliders for user input
* Real-time cluster prediction
* Visualized summary of all customer segments
* Easy to deploy as a Streamlit web app

---

### 🚀 How to Run

#### 1. Clone the repo

```bash
git clone https://github.com/yourusername/customer-segmentation-tool.git
cd customer-segmentation-tool
```

#### 2. Install dependencies

Make sure you activate your environment first (optional but recommended). Then run:

```bash
pip install -r requirements.txt
```

#### 3. Launch the Streamlit app

```bash
streamlit run app.py
```

---

### 📁 Folder Structure

```
├── app.py                  # Streamlit UI code
├── rfm_clustered.csv       # Final dataset with cluster labels
├── kmeans_model.pkl        # Saved clustering model
├── scaler.pkl              # Saved scaler
├── segmentation.ipynb      # Jupyter notebook with full analysis
└── README.md               # Project documentation
```

---

### 📷 UI Preview

| Cluster Summary Table             | Streamlit Input UI        |
| --------------------------------- | ------------------------- |
| ![table](screenshots/summary.png) | ![ui](screenshots/ui.png) |

> *Add screenshots to a `/screenshots/` folder and link them as above.*

---

### 🧠 Learnings

* Practical experience with **unsupervised learning**
* Applied RFM analysis to real-world retail data
* Built and deployed a working data science UI with Streamlit
* Understood customer behavior via visual and statistical profiling

---

### 📌 Future Enhancements

* Add login & session history
* Deploy on cloud (e.g., Streamlit Cloud, Heroku)
* Support CSV file uploads for batch segmentation

---

### 📜 License

This project is under the [MIT License](LICENSE).

---

> **Note**: The dataset files are not uploaded in this repository due to size and licensing restrictions. You can download the dataset manually from the [Kaggle link above](https://www.kaggle.com/datasets/carrie1/ecommerce-data) and place it in the working directory before running the code.
