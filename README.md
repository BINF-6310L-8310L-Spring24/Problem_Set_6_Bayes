# Problem_Set_5_Bayes


In this week's problem set we will explore the basics of the Bayes Box and the Bayes Formula

Background:

Your lab has been searching for environmental samples with the illusive bacteria *B. harpocrates*. Previous experiments in your lab have found that this bacteria is found in only 10% of samples across all metagenomic experiments done previously in the lab. 


You collected 100 metagenomics samples in Field Site A. Your budget is very limited so you decide to test a few samples to see if you want to sample more. 

You sequence 5 samples randomly to give you an idea of the presence of *B. harpocrates* in this field. 
You are **so** excited when 2 of your 5 samples contain your species of interest. 

## Question Set A
 
1. What is the binomial probability of getting 2 out of 5 positive samples with a true rate of 0.10?

2. Using the previously known probability (0.10) what are the chances that your _next_ sample will contain *B. harpocrates*? This would bring your total sample to 3 out of 6. 

3. Using your sample proportion (2/5) what are the chances that your _next_ sample will contain *B. harpocrates*? This would bring your total sample to 3 out of 6. 

 &nbsp;

You tell your PI that your field is probably a JACKPOT of samples. They are not so convinced and are fairly confident that the true rate is closer to 5%. 
Your PI asks you to use Bayesian theory to estimate the true rate in your field site. 

To do this you complete the following steps

 &nbsp;

### Question Set B

You will be assessing the continuous variable &theta; or the percent of your samples in Field A with your bacteria in it.

First step will be to decide on a prior distribution for &theta; You decide to use the binomial prior with a mean of 0.1 and an intermediate amount of confidence. 

1. Create a function containing a binomial distribution (**don't use the built-in distribution**) such that the mean of the distribution is 0.10 and &beta;=20. The mean of the binomial distribution is &alpha;/(&alpha;+&beta;). What is the &alpha; value of the binomial prior distribution?
  
3. Plot the prior distribution. For this case remember that our beta distribution for the prior is _x_^(&alpha;-1)(1-_x_)^(&beta;-1). This is our PRIOR. Report your prior formula.

4. Create a function containing a binomial likelihood distribution (**don't use the built-in distribution**) that reflects our sampling for Field Site A. Plot this distribution. This is our LIKELIHOOD. Report your likelihood formula.

5. Create another function that represents our binomial likelihood multiplied by our prior. Plot this distribution

6. Integrate over our likelihood x prior to get a sum of the area under the curve. Report the area under the curve from 0 to 1

7. Create a final function that represents our posterior distribution by dividing the prior x likelihood function by the area under the curve. Plot this function!

8. Use the `optimize()` function in R to find the &theta; with the maximum posterior value. This will provide you with a single point-estimate for the proportion of samples with the bacteria. Using this maximum posterior value (probability), what is the probability that in the five samples, you will get 3 containing a sample of *B. harpocrates*

 &nbsp;

### Question Set 3

You have convinced your PI there *might* be more than 5% presence of *B. harpocrates*. So they let you sequence 5 more samples. Now you have 5/10 samples that contain this species of interest. 

1. Plot the posterior distribution but this time using the built in R beta function. To do this we need to remember that for the posterior distribution we use Beta(&alpha; + *x*, &beta; + *N* - *x*). This is for observing *x* successes out of _N_ trials. Use the same &alpha; and &beta; values as you did in the previous section

2. Use the `optimize()` function in R to find the &theta; with the maximum posterior value. Using this maximum posterior value (probability), what is the probability that in the five samples you will get 3 containing a sample of *B. harpocrates*
3. 
 &nbsp;

### Question Set 4

You updated the likelihoods in question set 3. But you also wanted to update the prior to lower your confidence in 0.1 as the true probability.

1. You want to maintain a prior distribution with a mean of 0.1, but you want that distribution to be more widely distributed. Therefore, adjust the &beta; value and then recalculate &alpha;. Do you use a beta of 10 or 30?

2. Plot the posterior distribution for your new dataset (5/10 samples) using the Beta function in R.

3. Use the `optimize()` function in R to find the &theta; with the maximum posterior value for &theta;.  


### Knit and upload your data




