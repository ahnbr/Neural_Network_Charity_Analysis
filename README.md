# Neural_Network_Charity_Analysis

## Overview of the Analysis

- The purpose of this project was to use neural networks and machine learning in order to create a binary classifier that would help us determine the success of those applicants that received help from the Alphabet Soup charity would be successful. We were provided a data set containing over 30,000 organizations that had previously received funding to aid us in our analysis. 

## Results

### Data Preprocessing

**What variable(s) are considered the target(s) for your model?**
- The variable that would be considered the target of our model is the column that is labeled "IS_SUCCESSFUL

**What variable(s) are considered to be the features for your model?**
- The variables that are considered to be featured are Application Type, Affiliation, Classification, Use Case, Organization, Status, Income Amount, Special Considerations and Ask Amount
- The variables that are not features are the ones we dropped from the data set, which were EIN and Name

**What variable(s) are neither targets nor features, and should be removed from the input data?**
- The variables that were neither targets nor features, as mentioned above and removed from the input data, were EIN and Name

### Compiling, Training and Evaluating the Model

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**
- Our initial model contained 80 neurons in the first hidden layer and 30 neurons in the second hidden layer as well as an output layer. The first and second had relu activation functions while the output layer was sigmoid.

<img width="752" alt="Screen Shot 2021-01-30 at 12 24 17 AM" src="https://user-images.githubusercontent.com/68168883/106348092-8f5dc800-6291-11eb-87d7-1e43b49f0ca6.png">

**Were you able to achieve the target model performance?**
- The target for this analysis was to achieve 75% of better for this particular model. Unfortunately, we were not able to achieve that goal, coming in at ~72.5%. This meant we would have to make adjustments to our approach to hit our target.

<img width="752" alt="Screen Shot 2021-01-30 at 12 28 09 AM" src="https://user-images.githubusercontent.com/68168883/106348154-0c893d00-6292-11eb-8a16-051b674a1fbc.png">

**What steps did you take to try and increase model performance?**
- We tried several different methods in order to increase model performance. The first was to use the Random Forest Classifier but this did not help us achieve the target and produced less accuracy than our original model. 

<img width="752" alt="Screen Shot 2021-01-30 at 12 30 29 AM" src="https://user-images.githubusercontent.com/68168883/106348216-95a07400-6292-11eb-8ff8-076d85b2ce21.png">

- The next step included increasing the number of neurons in our 2 hidden nodes as well as more epochs. The results returned similar results as our original model.

<img width="752" alt="Screen Shot 2021-01-30 at 12 30 53 AM" src="https://user-images.githubusercontent.com/68168883/106348246-cd0f2080-6292-11eb-8eaa-6fd15dae4820.png">

- The third step included adding an addition node to 3 nodes and reducing the number of epochs in order to avoid potentially oversampling the data. These results also returned similar results to our original model.

<img width="750" alt="Screen Shot 2021-01-30 at 12 31 27 AM" src="https://user-images.githubusercontent.com/68168883/106348252-d0a2a780-6292-11eb-982d-d9ea2f2a97b1.png">


## Summary

- The best accuracy score we were able to provide was ~72.7%, which unfortunately fell below the target expectation of 75%+. In our initial analysis, we dropped 2 columns - EIN and Names - and it's possible that removing or binning data would allow us to provide a more accurate model. I think some adjustments to the number of nodes and neurons could likely have a beneficial outcome but even more data would certainly provide a much more likelihood of creating a more accurate model.
