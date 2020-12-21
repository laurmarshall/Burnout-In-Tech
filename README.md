# Burn Baby Burn
## Burnout in the Tech Industry
## Lauren Marshall, Data Scientist
![LinkedIn](https://www.linkedin.com/in/lauren-marshall-7603491b5/)|![GitHub](https://github.com/laurmarshall)|![Slides]()
## Background and Motivation
Burnout is the result of excessive and prolonged stress in the workplace. It impacts you physically, emotionally, and mentally. It has a negative impact on work performance as well.
Coined in the 1970’s by American psychologist Herbert Freudenberger, it is a relatively new concept. A general dfinition of burnout is the result of excessive and prolonged stress in the workplace. The impact it can have on a person includes symptoms such as lower productivity, fatigue, insomnia, detached relationships, vulnerability to illness, and many more. Burnout was recently recognized as a medical diagnosis, Burnout Syndrome, in 2019.

## Data
The datawas acquired from a SQL dataset from ![Kaggle](https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry), consisting of three tables. The first table was a collection of the years the survey was conducted (2014, 2016-2019). The second table was a collection of all the 118 questions asked to participants. The third table included all of the participants' answers. The majority of the questions were openended, for example: 
- Do you believe your productivity is ever affected by a mental health issue? 
- Describe the conversation with coworkers you had about your mental health including their reactions.
As a result much of the data is non-numerical. Responses were not required and as a result there was a significant absence of responses. For example, in response to the question: Overall, how much importance does your employer place on physical health? 17% of the responses were null. In dealing with these values I decided to drop them instead of averaging. I couldn't assume why someone was choosing to not respond or that it would necessarily reflect an average.


## Exploratory Data Analysis
![Conversation With Employer](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Conversation%20With%20Employeer.png)
This word cloud was generated in response to the prompt: Describe the conversation you had with your employer about your mental health, including their reactions and what actions were taken to address your mental health issue/questions.

![Rating of Support for Mental Health in Tech](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Rating%20of%20Support%20for%20Mental%20Health%20in%20Tech.png)
The first graph I generated included responses to the question, what would you give the overall rating of support for mental health in tech. Though the survey start in 2014, not all of the questions where used over the five years. You can also see that there were significantly more responses in 2017 than the following years. On a range of 1, being the lowest, and 5, being the highest. The average is in the middle, but the data is skewed to the right.


![Importance Placed by Employer on Mental Health](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Importance%20Placed%20by%20Employer%20on%20Mental%20Health.png)
This led to a more detailed exploration of the Importance placed by the Employer on Mental Health. Again, there was a larger dataset in 2017. Overall the peak for each year was in the middle at 5, double the majority of the other values. You could also argue that besides the peak, a lot of the data for 2018 and 2019 is uniform. From this data, 17% of the responses were null values. 

![Importance Placed by Employer on Physical Health](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Importance%20Placed%20by%20Employer%20on%20Physical%20Health.png)
I then created a similar detailed graph, but focused on the perceived Importance employers placed on physical health. I noticed a different distribution. The peak was still at five, but now there were significantly more values within a close proximity to the right of the peak. Again, 17% of those surveyed did not give a response.


![Comparison of the Importance Placed By Employer](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Comparison%202019.png)
This lead to my graph, a comparison of mental and physical health for 2019, the most recent year in the data. As you can see the most popular response is 5, the average. Both are relatively close. However for the rest of the values there is a noticeable difference from the left and right side. This significance led me to my final conclusions.



## Conclusion
Both the perceived importance of mental health and physical health share the same peak. Outside of that value, physical health had a higher rating for all values to the right of the middle and mental health had a higher rating for all values to the left of the peak. In general this dataset brings up more questions than answers. 

## Questions and Future Study
How can a dataset with limited absence of responses be obtained to generate a hypothesis test? There were too many imbalanced classes.
How does the tech industry compare to other fields? Another ![survey](https://www.teamblind.com/blog/index.php/2018/05/29/close-to-60-percent-of-surveyed-tech-workers-are-burnt-out-credit-karma-tops-the-list-for-most-employees-suffering-from-burnout/) suggests that 60% of people in the tech industry are struggling with burnout, compared to 44% of ![physicians](https://www.ama-assn.org/practice-management/physician-health/physician-burnout-which-medical-specialties-feel-most-stress).
How can a measurable value be established for burnout? Since this survey is 
What are action responses that can be implemented with better data? The word clouds generated suggest that steps do need to be taken. Focusing on improving the culture, reducing stigma, and increasing awareness are a few ways companies can take a step forward the help reduce burnout in their employees.
