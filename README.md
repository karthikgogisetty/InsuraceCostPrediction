# 💰 Insurance Cost Prediction Using Machine Learning

This repository focuses on predicting **health insurance charges** using regression-based machine learning models. The project evaluates the effectiveness of **Multiple Linear Regression (MLR)** and **Random Forest Regression (RFR)** both **with** and **without PCA (Principal Component Analysis)** for dimensionality reduction.

---

## 📦 Project Structure

| File                          | Description |
|------------------------------|-------------|
| `code/MLRwithoutPCA.ipynb`      | Implements basic Multiple Linear Regression on preprocessed insurance data. |
| `code/RFRwithoutPCA.ipynb`      | Random Forest Regression without dimensionality reduction, shows the best fit. |
| `code/MLRwithPCA.ipynb`         | Applies PCA before training a linear model to observe dimensionality trade-offs. |
| `code/RFRwithPCA.ipynb`         | Combines PCA with Random Forest to evaluate overfitting vs. performance. |
| `Report.pdf`                 | Detailed project report: methodology, visualizations, metrics, and analysis. |

---

## 📊 Dataset Description

The dataset contains 7 features related to medical insurance costs:

- `age`: Age of the insured person
- `sex`: Gender (encoded)
- `bmi`: Body mass index
- `children`: Number of dependents
- `smoker`: Smoking status (encoded)
- `region`: US region (encoded)
- `charges`: Medical insurance cost (target variable)

---

## ⚙️ ML Concepts Used

### 🔹 Multiple Linear Regression (MLR)
- A statistical method to model the linear relationship between a dependent variable and multiple independent variables.
- Evaluated using MSE, RMSE, and R² score.

### 🔹 Random Forest Regression (RFR)
- An ensemble model combining multiple decision trees.
- Shows higher predictive power, especially on the original dataset (without PCA).

### 🔹 Principal Component Analysis (PCA)
- A technique for dimensionality reduction that retains maximum variance.
- Applied before training models to study effects on performance and overfitting.

---

## 📈 Performance Summary

| Model                 | RMSE (Test) | R² Score (Test) | Notes |
|----------------------|-------------|------------------|-------|
| MLR without PCA      | 0.0161      | 90.87%           | Good fit, simple model |
| RFR without PCA      | 0.0124      | 94.38%           | Best overall performance |
| MLR with PCA         | 0.104       | 70%              | Decent, underperforms due to loss of feature interpretability |
| RFR with PCA         | 0.118       | 64%              | Overfits; not optimal for this dataset |

---

## 🧠 Conclusion

- 📌 Random Forest Regression **without PCA** performed best with ~94% accuracy.
- 📌 PCA reduced dimensionality but also removed valuable features, harming performance.
- 📌 Feature selection and outlier removal were essential for improving model stability.

---

## 🛠 Libraries Used

- `numpy`, `pandas`
- `matplotlib`, `seaborn`
- `sklearn` (for regression, metrics, PCA, and preprocessing)

---

## 📚 References

- [Scikit-learn documentation](https://scikit-learn.org/stable/documentation.html)
- [PCA explained](https://towardsdatascience.com/principal-component-analysis-for-dummies-776d336e35d3)
- Dataset sourced from [Kaggle](https://www.kaggle.com/mirichoi0218/insurance)

---

## 👨‍💻 Contributors

- Karthik Gogisetty  
- Geeta Satya Surya Teja Adina  
- Siddhi Sanjay Shenoy  
- Vaibhavi Mohan Ubhe

---

> /* This project is part of my external colab & coursework, which explores real-world machine learning applications and can be used for **any** insurance prediction tasks. */
