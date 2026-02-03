***Amazon Prime Content Success Predictor***
An end-to-end Machine Learning pipeline designed to predict whether a movie or TV show on Amazon Prime will be a "Hit" (IMDb score > 7.5). This project transforms raw streaming data into a deployable strategic tool for content acquisition.

***Project Highlights***
High Accuracy: Achieved a final model accuracy of 92% using optimized LightGBM.
Data Balancing: Successfully handled a highly imbalanced dataset (113k average titles vs. 10k hits) using SMOTE.
Explainable AI: Integrated SHAP (SHapley Additive exPlanations) to identify that Popularity and Runtime are the primary drivers of content ratings.
Production Ready: Final model is serialized via joblib for immediate deployment into business dashboards.

***Tech Stack***
Language: Python 3.12
Libraries: Pandas, NumPy, Matplotlib, Seaborn
ML Algorithms: Random Forest, XGBoost, LightGBM
Optimization: GridSearchCV, RandomizedSearchCV
Evaluation: Precision, Recall, F1-Score, Confusion Matrix

***Business Impact***
Risk Mitigation: High Precision scores ensure Amazon Prime avoids over-investing in titles predicted to be low-rated.
Content Discovery: Strong Recall allows the platform to identify "Hidden Gems" that might otherwise be overlooked.
Data-Driven Strategy: Replaces intuition-based acquisition with a mathematical framework, optimizing content budgets for maximum subscriber satisfaction.

***Dataset Information***
The analysis utilized two primary datasets:
titles.csv: Metadata regarding movies and shows (Runtime, Genres, IMDb Scores).
credits.csv: Information regarding cast and crew popularity.

***Implementation Workflow***
Data Cleaning: Handled missing values and filtered non-numeric identifiers.
Feature Engineering: Created targeted features like genre_count and normalized tmdb_popularity.
Class Balancing: Applied SMOTE to synthesize minority class samples and prevent model bias.
Hyperparameter Tuning: Used GridSearchCV to fine-tune the num_leaves and learning_rate for the final LightGBM model.
Validation: Performed cross-validation to ensure the model generalizes well to unseen content.

***Final Model Performance***
The final LightGBM model achieved an outstanding 92% Accuracy, making it a highly reliable tool for predicting Amazon Prime "Hits". With a 90% Precision and 91% Recall, the model effectively balances the need to avoid "flops" while successfully discovering high-quality content. This performance is summarized by a strong 90% F1-Score, ensuring the model generalizes well to new, unseen titles.
