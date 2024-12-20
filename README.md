# Neural Network-Based Financial Pricer  


## Key Idea  

Instead of directly predicting prices, the model decomposes the pricing process into two distinct stages:  

1. **Market Vectorization**:  
   A neural network transforms the given market data (e.g., interest rates, volatilities, spreads) into a compact, high-dimensional vector representation.  

2. **Derivative Vectorization**:  
   Another neural network processes derivative-specific information (e.g., payoff structure, maturity, underlying assets) to generate its vector representation.  

The product of these two vectors is designed to approximate the derivative's price.  

## Workflow  

1. **Data Preparation**:  
   Prepare market data and derivative data in the required format.  

2. **Training**:  
   The model optimizes the vectorization and pricing process by minimizing the MSE between predicted and observed prices.  

3. **Prediction**:  
   Given market data and derivative descriptions, the model computes vector representations and predicts prices as the product of these vectors.  


## Installation  

Clone the repository and install dependencies:  

```bash  
git clone https://github.com/v0r0bi0v/PricerMarketDotDerivative.git  
cd PricerMarketDotDerivative
pip install -r requirements.txt  