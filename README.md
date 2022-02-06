# Neural_Network_Charity_Analysis

### Overview of the Analysis 

In this analysis, Charity data from the organization alphabet Soup was examned and analyzed in order to create a model that would help predict the performance or success of charitable donations using deep-learning neural networks with the TensorFlow platform in Python. This analysis was executed using **Data Preprocessing**, **Compiling, Training, and Evaluating the Model**, and then we optimized for performance.

### Results 

*Data Preprocessing*
 * What variable(s) are considered the target(s) for your model?
        **IS_SUCCESSFUL Column**:The column IS_SUCCESSFUL contains binary data that points to whether the donations were utilized in an effective manner.
 * What variable(s) are considered to be the features for your model?
        **Every Column apart from the target for the model was considered.** This includes: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
 * What variable(s) are neither targets nor features, and should be removed from the input data?
        **EIN & NAME** were dropped.

*Compiling, Training, and Evaluating the Model*
 * How many neurons, layers, and activation functions did you select for your neural network model, and why?


    *Two hidden layers and one output layer.*
    1. 80 neurons with relu activation
    2. 30 neurons with relu activation
    3. Output Layer with sigmoid activation.
    *These were chosen given the use case for nonlinear data and binary clasification.*

![image](https://user-images.githubusercontent.com/89872154/152696727-bf52f9f0-f3a2-4afb-a778-2c151ff3f9c5.png)

 * Were you able to achieve the target model performance?

The accuracy of this model was shy of the target at 73%
![image](https://user-images.githubusercontent.com/89872154/152696696-7bd2e0fc-f958-4bcc-8dbc-2f3616ab642e.png)

 * What steps did you take to try and increase model performance?
1. The first optimization attempt included 3 hidden layers. There were 80 neaurons in the first layer, 30 neurons in the second layer and 15 neurons in the 3rd layer.
![image](https://user-images.githubusercontent.com/89872154/152696872-ae24e3ef-1936-4f50-b42b-f6fbfb6b2fbd.png)
**73% Accuracy**
![image](https://user-images.githubusercontent.com/89872154/152697689-1b13066b-f7f8-4875-9806-daa1fd6d7919.png)


2. The second optimization attempt included 3 hidden layers. There were 80 neaurons in the first layer, 35 neurons in the second layer and 10 neurons in the 3rd layer.
![image](https://user-images.githubusercontent.com/89872154/152697025-a4b772bb-21f5-4369-ba86-f0f90c84468a.png)
**72.9% Accuracy**
![image](https://user-images.githubusercontent.com/89872154/152697773-b25ce27c-a9bc-4286-b9ea-75e2eaf68746.png)


3. The third optimization attempt included 3 hidden layers. There were 80 neaurons in the first layer, 30 neurons in the second layer and 15 neurons in the 3rd layer. With flipped activation orders from the original model. 
![image](https://user-images.githubusercontent.com/89872154/152697367-73efac23-7cca-4541-ae89-c9b3ce72759e.png)
**72.8% Accuracy**
![image](https://user-images.githubusercontent.com/89872154/152697794-bc23fb1c-b769-4135-bfe3-b0ec4668a27c.png)

### Summary
The multiple optimization attempts yielded similar results all hovering around 73% accuracy which is not an acceptable level of accuracy for predictions. We would need to continue such trial and error testing until we reached an accuracy level closer to 75%. 
