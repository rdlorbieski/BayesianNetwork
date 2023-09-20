
# Loan Risk Modeling with Bayesian Network

A Bayesian Network provides a graphical representation of the probabilistic dependencies between a set of variables.
It is widely used in various domains, including finance, to model uncertainty and complex interrelationships among different factors.


# Project Objective

The primary goal of this project is to design a Bayesian network in Python to address the credit risk assessment of a loan. 
By employing this Bayesian Network, the credit risk associated with a loan can be determined using an inference algorithm, which considers the conditional values of the network's variables. For this project, specific observed variable values, such as monthly income and credit history, will be hardcoded.



# Dataset Creation
To evaluate the risk of a customer defaulting on a loan, we consider the following variables:
```
Monthly Income (R): The customer's monthly earnings.
Credit History (H): The customer's past credit payment record.
Employment (E): The current employment status of the customer (e.g., employed, unemployed).
Current Debt (D): The customer's total existing debts.
Loan Risk (Risk): Our target variable, which represents the default risk associated with the loan.
```

The interrelationships between these variables can be described as:

* **Monthly Income influences both Current Debt and Credit History.**
* **Credit History has a direct impact on Loan Risk.**
* **Employment affects both Monthly Income and Loan Risk.**
* **Current Debt influences Loan Risk.**

The conditional probabilities for each variable were formulated intuitively, without aiming to reflect real-world scenarios comprehensively. 
The main intent behind this formulation was for educational purposes.

The resulting Bayesian Network can be represented as an acyclic directed graph (DAG) with the nodes and edges representing the variables and their dependencies, respectively:

![Logo](https://rodolfo.lorbieski.eti.br/portfolio/bayesian_net.png)


For constructing the network, the pgmpy library was utilized. 
The culmination of the code showcases an example inference to evaluate loan risk. 
Specifically, the risk associated with granting credit to an individual with a favorable credit history but is currently unemployed is assessed.

	
## Setup
To run this project, be sure to install the pgmpy library first:
```
$ [sudo] pip install pgmpy

```

## Demonstration of Results in Netica
![Logo](https://rodolfo.lorbieski.eti.br/img/portfolio/projetos/final.gif)


## Autores

- [@rdlorbieski](https://github.com/rdlorbieski)
