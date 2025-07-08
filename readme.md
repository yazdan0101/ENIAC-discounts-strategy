# ENIAC Discounts Strategy

Welcome to **ENIAC Discounts Strategy**,  
This project aims to analyze the impact of product discounts using internal (non-anonymized) data, with a focus on answering a central business question:  

> _Are product discounts beneficial for the company in the long run?_

---

## 🧠 Project Background

Eniac’s leadership is divided:

- **The Marketing Team Lead** strongly believes discounts are a growth tool — helping with customer **acquisition**, **satisfaction**, and **retention**.
- **The Board of Investors**, on the other hand, is concerned about recent trends: **more orders but less revenue**. They favor a focus on **quality** over price competition.

You’ve been tasked with using Python to uncover insights and settle this debate.

---

## 📁 Project Structure

The project uses four main datasets:

### 1. `orders.csv`
Each row represents a **customer order**.

| Column         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `order_id`     | Unique ID for the order                                                     |
| `created_date` | Timestamp when the order was created                                        |
| `total_paid`   | Total amount paid (in euros)                                                |
| `state`        | Order status: Shopping basket, Placed, Pending, Completed, or Cancelled     |

---

### 2. `orderlines.csv`
Each row represents an **item** in an order.

| Column            | Description                                                  |
|-------------------|--------------------------------------------------------------|
| `id`              | Unique row ID                                                |
| `id_order`        | Matches `order_id` from `orders.csv`                         |
| `product_id`      | Legacy product ID (no longer used)                           |
| `product_quantity`| Quantity of the product ordered                              |
| `sku`             | Unique product identifier (Stock Keeping Unit)              |
| `unit_price`      | Price per unit at the time of the order                      |
| `date`            | Timestamp when the product was processed                     |

---

### 3. `products.csv`
Each row describes a **product**.

| Column       | Description                                               |
|--------------|-----------------------------------------------------------|
| `sku`        | Unique product identifier                                 |
| `name`       | Product name                                              |
| `desc`       | Description                                               |
| `price`      | Base price (in euros)                                     |
| `promo_price`| Promotional (discounted) price (in euros)                |
| `in_stock`   | Whether the product was in stock at data extraction       |
| `type`       | Numerical code for product type                           |

---

### 4. `brands.csv`
Each row describes a **brand**.

| Column | Description                                                  |
|--------|--------------------------------------------------------------|
| `short`| 3-character brand code (matches first 3 characters of SKU)   |
| `long` | Full brand name                                              |

---

## 🧰 Technologies Used

- **Python** (data analysis & visualization)
- **pandas** (data wrangling)
- **seaborn** (for plots)
- **Jupyter Notebooks** (recommended for exploration)

---

## 📦 How to Use

1. Clone the repo:
   ```bash
   git clone https://github.com/yazdan0101/ENIAC-discounts-strategy.git
   cd ENIAC-discounts-strategy
   ```
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```


