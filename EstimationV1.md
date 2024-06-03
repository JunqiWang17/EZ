# Project Estimation - CURRENT
Date: 30/04/2024

Version: V1


# Estimation approach
Consider the EZElectronics  project in CURRENT version (as given by the teachers), assume that you are going to develop the project INDEPENDENT of the deadlines of the course, and from scratch
# Estimate by size
### 
|             | Estimate                        |             
| ----------- | ------------------------------- |  
| NC =  Estimated number of classes to be developed   |20|             
|  A = Estimated average size per class, in LOC       |250| 
| S = Estimated size of project, in LOC (= NC * A) |5000|
| E = Estimated effort, in person hours (here use productivity 10 LOC per person hour)  |500|   
| C = Estimated cost, in euro (here use 1 person hour cost = 30 euro) |15 000| 
| Estimated calendar time, in calendar weeks (Assume team of 4 people, 8 hours per day, 5 days per week ) |3-4|               

# Estimate by product decomposition
### 
|         component name    | Estimated effort (person hours)   |             
| ----------- | ------------------------------- | 
|requirement document    |12|
| GUI prototype |8|
|design document |4|
|code|570|
| unit tests |40|
| api tests |70|
| management documents  |3|



# Estimate by activity decomposition
### 
|         Activity name    | Estimated effort (person hours)   |             
| ----------- | ------------------------------- | 
|**Group Management**||
|Planning PM|2|
|Scheduling|2|
|Estimation of risk|3|
|**Requirements**||
|Doing a state of the art|10|
|Identify users requirement|7|
|Identify performance requirements|3|
|**Design**||
|Identify and develop the prototype design|2|
|GUI prototype|8|
|**Coding**||
|Back-end Coding|300|
|Front-end Coding|220|
|Merging both sides|50|
|**Testing**||
|API testing|70|
|Unit testing|40|
|Correcting potential errors|50|
|Check performance|10|
###
We obtain the following GANTT chart:  
![GANTT chart V1](/uploads/8edbdfc3453ef91e2bd940a46bdec093/GANTTV1.PNG)

  

# Summary


|             | Estimated effort (person hours)      |   Estimated duration (days) |          
| ----------- | ------------------------------- | ---------------|
| estimate by size |500| 16|
| estimate by product decomposition |707| 23 |
| estimate by activity decomposition |777|25|

The three estimation made have different results, which is totally normal considered that the approaches were completely different.  
In the estimation by size, we only have an average approache and we only look at the project by the prism of LOC, without considering the testing, requirements and project management parts.  
For the two other approaches, the difference comes from the fact that the estimation by activity decomposition is more detailled in general that the estimation by product decomposition.