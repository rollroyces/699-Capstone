# Understanding the in-situ Solar Wind Properties through Machine Learning

## Description

## Features

- **O7_O6_ratio**: This ratio indicates the loss of 7 electrons (+7) and 6 electrons (+6) by the oxygen atom. The ratio is always non-negative, and any negative value suggests data errors that need to be eliminated.
- **C6_C4_ratio**: This is the ratio of carbon atoms losing 6 electrons (+6) to those losing 4 electrons (+4). Similar to the oxygen ratio, negative values are considered invalid and excluded from the dataset.
- **C6_C5_ratio**: This measures the ratio of a carbon atom losing 6 electrons (+6) to one losing 5 electrons (+5). Any negative value is treated as an error and removed.
- **Fe_O_ratio**: This represents the ratio of iron to oxygen atoms in solar wind. A negative value for this ratio has no physical significance and is therefore excluded.
- **O_ave_charge**: The average charge of oxygen atoms in solar wind cannot exceed eight, given their potential loss of up to eight electrons. Any higher value will be removed from the dataset.
- **Velocity**: Particle velocity in solar wind typically ranges within a few hundred kilometers per second. Significantly higher or lower values are considered outliers and are removed.
- **Density**: Solar wind particle density is expected to range between 0 and several hundred particles per cubic centimeter. Negative density values are not possible and will be removed.
- **Mass_flow_rate**: It is calculated as the product of density and velocity.


## Files

## Execution
