# Customer Segmentation & Reinforcement Learning

An applied machine learning project demonstrating how **Unsupervised Learning** and **Reinforcement Learning** can support business decision-making.

The project covers two practical business use cases:

* **Customer Segmentation using K-Means Clustering**
* **Delivery Route Selection using Reinforcement Learning concepts**

---

## 📌 Project Overview

Businesses generate large amounts of customer and operational data. Machine learning can help identify hidden patterns and support better decisions.

This project demonstrates:

1. How customers can be grouped based on spending and engagement.
2. How clustering can support targeted marketing strategies.
3. How an agent can learn from rewards when selecting between different actions.
4. The difference between exploration and exploitation.

---

## 🎯 Business Problems

### 1. Customer Segmentation

An online retailer wants to understand different customer groups using:

* Monthly Spending
* App Visits

K-Means Clustering is used to divide customers into **three behavioral segments**.

### 2. Delivery Route Optimization

A delivery company has two possible routes:

* Route A
* Route B

Each route receives different rewards based on delivery performance. The project demonstrates how reward information can influence future decisions.

---

## 🧠 Machine Learning Concepts

### Unsupervised Learning

Unsupervised Learning identifies patterns in data without predefined target labels.

In this project, **K-Means Clustering** is used to discover customer groups.

### K-Means Clustering

The model is configured with:

```python
KMeans(n_clusters=3, random_state=42, n_init=10)
```

## The customer identifier is excluded from the clustering features. The model uses **Monthly Spending** and **App Visits**.

## 📊 Customer Segmentation

The practical dataset contains eight sample customers with different spending and app-usage behaviors.

The model identifies three clusters:

| Segment                     | Business Interpretation               | Potential Action             |
| --------------------------- | ------------------------------------- | ---------------------------- |
| High-value / highly engaged | High spending and frequent app visits | Loyalty rewards              |
| Medium-value                | Moderate spending and engagement      | Personalized recommendations |
| Low-engagement              | Lower spending and fewer visits       | Re-engagement campaigns      |

## The cluster numbers themselves are only model-generated labels; business interpretation should be based on the underlying customer behavior.

## 🤖 Reinforcement Learning

The second part introduces the fundamental Reinforcement Learning framework:

**Action → Reward → Learning from Result**

The delivery scenario maps the concepts as follows:

| RL Component | Business Example              |
| ------------ | ----------------------------- |
| Agent        | Delivery decision system      |
| Environment  | Roads and traffic             |
| Action       | Choose Route A or Route B     |
| Reward       | Delivery performance feedback |

### Exploration vs Exploitation

**Exploration** means trying a new or less-used option to gather more information.

**Exploitation** means selecting an option that is already known to perform well.

In the example, Route B has the higher historical average reward and is therefore selected as the best-known route.

---

## 📈 Results

### Customer Segmentation

K-Means successfully groups customers into three behavioral clusters based on:

* Monthly Spending
* App Visits

### Route Selection

The example produces:

```text
Route A Average Reward = 4.8
Route B Average Reward = 8.4
```

Therefore, Route B has the higher observed average reward in this simplified scenario.

---

## 💼 Business Applications

The concepts demonstrated in this project can be extended to real-world applications such as:

* Customer segmentation
* Personalized marketing
* Loyalty programs
* Customer re-engagement
* Recommendation systems
* Delivery route optimization
* Dynamic decision-making
* Operational optimization

---

## 🛠️ Tech Stack

* Python
* Pandas
* Scikit-learn
* Matplotlib
* Google Colab / Jupyter Notebook

---

## 📂 Repository Structure

```text
customer-segmentation-reinforcement-learning/
│
├── README.md
├── requirements.txt
├── LICENSE
│
├── notebooks/
│   └── unsupervised-reinforcement-learning.ipynb
│
├── data/
│   └── customer_data.csv
│
├── outputs/
│   └── customer_segments.png
│
└── src/
    └── README.md
```

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/<your-username>/customer-segmentation-reinforcement-learning.git
cd customer-segmentation-reinforcement-learning
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the notebook

Open:

```text
notebooks/unsupervised-reinforcement-learning.ipynb
```

The notebook can be executed using Jupyter Notebook, JupyterLab, or Google Colab.

---

## 📦 Requirements

Create a `requirements.txt` file containing:

```text
pandas
matplotlib
scikit-learn
```

---

## 🔍 Key Takeaways

* K-Means can identify natural customer segments from behavioral data.
* Customer segmentation can support targeted marketing decisions.
* Reinforcement Learning uses feedback in the form of rewards.
* Exploration helps discover potentially better actions.
* Exploitation uses previously successful actions.
* Machine learning becomes more valuable when model outputs are connected to business decisions.

---

## ⚠️ Project Scope

This is an educational proof-of-concept using a small synthetic dataset and simplified Reinforcement Learning logic.

The clustering example demonstrates the concept rather than a production customer segmentation pipeline, while the route-selection example introduces RL principles without implementing a full RL algorithm or production optimization system.

---

## 👤 Author

**Dushant Wadhwa**

BBA – FinTech
Chitkara University

**Focus Areas:** FinTech • Finance • AI • Machine Learning • Data Analytics

---

## 📜 License

This project is intended for educational and portfolio purposes.
