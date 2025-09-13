****Explainable AI for Multi-modality Crop Yield Prediction****

This repository presents the research conducted for the Master of Information Technology (Artificial Intelligence and Data Science) thesis titled "Application of Explainable Machine Learning Methods in Predicting Crop Yield Using Multi-modality Datasets."

**Overview**

Modern machine learning models, especially deep learning, often operate as "black boxes," making their predictions difficult to understand. In critical sectors like agriculture, understanding why a crop yield prediction is made is crucial for building trust, enabling informed decision-making, and optimizing farming practices. This thesis explores the integration of Explainable Artificial Intelligence (XAI) with deep learning to address this challenge in crop yield prediction.

**Key Contributions**

*Multi-modality Data Integration*: Developed and evaluated models that integrate diverse data sources, including genomic (SNP markers), phenotypic (plant traits, experimental conditions), and environmental (rainfall, solar exposure, temperature) data, to achieve a comprehensive understanding of crop yield drivers.

*Novel Attention-based Hybrid Model*: Designed and implemented an Attention-based Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) hybrid model. This architecture leverages CNNs for spatial pattern extraction from genomic/phenotypic data and LSTMs for temporal dependencies in environmental data, with an attention mechanism to focus on the most relevant features across modalities.

*Enhanced Predictive Performance*: Demonstrated that the attention-based hybrid model achieved superior predictive accuracy and better generalization compared to baseline (Random Forest) and uni-modal CNN/LSTM models.

*Actionable XAI Insights*: 
Applied various XAI techniques (including DeepSHAP and attention weights) to interpret model decisions, revealing:
- *Dominant Role of Genetic Markers*: In the multi-modal model, genetic markers were identified as the most impactful features for yield prediction.

- *Critical Phenotypic and Environmental Factors*: Highlighted the significance of specific phenotypic traits ("Year," "Location") and early-season environmental conditions (e.g., April rainfall) in influencing crop outcomes.

*Transparency and Trust*: The research contributes to transforming opaque AI models into transparent tools, providing valuable, interpretable insights for farmers, agricultural managers, and plant breeders to optimize resource allocation, crop management strategies, and develop more resilient crop varieties.


**Methodology Highlights**

*Dataset*: Utilized a comprehensive barley dataset from the Western Barley Genotyping Alliance (WCGA) (2014-2016), encompassing detailed genomic, phenotypic, and environmental records.

*Model Architectures*
- *Baseline*: Random Forest Regressor (RFR) with hyperparameter tuning.

- *Uni-modal*: CNN for genomic data, LSTM for environmental data.

- *Hybrid*: Attention-based CNN-LSTM, fusing feature-level representations from all modalities.

*XAI Techniques*: Mean Decrease in Impurity (MDI) for RFR, DeepSHAP for CNN (genomic data), and Attention Weights for LSTM (environmental data) and the hybrid model.

*Evaluation Metrics*: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and Mean Squared Error (MSE).

**Impact**

This thesis aims to bridge the gap between advanced AI capabilities and practical agricultural needs, enabling more data-driven, informed, and trusted decisions to enhance crop productivity and food security.