### Predicting Replication: Assessing the Quality of Empirical Research Results

**Joshua Beattie**

#### Executive summary

The goal of this project is to improve the informational quality of empirical research by predicting the results of (hypothetical) replications. Providing a more fine-tuned assessment of the dependability of research results allows for more accurate conclusions regarding the scale of purported effects or patterns. There is currently relatively little replication data available, but the predictive model developed here improved upon a simple, but already quite helpful heuristic by ~11%. 

#### Rationale
Replication, i.e. repeating a study that has already been carried out, is a crucial part of the scientific process. It aids in separating genuine effects from statistical artifacts and in determining how large the genuine effects actually are. In recent years, it has become clear that due to various factors (publication and grant-making practices, conventional statistical methodologies, etc.), published research is less dependable - less replicable - than might be hoped. This is often referred to as a "replication crisis". Countless important decisions - in science and technology, in public policy, in business, etc. - are informed by empirical research results, so anything that can improve the informational quality of those results will be highly beneficial. Here, the focus is on gaining an improved *interpretation* or *assessment* of the available empirical research.   

#### Research Question
Given the statistical and methodological features of a particular empirical research result, along with historical information about actually performed replications, can we predict what the total evidence would look like if a replication were to be carried out? Put another way, how ought we to adjust or calibrate our assessments of published results, in light of all the information we have available to us?     

#### Data Sources
One response to the replication crisis has been the organization of several "replication projects", in which resources are devoted to replicating a collection of studies in a given field. These have so far been carried out for research in psychology, experimental economics, social sciences, and experimental philosophy. The data used for this project is taken from a paper entitled "Probabilistic forecasting of replication studies" (https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0231416), which collected and standardized the results from these 4 replication projects.

#### Methodology
I test a variety of regression models - linear regression, ridge regression, and lasso regression - against a simple model based on the average change between original studies and their replications. I also test a single regression model against a suite of models developed separately for each research discipline. 

#### Results
As expected, the results of replications are systematically smaller in scale than the results of original studies. As such, if we were to use published research results as a basis for predicting replication results, there would be considerable error. A simple heuristic model yields improved predictions (33% lower mean squared error). The best regression model found in this project - a linear regression model of degree 1 (performed on numeric features only) - provides an additional 11% improvement on that heuristic.    

#### Next steps
The most important next step is to get much more data. My plan for this is to shift focus slightly - instead of looking at the results of direct replications (of which there are few), I will examine the combined results reported in meta-analyses (of which there are many) and see how they compare to the original studies the meta-analysis draws upon. 

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
Joshua Beattie
jsbeattie@gmail.com