# 🎬 Movie Trends Analysis

## 📌 Project Overview
This project analyzes global movie trends using **pandas, NumPy, SQLite, Matplotlib, Seaborn, and Power BI**. The dataset includes details on movies, such as release dates, budgets, revenues, ratings, and genres. 

The goal is to explore:
- Trends in movie releases over the years
- Distribution of movie ratings
- Budget vs. revenue analysis
- Most profitable movies and popular genres

## 🗂 Dataset
- **Source:** [Kaggle - IMDB or TMDB Movie Dataset](https://www.kaggle.com/)
- **Contents:** Movie titles, genres, revenue, ratings, and release years
- **Size:** ~10,000+ records

## 🛠 Tech Stack
| Tool | Purpose |
|------|---------|
| `pandas` | Data manipulation |
| `NumPy` | Numerical computations |
| `SQLite` | Database storage |
| `Matplotlib & Seaborn` | Data visualization |
| `Power BI` | Dashboard creation |

## 📊 Data Analysis Steps
### **1️⃣ Data Preprocessing**
- Cleaned missing values, formatted dates, and handled duplicate entries.
- Stored structured data in **SQLite** for efficient querying.

### **2️⃣ Exploratory Data Analysis (EDA)**
✔️ **Top 10 Highest-Grossing Movies**  
✔️ **Movie Release Trends (Year-wise count)**  
✔️ **Distribution of Movie Ratings**  
✔️ **Budget vs. Revenue Correlation**  

### **3️⃣ Power BI Dashboard**
- **Visuals Created:**
  - Movies Released per Year 📈
  - Top 10 Movies by Revenue 💰
  - Budget vs. Revenue Scatter Plot 🎭
  - Genre Popularity Bar Chart 📊

## 📌 Power BI DAX Formulas Used
```DAX
# Average Movie Rating Per Year
Avg_Rating_Per_Year = AVERAGEX(FILTER(movies, movies[release_year] = EARLIER(movies[release_year])), movies[vote_average])

# Profit Calculation
Profit = movies[revenue] - movies[budget]

# Movie Count by Genre
Movie_Count_Genre = COUNTROWS(movies)
