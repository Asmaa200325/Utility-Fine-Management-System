# Foundations of Program Logic: Water Billing System 💧

## 📌 Project Overview
The **Water Bill Program** is a practical demonstration of financial management logic designed to solve real-world problems by processing data and making automated decisions. It serves as a system to manage user consumption, apply fines for high usage, and enforce payment policies through a structured logic flow.

## 🧠 Core Programming Logic
To build this system, we rely on two fundamental building blocks: **Constants** and **Variables**.

### 1. The Anchor: Constants (Fixed Rules)
Constants act as the "rules of the game" that remain fixed throughout the program's execution to ensure consistency.
* **`Amount_of_fine` (200.0):** The fixed penalty fee applied to high-consumption accounts.
* **`size` (2):** Defines the structural limits for data sets and payment tracking.

### 2. The Containers: Variables (Dynamic Data)
The program uses specific variables to handle unique, changing user data:
* **Input Variables:** `Thebasicwaterbill` (initial charge) and `fineispaied` (transaction amount).
* **Tracking Variables:** `totalpaid` (cumulative tally) and `numberofwarningmessages` (the system enforcer for the 3-chance limit).
* **Calculation Variables:** `rest` (decimal precision) and `therest` (whole-number container).

## 🛠️ Data Types & Technical Precision
The program distinguishes between `int` and `double` to ensure accurate processing:
* **Whole Numbers (int):** Used for counters and limits like `numberofwarningmessages` and `totalpaid`.
* **Decimal Numbers (double):** Used for financial values requiring precision like `Thebasicwaterbill` and `Amount_of_fine`.

> **Senior Architect Note:** While `totalpaid` is an `int` in this logic, using `double` for all financial variables is recommended to avoid "truncation" (losing decimal precision).

## 🔄 The Billing Lifecycle
1. **Input:** User enters water usage data.
2. **Logic Trigger:** Comparison against rules to apply the `Amount_of_fine`.
3. **Cumulative Tracking:** Payments are added to the `totalpaid` variable.
4. **Iteration:** The program increments the `numberofwarningmessages` counter against the three-chance limit.
5. **Final Calculation:** Subtracts `totalpaid` from the `Amount_of_fine` to inform the user of the remaining balance.

---
*Developed as a case study in building maintainable and structured code.*
