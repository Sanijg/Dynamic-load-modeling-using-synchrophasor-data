# Dynamic-load-modeling-using-synchrophasor-data

Load models have evolved from simple ZIP model to composite model that incorporates the transient dynamics of motor loads. This research utilizes the latest trend on Machine Learning and builds reliable and accurate composite load model. A composite load model is a combination of static (ZIP) model paralleled with a dynamic model. The dynamic model, recommended by Western Electricity Coordinating Council (WECC), is an induction motor representation. In this research, a dual cage induction motor with 20 parameters pertaining to its dynamic behavior, starting behavior, and per unit calculations is used as a dynamic model. For machine learning algorithms, a large amount of data is required. The required PMU field data and the corresponding system models are considered Critical Energy Infrastructure Information (CEII) and its access is limited. The next best option for the required amount of data is from a simulating environment like PSSE. The IEEE 118 bus system is used as a test setup in PSSE and dynamic simulations generate the required data samples. Each of the samples contains data on Bus Voltage, Bus Current, and Bus Frequency with corresponding induction motor parameters as target variables. It was determined that the Artificial Neural Network (ANN) with multivariate input to single parameter output approach worked best. Recurrent Neural Network (RNN) is also experimented side by side to see if an additional set of information of timestamps would help the model prediction. Moreover, a different definition of a dynamic model with a transfer function-based load is also studied. Here, the dynamic model is defined as a mathematical representation of the relation between bus voltage, bus frequency, and active/reactive power flowing in the bus. With this form of load representation, Long-Short Term Memory (LSTM), a variation of RNN, performed better than the concurrent algorithms like Support Vector Regression (SVR). The result of this study is a load model consisting of parameters defining the load at load bus whose predictions are compared against simulated parameters to examine their validity for use in contingency analysis.
