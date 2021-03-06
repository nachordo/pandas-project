# Shark attacks: a pandas project

In this exercise we worked with a Global Shark Attack File dataset as found in the Kaggle webpage.

https://www.kaggle.com/teajay/global-shark-attacks/version/1

The objective of this mini-project is to do an exercise to clean this messy dataset. This will allow us to perform an analysis of the shark incident information. With the cleaned dataset, the objective is to visualize this data using matplotlib and seaborn to better draw a series of concrete conclusions from this noisy information.

In my work I will try to understand the nature of the different types of shark attack incidents using a word frequency analysis. This is, without the need to spend days and days reading the injuries reports and the description of the activities related to the shark incident, to automatically mine information about the nature of the shark attacks and its circumstances. To test this, I will check the hypotheses that provoked incidents are related to fishing (rather than vandalism, as the name of the incident type could suggest), and that almost all surfing incidents are unprovoked incidents.

In this readme, I will provide a summary of the data cleaning process and the analysis performed. In the jupyter-notebooks in the folder named "your-code" it is listed step by step all the processes related to this project.

The data-clean file describes the data cleaning process, while the data-wrangling one shows the visualization and analysis.

![Shark attack](images/shark.jpg)


## Data cleaning

As downloaded from the Kaggle site, this dataset is very messy, but with only a few commands we can transform this file into a valuable dataset. I conducted this with a diverse set of tools in Python, as Pandas or Regex. I identified repeated columns and others without information. I corrected typos replacing text and obtained data from columns to create others. From the reports I cleaned the data to obtain species information when available.

Finally, there is a fraction of information that is not reliable and only introduces noise. To handle this either I labeled these unreliable datapoints accordingly or dropped it to create a valuable and reliable dataset to visualize and analyze.



## Visualization

With the information from the cleaned file, I plotted various columns of the dataset to obtain a broad description of the shark attacks available information. Here I list some properties of the data.

- The number of shark incidents recorded is growing constantly since the beginning of the reporting, except for one spike of shark incidents around 1960.
- The vast majority of the people involved with shark attacks are men.
- More people survive these attacks than die from shark incidents.
- The vast majority of the incidents are unprovoked, but both unprovoked incidents and sea disasters show the highest rates of fatality.
- There is a higher shark incident rate in summer time of the northern hemisphere.
- The countries with the most recorded cases are USA, Australia and South Africa. The rest of the countries have less than 500 reported incidents since the XIX century.
- Normally there is no available information about the shark species, but when reported, the three species most frequent are White, Tiger and Bull sharks, in that order.



## Word frequency

By computing the word frequency of the activity and injuries reports in the dataset, we can obtain the nature of the sharks attacks in the different types reported (unprovoked, provoked, boat related, sea disasters and unknown ones). Below I show some of the highlights of the results that can be obtained just looking at the word frequency:

- The majority of the words in unprovoked incidents are related to water activities (surfing, swimming, diving,...) and followed by fishing (fishing, spearfishing,...). There are many repetitions of the word fatal (as in sea disasters) compared with other categories. Sea Disasters, followed by Unprovoked incidents, show the highest fatality rates among all categories.
- Sea Disaster: These are more related to boat sanks and war events. In the injuries reports, the most common word is fatal. In this category, the mortality rate is the highest, so even if we wouldn't have the mortality, this would give us a hint
- Provoked: The most frequent words are related to fishing activities.
- Boating: As in the previous category, the most frequent word is fishing.

![Word frequency](images/wf.png)

## Check with hypothesis

After obtaining the information from the word frequencies, I test the hypotheses that provoked incidents are fishing-related in most cases, and that shark attacks related to surfing are unprovoked in general. Using Regex and Pandas, I labeled every shark attack related to these activities, and then checked that these hypotheses based on the word analysis are true.

## Final Thoughts

Even considering the very limited time to perform analysis on this dataset, and just conducting only a few data cleaning and analysis techniques, we can obtain valuable and concrete information about shark incidents using word frequency. The tools that are available in Python, that I applied only some of them in this exercise, have a lot of potential for researching information in large datasets, that with classic approaches are impossible to handle.




