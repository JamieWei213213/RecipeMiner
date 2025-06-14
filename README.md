# RecipeMiner

# 🥗 Nutritional Intelligence from Recipes

This project extracts and analyzes nutrition data from two primary sources: the **FatSecret API** and **DiabetesFoodHub.org**. It builds a unified, structured dataset of 2,000+ food items and recipes to support macronutrient analysis, diet comparison, and health-focused data applications.

---

## 📌 Features

### 🔐 FatSecret API Integration
- Authenticates via OAuth 2.0 (client credentials flow)
- Searches foods (e.g., `"apple"`) and paginates results
- Extracts:  
  - Food name  
  - Brand name  
  - Nutritional description  
  - Macronutrients (calories, fat, protein, carbs)  
  - Food type and URL  
- Saves to `foods_data.csv`

### 🌐 Web Scraping: DiabetesFoodHub
- Scrapes recipe data from 12+ dietary categories (e.g., low-carb, vegetarian, dessert)
- Collects recipe links across all pages in each category
- Extracts embedded JSON-LD nutrition info
- Compiles results in `diabetes_recipes.csv`

### 📊 Additional Diet Datasets
Includes cleaned nutrition data from curated datasets for:
- Keto
- Paleo
- Dash
- Mediterranean
- Vegan
- Vegetarian
- Trend diets

Each file (e.g. `keto.csv`) contains:
- Recipe name, cuisine type
- Protein, Carbs, Fat (g)
- Extraction metadata (date/time)

---

## 🛠 Technologies Used
- **Python**
- `requests`, `BeautifulSoup`, `pandas`, `json`, `time`, `random`
- **OAuth 2.0** via `requests_oauthlib`
- HTML scraping with `BeautifulSoup`
- FatSecret API: [https://platform.fatsecret.com/](https://platform.fatsecret.com/)
- Targeted scraping: [https://diabetesfoodhub.org](https://diabetesfoodhub.org)

---

## 📁 Output Files
| File Name            | Description                                 |
|----------------------|---------------------------------------------|
| `foods_data.csv`     | FatSecret API results                       |
| `diabetes_recipes.csv` | Scraped recipe + nutrition data          |
| `keto.csv`, `paleo.csv`, etc. | Structured datasets by diet       |

---

## 📌 Example Use Cases
- Compare macro breakdowns between diets (e.g. keto vs paleo)
- Identify high-protein, low-carb meals for diabetics
- Build dashboards or ML pipelines for dietary recommendations

---

## ⚠️ Important Note
For security, do **not expose your API `client_id` or `client_secret`** in code. Use a `.env` file and `python-dotenv` to manage secrets safely.

---

## ✅ TODO / Future Ideas
- Visualize macro distribution across diets
- Add text classification on ingredients
- Build a nutrition recommender system

---

## 📬 Contact
Open an issue or pull request if you’d like to contribute, ask a question, or collaborate!
