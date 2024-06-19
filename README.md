# Breast-Cancer-Classification-
Using decision trees to predict cancer diagnosis 

## Build Decision Tree Classifier
![Screenshot 2024-06-19 at 1 22 08 PM](https://github.com/lex910/Breast-Cancer-Classification-/assets/101606445/21a21a45-034c-4ac0-a5f9-789c79df6f5b)

The confusion matrix helps us see how well our tree performs by looking at how many actual diagnosis were predicted correctly. We can see that 101 actual benign cases were predicted to be benign while 11 were predicted as malignant. The tree also correctly predicted 50 as malignant when they actually were malignant and incorrectly classified 9 malignant cases as benign.

## Visualize The Tree 
![Screenshot 2024-06-19 at 1 22 59 PM](https://github.com/lex910/Breast-Cancer-Classification-/assets/101606445/ec6a9da9-8172-45c2-8f0f-3578d2cc0987)

The variables that appeared in the tree and are significant predictors of diagnosis are perimeter_worst, texture_mean, smoothness_worst, radius_se, area_worst, concave_points_mean, texture_worst, concavity_se,symmetry_worst, and concave_points_se.

## Considerations of pruning 
This tree would need to be pruned. A decision tree always finds a better split until we have homogeneous leaves. This will result in overfitting, thus we need to have some sort of stopping criteria. We can create a hyperparameter that will stop the growth of the tree when the size of leaf nodes hits a minimum threshold or when there is a minimum deviance improvement. Another solution is to let the tree grow all of the way and then prune it by removing nodes from the bottom up. At each step we remove the node that contributes the least to reducing deviance. We can create different candidate trees and then use cross validation to estimate the out of sample prediction performance of the candidate trees. Using a random forest is also an option. Random forests allow for a better understanding of variable selection, but results in a loss of interpretability of where splits are being made. 

