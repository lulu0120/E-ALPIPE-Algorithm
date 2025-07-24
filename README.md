
# **E-ALPIPE-Algorithm**

This repository contains the code for algorithm implementation and data analysis for the paper “Efficient data collection for establishing practical identifiability”.

**Overview**

The code is written in R notebook format and can be run in RStudio. It demonstrates how to efficiently establish practical identifiability through active learning in our 3 case study models, as discussed in the associated research paper *“Efficient data collection for establishing practical identifiability”*.

**Requirements**

	•	RStudio  

**Getting Started**

	Download and open the R notebook files in RStudio.
	You can control the number of replications and iterations by modifying the parameters in the last row of both files.
	Example: trials(Replication, Iteration, Time length)
	Replication: Number of replications to run
	Iteration: Number of iterations per replication
	Time length: Range for the time axis is (0, Time length)

**Output Explaination**

Calling A = trials(Replication, Iteration, Time length) returns an object A, which contains multiple result components.

	Each replication result can be accessed using A[[i]][[j]], where:
	•	i refers to the type of result (from 1 to 5, as listed below).
	•	j refers to the specific replication number.

The outputs for i follow the order below:

	1.	estimated_params: The estimated model parameters (Maximum Likelihood Estimator) based on collected data.
	2.	observations: The data collected by the algorithm.
	3.	obs_locations_df: A data frame indicating the locations (time) of collected observations.
	4.	pl_check: A validation check for practical identifiability using profile likelihood.
	5.	bounds: The profile likelihood confidence intervals based on existing data; for non-identifiable parameter NA is shown.

