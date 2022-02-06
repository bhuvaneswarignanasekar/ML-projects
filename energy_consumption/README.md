# #Currently working on this project#

<h1> Energy Consumption Prediction <h1>

<h2> Problem statement</h2>

Find the optimal working days of the store with respect to the enerygy consumption of the store

<h2> Dataset </h2>

- This is a small dataset with the size of 889 rows
- The dataset contains three columns date, energy and enthalpy
- The dataset is divided into two train dataset and testing dataset.
- The dataset is not labeled

<h2> To Assume </h2>

- It is said to assume that every row in the training dataset is optimal

<h2> Extra information</h2>
- There is a relationship between energy and enthalpy

<h2> Experiments </h2>

<h3> Experiment 1 </h3>

- As the dataset is not labeled we can use unsupervised algorithms
  - reasons why can't use supervised
    - The training dataset is all labelled to be optimal, so unbalanced dataset
    - This dataset can't be balanced as there is no additional information about what is optimal and not
- Trained the model with energy and enthalpy
  
_ relation between energy and enthalphy:

  <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/E_E_relation.png" alt="relation">
  </a>
  </div>
  
- This didn't yield any good results

<h3> Experiment 2 </h3>

- As experiment 1 with just energy and enthalpy didn't yield any meaningful results
  - That's because the enerygy consumption differs depending on the weather/ month/ season
- Now, I experimented with feeding the model with month, energy and enthalpy
- Relation between month, energy and enthlapy:

  - 3D
  
    <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/3D_E_E_D_relation.png" alt="relation">
  </a>
  </div>
  
  - 2D
  
  <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/2D_E_E_M_relation.png" alt="relation">
  </a>
  </div>
  
- Can clearly see that optimal energy differs for every month.
- So clustered depending on month
- <h3> Result </h3>

  <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/prediction/all_together.png" alt="predict">
  </a>
  </div>
  
  - We still can see the result is not good
  
<h2> Experiment 3 </h2>

- I realized it's because I haven't scaled the variable
  - Energy ranges in 1000's
  - Enthalpy ranges in 10000's
  - month ranges in 1's
- Scaled the energy and Enthalpy
- <h3>Results </h3>

  <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/prediction/Scaled.png" alt="scaled">
  </a>
  </div>
  
  - we can see this result is way more better than the previous, so I realized I'm in a right direction
  
<h2> Experiment 4</h2>

- I realized again that the model learning from the overall data and not for each month
- hence clustered for a single month and saw that the clustering is better for each month

- <h3>Results</h3>

  - Cluster for single month
  
<div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/prediction/Single_month.png" alt="month">
  </a>
  </div>
  
  - Clustering in respective to each month
  
  <div align="center">
  <a href="https://github.com/bhuvaneswarignanasekar/ML-projects">
    <img src="energy_consumption/Images/prediction/per_month.png" alt="month">
  </a>
  </div>
  
  <h2> Upcoming</h2>
  <h3> Experiment 4</h3>
  
 - Planning to experiment with mixture of unsupervised and supervised 
 - Cluster it and feed it to supervised algorithm
 

