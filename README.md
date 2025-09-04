# AtliQo Bank Credit Card Launch Analytics

A comprehensive data analytics project to identify optimal customer segments for AtliQo Bank's inaugural credit card launch in the competitive Indian banking market.

## Table of Contents

- [Business Problem](#business-problem)
- [Project Objective](#project-objective)
- [Project Phases](#project-phases)
- [Key Insights](#key-insights)
- [Tech Stack](#tech-stack)
- [Installation and Setup](#installation-and-setup)
- [How to Run the Analysis](#how-to-run-the-analysis)
- [Project Structure](#project-structure)
- [Data Schema](#data-schema)
- [Analysis Highlights](#analysis-highlights)
- [Contributing](#contributing)

## Business Problem

AtliQo Bank, an emerging player in the Indian banking sector, faces the challenge of launching their first credit card in a highly saturated and competitive market. The bank needs to:

- Differentiate from established competitors
- Target the right customer segments
- Leverage data-driven insights for strategic decision making
- Optimize risk and profitability expectations

The core challenge lies in identifying the most promising customer group whose financial behavior and credit readiness align with the bank's risk and profitability expectations.

## Project Objective

**Primary Goal:** Identify high-potential customer segments for credit card launch through comprehensive analysis of customer demographics, financial behavior, and credit profiles using a strategic two-phase approach.

## Project Phases

### Phase 1: Data-Driven Target Market Identification

- **Data Cleaning:** Handle missing values and ensure data consistency
- **Distribution Analysis:** Evaluate normality and skewness of financial indicators
- **Exploratory Data Analysis:** Uncover behavioral and financial trends
- **Outlier Treatment:** Address extreme values for improved model accuracy
- **Visualization:** Generate actionable insights and customer segment profiles

### Phase 2: Pilot Launch and Validation

- **Trial Campaign:** Small-scale rollout to identified segments
- **Hypothesis Testing:** Statistical validation of business assumptions
- **Performance Metrics:** Monitor response rates and credit performance

## Key Insights

### Target Segment: Age Group 18-25

| Metric | Value | Insight |
|--------|-------|---------|
| **Market Share** | ~24.6% | Significant portion of customer base |
| **Average Income** | <$50K | Limited earning capacity, growth potential |
| **Credit Profile** | Low-Medium | Building credit history phase |
| **Card Usage** | Low | Opportunity for engagement |

#### Top Spending Categories
1. **Electronics** - Tech-savvy demographic
2. **Fashion & Apparel** - Lifestyle-focused spending
3. **Beauty & Personal Care** - Aspirational purchases

**Strategic Insight:** This segment shows high interest in lifestyle and aspirational spending despite limited financial leverage, presenting an excellent opportunity for targeted credit products.

## Tech Stack

### Core Technologies
- **Python 3.8+** - Primary programming language
- **Jupyter Notebook** - Interactive development environment
- **MySQL** - Database management system

### Libraries and Frameworks
```
Data Operations:    NumPy, Pandas
Visualizations:     Matplotlib, Seaborn
Database:          SQLAlchemy
Analysis:          SciPy, Statsmodels
```

### Analytical Techniques
- Exploratory Data Analysis (EDA)
- Distribution and Skewness Analysis
- Statistical Outlier Detection
- Hypothesis Testing
- Customer Segmentation

## Installation and Setup

### Prerequisites
- Python 3.8 or higher
- MySQL Server
- Jupyter Notebook
- Git

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Atliqo-Bank-CreditCard-Statistical-Analysis.git
   cd Atliqo-Bank-CreditCard-Statistical-Analysis
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up database connection**
   Create a `.env` file in the project root with your database credentials:
   ```
   DB_HOST=your_host
   DB_USER=your_username
   DB_PASSWORD=your_password
   DB_NAME=atliqo_bank
   DB_PORT=3306
   ```

5. **Install Jupyter Notebook (if not already installed)**
   ```bash
   pip install jupyter
   ```

## How to Run the Analysis

### Method 1: Using Jupyter Notebook (Recommended)

1. **Start Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   This will open Jupyter in your default web browser at `http://localhost:8888`

2. **Navigate to the notebook**
   - In the Jupyter interface, click on `AtliQo Bank CreditCard Launch.ipynb`

3. **Run the analysis**
   - Execute cells sequentially by pressing `Shift + Enter` for each cell
   - Alternatively, use `Cell → Run All` to execute all cells at once

4. **View results**
   - Visualizations and insights will appear inline within the notebook
   - Generated plots and tables will display directly below each code cell

### Method 2: Using Jupyter Lab

1. **Start Jupyter Lab**
   ```bash
   jupyter lab
   ```

2. **Open the notebook file and run cells as described above**

### Method 3: Using VS Code (Alternative)

1. **Open the project in VS Code**
2. **Install the Jupyter extension for VS Code**
3. **Open the `.ipynb` file and run cells interactively**

### Troubleshooting

- **Database Connection Issues:** Verify your `.env` file contains correct credentials
- **Package Import Errors:** Ensure all required packages are installed via `pip install -r requirements.txt`
- **Kernel Issues:** Restart the Jupyter kernel using `Kernel → Restart & Clear Output`

## Project Structure

```
Atliqo-Bank-CreditCard-Statistical-Analysis/
├── AtliQo Bank CreditCard Launch.ipynb  # Main analysis notebook
├── README.md                           # Project documentation
├── requirements.txt                    # Python dependencies
├── data/                               # Data files (if applicable)
├── scripts/                            # Utility scripts
├── .env.example                        # Environment template
├── .gitignore                          # Git ignore rules
└── LICENSE                             # License file
```

## Data Schema

### Customer Table
| Column | Type | Description |
|--------|------|-------------|
| `cust_id` | String | Unique customer identifier |
| `name` | String | Customer full name |
| `gender` | String | Gender (Male/Female) |
| `age` | Integer | Customer age in years |
| `location` | String | Geographic location |
| `occupation` | String | Primary profession |
| `annual_income` | Float | Yearly income |
| `marital_status` | String | Marital status |

### Credit Score Table
| Column | Type | Description |
|--------|------|-------------|
| `cust_id` | String | Customer identifier |
| `credit_score` | Integer | Creditworthiness score |
| `credit_utilisation` | Float | Credit usage ratio |
| `outstanding_debt` | Float | Total unpaid debt |
| `credit_inquiries_last_6_months` | Integer | Recent credit checks |
| `credit_limit` | Float | Maximum credit amount |

### Transactions Table
| Column | Type | Description |
|--------|------|-------------|
| `tran_id` | String | Transaction identifier |
| `cust_id` | String | Customer identifier |
| `tran_date` | Date | Transaction date |
| `tran_amount` | Float | Transaction value |
| `platform` | String | E-commerce platform |
| `product_category` | String | Product category |
| `payment_type` | String | Payment method |

## Analysis Highlights

- **Customer Segmentation** based on demographics and financial behavior
- **Spending Pattern Analysis** across different categories and platforms
- **Credit Risk Assessment** using historical data
- **Market Opportunity Identification** for targeted campaigns

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -m 'Add some NewFeature'`)
4. Push to the branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

---

**This project is part of a data analytics portfolio demonstrating customer segmentation and market analysis capabilities for the banking sector.**
