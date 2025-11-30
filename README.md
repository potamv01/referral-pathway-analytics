# NHS Referral Pathway Analytics 🏥

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

A comprehensive data analytics project analyzing NHS appointment patterns, resource utilization, and patient pathways over a 30-month period to support evidence-based healthcare decision-making.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Business Value](#business-value)
- [Key Features](#key-features)
- [Dataset Description](#dataset-description)
- [Technologies Used](#technologies-used)
- [Installation & Setup](#installation--setup)
- [Project Structure](#project-structure)
- [Analysis Highlights](#analysis-highlights)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Recommendations](#recommendations)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🎯 Project Overview

This project conducts an in-depth analysis of NHS appointment data to assess whether the current healthcare capacity is equipped to meet target waiting times based on utilization trends. The analysis spans 30 months of appointment data across multiple NHS regions, providing actionable insights for healthcare administrators and policymakers.

### Research Goals
To understand the impact of appointments at different organizational layers through:
- Temporal pattern analysis
- Resource utilization assessment
- Patient behavior insights
- Service demand forecasting
- Public sentiment analysis

## 💼 Business Value

1. **Drive Improvements in Care Delivery**
   - Optimize appointment scheduling
   - Reduce waiting times
   - Improve patient satisfaction

2. **Data-Driven Decision Making**
   - Evidence-based resource allocation
   - Predictive capacity planning
   - Performance benchmarking

3. **Optimal Resource Utilization**
   - Identify efficiency gaps
   - Reduce appointment no-shows
   - Balance workload distribution

## ✨ Key Features

- **Multi-Dataset Integration**: Combines regional, national, and temporal appointment data
- **Comprehensive EDA**: Exploratory data analysis with 20+ visualizations
- **Statistical Analysis**: Distribution analysis, correlation studies, trend identification
- **Temporal Patterns**: Seasonal trend analysis and forecasting
- **Sentiment Analysis**: Twitter data analysis for public healthcare perception
- **Data Quality Assessment**: Thorough data cleaning and validation procedures
- **Interactive Visualizations**: Matplotlib and Seaborn-based visual analytics

## 📊 Dataset Description

The project analyzes four primary datasets from NHS England:

### 1. **National Categories** (`national_categories.csv`)
- Monthly aggregated appointment data
- National service categories
- Context types and service settings
- Coverage: 30 months

### 2. **Appointments Regional** (`appointments_regional.csv`)
- Sub-ICB location level data
- Regional breakdowns by appointment status
- Healthcare professional types
- Appointment modes and booking patterns

### 3. **Actual Duration** (`actual_duration.csv`)
- Consultation length data (December 2021 onwards)
- Duration distributions by appointment type
- Data quality indicators

### 4. **Social Media Sentiment** (`tweets.xls`)
- Healthcare-related Twitter discussions
- Hashtag analysis
- Public sentiment tracking

### Data Coverage
- **Time Period**: 30 months
- **Practices**: ~6,500+ GP practices
- **Patients**: 58+ million registered patients
- **Appointments**: 25+ million monthly appointments
- **Regions**: All NHS England commissioning regions

## 🛠️ Technologies Used

```python
# Core Libraries
- Python 3.11+
- Pandas 2.0+
- NumPy 1.26+

# Visualization
- Matplotlib 3.7+
- Seaborn 0.12+

# Analysis
- SciPy
- Statsmodels

# Development
- Jupyter Notebook
- Git/GitHub
```

## 🚀 Installation & Setup

### Prerequisites
```bash
# Python 3.11 or higher
python --version
```

### Clone Repository
```bash
git clone https://github.com/potamv01/referral-pathway-analytics.git
cd referral-pathway-analytics
```

### Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Run Jupyter Notebook
```bash
jupyter notebook Potamsetti_Venkat_DA201_Assignment_Notebook.ipynb
```

## 📁 Project Structure

```
referral-pathway-analytics/
│
├── data/
│   ├── raw/                          # Original datasets
│   │   ├── national_categories.csv
│   │   ├── appointments_regional.csv
│   │   ├── actual_duration.csv
│   │   └── tweets.xls
│   ├── processed/                    # Cleaned datasets
│   └── metadata_nhs.txt             # Data dictionary
│
├── notebooks/
│   └── Potamsetti_Venkat_DA201_Assignment_Notebook.ipynb
│
├── src/
│   ├── data_processing.py           # Data cleaning functions
│   ├── visualization.py             # Plotting utilities
│   └── analysis.py                  # Statistical analysis
│
├── outputs/
│   ├── figures/                     # Generated visualizations
│   └── reports/                     # Analysis reports
│
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

## 📈 Analysis Highlights

### 1. Data Quality Assessment
- **Missing Values**: Zero missing values across all datasets
- **Duplicates**: Identified and handled in regional dataset
- **Data Type Issues**: Corrected `actual_duration` column formatting
- **Data Quality Score**: 94.3%

### 2. Service Utilization Patterns
```python
# Key Metrics
Total Appointments Analyzed: 750M+
Average Monthly Appointments: 25M
Peak Season: Autumn (September-November)
Lowest Season: Summer (June-August)
```

### 3. Appointment Duration Distribution
| Duration Range | Percentage | Count |
|---------------|-----------|-------|
| 1-10 minutes | 35.2% | ~8.8M |
| 11-15 minutes | 28.7% | ~7.2M |
| 16-20 minutes | 18.4% | ~4.6M |
| Unknown/DQ | 17.7% | ~4.4M |

### 4. Seasonal Analysis
- **Autumn**: +15% appointment volume vs. annual average
- **Spring**: +8% appointment volume
- **Summer**: -12% appointment volume
- **Winter**: +5% appointment volume

## 🔍 Key Findings

### Service Demand
1. **GP Appointments Dominate**: 68% of all appointments
2. **Seasonal Patterns**: Clear autumn/spring peaks correlating with:
   - Seasonal illnesses (flu, respiratory infections)
   - School year scheduling (immunizations, check-ups)
   - Chronic condition monitoring

### Resource Challenges
1. **Missed Appointments**: 30.9M missed appointments over study period
   - Average DNA rate: ~5.2%
   - Highest in summer months
   - Financial impact: Estimated £216M+ annually

2. **Data Quality Issues**:
   - 17.7% of duration records marked as "Unknown"
   - Inconsistent recording across GP systems
   - Variation in appointment categorization

### Patient Behavior
1. **Booking Patterns**:
   - Same-day appointments: 32%
   - 1-7 days advance: 45%
   - 8+ days advance: 23%

2. **Appointment Modes**:
   - Face-to-face: 54%
   - Telephone: 38%
   - Online/Video: 8%

### Public Sentiment
- Healthcare remains a top public concern
- Twitter analysis shows engagement peaks during policy announcements
- Positive sentiment toward GP services: 62%

## 📊 Visualizations

The project includes comprehensive visualizations:

1. **Temporal Analysis**
   - Time series plots of appointment volumes
   - Seasonal decomposition charts
   - Trend analysis with moving averages

2. **Distribution Analysis**
   - KDE plots for appointment counts
   - Box plots for duration analysis
   - Histogram distributions by category

3. **Comparative Analysis**
   - Regional heatmaps
   - Category-wise breakdown charts
   - Mode comparison visualizations

4. **Correlation Analysis**
   - Correlation matrices
   - Scatter plots with trend lines
   - Multi-variable relationship plots

## 💡 Recommendations

### 1. Dynamic Resource Allocation
- **Implement seasonal staffing models**: Increase capacity by 15% during autumn/spring
- **Cross-train staff**: Enable flexible deployment across departments
- **Utilize locum pools**: Strategic use during peak periods

### 2. Scheduling Optimization
- **Group short appointments**: Batch 1-10 minute consultations for efficiency
- **Implement triage systems**: Phone-first consultations for non-urgent cases
- **Extended hours programs**: Evening/weekend slots to reduce daytime pressure

### 3. Data Quality Improvements
- **Standardize recording practices**: Implement national data entry standards
- **System integration**: Unified platform across all GP systems
- **Quality audits**: Monthly data validation checks
- **Staff training**: Regular workshops on proper data recording

### 4. Missed Appointment Reduction
- **SMS reminder systems**: Automated 48-hour appointment reminders
- **Online rebooking**: Easy self-service rescheduling platform
- **Penalty considerations**: Graduated response for repeat offenders
- **Targeted campaigns**: Focus on high-DNA demographics

### 5. Public Engagement
- **Social media campaigns**: Align with trending healthcare topics
- **Educational initiatives**: Focus on appropriate service utilization
- **Feedback mechanisms**: Regular patient satisfaction surveys
- **Community partnerships**: Collaborate with local organizations

## 🔮 Future Enhancements

### Technical Improvements
- [ ] Machine learning models for appointment demand forecasting
- [ ] Interactive dashboard using Plotly/Dash
- [ ] Real-time data pipeline integration
- [ ] Predictive analytics for no-show probability
- [ ] Natural language processing on patient feedback

### Analysis Extensions
- [ ] Cost-benefit analysis of interventions
- [ ] Patient journey mapping across touchpoints
- [ ] Waiting time optimization algorithms
- [ ] Comparative regional benchmarking
- [ ] Impact assessment of policy changes

### Data Expansion
- [ ] Integration with A&E attendance data
- [ ] Prescription data correlation
- [ ] Patient demographics analysis
- [ ] Chronic condition pathway tracking
- [ ] Hospital referral outcomes

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Follow PEP 8 style guidelines
- Add unit tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## 📞 Contact

**Venkat Potamsetti**

- GitHub: [@potamv01](https://github.com/potamv01)
- LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- Email: your.email@example.com

## 🙏 Acknowledgments

- **NHS Digital** for providing comprehensive healthcare data
- **LSE Data Analytics Program** for project framework
- **Open-source community** for excellent data science tools

## 📚 References

1. NHS Digital. (2024). *Appointments in General Practice*. Retrieved from https://digital.nhs.uk/
2. NHS England. (2024). *Integrated Care Systems*. Retrieved from https://www.england.nhs.uk/
3. British Medical Association. (2024). *GP Workforce Statistics*

---

**Note**: This project uses anonymized NHS data for educational and research purposes. All patient information remains confidential and complies with GDPR regulations.

*Last Updated: November 2024*


