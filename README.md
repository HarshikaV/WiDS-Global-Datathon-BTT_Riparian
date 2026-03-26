# WiDS-Global-Datathon-BTT_Riparian
This project focuses on building survival models for predicting whether a wildfire will threaten an evacuation zone within 12, 24, 48, and 72 hours, using only data from the first 5 hours after ignition. 

Our goal is to give emergency responders urgency rankings and reliable probability estimates to guide decisions regarding resource deployment, warnings, and evacuations.

Dataset
- Provided by WatchDuty and WiDS 
- Contents: Wildfire perimeter and early incident features
- Targets: Survival probabilities at multiple time horizons
  - prob_12h: probability of threat within 12 hours
  - prob_24h: probability of threat within 24 hours
  - prob_48h: probability of threat within 48 hours
  - prob_72h: probability of threat within 72 hours
- Notes:
  - Right-censored survival problem: some fires may not reach reach evacuation zones within 72hrs
  - Only data from the first 5 hours is used

## 👥 Team Members
| Name                       | GitHub Handle   | Contribution                                                                         |
| -------------------------- | --------------- | ------------------------------------------------------------------------------------ |
| **Harshika Vijayabharath**        | @HarshikaV | Developed and evaluated predictive models for 48h and 72h wildfire threat horizons, including hyperparameter tuning, monotonocity enforcement, and performance evaluation using ROC-AUC, log-loss, calibration curves, and Brier scores; currently contributing to survival model comparisons (Classification vs Cox vs RSF)|
| **Yamini Karthik**             | @Yamini1025 | Conducted exploratory data analysis, trained probabilistic models for 12h and 24h prediction, and evaluated model performance using ROC-AUC, log-loss, and calibration techniques; contributing to Random Survival Forest modeling |
| **Taanyaa Haridass Prasad**             | @taanyaaharidassprasad06 | Implemented data preprocessing and feature transformations (scaling, encoding, feature engineering), and developed evaluation metrics including weighted Brier score and hybrid scoring (C-index + Brier) |

## Current Progress
- Built baseline and advanced models for multi-horizon prediction (12h–72h)  
- Implemented feature transformations (scaling, log/sqrt, interactions)  
- Trained and evaluated models using ROC-AUC, log-loss, calibration curves, and Brier score  
- Enforced monotonicity across time horizons to ensure consistent probability behavior  
- Achieved strong initial results (Kaggle score: ~0.95+)  
- Currently comparing classification vs survival models (Cox, Random Survival Forest)
  
## Key Work
- Feature engineering from early wildfire incident data (first 5 hours)  
- Training probabilistic models across multiple time horizons (12h, 24h, 48h, 72h)  
- Hyperparameter tuning and model optimization (depth, splits, learning rate)  
- Calibration techniques (isotonic vs sigmoid) for reliable probability estimates  
- Evaluation using ROC-AUC, log-loss, calibration curves, and Brier score  
- Exploration of survival analysis models (Cox, Random Survival Forest)

## 📈 Results (So Far)
- Kaggle Public Score: 0.95356 → 0.95702  
- Improved model calibration and probability consistency across time horizons  
