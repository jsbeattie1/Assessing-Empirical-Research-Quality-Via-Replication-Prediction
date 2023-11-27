### Predicting Replication: Assessing the Quality of Empirical Research Results

**Joshua Beattie**

#### Executive summary

The model developed here improves the informational quality of empirical research. It does so by predicting the results of (hypothetical) replications, thereby providing a more fine-tuned assessment of the dependability of the results and allowing for more accurate conclusions regarding the scale of purported effects or patterns. There is currently relatively little replication data available, but the model still improves upon a simple (but already quite helpful) heuristic by ~20-25%. 


#### Rationale
Replication, i.e. repeating a study that has already been carried out, is a crucial part of the scientific process. It aids in separating genuine effects from statistical artifacts and in determining how large the genuine effects actually are. In recent years, it has become clear that due to various factors (publication and grant-making practices, conventional statistical methodologies, etc.), published research is less dependable - less replicable - than might be hoped. This is often referred to as a "replication crisis". Countless important decisions - in science and technology, in public policy, in business, etc. - are informed by empirical research results, so anything that can improve the informational quality of those results will be highly beneficial. One option, already being pursued in various ways, is to institute or incentivize better methodological practices (e.g. making publication dependent on pre-registering the study design). Here, the focus is on gaining an improved *interpretation* or *assessment* of empirical research results, however that research has been conducted.   

#### Research Question
Given the statistical and methodological features of a particular empirical research result, along with historical information about replications that have been performed in other cases, can we predict what the overall best estimate of the measured effect would be if a replication were to be carried out in this instance? Put another way, how ought we to adjust or calibrate our assessments of published results, in light of all the information we have available to us?     

#### Data Sources
One response to the replication crisis has been the organization of several "replication projects", in which resources are devoted to replicating a collection of studies in a given field. These have so far been carried out for research in psychology, experimental economics, social sciences, and experimental philosophy. The data used for this project is taken from a paper entitled "Probabilistic forecasting of replication studies" (https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0231416), which collected and standardized the results from these 4 replication projects.

#### Methodology
I test a variety of predictive models - 6 individual models (standard linear regression, ridge, lasso, decision tree, k-nearest neighbors, support vector machine), 3 ensemble models (voting regressor, random forest, gradient boosting), and an artificial neural network - against a simple heuristic model that is based on the average difference between original studies and their replications. I also compare the use of a single model (with discipline-specific information in the input data) against a suite of 4 models, one developed separately for each research discipline. 

#### Results
As expected, the results of replications are systematically smaller in scale than the results of original studies. As such, if we were to use published research results alone as a basis for predicting the best post-replication estimates, there would be considerable error. A simple heuristic model yields improved predictions (31% lower mean squared error), while the best regression model found in this project - a linear regression model of degree 1 (performed on numeric features only) - provides an additional 22% improvement on that heuristic.    

#### Next steps
The most important next step is to get a great deal more data. My plan for this is to shift focus slightly - instead of looking at the results of direct replications (of which there are few), I will examine the combined results reported in meta-analyses (of which there are many) and see how they compare to the original studies the meta-analysis draws upon. 

#### Project notebook

https://github.com/jsbeattie1/Project-Predicting-Replications/blob/main/Predicting%20Replication.ipynb


##### Contact and Further Information
Joshua Beattie
jsbeattie@gmail.com
