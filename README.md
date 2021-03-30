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

![consoles](https://user-images.githubusercontent.com/63601020/112495230-18592300-8d5a-11eb-9eec-e3cd3ad9b270.png)

To get an idea of what the data was comprised of I represented the data with how many games were exclusive to each console and which were shared between both

![rating](https://user-images.githubusercontent.com/63601020/112495245-1b541380-8d5a-11eb-8935-799dfff310f4.png)

With the variety available in classifying a games rating I wanted to see how many ratings I was working with with a visual representation

![heatmap](https://user-images.githubusercontent.com/63601020/112990747-64c6a900-9134-11eb-8eff-02c1eca825a5.png)

Along the bottom row we can see how the esrb rating is coorelated to the variables; some having a positive and negative influence. A curious note we'll come back to is the strong coorelation between the rating and a variable called No_Descriptors

# M - Model
While running different types of models I decided per the metrics I was targeting that my final model would be a Random Forest model. F1 Score was my most important metric as overall accuracy and ability for the model to rate games in the correct category and not categorize games in the wrong category.
![rfc_model](https://user-images.githubusercontent.com/63601020/112495351-34f55b00-8d5a-11eb-97b8-56dac7dc55a6.png)


# N - iNterpret

A table better describing the above model. F1 Score was determined to be my most important metric, as I wanted both the accuracy in ability to correctly predict a games rating, but also a high recall so as to not accidently rate a game E when it really should be rated M.

\begin{table}[]
\begin{tabular}{lllll}
                              & Precision                 & Recall                    & F1-Score                  & Support                  \\ \hline
\multicolumn{1}{|l|}{0 = E}   & \multicolumn{1}{l|}{93\%} & \multicolumn{1}{l|}{99\%} & \multicolumn{1}{l|}{96\%} & \multicolumn{1}{l|}{138} \\ \hline
\multicolumn{1}{|l|}{1 = ET+} & \multicolumn{1}{l|}{74\%} & \multicolumn{1}{l|}{85\%} & \multicolumn{1}{l|}{79\%} & \multicolumn{1}{l|}{143} \\ \hline
\multicolumn{1}{|l|}{2 = T}   & \multicolumn{1}{l|}{84\%} & \multicolumn{1}{l|}{78\%} & \multicolumn{1}{l|}{80\%} & \multicolumn{1}{l|}{268} \\ \hline
\multicolumn{1}{|l|}{3 = M}   & \multicolumn{1}{l|}{89\%} & \multicolumn{1}{l|}{82\%} & \multicolumn{1}{l|}{85\%} & \multicolumn{1}{l|}{163} \\ \hline
                              &                           &                           &                           &                          \\
Weighted Average              & 85\%                      & 86\%                      & 85\%                      & 712                      \\
Accuracy: 84.41\%             &                           &                           &                           &                         
\end{tabular}
\end{table}



# Observations
The model is effective at distinguishing between the extremes in the rating system, and shows subsequent robustness in its ability to to correctly rate games rated T. Some bleedthough and mislabeling occurs mostly between the steps of classes E and ET, ET and T. A few rare instances of E being rated T. Although in the past some games actual ratings have been called into question. Legend of Zelda: Twilight Princess and Super Smash Bros. Melee & Brawl both being rated T for teen when I myself can remember playing games would have been classified the same at the age of 8. Cartoon and mischief humor that blurs the lines between the lower classes of rating. See supplemental article below about other games that have been mislabeled for better or for worse.

# Future Work
Exploring the variables further, upon investigating the mysterious 'No_Descriptors' and its strong influence on E rated games.

![no_descriptors](https://user-images.githubusercontent.com/63601020/112495425-450d3a80-8d5a-11eb-948f-e582dc78ede1.png)


# For More Information
Article from TheGamer about mislabeled games. 
https://www.thegamer.com/classic-games-esrb-rating-wrong/

See the full analysis in the Jupyter Notebook or review the presentation.
For additional info, contact me here:
[Cody D. Freese](mailto:c_freese@ymail.com)

# Bibliography
RetroPete. “Pile of Video Games.” 8-Bit Central, RetroPete, 21 May 2013, www.8-bitcentral.com/blog/2013/gameManuals.html. 

Sharp, Nathan. “10 Classic Games That Probably Have The Wrong ESRB Rating.” TheGamer, 15 June 2019, www.thegamer.com/classic-games-esrb-rating-wrong/. 
