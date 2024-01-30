# Amazon Co-Purchasing Trend Analysis 

## General information 
***Objective: Carry out co-purchasing trend analysis of books from Amazon marketplace in 2006 by using graph networks.***

Among many other factors that define the exchange rate of USD/RUB, such as inflation rate, interest rate,, and government debt, we wanted to evaluate the extent to which the oil price affects the USD/RUB rate. 

## Methodology
***Step 1: DATA COLLECTION AND CLEANING*** 

The data was sourced from Stanford University’s SNAP program, where metadata on Amazon’s product co-purchasing network was collected as a text file. From this, the data was parsed using Python packages like regex and pandas to form the schemas described below:
Products <id, asin, title, group, salesrank>
Similarity <id, sim1, sim2, sim3, sim4, sim5>
Review <id, cus1, cus2, cus3, cus4, cus5>
where id - product id, asin - Amazon Standard Identification Number, title - name of the product, simn - the ASIN of similar product, cusn - customer id.

***Step 2: CO-PURCHASING INVESTIGATION***

A subset of the tuples from the original schemata was selected for the analysis. The out-degree of each node shows how many similar  products it has, and in-degree describes how many times a product was encountered as a product similar to another product. 

***Step 3:  GRAPH NETWORK ANALYSIS***

In order to create a social network depicting the co-purchase trends, all of the connected nodes to a specific node based on in-degree and out-degree of all involved nodes were collected. Their corresponding nodes and edges were then connected where the most-connected nodes appear larger in size and darker in color.


## Technologies 
* Jupyter Notebook
* Visual Studio Code

## Setup 
The following Python packages were used for this project: 

* pandas
* numpy
* networkx
* matplotlib
* pylab
* community
* re
* statsmodels
* statsmodels.formula.api
* statsmodels.genmod.families

## Features 
The following features were explored in this project:

* presence or absence of a product_id for a given prodcut_id

## Results 
From the graph networks and degree analyses, it was observed that a minority of nodes have very high degrees, making their resulting subgraph networks densely connected. Book titles with related themes create dense clusters, which predicts higher co-purchasing rate in the cluster of similar books. 
![Co-purchasing network.](https://github.com/juldyzmurat/Amazon_co_purchasing_graph/blob/main/nw577_sr5000_titles.png?raw=true)

## Status 
Project is: complete


## Contact 
* zxu4@case.edu
* ktn37@case.edu
* vsm21@case.edu
## Acknowledgements 
* Data was taken from Stanford Network Analysis Project
