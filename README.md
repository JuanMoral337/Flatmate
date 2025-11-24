# Flatmate
# IE Flatmate Finder

**IE Flatmate Finder** is a Python-based console application that helps IE University students find compatible flatmates based on lifestyle preferences, personal habits, and budget.  
It ensures that only IE students can access the system by requiring an official `.ieu2024@student.ie.edu` email.
---
##Overview

The program collects user preferences (cleanliness, noise tolerance, guest frequency, smoking, budget, etc.) through a simple questionnaire.  
It then compares these preferences with a small database of existing users and calculates a **compatibility score** using weighted similarity metrics.

Users can also apply optional filters (gender, budget range, smoking preference) to refine their results.

---

## Main Features

-  **IE Email Verification:** Only IE student emails are accepted.  
-  **Lifestyle Questionnaire:** Collects lifestyle and budget preferences.  
-  **Flexible Budget Matching:** Accepts matches within ±€200.  
-  **Weighted Compatibility Algorithm:** Calculates compatibility using multiple lifestyle factors.  
-  **Optional Filters:** Users can specify gender preference, smoking preference, and budget range.  
-  **Top-K Matching:** Displays the top flatmate matches based on compatibility scores.

---

##  Compatibility Weights

| Factor        | Weight |
|----------------|---------|
| Area           | 0.1 |
| Cleanliness    | 0.3 |
| Noise Tolerance| 0.3 |
| Guests         | 0.2 |
| Smoking Habit  | 0.1 |

Each score is normalized and combined into an overall **compatibility percentage (0–100%)**.

---

## 🗂 Project Structure

