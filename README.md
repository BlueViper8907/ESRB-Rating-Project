# ESRB-Rating-Project
<br>- Course: Flatiron Data Science </br>
<br>- Pace: Self Paced </br>
<br>- Instructor: Jeff Herman </br>
<br>- Author: [Cody D. Freese](mailto:c_freese@ymail.com) </br>
![gamePile](https://user-images.githubusercontent.com/63601020/112144877-0b003500-8bb0-11eb-9923-1d8fbdf33564.jpg) </br>

# Overview:
Predict a Video Games ESRB rating & find a model that provides the highest level of confidence in classifiying and distinguishing E rating from M rating.

# The Data
Accompanying CSV's provided by Kaggle
- The data was packaged into separate train and test sets. Ratings ranged from E for Everyone, E10+/ET for Everyone 10 and up, T for Teen and M for Mature. Several factors, variables and scales of the factors weigh on a games ability to be scored and rated. With categories like Blood having several variations as Blood, Blood and Gore, Mild Blood and Animated Blood.

# The Process
I used Python in Jupyter Notebook to perform <a href=https://machinelearningmastery.com/classification-and-regression-trees-for-machine-learning/> Decision Tree </a> , <a href=https://machinelearningmastery.com/k-nearest-neighbors-for-machine-learning/> KNN </a> & <a href=https://machinelearningmastery.com/bagging-and-random-forest-ensemble-algorithms-for-machine-learning/> Random Forest </a> models to predict a video games rating and it's ability to distinguish between ratings.

# O - Obtain
I obtained the ESRB Rating dataset from Kaggle. If you want to get started on your own, <a href="https://www.kaggle.com/imohtn/video-games-rating-by-esrb"> for this repo.</a><br>

# S - Scrub
After importing all the data I checked it for null values, duplicates and any datatype errors that may present a problem in Exploratory Data Analysis or Machine Learning Modeling

# E - Explore
To get an idea of what the data was comprised of I represented the data with how many games were exclusive to each console and which were shared between both

![consoles](https://user-images.githubusercontent.com/63601020/112495230-18592300-8d5a-11eb-9eec-e3cd3ad9b270.png)

With the variety available in classifying a games rating I wanted to see how many ratings I was working with with a visual representation

![rating](https://user-images.githubusercontent.com/63601020/112495245-1b541380-8d5a-11eb-8935-799dfff310f4.png)

With only one variable really falling below the threshold of relavence I decided to leave all the available variables in for now

# M - Model
My final model I settled on a twice refined GridSearched Random Forest model. F1 Score was my most important metric as overall accuracy and ability for the model to rate games in the correct category and not categorize games in the wrong category.

![rfc_model](https://user-images.githubusercontent.com/63601020/112495351-34f55b00-8d5a-11eb-97b8-56dac7dc55a6.png)


# N - iNterpret
Text Wall

# Observations
Text Wall

# Future Work
Exploring the variables further, upon investigating the mysterious 'No_Descriptors' 

![no_descriptors](https://user-images.githubusercontent.com/63601020/112495425-450d3a80-8d5a-11eb-948f-e582dc78ede1.png)


# For More Information
See the full analysis in the Jupyter Notebook or review the presentation.
For additional info, contact me here:
[Cody D. Freese](mailto:c_freese@ymail.com)

# Bibliography
RetroPete. “Pile of Video Games.” 8-Bit Central, RetroPete, 21 May 2013, www.8-bitcentral.com/blog/2013/gameManuals.html. 
