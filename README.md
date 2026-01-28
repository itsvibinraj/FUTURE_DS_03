# FUTURE_DS_03
# 🎓 College Event Feedback Analysis (NLP)

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![TextBlob](https://img.shields.io/badge/TextBlob-NLP-green?style=for-the-badge)

## 📌 Project Overview
This project was developed as **Task 3** for the **Future Interns Data Science Internship**. 

The goal was to analyze student feedback from various campus events (Tech Fests, Hackathons, Workshops) to understand satisfaction levels and identify key areas for improvement. I utilized **Natural Language Processing (NLP)** to classify student comments as Positive, Negative, or Neutral.

## 🚀 Key Features
* **Synthetic Data Generation:** Created a realistic dataset of 1,000+ student reviews including Event Names, Departments, Ratings, and Text Comments.
* **Hybrid Sentiment Analysis:** * Implemented a **Rule-Based Filter** to correct common NLP errors (e.g., detecting "Hot" and "Crowded" as negative in the context of events, whereas standard libraries often view them as positive).
    * Used **TextBlob** for polarity scoring.
    * Implemented a "Buffer Zone" to accurately capture **Neutral** sentiment.
* **Data Visualization:** Generated insightful charts using Matplotlib and Seaborn.

## 📊 Methodology
### 1. Data Cleaning & Preparation
* Generated synthetic data to simulate real-world scenarios.
* Handled categorical data (Departments, Event Names).

### 2. The NLP Challenge (Problem Solving)
Standard NLP libraries often misclassify context-specific words.
* *Issue:* TextBlob classified **"The room was too crowded and hot"** as **Positive** (Score: +0.25).
* *Solution:* I wrote a custom function to pre-scan for "Event Killer" keywords (`crowded`, `late`, `hot`, `wifi`) and force a **Negative** classification before calculating the polarity score.

### 3. Visual Insights
* **Bar Charts:** Compared average ratings across different events.
* **Pie Chart:** Visualized the overall sentiment distribution (Positive vs. Negative vs. Neutral).
* **Word Cloud:** Isolated **Negative** comments to visualize the most frequent complaints (Pain Points).

## 📈 Key Findings
* **Top Event:** The *Tech Fest* received the highest engagement and positive sentiment.
* **Major Pain Point:** The *Hackathon* received low ratings due to specific logistic failures.
* **Recurring Complaints:** The words "Wifi", "Late", and "Crowded" appeared most frequently in negative reviews.

## 🛠️ Technologies Used
* **Python** (Core Logic)
* **Pandas** (Data Manipulation)
* **TextBlob** (Sentiment Analysis)
* **Matplotlib / Seaborn** (Graphing)
* **WordCloud** (Text Visualization)
* **Google Colab** (Development Environment)

## 💻 How to Run
1.  Open the `Task_3.ipynb` file in **Google Colab** or Jupyter Notebook.
2.  Run the first cell to generate the dataset (no external CSV download required).
3.  Run the subsequent cells to perform the analysis and generate the report.

## 📢 Conclusion & Recommendations
Based on the data, the following recommendations were generated for the event committee:
1.  **Infrastructure:** Conduct mandatory WiFi speed tests 24 hours before technical events.
2.  **Logistics:** Larger venues are required for the "Cultural Night" to avoid overcrowding.
3.  **Scheduling:** Enforce strict start times to reduce "Late" complaints.

---
*Created by Vibin Raj*
