https://www.kaggle.com/c/home-credit-default-risk/

This repository contains my python code for Kaggle's most challenging competition so far(09/01/18) with about 7200 teams conducted by Home Credit to predict Default Risks. It helped me secure top 1% (69th position)  and can secure 31st place in private leaderboard (0.80054) with a minor tweak in my final submission.

Approach:

Step 1: Basic Exploratory Data Analysis

Step 2: Build LightGBM models with different feature set(using PCA, null importance feature selection, feature engineering, 
        SHAP etc.) with appropriate parameters tuned by Bayesian Optimization and collected Out of Fold predictions.
        Single model max CV - 0.7979 | max public LB - 0.802
        
Step 3: Weighted Average / Blend of submission files that helped me to reach .805 in public LB

Step 4: Ensemble Voting of OOF predictions (4 files) - CV - 0.80021 | public LB - 0.802

Step 5: Rank Averaging of LB topper (blending) obtained from step 3, Submission file from Voting, LightGBM model with no               External Sources features(Credit scores reported by external agencies) and public kernel submission by GP method
        public LB - 0.80594 | private LB - 0.79930
        
Step 6: After deadline - Removing public kernel submission by GP method would have helped me to secure 31st position.
        public LB - 0.8068 | private LB - 0.80054
        
        
Cheers!

-Harish
