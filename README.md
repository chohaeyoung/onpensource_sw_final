# opensource_sw_final

## What I Do?
* Brain tumor claaissification

I classified brain tumor by *scikit-learn*
    
    
## What Is the Train set?
* Brain tumor
 
 There are MRI datas about brain tumor 
 
![image](https://user-images.githubusercontent.com/115198496/207895287-669d3924-6515-4132-abb8-27756b59e621.png)
![image](https://user-images.githubusercontent.com/115198496/207895315-fba2869c-be38-4687-baec-68d2b70709df.png)
![image](https://user-images.githubusercontent.com/115198496/207895336-d034c307-f6f3-4fb4-9eb9-bc2271d53f5e.png)
![image](https://user-images.githubusercontent.com/115198496/207895359-5ef7e675-3349-4d87-ac10-b88200bcf89a.png)

## How Do I Classify the Datas?
* algorithm

I choose **random forest**
Random forest method composes a subset from train data and makes a decision tree through *Bagging*
It makes some decision trees.
And it makes some decision trees and vote the result.

Random forest has some benefits.
First, It is flexible. It can be applied to a variety of problems.
And it can avoid overfitting increase the accuracy.
This is why I choose random forest.

* hyperparameter tuning 

*n_estimators* : The number of trees in the forest. The higher n_estimators, the higher accuracy, but n_estimators is too high, then the effiency decreases.

*max_samples* : If bootstrap is True, the number of samples to draw from X to train each base estimator.

*max_features* : The number of features to consider when looking for the best split

*max_depth* : The maximum depth of the tree. 

*max_leaf_node* : Grow trees with max_leaf_nodes in best-first fashion.

## My code
```
rbf = sklearn.ensemble.RandomForestClassifier(random_state = 100, 
                                              max_samples = 0.7,
                                              n_estimators = 400,
                                              max_features = 5,
                                              max_depth = 50
                                              
                                              )
rbf.fit(X_train, y_train)

y_pred = rbf.predict(X_test)

print('Accuracy: %.5f' % sklearn.metrics.accuracy_score(y_test, y_pred))
    


