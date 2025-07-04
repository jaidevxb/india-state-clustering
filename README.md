# Clustering Indian States Based on Socioeconomic Indicators

### 👨‍🔬 Objective
We cluster the 28 Indian states into 3 meaningful groups using key socioeconomic indicators:
- 📚 Literacy Rate (%)
- 💰 Per Capita Income (₹)
- 👥 Population Density (people/km²)
- 📉 Unemployment Rate (per 1000 people)

---

### ⚙️ Methodology
- ## 📄 Data Sources
- **Literacy Rate (%)**: Taken from the **2011 Census of India**
- **Per Capita Income (₹)**: Sourced from **2023–24 NSDP** values on [Wikipedia](https://en.wikipedia.org/wiki/List_of_Indian_states_and_union_territories_by_GDP_per_capita)
- **Population Density (people/km²)**: From the **2011 Census of India**
- **Unemployment Rate (per 1000)**: Averaged from **RBI 2022–23 statistics** (combined rural + urban rates)

> **Note**: Since **Telangana** was formed in 2014, its **literacy rate and population density** are taken from **undivided Andhra Pradesh** as per 2011 data.

- **🔧 Preprocessing**:
- Cleaned and formatted the data manually in Excel before loading into the notebook
- Normalized all numeric columns using `StandardScaler`
  
- **📌 Clustering**: Applied **K-Means Clustering** (`k=3`) using `scikit-learn`
  
- **📊 Visualization**:
  - Reduced 4D data to 2D using **PCA**
  - Plotted clusters using `matplotlib` and `seaborn`
  - Labeled each state on the scatter plot

---

### 📊 Cluster Interpretations

Based on the cluster-wise averages of literacy rate, income, density, and unemployment:

#### 🟢 Cluster 0 – Richer & Literate States
- **Traits**: Highest literacy and income, moderate density, moderate unemployment
- **Examples**: Kerala, Tamil Nadu, Goa, Maharashtra, Karnataka

#### 🟠 Cluster 1 – Densely Populated, Lower Literacy & Income
- **Traits**: Lowest literacy and income, highest population density, better unemployment
- **Examples**: Bihar, Uttar Pradesh, Jharkhand, Madhya Pradesh

#### 🔵 Cluster 2 – Possibly Northeastern or Smaller States
- **Traits**: Mid literacy and income, lowest density, highest unemployment
- **Examples**: Nagaland, Mizoram, Meghalaya, Sikkim

> Even though clusters overlap visually in PCA space, they show clear separation in statistical summary.

---

### 📈 Outcome: Why This Matters

This clustering provides a **data-driven perspective** of regional development and can be used for:
- 🧩 **Policy design & targeting** (education, job creation, etc.)
- 📊 **Resource allocation** by identifying similar state clusters
- 💼 **Business insights** for targeting regions by development tier
- 🎓 **Further ML modeling** (classification, prediction, etc.)
- 📚 **Academic research** on economic disparity and development patterns

---

### 📁 Files Included
- `indian_states_data.csv` — Cleaned dataset with all 28 states
- `indian_states_clustering.ipynb` — Jupyter notebook with code, plots, and analysis
- `README.md` — Project summary (this file)

---

### 🔭 Next Steps
- 🔄 Update the clustering when newer Census or NSDP data becomes available
- 🏥 Include more features like **health index, female literacy, infrastructure**
- 🧠 Try **other clustering algorithms** (e.g., DBSCAN, Hierarchical) for comparison
- 🌍 Build an **interactive map** using Plotly or Folium

---

### 🙌 Author
**Jaidev B**  
Connect on [LinkedIn](https://www.linkedin.com/in/jaidevb) | Reach out via GitHub Issues for questions

---

## 🤖 GenAI Prompt Log

This project was built using Python, Jupyter Notebook and guidance from ChatGPT to complete the analysis within few hours. Below is a transparent log of how GenAI was used to assist in accelerating this project.

### 🗂️ 1. Project Setup & Data Check
> I manually collected data from Census, RBI and Wikipedia. Can you verify if these features (literacy, per capita income, population density, unemployment) are valid for clustering Indian states?

✅ Used to confirm that feature choices were appropriate.

### 🔧 2. KMeans Clustering Code
> I want to use KMeans to group Indian states into 3 clusters based on the given data. Help me write a clean Jupyter Notebook with normalization, PCA visualization, and cluster labeling.

✅ Used to generate baseline clustering pipeline and visualization code.

### ⚙️ 3. Normalization Clarification
> Do I need to normalize the data before clustering? What happens after using StandardScaler?

✅ Helped understand the necessity of normalization and how it affects clustering accuracy.

### 📉 4. PCA & Cluster Overlap Doubt
> My PCA plot shows overlapping clusters — is that normal in KMeans?

✅ Helped interpret PCA visualization and confirmed overlap is normal in 2D projections.

### 📄 5. README Formatting
> I wrote the README contents in English — just needed help making it look clean and structured in markdown.

✅ Used to polish documentation professionally for public showcasing.

### 🧽 6. Minor Clarifications
- Whether to remove commas manually or in code ✅  
- Whether it's okay to use mixed-year data (2011–2024) ✅  
- Whether to show normalized data ranges ✅  
- Whether project is complete and showcase-ready ✅  

---


