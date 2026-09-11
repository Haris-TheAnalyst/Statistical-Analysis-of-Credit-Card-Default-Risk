# Credit Card Default Analysis

## What is this project?

This project looks at credit card customers and tries to answer one question:

**Which factors (like age, education, credit limit, or payment history) make a customer more likely to default on their credit card payment?**

---

## Why did we do this?

We wanted to practice real data analysis using a real-world problem. Credit card default is a common topic in finance, and this dataset let us apply what we know — data cleaning, statistics, and building a model — on actual numbers instead of made-up examples.

Simply put: we picked a real question (why do people default on payments?) and used data and statistics to actually answer it, step by step.

---

## About the Data

- The dataset contains information on **30,000 credit card clients**.
- It includes:
  - **Demographic info** – age, sex, education, marital status
  - **Financial info** – credit limit, bill amounts
  - **Repayment history** – whether the customer paid on time in past months, and how much they paid
  - **Target column** – whether the customer defaulted (did not pay) the next month or not

---

## What We Did (Step by Step)

### Step 1: Cleaned the Data
- Loaded the raw data into R
- Fixed messy category labels (example: turned number codes like `1`, `2`, `3` into readable labels like "Male", "Female", "Married", "Single")
- Grouped unclear/unknown categories into an "Others" group

### Step 2: Explored the Data (EDA)
- Checked how many customers defaulted vs. did not default
- Made simple charts to see patterns, such as:
  - Do people with lower credit limits default more?
  - Does education level affect default rate?
  - Does marital status affect default rate?

### Step 3: Tested Our Ideas (Hypothesis Testing)
- Used statistical tests (Chi-square tests and T-tests) to check if these differences were **real** or just due to chance
- Tested things like:
  - Does sex/education/marriage actually relate to default?
  - Is there a real difference in average age, credit limit, or payment amount between people who default and people who don't?

### Step 4: Built a Prediction Model (Logistic Regression)
- Combined all the factors together into one statistical model
- This model tells us **which factors actually matter** once we look at everything together, not just one at a time
- Calculated "odds ratios" — simple numbers that show how much each factor increases or decreases the chance of default

### Step 5: Found the Key Answers
- **Repayment history** (whether someone paid late before) was the strongest sign of future default
- **Credit limit** also mattered — lower limits were linked to higher default risk
- **Demographic factors** (age, education, marriage) had some effect, but a much smaller one

### Step 6: Wrote the Report
- Put everything together into a clear report with charts, tables, and a plain explanation of the results

---

## Tools Used
- **R** – for cleaning data, running statistics, and building the model
- **ggplot2** – for making charts
- **Logistic Regression** – the main statistical technique used for prediction

---

## Final Takeaway

Out of everything we checked, **how someone paid their bills in the past** was by far the best clue about whether they would default in the future — much more important than their age, education, or marital status.
