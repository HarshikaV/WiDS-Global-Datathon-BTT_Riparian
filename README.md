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
| **Harshika Vijayabharath**        | @HarshikaV | |
| **Yamini Karthik**             | @Yamini1025 | |
| **Taanyaa Haridass Prasad**             | @taanyaaharidassprasad06 | |

Key Tasks
- Data cleaning, preprocessing, and feature engineering
- Exploratory data analysis
- Build survival models to predict wildfire threat probabilities
- Predict probability of threatening evacuation zones at 12h, 24h, 48h, and 72h
- Evaluate model performance using Hybrid Score (C-index + Weighted Brier Score)
