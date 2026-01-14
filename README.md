# 🏆 Forest Fire Prediction - 1st Place Solution

**Winner of the Forest Fire Prediction Epoch Hackathon** organized by the ML Dream Team at TU Delft

[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/code/nicolaemario/sample-notebook123-11cc6e?scriptVersionId=223922033)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

## 🎯 Competition Overview

This project won **1st place** in the Forest Fire Prediction Epoch Hackathon, a machine learning competition focused on predicting wildfire surface areas across American states from 2011-2015.

**Competition Details:**
- **Goal:** Predict the total forest fire surface area for each US state and calendar month (2011-2015)
- **Host:** ML Dream Team - TU Delft
- **Participants:** 103 entrants, 84 participants, 36 teams
- **Submissions:** 551 total submissions
- **Achievement:** 🥇 **1st Place**

## 📊 Problem Statement

The challenge involved creating a predictive model for wildfire surface areas using:
- Historical wildfire data (1992-2010)
- Monthly weather aggregates (precipitation, evaporation, temperature)
- State-level geographic and demographic data
- Urbanization and land use statistics

The model had to predict `total_fire_size` for each state and month in the test period (post-2010).

## 🔬 Evaluation Metric

The competition used a custom logarithmic scoring metric:

$$\text{Score} = \frac{1}{N} \sum_{i=1}^{N} \min\left(\left|\log\left(\frac{\hat{y}_i}{y_i}\right)\right|, 10\right)$$

Where:
- *N*: total number of predictions
- *ŷᵢ*: predicted fire size for instance *i*
- *yᵢ*: ground truth fire size

The goal was to minimize this metric, with lower scores indicating better performance.

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib/Seaborn** - Data visualization (if applicable)
- **Jupyter Notebook** - Interactive development environment

## 📁 Dataset

The competition provided multiple data sources:

1. **merged_state_data.csv** - State-level geographic and demographic data
   - Average elevation, land/water area
   - Federal land percentage
   - Urbanization rate

2. **weather_monthly_state_aggregates.csv** - Monthly weather data
   - Precipitation (PRCP)
   - Evaporation (EVAP)
   - Min/Max Temperature (TMIN/TMAX)

3. **wildfire_sizes_before_2010.csv** - Historical wildfire records (1992-2010)
   - Training data for model development

**Note:** Competition data can be accessed through the [Kaggle competition page](https://www.kaggle.com/competitions/forest-fire-prediction-epoch-hackathon).

## 🚀 Approach & Methodology

My winning solution involved:

1. **Data Preprocessing**
   - Handling missing values in weather and geographic data
   - Feature engineering from temporal patterns
   - Scaling and normalization of input features

2. **Feature Engineering**
   - Temporal features (month, year trends)
   - State-specific characteristics
   - Weather pattern aggregations
   - Interaction features between weather and geography

3. **Model Development**
   - Experimentation with multiple regression approaches
   - Careful handling of the logarithmic evaluation metric
   - Cross-validation strategy aligned with temporal nature of data

4. **Optimization**
   - Hyperparameter tuning
   - Ensemble methods for improved predictions
   - Custom loss functions matching the competition metric

## 📈 Results

- **Final Rank:** 🥇 **1st Place**
- **Competition Performance:** Top performer among 103 entrants
- Successfully predicted wildfire patterns across diverse US states and seasonal conditions

## 💻 How to Run

### Prerequisites

```bash
pip install -r requirements.txt
```

### Running the Notebook

1. Clone this repository:
```bash
git clone https://github.com/FrozenBike265/forest-fire-prediction-kaggle.git
cd forest-fire-prediction-kaggle
```

2. Download the competition data from [Kaggle](https://www.kaggle.com/competitions/forest-fire-prediction-epoch-hackathon/data)

3. Place data files in the `data/` directory

4. Open and run the Jupyter notebook:
```bash
jupyter notebook forestFirePrediction.ipynb
```

## 📚 Key Learnings

- Working with multi-source environmental datasets
- Handling temporal prediction tasks with geographic variation
- Optimizing for custom evaluation metrics
- Feature engineering for climate and geographic data
- Competing and succeeding in Kaggle-style ML competitions

## 🔗 Links

- [Kaggle Notebook](https://www.kaggle.com/code/nicolaemario/sample-notebook123-11cc6e?scriptVersionId=223922033)
- [Competition Page](https://www.kaggle.com/competitions/forest-fire-prediction-epoch-hackathon)

## 👤 Author

**Mario-Alexandru Nicolae**
- GitHub: [@FrozenBike265](https://github.com/FrozenBike265)
- 3rd Year Computer Science Student - TU Delft

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- ML Dream Team at TU Delft for organizing the competition
- Kaggle platform for hosting the hackathon
- Competition participants for fostering a collaborative learning environment

---

**Note:** This solution represents original work developed for the Forest Fire Prediction Epoch Hackathon. The approach and methodology reflect techniques learned and applied during my Computer Science studies at TU Delft.
