# congressional_tweet_neural_net
CS461 Intro to AI Project #3


### Data preparation:  
What did you do to prepare your data? What categories did you collapse? 
What standardizations, if any, did you employ? Why did you select those? Basically, 
describe what you did to get your data ready. NOTE: This may be one of the larger 
sections of your report. In the 'real world,' data scientists spend about 3/4 of their 
time curating, cleaning, filtering, and preparing data.   

To get my data ready, I used the Pandas dataframe CSV read-in function to format the raw data. From there, I skipped the first line of headers/column labels and read everything else in as it was.  
I was getting a lot of issues with the NaN (null) values from both the 'year' columns in the testing & training datasets, so I went ahead and popped those columns off of the pandas dataframes. I also just didn't find the years that tweets took place to be important information in deciding their political party. I'm sure you could use that data for this problem (e.g. political stances change over time within parties), but I just didn't.  
Overall, most of my time was formatting data, learning about tensorflow and necessary data structures, and what needed to be converted to other data structures. Definitely way more than 3/4 of my time.

### Network configuration: 
How is your network set up? How many layers? How many neurons 
in each? Did you try any nonlinear features (connecting outputs to inputs more than one 
layer ahead)? (There's probably no need for that, but if you did it, talk about it.) This 
data doesn't map to a 2-d structure, and each item is independent (they're not a series), 
so there's no need for convolutional or recurrent features.  

This is all sufficiently abstract and difficult to understand. I will admit that this 
program runs and 'works,' but I don't completely understand everything that's happening. So, from my understanding, there are 14 layers (listed below).
I did not try any nonlinear features; I really wanted to focus on having something to turn in that wasn't completely broken. 

[<keras.engine.input_layer.InputLayer at 0x18fe5aa40>,
 <keras.engine.input_layer.InputLayer at 0x15f278f70>,
 <keras.engine.input_layer.InputLayer at 0x18fe5bca0>,
 <keras.engine.input_layer.InputLayer at 0x150817df0>,
 <keras.layers.preprocessing.string_lookup.StringLookup at 0x18feba3b0>,
 <keras.layers.preprocessing.string_lookup.StringLookup at 0x184684790>,
 <keras.layers.preprocessing.normalization.Normalization at 0x18fe5abf0>,
 <keras.layers.preprocessing.normalization.Normalization at 0x18fe6bd30>,
 <keras.layers.preprocessing.category_encoding.CategoryEncoding at 0x18fe809a0>,
 <keras.layers.preprocessing.category_encoding.CategoryEncoding at 0x15efe2230>,
 <keras.layers.merge.Concatenate at 0x18fe59300>,
 <keras.layers.core.dense.Dense at 0x18fe5a200>,
 <keras.layers.core.dropout.Dropout at 0x18fe59ff0>,
 <keras.layers.core.dense.Dense at 0x1846855a0>]

### Validation strategy:  
How did you divide your data into training, test, and validation 
sets? What validation strategies did you use? If you used k-fold validation, what was k? 
How did you lower the risk of overtraining?

I divided my data into an 80/10/10 split (training/test/validation). I unfortunately did not use k-fold validation.  
As for reducing the chance of overtraining, I lowered the quantity of epochs. It seemed to me that my system memorized/learned the training data fairly well after only the third epoch. Something I would have continued to do would be to toy around with the size and quantity of epochs.  

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

I think I may have had too many epochs and overtrained a little.
### References:   
[1] TensorFlow. 2022. Classify structured data using Keras preprocessing layers  |  TensorFlow Core. [online] Available at: <https://www.tensorflow.org/tutorials/structured_data/preprocessing_layers> [Accessed 4 May 2022].  
[2] TensorFlow. 2022. Load a pandas DataFrame  |  TensorFlow Core. [online] Available at: <https://www.tensorflow.org/tutorials/load_data/pandas_dataframe> [Accessed 1 May 2022].  
[3] Python, R., 2022. Practical Text Classification With Python and Keras – Real Python. [online] Realpython.com. Available at: 
<https://realpython.com/python-keras-text-classification/> [Accessed 20 April 2022].   
