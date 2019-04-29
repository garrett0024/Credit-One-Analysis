# Credit-One-Analysis
UAT Course 5 
Overview

I have been tasked with assisting Credit One in investigating why customers are defaulting their loans, and how to prevent it from happening as much in the future. Credit One has supplied us with information for 30,000 of their customers, the information consists of their age, education level, marriage status, credit limit, bill payment and bill amount over the past 6 months, if and how they paid their bill over the past 6 months, and if they defaulted or not. 

Findings

Based on my observations, I was able to find a relationship between the given credit limit and defaulting, customers with smaller credit limits default much more than customers with higher credit limits. This can lead to possibly checking customers with lower credit scores more thoroughly, to see if it is worth the risk to lend them credit. The figure below displays this relationship, as the orange represents defaulting and the blue represents not defaulting. 



Another observation to note would be the relationship between defaulting and if/how the customer paid their bill. The figures below show that the more their bill amount is, how much they pay is, and how they paid their bill, the less likely they are to default.
![bill   pay graph](https://user-images.githubusercontent.com/49155042/56920080-43646a80-6a90-11e9-8856-b6715e796a48.PNG)




Confidence

For building and evaluating models to create a prediction on future customers defaulting, I prepared and engineered the data to evaluate multiple models. I used two forms of the dataset, out-of-the-box, which is the data untouched, and recursive feature elimination, which removes attributes with low importance and is then fit to the remaining attributes. To be able to run classifiers on a dataset, the data must be split between a training set and a testing set. For this evaluation, I used a 75/25 split. Three algorithms were performed on these datasets, Random Forest, Support Vector Machines, and K-Nearest-Neighbor. To make the Support Vector Machines algorithms execute efficiently, the attributes were scaled down to values between 0 to 1.  

Random Forest creates numerous decision trees, and merges them together. Support Vector Machines is the idea of finding a hyperplane that best divides a dataset into two classes. Finally, K-Nearest-Neighbor is based on the closest training examples in the dataset. 

The best performing model was using the out-of-the-box dataset with the Random Forest classifier. It generated an accuracy of .8348, and it predicted 6751 would stay in good standing, and 749 would default on the 30% testing split. 27004 in good standing, 2996 defaulting, scaling to the full set.

Implications

Based on my observations and model evaluations, the recommended course of action would be to increase the requirements to be approved for credit. Credit One must take into consideration customers that have a hard time paying their bills and have a low credit limit. Yes, Credit One profits from customers accruing interest on their debt, but it has reached the point of harming Credit One from acquiring future business customers. Increasing the approval requirements should bring down the prediction of 10% of the customer base defaulting.
