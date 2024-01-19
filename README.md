[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# [Quadratic Optimization Models for Balancing Preferential Access and Fairness: Formulations and Optimality Conditions](https://doi.org/10.1287/ijoc.2022.0308)

This archive is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](LICENSE).

The software and data in this repository are a snapshot of the software and data
that were used in the research reported on in the paper 
[Quadratic Optimization Models for Balancing Preferential Access and Fairness: Formulations and Optimality Conditions](https://doi.org/10.1287/ijoc.2022.0308) by Christian Schmitt and Bismark Singh. 

**Important: This code is being developed on an on-going basis at 
https://github.com/schmitt-hub/preferential_access_and_fairness_in_waste_management. Please go there if you would like to
get a more recent version or would like support**

## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/10.1287/ijoc.2022.0308

https://doi.org/10.1287/ijoc.2022.0308.cd

Below is the BibTex for citing this snapshot of the respoitory.

```
@article{CacheTest,
  author =        {C. Schmitt and B. Singh},
  publisher =     {INFORMS Journal on Computing},
  title =         {{Quadratic Optimization Models for Balancing Preferential Access and Fairness: Formulations and Optimality Conditions}},
  year =          {2023},
  doi =           {10.1287/ijoc.2022.0308},
  url =           {https://github.com/INFORMSJoC/2019.0000},
}  
```

## Description

This directory provides code used for the computations associated with the quadratic optimization models in the context of undesirable facility location problems for the abovementioned article.

`src` contains scripts for the optimization of the MIQP model and visualization of the results: model.py contains functions for building and optimizing the MIQP model, while greedy_heuristic.py applies a greedy heuristic to achieve a feasible solution. plotting.py and results.py contain functions tasked with visualizing results through various different plots as well as excel tables. They also contain superordinate functions that create the corresponding results first by running functions from model.py and/or greedy_heuristic.py before creating the corresponding visualization. These functions are called by functions in tables_and_figures.py to create the exact same figures and tables that are included in the paper from scratch. Lastly, utils.py contains helper and utility functions.

`catchment_population` presents an efficient algorithm to compute the "catchment population" of each recycling center that was used to estimate the capacities. An implementation of this algorithm is contained in catchment_population.py. Further, this directory contains two corresponding input data files in csv format: bavaria_grid_population.csv is a file containing the latitude and longitude of the centroid of each 100m x 100m grid in Bavaria as well as the residing population. rc_locations.csv contains the latitude and longitude of each recycling center in Bavaria.

`data` contains the two input data files that are used in the MIQP model: users_and_facilities.xlsx contains all ZIP codes and recycling centers related data like the population, centroid and regional spatial type (rural/urban) of each ZIP code as well as the capacity, centroid and regional spatial type of each recycling center. travel_dict.json.pbz2 is a compressed json file that contains the travel probabilities from each ZIP code to each recycling center.

`results` contains the excel tables and figures visualizing the results that are included in the paper.


## Requirements to run code

The code uses the following open-source Python packages. 

Pyomo, a Python-based optimization modeling language that allows building optimization models.
Gurobi, a software well-equiped for solving complex optimization models such as MIQPs.
Geopy, which was used for calculating geodesic distances (i.e. shortest distances on the surface of the earth) between two locations.

## Results

Results are provided here.



## Ongoing Development

This code is being developed on an on-going basis at the authors'
[Github site]([https://github.com/tkralphs/JoCTemplate](https://github.com/schmitt-hub/preferential_access_and_fairness_in_waste_management)).

## Support

For support in using this software, contact the authors.
