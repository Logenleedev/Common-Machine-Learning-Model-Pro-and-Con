Classification Model Pros and Cons (Generalized)

* Logistic Regression (continuous value)
	* Pros
		* low variance
		* provides probabilities for outcomes
		* works well with diagonal (feature) decision boundaries
		* NOTE: logistic regression can also be used with kernel methods
	* Cons
		* high bias
* Polynomial Regression
  	* Pros
		* Polynomial provides the best approximation of the relationship between the dependent and independent variable.
		* A Broad range of function can be fit under it.
		* Polynomial basically fits a wide range of curvature.
	* Cons
		* The presence of one or two outliers in the data can seriously affect the results of the nonlinear analysis.
		* These are too sensitive to the outliers.
		* In addition, there are unfortunately fewer model validation tools for the detection of outliers in nonlinear regression than there are for linear regression.
* Decision Trees (labeled data)
	* Regular (not bagged or boosted)
		* Pros
			* easy to interpret visually when the trees only
				contain several levels
			* Can easily handle qualitative (categorical) features
			* Works well with decision boundaries parellel to the feature axis
		* Cons
			* prone to overfitting
			* possible issues with diagonal decision boundaries
	* Bagged Trees : train multiple trees using bootstrapped data
		to reduce variance and prevent overfitting 
		* Pros
			* reduces variance in comparison to regular decision trees
			* Can provide variable importance measures
				* classification: Gini index
				* regression: RSS
			* Can easily handle qualitative (categorical) features
			* Out of bag (OOB) estimates can be used for model validation
		* Cons
			* Not as easy to visually interpret
			* Does not reduce variance if the features are correlated
	* Boosted Trees : Similar to bagging, but learns sequentially and builds off
		previous trees
		* Pros
			* Somewhat more interpretable than bagged trees/random forest
				as the user can define the size of each tree resulting in 
				a collection of stumps (1 level) which can be viewed as an additive model
			* Can easily handle qualitative (categorical) features
		* Cons
			* Unlike bagging and random forests, can overfit if number of trees is too large
* Random Forest
	* Pros
		* Decorrelates trees (relative to bagged trees)
			* important when dealing with mulitple features which may be correlated
		* reduced variance (relative to regular trees)
	* Cons
		* Not as easy to visually interpret
* SVM
	* Pros
		* Performs similarly to logistic regression when linear separation
		* Performs well with non-linear boundary depending on the kernel used
		* Handle high dimensional data well
	* Cons
		* Susceptible to overfitting/training issues depending on kernel
* KNN(numerial data)
	* Pros
	        * K-NN has no assumptions: K-NN is a non-parametric algorithm which means there are assumptions to be met to implement K-NN. Parametric models like linear regression has lots of assumptions to be met by data before it can be implemented which is not the case with K-NN.
		* It constantly evolves: Given it’s an instance-based learning; k-NN is a memory-based approach. The classifier immediately adapts as we collect new training data. It allows the algorithm to respond quickly to changes in the input during real-time use.
	* Cons
		* K-NN slow algorithm: K-NN might be very easy to implement but as dataset grows efficiency or speed of algorithm declines very fast.
		* Outlier sensitivity: K-NN algorithm is very sensitive to outliers as it simply chose the neighbors based on distance criteria.
* Naive Bayes
	* Pros
		* Computationally fast
		* Simple to implement
		* Works well with high dimensions
		* 在数据较少的情况下仍然有效，可以处理多类别问题。
	* Cons
		* Relies on independence assumption and will perform 
			badly if this assumption is not met
