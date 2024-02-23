1. Prior probability and posterior probabilty are prior to and posteriro to you learning stuff. Before I know anything about how often externalities are internalised, I have a prior belief that the probaility of it follows a Gamma distribution. So I choose a Gamma prior. When I learn that out of 100 companies, 20 internalise an externality, I can update my prior beliefs and get a posteriro probability. I can then use that posterior probability as my prior beliefs in the next model run.


#### Why Thousands of Samples?

At first, returning thousands of samples to the user might sound like being an inefficient way to describe the posterior distributions. I would argue that this is extremely efficient. Consider the alternative possibilities:

1. Returning a mathematical formula for the "mountain ranges" would involve describing a N-dimensional surface with arbitrary peaks and valleys.
2. Returning the "peak" of the landscape, while mathematically possible and a sensible thing to do as the highest point corresponds to most probable estimate of the unknowns, ignores the shape of the landscape, which we have previously argued is very important in determining posterior confidence in unknowns. 

Besides computational reasons, likely the strongest reason for returning samples is that we can easily use *The Law of Large Numbers* to solve otherwise intractable problems. I postpone this discussion for the next chapter. With the thousands of samples, we can reconstruct the posterior surface by organizing them in a histogram.


**This ArviZ factoid is great!** The reason for this choice is that 94 is close to the widely used 95 but is different enough to serve as a friendly reminder that there is nothing special about these round values [10]. Ideally you should choose a value that fits your needs [11], or at least acknowledge that you are using a default.

The mean of the Beta distribution is 
 
, thus the prior mean is:

(1.15)
 
and the posterior mean is:

(1.16)
 
We can see that if the value of 
 is small in relation with the values of 
 and 
 then the posterior mean will be closer to the prior mean. That is, the prior contributes more to the result than the data. If we have the opposite situation the posterior mean will be closer to the sampling proportion estimator 
 
, in fact in the limit of 
 the posterior mean will exactly match the sample proportion no matter which prior values we choose for 
 and 
.