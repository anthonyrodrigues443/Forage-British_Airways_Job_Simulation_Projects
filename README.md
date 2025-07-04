# Forage -British Airways Data Science Job Simulation

<img src="https://github.com/anthonyrodrigues443/Forage-British_Airways_Job_Simulation_Projects/blob/main/powered_by-logos/forage_logo.png" height="200px" >&nbsp;&nbsp; <img src="https://github.com/anthonyrodrigues443/Forage-British_Airways_Job_Simulation_Projects/blob/main/powered_by-logos/british_airways_logo.jpg" height="200px">

A comprehensive data science project completed through Forage's British Airways virtual job simulation program, focusing on customer analytics and predictive modeling in the aviation industry.

## 🎯 Project Overview

This project consists of two main tasks that simulate real-world data science challenges at British Airways:

1. **Flight-Based Customer Grouping via Lookup Analysis** - Customer segmentation and lounge utilization analysis
2. **Customer Purchase Prediction Model** - Machine learning model to predict customer booking behavior

## 📋 Table of Contents

- [Task 1: Customer Grouping Analysis](#task-1-customer-grouping-analysis)
- [Task 2: Purchase Prediction Model](#task-2-purchase-prediction-model)
- [Technologies Used](#technologies-used)
- [Key Results](#key-results)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Certificate](#certificate)

## 🔍 Task 1: Customer Grouping Analysis

### Objective
Analyze customer segments and lounge utilization patterns across different flight groups to optimize resource allocation and improve customer experience.

### Key Features
- **Feature Engineering**: 
  - Aircraft Manufacturer classification (Airbus/Boeing) from Aircraft Type data
  - DayType categorization (Weekday/Weekend) from Flight Date
- **Customer Segmentation**: Three-tier customer grouping based on loyalty status
- **Lounge Utilization Calculations**: Complex formulas for predicting lounge usage across customer tiers

### Methodology
Developed tier-specific lounge utilization formulas:

**For flights with First Class seats:**
- Tier1% = Tier1_Eligible_Pax/(First_Class_Seats + 0.05×Business_Class_Seats)
- Tier2% = Tier2_Eligible_Pax/(First_Class_Seats + 0.05×Business_Class_Seats)
- Tier3% = Tier3_Eligible_Pax/(First_Class_Seats + Business_Class_Seats + 0.1×Economy_Seats)

**For flights without First Class seats:**
- Tier1% = Tier1_Eligible_Pax/(0.5×Business_Class_Seats)
- Tier2% = Tier2_Eligible_Pax/(0.8×Business_Class_Seats + 0.1×Economy_Seats)
- Tier3% = Tier3_Eligible_Pax/(Business_Class_Seats + 0.1×Economy_Seats)

### Key Findings
Identified significant behavioral differences across flight groups:
- **Long-haul Airbus flights**: Morning/Afternoon vs Evening/Lunchtime patterns
- **Long-haul Boeing flights**: Consistent patterns across all times
- **Short-haul Airbus flights**: Time-based segmentation reveals distinct usage patterns

## 🤖 Task 2: Purchase Prediction Model

### Objective
Build a machine learning model to predict customer purchase behavior and identify key factors influencing booking decisions.

### Data Preprocessing
- **Data Cleaning**: Handled null values, removed duplicates, dropped single class features, grouped countries, airport-codes from booking origin and route features respectively to their continents.
- **Feature Engineering**: Created meaningful features from raw data(flight reachday, flight reachhour from flight hour + flight duration)
- **Multicollinearity**: Detected and addressed correlated features
- **Outlier Removal**: Used percentile based outlier method to identify and handle outliers( lower limit - 0.00, upper limit-99.7)
- **Encoding**: Advanced categorical encoding techniques
- **Class Imbalance**: Implemented Borderline SMOTE for oversampling

### Model Development
- **Algorithm**: LightGBM Classifier
- **Data Splitting**: Proper train-test split methodology
- **Feature Scaling**: Standardized numerical features
- **Dimensionality Reduction**: Applied techniques to optimize feature space
- **Hyperparameter Tuning**: Randomized Search CV for optimal parameters

### Model Performance
- **Recall**: 86% (6% improvement after hyperparameter tuning)
- **F1 Score**: 90% (6% improvement after hyperparameter tuning)
- **Key Features**: Purchase lead time, flight duration, and length of stay identified as most important predictors

## 🛠️ Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms and preprocessing
- **LightGBM**: Gradient boosting framework
- **Imbalanced-learn**: Handling class imbalance (SMOTE)
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter Notebook**: Development environment

## 📊 Key Results

### Task 1 Results
- Successfully identified distinct customer behavior patterns across flight segments
- Developed actionable insights for lounge capacity planning
- Created a scalable methodology for ongoing customer analysis

### Task 2 Results
- Achieved a high-performance predictive model with 90% F1 Score
- Identified key purchase drivers for targeted marketing strategies
- Demonstrated end-to-end ML pipeline development skills

## 🚀 Installation & Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ba-data-science-simulation.git
   cd ba-data-science-simulation
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the notebooks**
   ```bash
   jupyter notebook
   ```

5. **Execute tasks**
   - Open `Task_1_Customer_Grouping.ipynb` for customer segmentation analysis
   - Open `Task_2_Purchase_Prediction.ipynb` for ML model development

## 📁 Project Structure

```
Forage-British_Airways_Job_Simulation_Projects/
│
├── .git/                                    # Git repository files
├── ba_airways_jobsim/                       # virtual env
├── powered_by-logos/                        # Logo assets
├── Task1-Lounge_estimation_with_logical_assum.../  # Task 1 analysis folder
├── Task2-dataset/                           # Task 2 dataset folder
│
├── .gitignore                               # Git ignore file
├── Certificate-BritishAirways_jobsim.pdf    # Completion certificate
├── Customer Prediction Presentation.pptx    # Project presentation
├── customer_booking_project.nb              # Main analysis notebook
├── Forage-BritishAirways_JobSim_Certificate.jpg  # Certificate image
├── LICENSE                                  # Project license
├── README.md                               # Project documentation
└── requirements.txt                        # Python dependencies
```

## 🏆 Certificate

Successfully completed the British Airways Data Science Job Simulation program through Forage, demonstrating proficiency in:
- Customer segmentation and behavioral analysis
- Advanced machine learning model development
- Business problem-solving in the aviation industry
- End-to-end data science project execution

[View Certificate](./BA_Certificate.pdf)

## 🔗 Connect

  <a href="mailto:anthonyrodrigues443@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Gmail-anthonyrodrigues443@gmail.com-B22222?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://linkedin.com/in/anthonyrodrigues443" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-anthonyrodrigues443-005B8A?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>&nbsp;

---

*This project was completed as part of the British Airways Data Science Job Simulation program offered by Forage. It represents practical application of data science skills in a real-world aviation industry context.*
