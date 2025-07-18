House Price Prediction Using Linear RegressionProject OverviewThis repository implements a simple linear regression model to predict house sale prices based on a subset of features from the Kaggle House Prices dataset. The project covers data loading, preprocessing, exploratory data analysis (EDA), model training, evaluation, and visualization of results.
DatasetSource: train.csv from Kaggle’s “House Prices: Advanced Regression Techniques” competition.
Sample Size: 1460 observations in train.csv.
Features SelectedFeature ColumnDescriptionRenamed AsGrLivAreaAbove grade (ground) living area (sq ft)Sqr.FtBedroomAbvGrNumber of bedrooms above groundNo of BedroomFullBathNumber of full bathroomsNo of BathroomSalePriceSale price of the house (target)SalePriceMethodologyData Loading:
Imported train.csv using pandas.
Preprocessing:
Selected only the columns of interest (GrLivArea, BedroomAbvGr, FullBath, SalePrice).
Renamed columns for readability.
Checked for missing values and basic statistics.
Exploratory Data Analysis:
Displayed descriptive statistics and data types.
Visualized feature distributions and relationships using scatter plots and a 3D scatter plot.
Data Splitting & Scaling:
Split data into training (90%) and testing (10%) sets using train_test_split.
Applied StandardScaler to standardize feature means and variances.
Model Training:
Trained a LinearRegression model on the standardized training data.
Model Evaluation:
Predicted sale prices on the test set.
Calculated the R² score to assess model performance.
Plotted predicted vs. actual values with a perfect prediction reference line and error bars.
Generated a comparison table of actual vs. predicted values.
InstallationClone this repository:
git clone https://github.com/<your-username>/house-price-linear-regression.git
cd house-price-linear-regressionCreate a virtual environment and install dependencies:
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txtUsageEnsure train.csv is placed in the project root directory.
Run the Jupyter notebook:
jupyter notebook "House Price Linear Regression.ipynb"Execute cells sequentially to reproduce data analysis, model training, and visualizations.
ResultsR² Score: Achieved an R² score of approximately 0.62 on the test set.
Visualization: The scatter plot of predicted vs. actual sale prices demonstrates the fit quality. A perfect prediction line (dashed red) helps assess deviations.

Future ImprovementsFeature Engineering: Incorporate additional relevant features such as OverallQual, YearBuilt, and neighborhood-based variables.
Model Selection: Compare with more complex models (e.g., Ridge, Lasso, Random Forest) and perform hyperparameter tuning.
Cross-Validation: Implement k-fold cross-validation to obtain a more robust estimate of model performance.
File Structure├── House Price Linear Regression.ipynb  # Jupyter notebook with analysis and modeling
├── train.csv                          # Raw dataset
├── plots/
│   └── predicted_vs_actual.png        # Generated scatter plot
├── requirements.txt                   # Python dependencies
└── README.md                          # Project documentationLicenseThis project is licensed under the MIT License. Feel free to use and modify.
