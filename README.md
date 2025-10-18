# Amazon_ML_Challenge_2025

Our team "Optimizers" attempt to solve amazon ml problem 2025 in this repo 

![Web_Photo_Editor](https://github.com/user-attachments/assets/d046d6da-0ea1-41f2-8761-4dbeea515fab)


# 🧠 ML Challenge 2025 – Smart Product Pricing Challenge

## 📋 Problem Statement
In e-commerce, determining the **optimal price point** for products is crucial for both marketplace success and customer satisfaction.  

Your challenge is to **develop an ML solution** that analyzes product details and predicts the **price of a product**. The relationship between product attributes and pricing is complex — factors like **brand**, **specifications**, and **quantity** directly influence pricing.  

Your task is to build a model that can **holistically analyze product details** and **suggest an optimal price**.

---

## 🗂️ Data Description

The dataset consists of the following columns:

| Column | Description |
|---------|--------------|
| `sample_id` | A unique identifier for each product sample |
| `catalog_content` | Text field containing product title, description, and Item Pack Quantity (IPQ) concatenated together |
| `image_link` | Public URL of the product image. Example: [https://m.media-amazon.com/images/I/71XfHPR36-L.jpg](https://m.media-amazon.com/images/I/71XfHPR36-L.jpg) |
| `price` | Target variable — the product price (available only in training data) |

### Dataset Details
- **Training Dataset:** 75,000 products with complete details and prices  
- **Test Dataset:** 75,000 products (without prices, for evaluation)

---

## 🧾 Output Format
The output must be a **CSV file** with exactly two columns:

| sample_id | price |
|------------|--------|
| 12345 | 249.99 |
| 67890 | 109.00 |

**Notes:**
- The `sample_id` values **must exactly match** the ones in the test set.  
- The file should have the **same number of rows** as the test data.  
- Predicted prices must be **positive float values**.

---

## 🧱 File Descriptions

### 📁 Source Files
- **`src/utils.py`** — Helper functions for downloading product images from URLs. You may need to retry downloads due to throttling.  
- **`sample_code.py`** — Example script that demonstrates how to format and generate a valid output file. (Optional usage)

### 📊 Dataset Files
- **`dataset/train.csv`** — Training data with `price` labels.  
- **`dataset/test.csv`** — Test data without `price` labels.  
- **`dataset/sample_test.csv`** — Sample input file for testing.  
- **`dataset/sample_test_out.csv`** — Example of correctly formatted output (note: predictions are placeholders).

---

## ⚙️ Constraints
- The **output format** must match the `sample_test_out.csv` file exactly.  
- Predicted prices must be **positive floats**.  
- Final model must be under **8 billion parameters**.  
- The model must be under an **MIT or Apache 2.0 license**.

---

## 🧮 Evaluation Criteria
Submissions are evaluated using **Symmetric Mean Absolute Percentage Error (SMAPE)**.

\[
\text{SMAPE} = \frac{1}{n} \sum \frac{|P_{pred} - P_{actual}|}{(|P_{pred}| + |P_{actual}|)/2}
\]

**Example:**
If `actual price = 100` and `predicted price = 120`  
\[
\text{SMAPE} = \frac{|100 - 120|}{(100 + 120)/2} \times 100 = 18.18\%
\]

- SMAPE is **bounded between 0% and 200%**  
- **Lower values indicate better performance**

### 🏆 Leaderboard Details
- **Public Leaderboard:** Based on 25K samples from the test set for real-time feedback.  
- **Final Rankings:** Based on the full 75K test set and documentation quality.

---

## 📝 Submission Requirements

### 1️⃣ Output File
Submit a file named **`test_out.csv`** with the format described above.

### 2️⃣ Documentation
Submit a **1-page report** describing:
- Methodology used  
- Model architecture or algorithms selected  
- Feature engineering techniques  
- Any additional implementation details  

A template (`Documentation_template.md`) is provided.

---

## ⚠️ Academic Integrity & Fair Play

**STRICTLY PROHIBITED:**  
Using any **external price lookup** methods such as:
- Web scraping product prices  
- Using APIs to fetch market prices  
- Manual lookup from websites  
- Using any external pricing datasets  

**Violations will result in immediate disqualification.**

This challenge is meant to test your **data science and ML problem-solving skills** using **only the provided data**.

---

## 💡 Tips for Success
- Use both **textual (`catalog_content`)** and **visual (`image_link`)** features.  
- Explore **feature engineering** for both text and images.  
- Consider **ensemble methods** combining multiple models.  
- Handle **outliers** carefully and preprocess the data well.  
- Ensure predictions are **realistic and positive**.

---

## ✅ Summary
You are building an ML model that predicts the **price of e-commerce products** using **text and image data**.  
Your final deliverables are:
1. **`test_out.csv`** — Predicted prices  
2. **1-page report** — Description of your method  

The goal is to achieve the **lowest SMAPE score** while adhering to fair play and good ML practices.

---
