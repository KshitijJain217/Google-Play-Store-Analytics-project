# Google Play Store Analytics & Internship Deliverables

**Author:** Kshitij Jain

## 📌 Project Overview
This repository contains a comprehensive, end-to-end Data Science and Machine Learning pipeline built to analyze the Google Play Store dataset. The core objective of this project is to understand the technical factors that drive application ratings, perform Natural Language Processing (NLP) on user reviews, and build a predictive algorithm using Random Forest Regression.

## 🚀 Key Achievements & Technical Pipeline
- **Advanced Data Cleaning:** Handled right-skewed data distributions via logarithmic scaling (`np.log1p`), standardized messy alphanumeric size data into unified Megabyte (MB) floats, and enforced strict data deduplication.
- **NLP Sentiment Analysis:** Engineered feature extraction on over 64,000 raw text reviews using NLTK's **VADER** (Valence Aware Dictionary and sEntiment Reasoner) to synthesize `Sentiment_Polarity` and subjectivity scores.
- **Predictive Modeling:** Deployed a Scikit-Learn `RandomForestRegressor` to predict app ratings based on purely technical heuristics (Size, Pricing, Engagement, and aggregate User Sentiment).
- **Interactive Dashboards:** Programmatically generated standard standalone HTML Plotly dashboards summarizing distributions across market sectors.

---

## 🏆 Internship Tasks Completion
In addition to the core pipeline, the following six complex, highly-filtered visualization tasks were successfully executed as part of the internship requirements.

*(Note: In the notebook, these visualizations operate under strict time-gated execution restrictions based on IST hours.)*

### 1. Top Category Engagement (Grouped Bar Chart)
Compared the average rating and total review count for the top 10 app categories by installs. 
* **Filters Applied:** Average rating >= 4.0, Size < 10 MB, updated in January.
* **Time Gate:** Displayed *only* between 3:00 PM – 5:00 PM IST.

![Internship Task 1 Output](Outputs/Internship%20Task%201)

### 2. Global Installs Distribution (Choropleth Treemap)
Visualized global installs by Category.
* **Filters Applied:** Filtered to the top 5 categories globally. Explicitly excluded categories starting with "A", "C", "G", or "S". Highlighted categories exceeding 1 Million installs.
* **Time Gate:** Displayed *only* between 6:00 PM – 8:00 PM IST.

![Internship Task 2 Output](Outputs/Internship%20Task%202)

### 3. Monetization Strategy: Free vs. Paid (Dual-Axis Chart)
Compared average installs against total accumulated revenue for Free vs. Paid applications across the top 3 categories.
* **Filters Applied:** Installs >= 10,000, Revenue >= $10,000, Android Version > 4.0, Size > 15 MB, Content Rating exactly "Everyone", and App Name length <= 30 characters.
* **Time Gate:** Displayed *only* between 1:00 PM – 2:00 PM IST.

![Internship Task 3 Output](Outputs/Internship%20Task%203)

### 4. Category Growth Trending (Time Series)
Visualized the trend of total installs over time, segmented by app category, highlighting months with >20% Month-over-Month growth.
* **Filters Applied:** App names cannot start with "x", "y", or "z" nor contain the letter "s". Categories restricted to those starting with "E", "C", or "B". Reviews > 500. 
* **Localization:** Translated "Beauty" to Hindi, "Business" to Tamil, and "Dating" to German in the chart legend.
* **Time Gate:** Displayed *only* between 6:00 PM – 9:00 PM IST.

![Internship Task 4 Output](Outputs/Internship%20Task%204)

### 5. Application Viability (Bubble Chart)
Analyzed the relationship between app size and average rating, weighting the bubble size by total installs.
* **Filters Applied:** Rating > 3.5, Installs > 50k, Reviews > 500, App name must not contain "s", and NLP Sentiment Subjectivity > 0.5. Categories strictly limited to: Game, Beauty, Business, Comics, Communication, Dating, Entertainment, Social, and Events.
* **Aesthetics:** Game category dynamically highlighted in Pink. "Beauty", "Business", and "Dating" dynamically translated.
* **Time Gate:** Displayed *only* between 5:00 PM – 7:00 PM IST.

![Internship Task 5 Output](Outputs/Internship%20Task%205)

### 6. Cumulative Trajectory (Stacked Area Chart)
Visualized the cumulative number of installs over time.
* **Filters Applied:** Rating >= 4.2, no numbers allowed in the App Name, category must start with "T" or "P", reviews > 1,000, and size bounded between 20 MB and 80 MB.
* **Localization:** Translated "Travel & Local" to French, "Productivity" to Spanish, and "Photography" to Japanese. Months with >25% MoM growth highlighted.
* **Time Gate:** Displayed *only* between 4:00 PM – 6:00 PM IST.

![Internship Task 6 Output](Outputs/Internship%20Task%206)

---

## 🛠 Setup & Usage
1. Clone the repository and ensure `Play Store Data.csv` and `User Reviews.csv` are in the root directory.
2. Install requirements: `pip install pandas numpy scikit-learn plotly nltk`.
3. Run `jupyter notebook play_store_analytics.ipynb`.

