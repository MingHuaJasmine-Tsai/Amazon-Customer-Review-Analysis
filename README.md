# Amazon Customer Review Analysis

### Data
Amazon Reviews 2023

### License
MIT License

### Dataset Access
https://amazon-reviews-2023.github.io/

---

## 1. Executive Summary
This project investigates the key drivers of customer satisfaction and product performance on Amazon by linking large-scale customer review data with product metadata. Using PySpark on Google Cloud, we cleaned, standardized, and prepared two large datasets — user reviews and product metadata — enabling efficient exploratory analysis and machine learning modeling.

Our analyses explore how elements such as **price**, **category**, **product content**, and **review text** impact customer ratings. We also evaluate **price fairness**, **product lifecycle behavior**, and **root causes of negative reviews**. A seller-focused pricing model helps determine whether products are overpriced, underpriced, or competitively aligned.

These findings support data-driven improvements in **pricing strategy**, **content optimization**, and **customer satisfaction management**.

---

## 2. Key Business Questions

### Product Category Performance
- Which categories perform best when adjusted for popularity and reliability?

### Price–Rating Relationship
- Does price influence customer ratings?  
- Are premium products consistently rated higher?

### Content Quality Impact
- Does richer content (images, videos, descriptions) improve ratings?

### Helpful Votes as Warning Signals
- Do high helpful-vote counts on negative reviews correlate with lower product ratings?

### Pricing Optimization
- Are low-rated listings priced appropriately?  
- Is a product overpriced or underpriced within its category?  
- Which categories contribute to unfair pricing patterns?

### Product & Category Lifecycle
- How do product ratings evolve from launch to maturity?  
- What lifecycle patterns exist across major categories?

### Review Text Behavior
- Are longer reviews more emotional (1-star or 5-star)?

---

## 4. Data Source
This project uses the **Amazon Reviews 2023 Dataset** from:  
Julian McAuley Lab – UC San Diego  
https://cseweb.ucsd.edu/~jmcauley/datasets.html

### Datasets Used
| Dataset | Description |
|--------|-------------|
| **User Reviews** | Rating, text, timestamps, helpful votes, verified purchase, user_id |
| **Item Metadata** | Title, description, price, category, images, videos, features |

Datasets are linked using **parent_asin**, the unique product identifier.

---

## 5. Sample Product Categories
Examples include:

- Cell Phones & Accessories  
- Arts, Crafts & Sewing  
- Grocery & Gourmet Food  
- Automotive  
- Baby Products  
- Office Products  
- Musical Instruments  
- All Beauty  
- Health & Personal Care  

---

## 6. Data Cleaning Pipeline
Raw `.gz` files were transformed into **Parquet** and processed into analytics-ready **Silver** datasets.

### Key Steps
- Normalize nested structures  
- Remove nulls and duplicates  
- Standardize schemas  
- Enhance metadata fields  

### Mini-Conclusion
Cleaning reduced dataset size by **35–40%**, enabling efficient joins and downstream analysis.

---

## 7. Exploratory Data Analysis (EDA)
Key EDA focus areas include:

### Category-Level Performance
### Price–Rating Dynamics
### Product Content Quality
### Helpful Votes on Negative Reviews
### Price Fairness & Outliers
### Lifecycle Analysis

---

## 8. Prediction Models

### Model 1 — Average Rating Prediction
**Features Used**
- Main category  
- Description word count  
- Price  
- Presence of images/videos  

**Most influential factor:** Product video availability

---

### Model 2 — Negative Review NLP Analysis
Topic modeling was used to identify root causes of dissatisfaction.

**Grouped Topics**
- Tech & functionality  
- Durability & quality  
- Assembly & installation  
- Shipping & misleading listings  
- Category-specific issues  
- Fitment & sizing  

---

## 9. Why This Matters
These insights help sellers:

- Optimize pricing strategy  
- Improve product listing content  
- Enhance customer satisfaction  
- Reduce return rates  
- Increase repeat purchases  
- Detect quality issues early (via helpful votes)

---

## ⚠️ Limitations
- Ratings may reflect personal preferences  
- Brand reputation not modeled  
- Content quality inferred from metadata (not actual visuals)  
- Only 10 out of 34 categories included  

---

## 🤝 Contributors
- **@Kapilan199** –
- **@marins0330** –
- **@ymk1003** –


---

## 🧠 Generative AI Disclosure
AI tools (e.g., ChatGPT) were used for:

- Code cleaning & debugging  
- Research assistance  
- Performance optimization  
- Visualization styling  
- NLP topic grouping  

All AI-generated outputs were manually reviewed for accuracy and integrity.

---

## 📚 References
- *Should a Direct-to-Consumer Company Start Selling on Amazon?* – Harvard Business Review  
- Amazon Reviews 2023 Dataset — https://amazon-reviews-2023.github.io/  
- UCSD Item Metadata Dataset — https://
