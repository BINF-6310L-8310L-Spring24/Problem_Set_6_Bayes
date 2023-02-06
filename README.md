# Problem_Set_5_Bayes


In this week's problem set we will explore the basics of the Bayes Box and the Bayes Formula

Background:

Your lab has been searching for environmental samples with the illusive bacteria *B. harpocrates*. Previous experiments in your lab have found that this bacteria is found in only 5% of samples across all metagenomic experiments done previously in the lab. 


You collected 100 metagenomics samples in Field Site A. Your budget is very limited so you decide to test a few samples to see if you want to sample more. 

You sequence 5 samples randomly to give you an idea of the presence of *B. harpocrates* in this field. 
You are **so** excited when 2 of your 5 samples contain your species of interest. 

### Question Set 1

1. What is the binomial probability of getting 2 out of 5 positive samples with a true rate of 0.05?

2. Using the previously known probability (0.05) what are the chances that your _next_ sample will contain *B. harpocrates*?

3. Using your sample proportion (2/3) what are the chances that your _next_ sample will conain *B. harpocrates*?



You tell your PI that your field is probably a JACKPOT of samples. They are not so convinced and are fairly confident that the true rate is closer to 5%. 
Your PI asks you to use Bayesian theory to estimate the true rate in your field site. 

To do this you complete the following steps

### Question Set 2

You will be assessing the continous variable &theta; or the percent of your samples in Field A with your bacteria in it.

First step will be to decide on a prior distribution for &theta; You decide to use the beta prior centered over 0.05 with an intermediate amount of confidence. 

1. Create a beta distribution such that (&alpha;-1)/(&beta-1); is 0.05 and (&beta-1);=20. Plot this distribution. For this case remember that our beta distribution for the prior is _x_^(&alpha;-1)(1-_x_)^((&beta;-1)


