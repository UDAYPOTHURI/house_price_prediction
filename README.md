# House Price Prediction

This repository contains a project to predict house prices using a neural network built with PyTorch. The dataset used is a common dataset for house price prediction and contains various features related to houses and their sale prices. The project involves preprocessing the data, encoding categorical variables, building a neural network, and training it to predict house prices.

## Project Structure

- `HousePricePrediction.ipynb`: Jupyter notebook containing the entire workflow from data loading to model training and evaluation.
- `HousePricePrediction.csv`: Dataset used for training and testing the model.
- `README.md`: Documentation for the project.

## Dataset

The dataset `HousePricePrediction.csv` contains the following columns:

- `Id`: To count the records.
- `MSSubClass`: Identifies the type of dwelling involved in the sale.
- `MSZoning`: Identifies the general zoning classification of the sale.
- `LotArea`: Lot size in square feet.
- `LotConfig`: Configuration of the lot.
- `BldgType`: Type of dwelling.
- `OverallCond`: Rates the overall condition of the house.
- `YearBuilt`: Original construction year.
- `YearRemodAdd`: Remodel date (same as construction date if no remodeling or additions).
- `Exterior1st`: Exterior covering on house.
- `BsmtFinSF2`: Type 2 finished square feet.
- `TotalBsmtSF`: Total square feet of basement area.
- `SalePrice`: The target variable to be predicted.

## Preprocessing

The preprocessing steps include:

1. Dropping the `Id` column as it is not needed for prediction.
2. Handling missing values by filling them with the mean for `SalePrice` and dropping rows with any other missing values.
3. Encoding categorical variables using `LabelEncoder`.

## Model

The neural network model is built using PyTorch and has the following structure:

- Input layer with 11 features
- Two hidden layers with 10 units each and ReLU activation
- Output layer with 1 unit for predicting the sale price

The model is trained using the L1 loss function and the SGD optimizer.

## Training

The training process involves:

1. Splitting the data into training and testing sets.
2. Training the model for 1000 epochs.
3. Recording the training and testing losses for each epoch.

## Evaluation

The model's performance is evaluated by plotting the training and testing losses over the epochs.

## Dependencies

- pandas
- numpy
- scikit-learn
- torch
- torchinfo
- matplotlib

## Results

The training and testing losses are plotted to show the model's performance over the epochs. The model can also be used to predict the sale price of a house given its features.

## Conclusion

This project demonstrates a basic approach to predicting house prices using a neural network in PyTorch. Further improvements can be made by tuning the model architecture, experimenting with different loss functions and optimizers, and using more advanced preprocessing techniques.
