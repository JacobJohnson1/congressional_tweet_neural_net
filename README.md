# congressional_tweet_neural_net
CS461 Intro to AI Project #3


### Data preparation:  
What did you do to prepare your data? What categories did you collapse? 
What standardizations, if any, did you employ? Why did you select those? Basically, 
describe what you did to get your data ready. NOTE: This may be one of the larger 
sections of your report. In the 'real world,' data scientists spend about 3/4 of their 
time curating, cleaning, filtering, and preparing data.  
### Network configuration: 
How is your network set up? How many layers? How many neurons 
in each? Did you try any nonlinear features (connecting outputs to inputs more than one 
layer ahead)? (There's probably no need for that, but if you did it, talk about it.) This 
data doesn't map to a 2-d structure, and each item is independent (they're not a series), 
so there's no need for convolutional or recurrent features.
### Validation strategy:  
How did you divide your data into training, test, and validation 
sets? What validation strategies did you use? If you used k-fold validation, what was k? 
How did you lower the risk of overtraining?
### Results:  
What did you find? How well did it work? During the project you will probably 
want to tweak your hyperparameters in various ways--add a layer, remove a layer, change 
the learning rate, etc. Did these make a difference? (One approach is to start with a 
very simple network, and slowly build it up. As long as results are improving, keep 
adding layers, neurons, etc.; as soon as they start to deteriorate, back off.)
### Comments:  
What do you think of the results? What might improve accuracy? Were there 
surprises along the way? Do you have any (disciplined) speculation about what might have 
gone wrong or what might have made it work better?
### References:  
[1] Python, R., 2022. Practical Text Classification With Python and Keras – Real Python. 
[online] Realpython.com. Available at: 
<https://realpython.com/python-keras-text-classification/> [Accessed 20 April 2022].