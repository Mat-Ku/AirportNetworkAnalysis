
# Airport Network Analysis

An analysis of airport locations and airline routes.


## Description
In this project, airport and airline data is thoroughly investigated in order to compare the interconnectivity of developed countries in contrast to developing countries. The airport network is therefore inspected in terms of popular graph theory figures, such as degree centrality, betweenness centrality and k-cores. Beyond this, potentially isolated airport clusters are identified. The results are presented in such a way that airports located in developed countries can be distinguished from airports in developing countries, thereby allowing an inference on the differences in terms of interconnectivity of both regions.
## Data
Airports: https://www.kaggle.com/datasets/moonnectar/airline-routes-92k-and-airports-10k-dataset?select=Full_Merge_of_All_Unique+Airports.csv

Airline routes: https://www.kaggle.com/datasets/moonnectar/airline-routes-92k-and-airports-10k-dataset?select=Full_Merge_of_All_Unique_Routes.csv

The file 'exploration_and_preprocessing.ipynb' reads in both datasets, conducts certain preprocessing steps and creates an altered Airports dataset in the end. The Airline routes dataset remains unchanged. 
This altered dataset, as well as the Airline routes dataset are then used in 'network_analysis.ipynb' for conducting the analysis and gathering the results.
## Assessment Methods
Degree centrality: Number of routes connected to an airport.

Betweenness centrality: Number of locations connected through an airport.

K-Cores: Subgraphs containing only vertices adjacent to at least k other vertices.
## Package Versions
python---3.7.6
numpy---1.21.6
matplotlib---3.1.3
pandas---1.0.1
networkx---2.4
geopy---2.2.0
## Results
Results are plotted in 'network_analysis.ipynb'.

Among the 20 highest-scoring airport locations in terms of degree centrality, only 7 are located in developing countries.

Among the 20 highest-scoring airport locations in terms of betweenness centrality, only 8 are located in developing countries.

The network contains six clusters. One cluster can be considered the main cluster as it contains more than 99% of airports. The five remaining clusters, which neither have any connection to the main cluster nor any connection between each other, are composed of small airports on the US Virgin Islands, in Alaska, Nevada and New Caledonia. However, a quick research revealed that, in reality, they do have connections to the main cluster, but data seems to be missing in the applied datasets.

With respect to the k-Core statistics, k=20, 30 and 40 were inspected. While the 20-Core scenario is almost equally split between developed (53%) and developing locations (47%), the ratio is changing in favor of airports located in developed countries for k=30 (57% to 43%) and k=40 (84% to 16%). This proves that developing countries tend to have a significantly denser airport interconnectivity. 
## Copyright Notice
No license is offered. Copyrights belong to the owner of this repository. The software provider does not represent or warrant that it has any rights whatsoever in the data used. Neither the software provider, nor any upstream software or data provider shall have any liability for any direct, indirect, incidental, special, exemplary, or consequential damages (including without limitation lost profits), however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the software, the data used or the produced results, even if advised of the possibility of such damages.
