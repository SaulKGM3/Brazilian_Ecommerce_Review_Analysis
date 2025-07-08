## Note:

This project is shared as a demonstration of technical proficiency and as part of an ongoing optimization process. It is understood that this work is not final and that there is usually room for refinement as more time and analysis are invested. The notebook itself includes a **Experimental Playground** section where current ideas are being tested. Future updates are expected.

# Brazilian Ecommerce Review Analysis

This project analyzes real-world data from Brazilian e-commerce transactions, focusing on customer reviews. The main objective is to build an **interpretable model** that explains the key factors behind positive and negative customer feedback, helping guide business decisions and service improvements.

## Data Source

The data comes from **Olist**, a Brazilian online retail platform, and includes anonymized information about customer orders, products, payments, reviews, and logistics.

## Project Overview

- The project offers a **reproducible step by step exploratory data analysis (EDA)**.
- Users may choose to **skip the EDA** and move directly to the **modeling and results** sections.
- Each section is **clearly divided and includes instructions** to ensure smooth execution.

## Key Notes

- The analysis focuses on **explainability over predictive accuracy**.
- The goal is to identify the most impactful variables on customer satisfaction.
- All results are reproducible with the provided datasets and notebook.

## Quick View

For a quick visualization of the relevant code, you can go directly to the `Notebook` folder and open the `Brasil_ECom.ipynb` file using GitHub's online viewer. The dashboard can be seen below this text. No need to download anything.

## Dashboard Overview

The main results are summarized in the following dashboard:

![Dashboard: RF_B_R2 (.49) Olist](Dashboard/RF_B_R2(.49)OlistPNG.png)

## Ongoing/Pending Updates and Corrections

The following improvements are planned for future revisions:
- The most recent findings suggest that failing to meet expectations or successfully exceeding them is the main driver of reviews. This may sound obvious, but the key is to declare A and deliver B, where B > A, but never B < A.
- An error was identified: tree based models were tested without base category columns (only required for linear models). The corrected model shows similar results but is preferred, as including base categories reveals meaningful patterns that enhance business understanding beyond predictive accuracy. **(results not yet updated to reflect this correction)**
- Reevaluate the actual relevance and contribution of the `Days_TA` variable. **UPDATE:** It was found that this variable is relevant, likely because a longer window increases the chance to "surprise" the customer with an early delivery. Since the model is Random Forest, collinearity between `Days_TA` and `Days_Early` is not considered a problem.
- Assess the benefits of transforming `Days_Early` into a binary feature instead of using it as a continuous variable. **UPDATE:** This did not improve the model.
- Explore an alternative analysis focused entirely on **product characteristics**, excluding all delivery-related features.
- Improve the dashboard by adding a page 2 for a more feature-focused analysis.
