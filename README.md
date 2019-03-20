# DIGITS RECOGNIZATION .
# Objective :
    To find the best MLP model for digit recognization.
# Note :
    1.   Here we have used MNIST dataset .
    2.   We have used  activation function as " ReLU " and optimizer as " Adam "
    3.   Here we have considered 3 MLP models :-
         -784 - 512 - 128 - 10 ( 2 hidden layer MLP )
         -784 - 512 - 360 - 256 - 10 ( 3 hidden layer MLP )
         -784 - 512 - 256 - 128 - 64 - 36 - 10 ( 5 hidden layer MLP )
         
# Final Table :
      +--------------------+---------------------+----------+-----------+---------------+
      |       MODEL        | BATCH_NORMALIZATION | DROP_OUT | TEST_LOSS | TEST_ACCURACY |
      +--------------------+---------------------+----------+-----------+---------------+
      | 2 hidden layer MLP |          NO         |    NO    |   0.0916  |     0.9808    |
      | 2 hidden layer MLP |         YES         |    NO    |   0.0817  |     0.9802    |
      | 2 hidden layer MLP |          NO         |   YES    |   0.0687  |     0.9825    |
      | 2 hidden layer MLP |         YES         |   YES    |   0.0588  |     0.9831    |
      | 3 hidden layer MLP |          NO         |    NO    |   0.0983  |     0.9812    |
      | 3 hidden layer MLP |         YES         |    NO    |   0.0686  |     0.9832    |
      | 3 hidden layer MLP |          NO         |   YES    |   0.0756  |     0.9787    |
      | 3 hidden layer MLP |         YES         |   YES    |   0.0588  |     0.9823    |
      | 5 hidden layer MLP |          NO         |    NO    |   0.0849  |     0.9808    |
      | 5 hidden layer MLP |         YES         |    NO    |   0.1028  |     0.9765    |
      | 5 hidden layer MLP |          NO         |   YES    |   0.122   |     0.9782    |
      | 5 hidden layer MLP |         YES         |   YES    |   0.0761  |     0.9818    |
      +--------------------+---------------------+----------+-----------+---------------+
# Conclusion :
    1.  The model having 2 hidden layers ( 784 - 512 - 128 - 10 ) and build with dropout and batch normalization has the highest accuracy on test dataset (0.9831 ).
    2.  The model having 5 hidden layers ( 784 - 256 - 128 - 64 - 36 - 10 ) and build with dropout and batch normalization has the lowest accuracy on test dataset (0.9765 ).
    3.  Shallow MLP models ( 2 hidden layered ) performs better than any other models .
    4.   As the layers of MLP increases the performance of our model decreases because of overfitting , etc .
    5.   For shallow MLP models dropout , affects the model results very much and batch - normalization don't affect much 
    6.   For non shallow MLP models , batch - normalization has hugh impact on the model results .
