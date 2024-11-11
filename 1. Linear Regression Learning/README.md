# 🍕 Linear Regression Model for Pizza Price Prediction 🍕

<p align="center">
  A machine learning-based linear regression model that predicts pizza prices based on size! 📊✨ The model uses data collected in a CSV file and applies statistical methods such as mean, deviation, and regression formula to estimate the price.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue" />
  <img src="https://img.shields.io/badge/Pandas-1.3.3-yellowgreen" />
  <img src="https://img.shields.io/badge/NumPy-1.21-lightblue" />
  <img src="https://img.shields.io/badge/Matplotlib-3.x-orange" />
</p>

---

## Requirements

- **Python 3.x**
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`

You can install the required libraries using pip:

```bash
pip install numpy pandas matplotlib
```

## Data Collection

The data for training the linear regression model is stored in a CSV file (`train_data.csv`). The dataset contains two columns:

- `Diameters (in Inches)` - The size of the pizza in inches.
- `Price (In Tk)` - The price of the pizza in Bangladeshi Taka.

## Steps

### 1. Import Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

### 2. Load the Training Data

The data is loaded from the CSV file into a pandas DataFrame.

```python
dataset = pd.read_csv('./train_data.csv')
dataset.head()
```

### 3. Plot the Data

A scatter plot is used to visualize the relationship between pizza size (diameter) and price.

```python
plt.scatter(dataset['Diameters (in Inches)'], dataset['Price (In Tk)'])
```

### 4. Calculate Mean of X and Y

We calculate the means of `Diameters (in Inches)` and `Price (In Tk)`.

```python
x = dataset['Diameters (in Inches)']
y = dataset['Price (In Tk)']
x_mean = x.mean()
y_mean = y.mean()

print(f'X Mean: {x_mean}')
print(f'Y Mean: {y_mean}')
```

### 5. Calculate the Deviations from the Mean

For each data point, we calculate the deviation from the mean.

```python
x_deviation = x - x_mean
y_deviation = y - y_mean
```

### 6. Calculate the Sum of Product of Deviations

The sum of the product of deviations is used to calculate the slope (m) of the linear regression line.

```python
sum_of_products = (x_deviation * y_deviation).sum()
print(f'Sum of the Product of Deviations: {sum_of_products}')
```

### 7. Calculate the Squared Deviation

We square the deviations of the `Diameters (in Inches)` values to calculate the sum of squared deviations for X.

```python
x_squared_deviation = x_deviation ** 2
sum_of_squared_deviations = x_squared_deviation.sum()
print(f'Sum of Squared Deviations: {sum_of_squared_deviations}')
```

### 8. Calculate the Slope (m) and Constant (c)

Using the formula for linear regression:

- \( Y = mX + c \)

Where:
- \( m \) is the slope
- \( c \) is the constant (intercept)

The slope `m` is calculated as:

The formula for the slope is: $m = \frac{\sum{(X_i - \mu_X)(Y_i - \mu_Y)}}{\sum{(X_i - \mu_X)^2}}$


```python
m = sum_of_products / sum_of_squared_deviations
print(f'Slope: {m}')
```

The constant `c` is calculated using the formula:
$m = \frac{\sum{(X_i - \mu_X)(Y_i - \mu_Y)}}{\sum{(X_i - \mu_X)^2}}$

\[ 
c = \mu_Y - (m \times \mu_X)
\]

```python
c = y_mean - (m * x_mean)
print(f'Constant: {c}')
```

### 9. Predict the Price for a Given Pizza Size

Once we have the slope and constant, we can predict the price for a new pizza size using the formula:

\[
\text{Price} = m \times \text{Size} + c
\]

```python
new_pizza_size = float(input('Enter the pizza size: '))
price = m * new_pizza_size + c
print(f'Price: {price}')
```

### 10. Apply Rounding Based on Decimal Part

If the decimal part of the calculated price is less than 0.5, we round it down; otherwise, we round it up.

```python
if price % 1 >= 0.5:
    round_price = int(price) + 1
else:
    round_price = int(price)
print(f'Rounded Price: {round_price}')
```

### 11. Final Output

The final rounded price is printed after applying the rounding logic based on the decimal value of the predicted price.

---

## Example Run

If the user enters a pizza size of `14`, the program will output the estimated price for that size, applying rounding as needed.

```bash
Enter the pizza size: 14
Price: 2099
```

If the pizza size entered is a decimal (e.g., `14.7`), the price will be rounded accordingly:

```bash
Enter the pizza size: 14.7
Price: 2253
```

---

## Conclusion

This project demonstrates how to build a simple linear regression model using Python, pandas, and matplotlib to predict the price of a pizza based on its size. The steps include data loading, plotting, calculating statistical measures, fitting a regression line, and making predictions.

---

## 📂 Directory Structure

```
Linear-Regression-Pizza-Price-Prediction/
│
├── train_data.csv           # The pizza size and price dataset
├── Linear-Regression-Pizza-Price-Prediction.ipynb # Jupyter notebook for prediction
└── README.md                # Documentation
```

---

## License

This project is open-source and available under the [MIT License](LICENSE)