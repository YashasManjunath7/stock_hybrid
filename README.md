# Stock Prediction Using Machine Learning

## Project Overview
This project investigates machine learning approaches to predict stock prices, comparing traditional statistical methods with advanced neural network models. The study focuses on evaluating the strengths and weaknesses of each method, ultimately proposing an integrated model for improved prediction.

---

## Objectives
1. **Evaluate Statistical Models**:
   - Assess traditional approaches such as ARIMA and ARIMA+GARCH for forecasting stock prices.
2. **Explore Machine Learning Models**:
   - Analyze the effectiveness of advanced techniques, including Long Short-Term Memory (LSTM), Convolutional Neural Networks (CNN), and hybrid models.
3. **Address Challenges**:
   - Investigate data complexities, overfitting, and the unpredictability of stock market movements.
4. **Propose an Integrated Model**:
   - Develop a hybrid architecture combining the strengths of statistical and neural network models.

---

## Methodology
### Data Collection
- **Sources**: Historical stock data from Yahoo Finance and APIs like Alpha Vantage.
- **Features**: Closing price, 25-day moving average, 100-day moving average.
- **Data Splitting**: Sequential data was split into training (2001-2019) and testing periods (2020-2022).

### Models Tested
1. **Traditional Statistical Models**:
   - ARIMA: Focused on trends and seasonality but required transformations for stationarity.
   - ARIMA+GARCH: Added volatility modeling but struggled with complex, non-linear data.
2. **Deep Learning Models**:
   - LSTM: Captured long-term dependencies but showed limitations in volatile markets.
   - CNN: Extracted local patterns effectively, performing better when combined with sequence models.
3. **Hybrid Models**:
   - CNN-GRU: Combined convolutional feature extraction with GRU’s sequential processing.
   - LSTM-CNN-GRU: Integrated strengths of LSTM, CNN, and GRU but faced challenges with generalization in volatile conditions.

### Hyperparameter Optimization
- **Techniques Used**:
   - Random Search for exploring diverse configurations.
   - Bayesian Optimization for reducing computational overhead while refining model performance.

### Evaluation Metrics
- **Error Metrics**: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE).
- **Performance Metrics**: R² score to assess explained variance.

---

## Key Findings
### Model Performance
#### ARIMA & ARIMA+GARCH
- **Strengths**:
   - Effective for linear trends and volatility clustering.
- **Weaknesses**:
   - Required stationary data and struggled with non-linear complexities.

#### Deep Learning Models
- **LSTM**:
   - Captured sequential dependencies effectively.
   - Poor generalization in volatile market conditions.
- **CNN**:
   - Extracted local patterns but needed sequential modeling for better performance.

#### Hybrid Models
- **LSTM-CNN and CNN-GRU**:
   - Performed well in stable markets, combining feature extraction and sequence modeling.
   - Required extensive hyperparameter tuning.
- **LSTM-CNN-GRU**:
   - Mixed results; failed to adapt to high volatility, showing large prediction errors.

### Challenges
1. **Overfitting**:
   - Complex models captured noise, leading to poor generalization.
2. **Interpretability**:
   - Neural networks lacked transparency, complicating decision-making.
3. **Data Complexity**:
   - High volatility and market randomness posed significant prediction hurdles.

---

## Conclusions
- **Deep Learning Superiority**:
   - Neural network models outperformed traditional techniques in handling non-linear trends.
- **Hybrid Models’ Potential**:
   - CNN-LSTM and CNN-GRU demonstrated significant promise but require enhancements in handling market volatility.
- **Future Directions**:
   - Incorporate alternative data sources like sentiment analysis and macroeconomic indicators.
   - Develop explainable AI (XAI) models for improved transparency.
   - Explore reinforcement learning to optimize trading strategies.

---

## Recommendations for Future Research
1. **Explainable AI (XAI)**:
   - Enhance model interpretability to improve usability in financial applications.
2. **Integration of Alternative Data**:
   - Leverage social media sentiment, news articles, and macroeconomic trends.
3. **Advanced Architectures**:
   - Experiment with attention mechanisms and transformer-based models for better handling of volatile markets.
4. **Reinforcement Learning**:
   - Utilize deep reinforcement learning for automated trading and portfolio management.

---

## Acknowledgements
Special thanks to Dr. Konstantinos Skindilias for guidance and support throughout this research. Gratitude also goes to peers and family for their encouragement.

---

## References
- Box, G.E.P., Jenkins, G.M., and Reinsel, G.C. (2015). *Time Series Analysis: Forecasting and Control*.
- Fischer, T., and Krauss, C. (2018). Deep learning with LSTM networks for financial market predictions.
- Bao, W., Yue, J., and Rao, Y. (2017). A deep learning framework for financial time series using CNN-LSTM models.

(*Additional references available upon request.*)

