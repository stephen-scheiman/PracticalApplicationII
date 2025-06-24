# Practical Application II
Repo for my practical application II submission

# What drives the price of a car?

![](images/kurt.jpeg)

**OVERVIEW**

In this application, you will explore a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing.  Your goal is to understand what factors make a car more or less expensive.  As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.

### CRISP-DM Framework

<center>
    <img src = images/crisp.png width = 50%/>
</center>


To frame the task, throughout our practical applications, we will refer back to a standard process in industry for data projects called CRISP-DM.  This process provides a framework for working through a data problem.  Your first step in this application will be to read through a brief overview of CRISP-DM [here](https://mo-pcco.s3.us-east-1.amazonaws.com/BH-PCMLAI/module_11/readings_starter.zip).  After reading the overview, answer the questions below.

### Business Understanding

From a business perspective, we are tasked with identifying key drivers for used car prices.  In the CRISP-DM overview, we are asked to convert this business framing to a data problem definition.  Using a few sentences, reframe the task as a data task with the appropriate technical vocabulary. 

This task can be reframed as a supervised regression problem where the target variable is the used car price and the predictor variables include features such as age, mileage, condition, make, and model. The objective is to perform feature selection and engineering, followed by exploratory data analysis and statistical testing, to determine the key explanatory variables that drive price variance. Ultimately, the goal is to build an interpretable predictive model using techniques like linear regression that quantify the impact of each feature on pricing.

### Data Understanding

After considering the business understanding, we want to get familiar with our data.  Write down some steps that you would take to get to know the dataset and identify any quality issues within.  Take time to get to know the dataset and explore what information it contains and how this could be used to inform your business understanding.

Load and Inspect the Data

Generate Summary Statistics

Visualize Data Distributions

Assess Missing Data

Check for Duplicates and Inconsistencies

Validate Data Ranges and Domain Constraints

Explore Relationships Among Variables

Document Initial Findings

## Initial Findings

There is almost no direct correlation between any original numeric features and price. The highest correlation between numeric features is price and odometer.

Ford is the most popular brand while Tesla is the most expensive. The largest percentage of vehicles sold are the sedan type while pickup trucks have the highest average selling price.

### Evaluation

With some modeling accomplished, we aim to reflect on what we identify as a high-quality model and what we are able to learn from this.  We should review our business objective and explore how well we can provide meaningful insight into drivers of used car prices.  Your goal now is to distill your findings and determine whether the earlier phases need revisitation and adjustment or if you have information of value to bring back to your client.

While I was able to develop several models that performed better than baseline, none that I came up with allowed me to make specific, reliable price predictions. I'm unsure as to whether this is due to my cleaning and prep, the transformations and normalizations or incorrect model selection.

I would have thought that the numeric categories would have provided a decent model but it was only after transforming categorical columns for inclusion that I began to see MSE improvements. Particularly frustrating was the fact that I had a good model working very early on in process with an MSE of less than 1 for both train and test but I lost it with iteration, and have been unable to reproduce. I will go back and iterate on which columns I select for inclusion and see if it helps, time permitting.

That said, there are some common sense measures that I've been able to derive from the dataset that will allow for some high-level inferences that address the business objective of advising used car dealers as to what inventory they should stock, enumerated below.