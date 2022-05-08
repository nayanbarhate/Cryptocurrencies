# Cryptocurrencies
Use unsupervised machine learning, PCA algorithm, and K-Means clustering to analyze and classify a database of cryptocurrencies.

## Analysis Overview
The purpose of this project is to use unsupervised machine learning to analyze a database of cryptocurrencies and create a report including the traded cryptocurrencies classified by group according to their features.\
This classification report could be used by an investment bank to propose a new cryptocurrency investment portfolio to its clients.\
We use the following methods for the analysis:
- preprocessing the database,
- reducing the data dimension using Principal Component Analysis,
- clustering cryptocurrencies using K-Means,
- visualizing classification results with 2D and 3D scatter plots.

## Resources
- Data Source: [crypto_data.csv](https://github.com/nayanbarhate/Cryptocurrencies/blob/main/Resources/crypto_data.csv), [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)
- Software: Python 3.7.7, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3

## Results
Following the preprocessing and cleaning phase we have a total of 532 tradable cryptocurrencies.

### Clustering Cryptocurrencies using K-Means - Elbow Curve
We don't know what would be the output of the analysis so we are using unsupervised machine learning to identify clusters of the cryptocurrencies.\
We produced the elbow curve below using the K-Means method iterating on k values from 1 to 10.

![ElbowCurve](https://github.com/nayanbarhate/Cryptocurrencies/blob/main/Resources/Elbow_Curve.png)

The best k value appears to be 4 so we would conclude on an output of 4 clusters to categorize the crytocurrencies.

### Visualizing Cryptocurrencies Results
#### 3D-Scatter plot with clusters

![3DScatterPlot](https://github.com/nayanbarhate/Cryptocurrencies/blob/main/Resources/3D_Scatter_Plot.png)

This 3-D scatter plot was obtained using the PCA algorithm to reduce the crytocurrencies dimensions to three principal components.

#### Tradable Cryptocurrencies Table

![TradableCryptocurrenciesTable](https://github.com/nayanbarhate/Cryptocurrencies/blob/main/Resources/Tradable_cryptocurrencies_table.png)

Most of the cryptocurrencies are part of class #0 and #3.<br>
The snapshot above shows that BitTorrent is the only cryptocurrency in class #2.

#### 2D-Scatter plot with TotalCoinMined vs TotalCoinSupply

![HvplotTotalCoinMinedvsTotalCoinSupply](https://github.com/nayanbarhate/Cryptocurrencies/blob/main/Resources/Hvplot_TotalCoinsMined_Vs_TotalCoinsSupply.png)

Plotting the scatter plot from two cryptocurrency features directly does not efficiently segregate the different classes. Then using the PCA algorithm is the right method for better visualizations.

## Summary
We have identified the classification of 532 cryptocurrencies based on similarities of their features.\
Particularities of each group need to be analyzed to determined their performance and potential interest for the investment bank's clients.

