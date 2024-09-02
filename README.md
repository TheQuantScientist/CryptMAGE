# Publication 

This project is under submission for presentation and publication in the Financial Innovation Journal (Q1-Top 5% Global Ranking), published on SpringerOpen as "[CryptMAGE: Vision Transformer for Intraday Cryptocurrency Time Series Price Movements Detection](https://lightning.ai/s3926339/studios/cryptmage-from-coins-to-images)". 

Train data can be found at: 
> https://drive.google.com/drive/folders/1tGVeAdG5HS4LJASb3UY-YysXC1GutXWI?usp=sharing

## Introduction 
In this project, the authors propose a novel approach to handling raw OHLCV cryptocurrency time series data. Instead of treating numerical sequences as mere numbers, each feature and indicator is converted into unique images, which are then fed into pre-trained Vision Transformer models for binary classification of upward or downward movement. To preserve valuable temporal dependencies inherent in crypto data, the time series are segmented into continuous 4-hour intervals. Additionally, due to the high correlation among OHLCV variables, feature engineering is employed to derive the Moving Average (MA) and Relative Strength Index (RSI) from closing prices. This ensures that the correlation between indicators remains below 50%, creating a more challenging environment for model performance. Results demonstrate that the base Swin Transformer consistently outperforms other baseline models from both image-based and traditional deep learning groups. This project aims to pioneer new research avenues in modern finance, enhancing pattern recognition capabilities for hourly crypto trading in the future.

## Features

- **Data Preprocessing**: Raw cryptocurrency price data is cleaned and normalized to ensure consistent and accurate input for the model before turning into 4-hour arbitrary images, subsequently generating 4500 images per dataset. 
- **Feature Engineering**: Custom features are generated to capture market trends and reduce dimensionality, resulting in a 60% reduction in feature correlation.
- **Model Training**: The vision model (ViT, Swin, DeiT, etc.) is trained using the engineered features, with hyperparameters optimized for optimal performance.
- **Evaluation**: The model is evaluated using standard metrics like Mean Absolute Error (MAE) and Root Mean Square Error (RMSE), showcasing its effectiveness in predicting market trends.

## Technologies Used

- **Python**: Primary programming language for developing the project.
- **Pandas**: For data manipulation and preprocessing tasks.
- **NumPy**: Utilized for numerical computations and data normalization.
- **Scikit-learn**: Employed for model training and evaluation.
- **Matplotlib**: Used for visualizing data correlations and model performance.
- **Hugging Face Transformers**: Used for pre-trained Vision Transformers during training processes.
- **Lightning AI**: Utlized for cloud environment, enabling the use of NVIDIA A10 Tensor Core GPU.

## Reproduce

- To reproduce the research, download the notebook file and run it from start to finish. The steps are organized sequentially, ensuring that the entire process—from data preprocessing to model evaluation—can easily be replicated. Modifications are needed only if users switch stock datasets. 
- NVIDIA A10 Tensor Core GPU is required for rendering.
- Visit [LightningAI Studio](https://lightning.ai/s3926339/studios/cryptmage-from-coins-to-images) for full access to graphical resources, training/testing data, and GPU. 
