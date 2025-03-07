# Understanding the in-situ Solar Wind Properties through Machine Learning

## Description

The aim of this project is to use machine learning to characterize properties of the solar wind. Using a machine learning approach to characterize solar wind can help researches in heliophysics learn more about this data.  Due to high pressure and temperatures of the Sun's atmosphere, partially ionized gas is expelled from the Sun.  This creates a plasma flow throughout the entire Solar System.  The Solar Orbiter can take measurements of the properties of the solar wind.  These measurements include elemental abundance/charge state ratios, average charge state, velocity, and density.  Events on the Sun, known as Coronal Mass Ejection Events, eject lots of energy that is spread throughout the Solar System.  These ejections can disrupt systems on Earth, such as electronic and communication systems. Data from the Solar Orbiter can help in prepare Earth for when these events occur.  In this project, we are using unsupervised learning techniques, such as dimension reduction and clustering, to help researchers eventually automatically detect these events on the Sun.  

## Features

- **O7_O6_ratio**: This ratio indicates the loss of 7 electrons (+7) and 6 electrons (+6) by the oxygen atom. The ratio is always non-negative, and any negative value suggests data errors that need to be eliminated.
- **C6_C4_ratio**: This is the ratio of carbon atoms losing 6 electrons (+6) to those losing 4 electrons (+4). Similar to the oxygen ratio, negative values are considered invalid and excluded from the dataset.
- **C6_C5_ratio**: This measures the ratio of a carbon atom losing 6 electrons (+6) to one losing 5 electrons (+5). Any negative value is treated as an error and removed.
- **Fe_O_ratio**: This represents the ratio of iron to oxygen atoms in solar wind. A negative value for this ratio has no physical significance and is therefore excluded.
- **O_ave_charge**: The average charge of oxygen atoms in solar wind cannot exceed eight, given their potential loss of up to eight electrons. Any higher value will be removed from the dataset.
- **Velocity**: Particle velocity in solar wind typically ranges within a few hundred kilometers per second. Significantly higher or lower values are considered outliers and are removed.
- **Density**: Solar wind particle density is expected to range between 0 and several hundred particles per cubic centimeter. Negative density values are not possible and will be removed.
- **Mass_flow_rate**: It is calculated as the product of density and velocity.

## Execution

1.  Run the _cleaning.ipynb_ notebook to clean the original dataset (removes values that are too large or small and removes missing values)
2.  Run the _pca_clustering_Kmeans_dbscan.ipynb_ followed by _pca_clustering_hdbscan.ipynb_ notebook to get the results of the PCA dimension reduction and then clustering based off of PCA
3.  Run the _umap_clustering.ipynb_ notebook to get the results of the UMAP dimension reductions and then clustering based off of UMAP
4.  Run the _SIADS 699 Isolation Forest and LSTM forecast.ipynb_ notebook to get the results of the isolation forest and the LSTM forecast


## Data Access Statement

The data required for this project is a combination of publicly available datasets and proprietary datasets created by the project lead. The publicly available datasets include:

- ACE Mission data: Available for download from the ACE Science Center website (https://www.srl.caltech.edu/ACE/)
- Solar Orbiter Mission data: Available for download from the Solar Orbiter Science Archive (https://soar.esac.esa.int/soar/)
- Sunspot Number data: Available for download from the World Data Center for the Production, Preservation and Dissemination of the International Sunspot Number (https://wwwbis.sidc.be/silso/datafiles)

The proprietary Heliospheric Current Sheet (HCS) Index dataset is owned by the project lead, Dr. Liang Zhao from the University of Michigan Climate and Space Sciences and Engineering department. Students will be provided access to this dataset upon signing a non-disclosure agreement (NDA) with the University of Michigan.

All data usage and redistribution must comply with the licensing terms of the respective datasets. The publicly available datasets typically have open data policies, while the proprietary HCS Index dataset is subject to the University of Michigan's NDA terms.
