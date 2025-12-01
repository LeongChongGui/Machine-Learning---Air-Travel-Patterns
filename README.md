# Airline Passenger Satisfaction Analysis: Pre- vs Post-COVID-19

## 📌 Project Overview
This project uses machine learning techniques to analyze shifts in airline passenger satisfaction and sentiment before and after the COVID-19 pandemic. By examining customer reviews and ratings, we identify key factors that changed during this period and provide data-driven insights to help airlines improve service delivery and resource allocation during future crises.

## 🎯 Problem Statement
The aviation industry faced significant disruptions during the COVID-19 pandemic, leading to changes in passenger expectations and satisfaction levels. This project aims to:
- Compare pre- and post-COVID passenger satisfaction
- Identify the factors most affected by the pandemic
- Analyze changes in customer sentiment
- Provide actionable insights for airlines to enhance services and decision-making

## 📚 Background
Before the pandemic, travellers prioritized price, convenience, and service quality. Post-pandemic, there has been a notable shift toward valuing health safety measures, sanitation, and visible cleaning protocols. Understanding these changes is crucial for airlines to remain competitive and meet evolving customer expectations.

## 🚀 Motivation
Airlines need to understand how passenger preferences have shifted due to the pandemic to:
- Design targeted strategies that meet emergent customer needs
- Enhance customer satisfaction and loyalty
- Support sustainable business growth in a transformed industry landscape

## 📊 Dataset Overview
We used a dataset containing airline passenger reviews with the following attributes:

### Qualitative Data:
- **Airline Name**, **Review Title**, **Review**, **Aircraft**, **Type of Traveller**, **Seat Type**, **Route**, **Date Flown**

### Quantitative Data:
- **Overall Rating** (1-10)
- **Service Ratings** (1-5): Seat Comfort, Cabin Staff Service, Food & Beverages, Ground Service, Inflight Entertainment, Wi-Fi & Connectivity, Value for Money
- **Recommended** (Yes/No)

## ⚙️ Methodology

### 1. Data Preprocessing
- **Feature Selection**: Removed irrelevant features (Serial Number, Review Date, etc.)
- **Time Segmentation**: Partitioned data into pre- (before March 1, 2020) and post-COVID periods
- **Missing Value Imputation**: Used median imputation for rating attributes
- **Data Balancing**: Applied Generative Adversarial Network (GAN) to address class imbalance between periods

### 2. Machine Learning Models Applied
- **Artificial Neural Network (ANN)**: For predicting recommendation likelihood
- **K-Medians Clustering**: To identify passenger segments based on ratings and features
- **Gaussian Mixture Model (GMM)**: For probabilistic clustering of passenger groups
- **Logistic Regression**: To determine feature importance in recommendations
- **Support Vector Machine (SVM)**: With RBF kernel for classification
- **Large Language Models (BERT)**: For sentiment and aspect-based sentiment analysis of reviews

### 3. Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrices, ROC-AUC curves
- Sentiment distributions and aspect-based analysis

## 📈 Key Findings

### Model Performance Insights:
- **ANN**: Showed significant improvement in post-COVID prediction accuracy (96.88% vs 75.72% pre-COVID)
- **Logistic Regression**: Pre-COVID model performed slightly better in precision, recall, and F1-score
- **SVM**: Maintained high accuracy in both periods (97.2% pre-COVID, 97.16% post-COVID)
- **BERT Embeddings with SVM**: Most effective for sentiment-based recommendation prediction

### Passenger Sentiment Shifts:
- **Overall Satisfaction**: Decline in average ratings across most service attributes post-COVID
- **Key Declining Areas**: Seat Comfort, Cabin Staff Service, Food & Beverages, Ground Service
- **Value Perception**: Increased negative sentiment toward "Value for Money" post-COVID
- **Sentiment Polarization**: More pronounced negative sentiment in specific aspects post-pandemic

### Clustering Results:
- **Pre-COVID**: Three distinct segments (High, Mixed, Low ratings)
- **Post-COVID**: More defined clusters with disappearance of "Mixed Ratings" group
- **Economy Focus**: Majority of travelers in both periods were economy class

## 💡 Recommendations for Airlines

1. **Prioritize Service Quality Improvements**:
   - Focus on Cabin Staff Service and Ground Service for immediate impact
   - Address Wi-Fi & Connectivity and Value for Money perceptions
   - Consider long-term improvements to Seat Comfort and Food & Beverages

2. **Leverage Customer Feedback Continuously**:
   - Implement sentiment analysis tools for real-time monitoring
   - Address recurring pain points identified in reviews
   - Demonstrate responsiveness to build customer trust

3. **Investigate Hidden Factors**:
   - Conduct surveys to uncover less obvious satisfaction drivers
   - Explore factors like booking experience, baggage handling, and personalization

## ⚠️ Limitations

### GAN Model Constraints:
- Generated data showed more continuous distributions than the original discrete ratings
- Difficulty capturing exact variance and discrete nature of original data
- Recommendations for improvement: specialized activation layers, larger batch sizes, correlation-aware loss terms

### General Limitations:
- Dataset skewed toward certain regions and time periods
- Limited demographic information
- Class imbalance between pre- and post-COVID periods

## 🛠️ Technical Implementation

### Requirements
- Python 3.8+
- Libraries: scikit-learn, TensorFlow/Keras, PyTorch, Transformers, spaCy, pandas, numpy, matplotlib, seaborn

## 🔮 Future Work
- Extend analysis to include more diverse geographic regions
- Incorporate demographic data for better passenger segmentation
- Enhance GAN architecture for more realistic synthetic data generation
- Explore real-time sentiment monitoring systems
- Investigate the impact of airline-specific policies on satisfaction

---

*This project provides actionable insights for airlines to adapt to changing passenger expectations and improve service delivery in the post-pandemic travel landscape.*
