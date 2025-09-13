# Explainable AI for Multi-modality Crop Yield Prediction

This repository provides a summary of the Master of Information Technology (Artificial Intelligence and Data Science) thesis titled "Application of Explainable Machine Learning Methods in Predicting Crop Yield Using Multi-modality Datasets."

## Overview

Traditional machine learning and deep learning models, especially in complex domains like agriculture, often act as "black boxes," making their decision-making processes opaque. This lack of transparency hinders trust and limits the ability of stakeholders (farmers, researchers, policymakers) to understand and act upon predictions.

This thesis addresses this challenge by exploring the integration of Explainable Artificial Intelligence (XAI) methods with deep learning to predict crop yield. The goal is not only to achieve accurate predictions but also to provide clear, interpretable insights into the underlying factors driving these predictions, particularly when leveraging diverse data types.

## Key Contributions

*   **Multi-modality Data Integration:** The research successfully developed and evaluated models capable of integrating heterogeneous data sources, including:
    *   **Genomic Data:** SNP markers for genetic insights.
    *   **Phenotypic Data:** Physical attributes and physiological features of barley plants.
    *   **Environmental Data:** Time-series weather parameters like rainfall, solar exposure, and temperature.
    This comprehensive integration allows for a more nuanced understanding of complex crop yield dynamics.

*   **Novel Attention-based Hybrid Model:** A key innovation is the design and implementation of an Attention-based Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) hybrid model.
    *   **CNNs** were utilized to capture spatial dependencies and intricate patterns within genomic and phenotypic data.
    *   **LSTMs** were employed to model temporal dependencies in environmental time-series data.
    *   An **attention mechanism** was integrated to allow the model to dynamically focus on and weigh the most relevant features across all modalities, enhancing both predictive performance and interpretability.

*   **Enhanced Predictive Performance:** The attention-based hybrid model demonstrated superior predictive accuracy (lower RMSE, MAE) and better generalization capabilities compared to a baseline Random Forest Regressor and individual uni-modal CNN/LSTM models.

*   **Actionable XAI Insights:** Various XAI techniques (Mean Decrease in Impurity for Random Forest, DeepSHAP for CNN, and attention weights for LSTM/Hybrid models) were applied to interpret model outputs, yielding practical insights:
    *   **Genetic Dominance:** Genetic markers were identified as the most significant predictors in the multi-modal context, with specific markers showing very high attention weights.
    *   **Phenotypic Influence:** Features like "Year" and "Location" from phenotypic data were crucial, indicating the importance of time-related and geographical environmental factors.
    *   **Critical Environmental Timestamps:** Early-season rainfall (e.g., April) was highlighted as a critical environmental factor influencing initial crop growth and overall yield, providing valuable temporal insights.

*   **Promoting Transparency and Trust:** By transforming opaque AI predictions into understandable explanations, this thesis empowers farmers and agricultural managers to make more informed decisions regarding crop management, resource allocation, and breeding strategies, ultimately contributing to more resilient and productive agriculture.

## Methodology Highlights

*   **Dataset:** Barley accession data from the Western Barley Genotyping Alliance (WCGA), spanning 2014-2016. The dataset included 30,543 high-quality SNP markers, 17 phenotypic features across 12,421 observations, and monthly environmental data.
*   **Data Pre-processing:** Involved imputation of missing values, one-hot encoding for genomic SNP data, and conversion of categorical variables using label encoding. Environmental data was aggregated to monthly averages relevant to the crop growth cycle.
*   **Model Architectures:**
    *   **Baseline:** Random Forest Regressor (RFR) with hyperparameter tuning via Optuna.
    *   **Uni-modal Models:** Separate CNN for gene data (DeepSHAP for explanation) and Attention-based LSTM for environmental data (attention weights for explanation).
    *   **Multi-modal Hybrid Model:** Attention-based CNN and LSTM with feature-level early fusion, explained using attention weights.
*   **Evaluation Metrics:** Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and Mean Squared Error (MSE).

## Impact

This thesis aims to bridge the gap between advanced AI capabilities and practical agricultural needs, enabling more data-driven, informed, and trusted decisions to enhance crop productivity and foster greater confidence in AI-driven agricultural solutions.

## Thesis Information

*   **Author:** Jigme Dorji 
*   **Degree:** Master of Information Technology (Artificial Intelligence and Data Science)
*   **University:** Murdoch University
*   **Submission Date:** November 2024
*   **Supervisor:** Dr. Guanjin Wang