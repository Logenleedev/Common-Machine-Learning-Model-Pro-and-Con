Classification Model Pros and Cons (Generalized)

* Random Forest
	* Pros
		* As we mentioned earlier a single decision tree tends to overfit the data. The process of averaging or combining the results of different decision trees helps to overcome the problem of overfitting.
		* Random forests also have less variance than a single decision tree. It means that it works correctly for a large range of data items than single decision trees.
		* Random forests are extremely flexible and have very high accuracy.
		* They also do not require preparation of the input data. You do not have to scale the data.
		* It also maintains accuracy even when a large proportion of the data are missing.
	* Cons
		*The main disadvantage of Random forests is their complexity. 
		*They are much harder and time-consuming to construct than decision trees.They also require more computational resources and are also less intuitive. When you have a large collection of decision trees it is hard to have an intuitive grasp of the relationship existing in the input data.
		* In addition, the prediction process using random forests is time-consuming than other algorithms.
		

* SVM
	* Pros 
		* Flexible
	* Cons
		* Too Slow!!
* Logistic Regression (continuous value)
	* Pros
		* low variance
		* provides probabilities for outcomes
		* works well with diagonal (feature) decision boundaries
		* NOTE: logistic regression can also be used with kernel methods
	* Cons
		* high bias
* Linear Regression
  	* Pros
		* Linear regression is an extremely simple method. It is very easy and intuitive to use and understand. A person with only the knowledge of high school mathematics can understand and use it. In addition, it works in most of the cases. Even when it doesn’t fit the data exactly, we can use it to find the nature of the relationship between the two variables.
	* Cons
		* By its definition, linear regression only models relationships between dependent and independent variables that are linear. It assumes there is a straight-line relationship between them which is incorrect sometimes. Linear regression is very sensitive to the anomalies in the data (or outliers).
		* Take for example most of your data lies in the range 0-10. If due to any reason only one of the data item comes out of the range, say for example 15, this significantly influences the regression coefficients.
		* Another disadvantage is that if we have a number of parameters than the number of samples available then the model starts to model the noise rather than the relationship between the variables.
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
