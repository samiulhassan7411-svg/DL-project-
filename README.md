# DL-project-
🎬 Movie Rating Prediction — Deep Learning Project

DL Lab Final Project | Applying Deep Learning on the Movie Rating Prediction dataset from the ML project.


📌 Project Description
This project extends the previous Machine Learning movie rating prediction project by applying Deep Learning techniques. We build and compare two neural network architectures — a Baseline ANN and a Deep ANN with Batch Normalization + Dropout — and benchmark them against the classical ML models.

🧠 Deep Learning Concepts Applied
ConceptDetailsFeedforward ANNFully connected layers with ReLU activationsBatch NormalizationStabilizes training, reduces internal covariate shiftDropoutRegularization to prevent overfitting (0.2–0.3 rate)Adam OptimizerAdaptive learning rate optimizationEarly StoppingStops training when validation loss stops improvingReduceLROnPlateauReduces learning rate when a metric has stopped improving

🏗️ Model Architectures
Model 1 — Baseline ANN
Input → Dense(64, ReLU) → Dense(32, ReLU) → Dense(1)
Model 2 — Deep ANN with BN + Dropout
Input → Dense(256) → BatchNorm → ReLU → Dropout(0.3)
      → Dense(128) → BatchNorm → ReLU → Dropout(0.3)
      → Dense(64)  → BatchNorm → ReLU → Dropout(0.2)
      → Dense(32)  → ReLU
      → Dense(1)

📊 Results & Comparison
ModelMAERMSER²Linear Regression (ML)~0.72~0.89~0.61Random Forest (ML)~0.51~0.64~0.78Baseline ANN (DL)———Deep ANN BN+Dropout (DL)———

DL values are populated after running the notebook on your machine.


📁 Repository Structure
MOVIE-RATING_DL/
│
├── DL_Movie_Rating_Prediction.ipynb   # Main DL notebook
├── project data.csv                   # Dataset (same as ML project)
├── best_movie_rating_dl_model.h5      # Saved best model (after running)
├── eda_plots.png                      # EDA visualizations
├── training_curves.png                # Loss & MAE training curves
├── predictions_scatter.png            # Predicted vs Actual scatter plots
├── residuals.png                      # Residual analysis
├── ml_vs_dl_comparison.png            # ML vs DL comparison bar charts
└── README.md

🚀 How to Run
1. Clone the repository
bashgit clone https://github.com/YOUR_USERNAME/MOVIE-RATING_DL.git
cd MOVIE-RATING_DL
2. Install dependencies
bashpip install tensorflow numpy pandas matplotlib seaborn scikit-learn
3. Launch the notebook
bashjupyter notebook DL_Movie_Rating_Prediction.ipynb
4. Run all cells (Cell → Run All)

📦 Requirements
tensorflow>=2.10
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter

🔗 Related Projects

🤖 ML Project (Previous): MOVIE-RATING_ML
