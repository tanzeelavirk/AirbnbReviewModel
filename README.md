# AirbnbReviewModel


Built with:

![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## Table of Contents
- [Overview](#overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [How to Use](#how-to-use)

---


## Overview

AirbnbReviewModel is a comprehensive developer tool designed to predict the overall review score of new Airbnb listings based on related features such as cleanliness, communication, check-in experience, location, and number of reviews. It streamlines the process of defining, solving, and evaluating ML problems, enabling data-driven insights that enhance recommendation systems and user experience.

This project uses **supervised regression models**. Two models were built and compared:

- Linear Regression

- Random Forest

Both models were also compared using **7 predictors vs 2 predictors**.
The best-performing model was **Linear Regression with 7 predictors**:

R² = 0.67

RMSE = 0.30

### Why AirbnbReviewModel?

As Airbnb entrepreneurship grows, this model can:

- Help hosts understand which features (like cleanliness and location) most strongly influence review scores.

- Provide an estimated review score for a listing based on its features, allowing better planning and improvements.

Key features:

- Data Analysis: Identifies which features matter most.

- Model Experimentation: Compares different models to find the best fit.

- System Integration: Can be used in larger applications or dashboards.

- Iterative Development: Designed for easy improvements and retraining.

## Getting Started

### Prerequisites

Prerequisites
- Python 3.x

- Jupyter Notebook

- Required Python libraries (see requirements.txt)

---

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/tanzeelavirk/AirbnbReviewModel
   cd AirbnbReviewModel
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

### How to Use

1. Prepare your input data:
- Label (what is being predicted): 
```bash 
review_scores_value
```
- Input features:
```bash
    'review_scores_rating',
    'review_scores_cleanliness',
    'review_scores_communication',
    'review_scores_checkin',
    'review_scores_location',
    'log_number_of_reviews',
    'log_number_of_reviews_l30d'
```
2. Preprocess your data
   ```bash
   import numpy as np
   df['log_number_of_reviews'] = np.log1p(df['number_of_reviews'])
   df['log_number_of_reviews_l30d'] = np.log1p(df['number_of_reviews_l30d'])
   ```
3. Load the trained model and predict!
