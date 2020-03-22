[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Jaroslav-Tran/Himalayas_Analysis/master)

# Himalayas_Analysis
Analysis of mountain climbers activity in Himalayas (Focused on Mt. Everest)

## SUMMARY
This was a group project in the Data Science Analytics class I took during Fall 2019. As part of the class, we were supposed to develop our own research project using the knowledge and skills we have developed during the class (SQL, R, Statistical Models).

The key takeaways from this project are:
<ol> 
  <li> To increase chances of success: </li>
  <ul>
    <li> Avoid going solo even if you are a confident and experienced climber. (Although most likely, those kind of climbers do it for challenge) </li>
    <li> Use oxygen to increase the odds of success </li>
    <li> Choose winter/fall seasons over spring/summer season. This one is suprising but our hypothesis is that spring or summer seasons are not sage due to monsoons at that time. </li>
    <li> Average age matters. "Younger" expeditions have higher chance of succeeding. (Howeverm the coefficint there is low) </li>
  </ul>

<li> To avoid or decrease number of accidents </li>
  <ul>
    <li> Go on the expedition during spring/summer although it may decrease your likelihood of successful climb. most likely due to monsoon season. </li>
    <li> Avoid expedition with longer duration if you can. Based on our model, the expeditions without accident take 30 days on average, while those with accidents tend to be longer than that. </li>
  </ul>
</ol>

## INTRODUCTION:
For our analysis, we extracted data from Elizabeth Hawley´s expedition archives. This database is publicly available and is frequently updated with the most recent information.
<ul>
  <li> Peaks records: 465+ </li>
  <li> Expedition records: 10,300+ </li>
  <li> Member records: 76,300+ </li>
  <li> Literature records: 14,500+ </li>
</ul>

As the dataset contained a wide variety of variables, we extracted only those that we needed for this analysis:
<ul>
  <li> Success - Whether the expedition was successful </li>
  <li> Season - 0 = Spring/Summer, 1 = Winter/Fall </li>
  <li> Totmembers - Total members of the expedition excluding personnel such as sherpas, etc. </li>
  <li> Solo - Whether there was a solo mountaineer: If Totmembers > 1 then it is 0 otherwise 1 </li>
  <li> O2used - Whether the oxygen was used: 1 TRUE, 0 FALSE </li>
  <li> Nohire - Whether there was a hired personnel: 1 TRUE (Nobody hired), 0 FALSE </li>
  <li> Average_age - Average age of the people on the expedition. (Sum of expedition member ages / totmembers) </li>
  <li> Accident_syn - Accident occurence (1 = ACCIDENT, 0 = NO ACCIDENT) </li>
  <li> Smtdays - Number of days to summit </li>
  <li> Personnelratio - Hired personnel ratio (tothired/totmembers) </li>
  <li> Host - Host country (1 = Nepal, 2 = China) </li>
  <li> CardPoint - Cardinal Point (Qualitative value created from route1 column taking values N, S, E, W, SE, SW, NE </li>
</ul>

## QUESTIONS INVESTIGATED:
<p> My team used data analysis proccess to explore a data set answer questions we were interested on: </p>

<ul>
  <li> Q1: Which factors contribute to the success of an expedition to Mount Everest? </li>
  <li> Q2: What conditions impact the likelihood of accidents to occur? </li>
  <li> Q3: What is the seasonal impact on the traffic of different cardinal points? </li>
</ul>

## PROCESS OUTLINE:
We spend a portion of our time finding a suitable database before we formed these questions. For our analysis, we extracted data from Elizabeth Hawley´s expedition archives. This database is publicly available and is frequently updated with the most recent information.

Once we pulled all the data we needed, we analogically determined our target variables, features and appropriate model for each research question. 

Afterward, we processed and cleaned data (NA values, Missing Values, etc.) and then split and shuffled data into training and testing datasets (60:40 in my case). 

Finally, we run the models for each question and wrapped up a project by giving final recommendations/implications, estimated impact of each question and potential problems/drawbacks for each question.
