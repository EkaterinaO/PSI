# PSI
Population stability index

The idea behind the PSI is to check whether distribution of some attributes, which you used in the model has changed or not. For example, if you constructed your model in February and used income as a feature in your model, when you are ready to apply it in March, you have to know would the distribution of the income be the same or not.  What if something has dramatically changed? Changes can be caused by some database flaws or some external problems like economics or politics. But it is better to know about them before applying your model to the real customers. 

To solve these questions, you can calculate PSI. You need to take slices of data (February and March) and create a new attribute, which will contain all data, for each observation in February as (x1, ..., xn), where you have n observations, and all data for March as (y1, ..., yn). You will get new attribute (x1, ..., xn, y1, ..., yn) and then you need to create artificial variable z which will be 1 for February and 0 for March. After that you can calculate Information Value, which in this context will show you how good is the separation is between zeros and ones. With that information you can understand if your data has changed significantly or slightly. 

