# 📊 Flipkart Customer Sentiment Analysis – iPhone 15 (128GB)

## ❓ What is the Objective?
The goal is to gauge **customer sentiment** towards the iPhone 15 (128GB) model by analyzing reviews scraped from Flipkart.  
This helps understand **public perception**, improve **customer experience**, and identify **product improvement areas**.

---

## ❓ How was the Data Collected?
- **Tool:** Selenium + BeautifulSoup  
- **Process:** Automated browser navigation to Flipkart’s product page and scraped:
  - Username
  - Rating (1–5 stars)
  - Review Text  
- **Handling:** Implemented pagination to collect **300+ reviews**.

---

## ❓ How was the Data Cleaned & Preprocessed?
- Removed duplicates & missing values  
- Preprocessing steps:
  - Lowercased all text  
  - Removed punctuation, special characters & extra spaces  
  - Tokenized into words  
  - Removed stopwords  
  - Lemmatized to base forms (e.g., *running → run*)  

---

## ❓ How was Sentiment Analyzed?
- **Tool:** TextBlob  
- **Polarity Score:** Ranges -1 (negative) to +1 (positive)  
- **Classification Rule:**
  - Positive → polarity ≥ 0.1  
  - Negative → polarity < 0.1  

Each review was labeled as **Positive** or **Negative**.

---

## ❓ What Analysis & Visualizations were Performed?
1. **Sentiment Distribution:** % of positive vs negative reviews  
2. **Ratings vs Sentiment:** Checked if higher ratings align with positive sentiment  
3. **Word Clouds:**  
   - Positive reviews → highlighted terms like *camera, display, performance*  
   - Negative reviews → highlighted terms like *battery, heating, price*  
4. **Review Length Analysis:** Longer reviews often expressed **detailed sentiment** (strong positive or negative).  

---

## ❓ What Insights were Found?
- ✅ Majority reviews were **positive**, praising **camera quality, smooth performance, and display**.  
- ❌ Negative reviews mentioned **battery drain & heating issues**.  
- ⭐ Ratings correlated strongly with sentiment (5★ = positive, 1–2★ = negative), but some 3★ reviews expressed negative experiences.  

---

## ❓ What Recommendations were Made?
- **For Apple:** Improve **battery optimization** and address **overheating issues**.  
- **For Flipkart:** Highlight **camera & display strengths** in product marketing.  

---

## 🛠️ Tools & Libraries
- **Selenium** – Web scraping automation  
- **BeautifulSoup** – HTML parsing  
- **Pandas** – Data cleaning & preprocessing  
- **TextBlob** – Sentiment analysis  
- **Matplotlib / Seaborn** – Visualization  
- **WordCloud** – Word frequency insights  

---


# Generate visualizations
python src/visualization.py
