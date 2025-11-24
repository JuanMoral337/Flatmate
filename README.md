#IE Flatmate Finder (Lovable + Python App)

Find your perfect flatmate match at IE University
Live App https://flatmate-ie-match.lovable.app(https://flatmate-ie-match.lovable.app)

---

#Overview

IE Flatmate Finder is a student matching tool developed for IE University. It helps students find compatible flatmates safely and efficiently by combining verified access (IE email authentication) with a personality-based matching algorithm.

The project exists in **two integrated versions**:
1. **Python prototype** — a console program built during the Algorithms & Data Structures course.  
2. **Lovable web app** — a no-code implementation with a full graphical interface.

Both versions share the same **matching logic**: lifestyle compatibility, hard constraints on budget and area, and verified IE student access.



#Technical Overview

| Component | Python Prototype | Lovable Web App |
|---------|-----------------|----------------|
| Platform* | Python 3.9+ (local execution) | Lovable (no-code builder) |
| Frontend | Console-based Q&A | Auto-generated React + Tailwind |
| Algorithm | Weighted similarity & Top-K matching | JavaScript logic blocks in Lovable |
| Database | CSV / in-memory list | Lovable internal table (`Students`) |
| Verification | Regex for `@student.ie.edu` | Input validation via Lovable Form Block |
| Hosting | Local execution | Lovable Cloud |
| Versioning | Manual | Lovable built-in project versions |

#Algorithm Summary

Both apps use the same **weighted compatibility algorithm**, validated during your course’s Section III.

#Matching Logic

1. Hard Constraints 
   - Must have the same preferred area.  
   - Budget difference ≤ ±150€.  
   - Matching smoking preference (if specified).

2. Weighted Similarity (Soft Constraints)
   Each lifestyle factor contributes to the compatibility score:

| Attribute | Weight | Type | Description |
|------------|---------|------|-------------|
| Cleanliness | 3.0 | Likert | Similarity between 1–5 values |
| Noise Tolerance | 2.5 | Likert | Inverse of absolute difference |
| Guest Frequency | 2.0 | Likert | Frequency alignment |
| Smoking | 3.0 | Boolean | Exact match required |
| Budget | — | Hard constraint | ±150€ accepted |
| Area | — | Hard constraint | Must match exactly |

Displayed as a percentage (0–100 %).

---

#Core Features

#1. IE Email Verification
- Restricted to emails ending with `@student.ie.edu`.  
- Prevents access from non-IE accounts.  
- Provides visual validation feedback (Lovable) or regex check (Python).

#2. Step-by-Step Onboarding Flow (Lovable)
- Step 1: Basic Info — Name, Gender, Preferred Area in Madrid.  
- Step 2: Lifestyle — Sliders for Cleanliness, Noise, Guests.  
- Step 3: Preferences — Smoking & Monthly Budget.

#3. Real-Time Matching
- Lovable logic blocks compute weighted scores instantly.  
- Results page shows Top 3–5 matches with:
  - Name, gender, area, budget, lifestyle traits.  
  - Compatibility percentage (e.g., “74 % Good Match”).  
- Optional filters: gender, smoking, budget range.

#4. Optional Filters (Python Version)
Users can refine results by:
- Gender preference  
- Smoking habit  
- Budget range  

---

#Project Structure

#Python Edition
- `algorithm.py` – core matching logic  
- `main.py` – questionnaire + console UI  
- `students.csv` – demo dataset  

#Lovable Edition
- Form blocks for questionnaire steps  
- Logic blocks for weighting and filtering  
- Repeater lists for displaying ranked matches  
- Email validation workflow for domain enforcement  

---

#UX / Usability Testing

Three remote usability sessions were conducted to fulfill the course’s Section III UX requirement.

#Test Goals
- Confirm that new users can complete the form without guidance.  
- Assess understanding of “Good Match” scores.  
- Measure trust and clarity of the IE verification step.

#Key Findings
- Email restriction improved perceived security.  
- Sliders made lifestyle input intuitive.  
- Users wanted clarity on match percentages.

#Implemented Improvements
- Added visual email feedback.  
- Added filter panel for gender and budget.  
- Improved readability and color contrast on cards.

---

#Installation & Access

#Lovable Web App
1. Visit: [https://flatmate-ie-match.lovable.app](https://flatmate-ie-match.lovable.app)  
2. Enter your name and IE student email.  
3. Complete the 3-step quiz.  
4. View your Top Matches instantly.

### Python Prototype
1. Ensure Python 3.8+ is installed.  
2. Run `python main.py` in a terminal, or paste the code into an IDE.  
3. Follow the on-screen questionnaire.  
4. View your top compatible flatmates in the console.  

(You can also visit the Lovable site for the same experience in a browser.)

---

#Credits

Developed by  
Angelo Pascarella, Juan Moral, Ignacio Roca de Togores, Bosco Oficialdegui, Lucas Parga, and Alejandro Montojo
for Algorithms & Data Structures (2025–2026) at IE University.

---
