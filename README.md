# OTIF---Time-to-Ready

Analytics of the time_to_ready status (time to order approval, hereafter referred to as time to approval). Its patterns, dependencies and impact on data, OTIF and delivery date.

The time of order coordination between the supplier and the customer is considered.
In this study, the dependencies of time to order reconciliation will be reflected. 
It will consider:
1. Its distribution
2. A simple clustering of status according to the order dwell time is performed
3. Hypotheses considered:
‘as time_to_ready increases, the late_% (percentage of late orders within the cluster) increases’
"The medians of time_to_ready differ for at least one day of the week. There is at least one day of the week for which the median time_to_ready is statistically significantly different from other days."
using statistical tests
4. Performed automatic search for ‘bad exceptions’ for dataset fiches. In particular, the following are marked as statistically bad: Distribution centres, Customers, Customer catalogues, Legal entities. 
It will be possible to automatically cut off (limit) the lines where time_to_ready is less than a certain value in days.
5. Time_to_ready significance threshold will be found and a visual graph will be implemented.
6. A machine learning model "catboost" will be used and using DummyRegressor (baseline for comparison) and SHAP to identify the significant features that the model focuses on when predicting the time_to_ready status
7. The conclusions of the study are written
