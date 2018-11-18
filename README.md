# PSI
Population stability index

The idea behind the PSI is to check whether distribution of some attributes, which you used in the model changed or not. For example, if you constructed your model in February and used income as a feature in your model, when you are ready to apply it in March, would the distribution of the income be the same? Or something has dramatically changed? The changes can be caused by some database flaws or some economic/politics problems. But it is better to know about them beforehand.

To answer these questions you can calculate PSI. You need to take slices of data (February and March) and create a new attribute, which will contain all data, for each observation in February as (x1, ..., xn), where you have n observation, and all data for March as (y1, ..., yn). You will get new attribute (x1, ..., xn, y1, ..., yn) and then create artificial variable z which will be 1 for February and 0 for March. After that you can calculate Information Value, which in this context will shows you how good is separation is between zeros and ones. With that you can understand if you data has change from February to March or not. 
