# Cryptocurrencies

## Overview
Fictional investment bank, Accountability Accounting, is interested in offering a new cryptocurrency investment portfolio to its clients; however, the company needs assistance in determining which cryptocurrencies they should offer.  Senior management has requested a report that include what cryptocurrencies are on the trading market and if they could be grouped to create a classification system for this new investment.

The data from Accountability Accounting needed to be cleaned in order to fit the machine learning models, and since there isn't a known output for what this investment bank is looking for, unsupervised machine learning was employed.  In order to group the cryptocurrencies, a clustering algorithm was utilized and the data was visualized so the finding could be shared with the board.


## Resources
- [crypto_data.csv](https://github.com/acfthomson/Cryptocurrencies/tree/main/Resources)
- [hvPlot Documentation](https://hvplot.holoviz.org/)
- [scikit-learn StandardScaler Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
- [scikit-learn MinMaxScaler Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html#sklearn.preprocessing.MinMaxScaler.fit_transform)
- [scikit-learn PCA Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html?highlight=pca#sklearn.decomposition.PCA)
- [scikit-learn KMeans Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html?highlight=kmeans#sklearn.cluster.KMeans)


## Dependencies
- Jupyter Notebook
- Python v3.x
    - Pandas
    - hvPlot
    - Path
    - Plotly
    - SciKit-Learn


## Results
Once [crypto_data.csv](https://github.com/acfthomson/Cryptocurrencies/tree/main/Resources) was cleaned and preprocessed, there were 532 tradable cryptcurrencies.

An elbow curve was produced in order to find the best value for K.  This would be used to determine the number of clusters that should be used in the K-Means clustering algorithm.  According to the elbow curve, k=4

![elbow_curve](https://user-images.githubusercontent.com/73897240/113917367-2160e000-97af-11eb-873d-3165f48cdd22.png)


The unsupervised machine learning algorithm Principal Componenet Analysis (PCA) was used to reduce the dimensions of the cryptocurrency components to three principal components.  The following 3D scatter chart shows the cryptocurrency dataset in four clusters.

![3D_plot](https://user-images.githubusercontent.com/73897240/113918097-05aa0980-97b0-11eb-9c14-440e36792f9f.png)


The 2D scatter chart shows the each cryptocurrency from the dataset as it related to total coins mined and total coin supply.

![hvplot](https://user-images.githubusercontent.com/73897240/113918608-a4cf0100-97b0-11eb-9923-c2ea84186a18.png)
