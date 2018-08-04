# Probability-of-default-model
Extra-curricular project. 

Trying to build a probability of default (credit-scoring) model for counterparties based on fitting the model to external PDs.

**Development process includes**:
  1. Features visualization
  2. Features transformation: logit transform and normalization
  3. One-factor analysis: APS (adjusted power statistic) and availability
  4. Multi-factor analysis: GLM regression, P-values and adjusted R^2 calculation
  
**Implemented functions during the development process**:
  1. sigmoid(x) - returns the logit transform of x
  2. transform(features,factors_cnt) - function to transform features (amount of features is factors_cnt)
  3. draw_distribution – used for histogram visualizations of features
  4. roc_plot(factor,K,x_current,y_current,save_path='',aps=np.nan) – auxiliary function for calculating points of the ROC-curve for ideal, random, and actual (realized in sample) feature
  5. calculate_aps(K,x_current,y_current) – auxiliary function for calculating the AUROC, returns the value of APS
  6. compute_roc_aps(sample,factors,factors_cnt,roc_path) – the main function, that uses roc_plot and calculate_aps for plotting for each feature the ROC-curve and calulating the value of APS
