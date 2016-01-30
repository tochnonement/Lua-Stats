# Lua-Stats
Statistical functions for Lua
# Reference
## Generic Functions
Function|Description
---|---
integral(*f, start, stop, delta, ...*)|Calculates the area under a function *f* from *start* to *stop* in *delta*-sized steps. The optional arguments *...* are passed on to the function to integrate
factorial(*x*)|Calculates the factorial recursively for integer *x* or using the gamma function if *x* is a float
findX(*y, f, accuracy = 0.001, ...*)|Finds the x needed for *f* to return *y* at a certain *accuracy*, given the optional arguments *...*
gamma(*x*)|the probability density function of the gamma distribution for *x*
beta(*x,y*)|The probability density function of the beta distibution
pValue(*q, f, ...*)| Calculates the p-value of a test statistic coming from the CDF *f*. The optional arguments *...* are passed on to *f*.
map(*t, f*)|Applies a function *f* to every value of a table *t*.
reduce(*t, f*)|Reduces a table *t* using a function *f* that takes two arguments.
in_table(*value, t*)|True if *value* is in table *t*.
unify(*...*)|Takes an arbitrary number of values and tables and concatenates them into one big table

## Arithmetic functions
All functions taking only arbitrary optional arguments *...* concatenate all supplied values into a table and calculate from that.  

Function|Description
---|---
sum(*...*)|Sum
count(*...*)|Count of values
mean(*...*)|Average of values
sumSquares(*...*)|Sum of the squared difference from the mean
var(*...*)|Variance
varPop(*...*)|Variance for the population
sd(*...*)|Standard deviation
sdPop(*...*)|Standard Deviation for the population
min(*...*)|Minimum value
max(*...*)|Maximum value
quantile(*t, q*)|Gets the *q*-th quantile of sequence *t*, where 0 >= *t* >= 1
median(*t*)|Median for table *t*
quartile(*t, i*)|Wrapper for quantile returning<br>0: Minimum<br>1: 1st quartile<br>2: Median<br>3: 3rd quartile<br>4: Maximum

## Normal Distribution Functions
Function|Description
---|---
dNorm(*x, mu = 0, sd = 1*)|Probability density function for the normal distribution with mean *mu* and standard deviation *sd* at point *x*
pNorm(*x, mu = 0, sd = 0, accuracy = 0.001*)|Cumulative distribution function for the Normal distribution with mean *mu* and standard deviation *sd* at point *x*
qNorm(*q, accuracy = 0.01*)| Calculates the z-value for *q* for N(0|1)
