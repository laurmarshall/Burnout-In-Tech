# Burn Baby Burn
## Burnout in the Tech Industry
### Lauren Marshall, Data Scientist
[LinkedIn](https://www.linkedin.com/in/lauren-marshall-7603491b5/)|[GitHub](https://github.com/laurmarshall)|[Slides](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/Burnout%20in%20the%20Tech%20Industry.pdf)
## Background and Motivation
Burnout is the result of excessive and prolonged stress in the workplace. It impacts you physically, emotionally, and mentally. It has a negative impact on work performance as well.
Coined in the 1970’s by American psychologist Herbert Freudenberger, it is a relatively new concept. A general dfinition of burnout is the result of excessive and prolonged stress in the workplace. The impact it can have on a person includes symptoms such as lower productivity, fatigue, insomnia, detached relationships, vulnerability to illness, and many more. Burnout was recently recognized as a medical diagnosis, Burnout Syndrome, in 2019.

## Data
The datawas acquired from a SQL dataset from [Kaggle](https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry), consisting of three tables. The first table was a collection of the years the survey was conducted (2014, 2016-2019). The second table was a collection of all the 118 questions asked to participants. The third table included all of the participants' answers. The majority of the questions were openended, for example: 
- Do you believe your productivity is ever affected by a mental health issue? 
- Describe the conversation with coworkers you had about your mental health including their reactions.
As a result much of the data is non-numerical. Responses were not required and as a result there was a significant absence of responses. For example, in response to the question: Overall, how much importance does your employer place on physical health? 17% of the responses were null. In dealing with these values I decided to drop them instead of averaging. I couldn't assume why someone was choosing to not respond or that it would necessarily reflect an average.


## Exploratory Data Analysis

### Word Clouds
I started by generating a few WordClouds, one of which answers the prompt: Briefly describe what you think the industry as a whole and/or employers could do to improve mental health support for employees. 

Some examples of responses:
- They don't take it seriously
- raise awareness, talk about it to lessen the stigma
- Education and awareness, statistics, add supportive writing to the company handbook

The word cloud includes the top 25 responses. Some of the unique keys words that are worth noting include: support, awareness, need, better, culture, stigma, and help. These are important concepts for companies to think about. How does a company's culture impact burnout? Is there a stigma? How is awareness communicated? What are employees needing? What can a company do better to support employees?

![Supports for Mental Health](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/word%20cloud%20with%20employee%20supports.png)


The word cloud below was in response to the prompt: Describe the circumstances of the badly handled or unsupportive response.

Some examples of responses:
- During a discussion about "mental health first aider" at work, a coworker dismissed the whole idea, saying that "no one here suffers from Mental Health Disorder
- I was suffering depression and I was open about that, that is why my numbers fell, but then I started drinking too much and admitted myself into a detox/psych facility to get better... 5 days later I get out to find myself fired

There was a similar prompt: Describe the circumstances of the supportive or well handled response. Unfortunately, I was unable to make a word cloud for question because there were no responses. This brings up a couple of questions, is this because it was not a valid sample, were there actually no positive response, or is there another factor to consider.

![Negative Response](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Neagtive%20Burnout%20Response.png)


The next word cloud below was in response to the prompt: Describe the conversation with coworkers you had about your mental health including their reactions.

Some examples of responses:
- Spoke about my anxiety they were very supportive
- the coworker was comprehensive, empathetic and understanding
- They all seemed understanding and some even admitted to having some issues themselves
- I've discussed mental illness with coworkers not in my business unit whom I have a primarily social relationship with. Even then I speak in very vague terms ("I'm not doing great this week", "have some mental health stuff going on"). One of the coworkers I play board games with during lunch on Fridays has expressed concern when I'm not in the office for board games or for the weekly catered lunch. They've been supportive, but also had the deer-in-headlights "I have no clue what to say here" look that makes me hesitant to share in the future. I'm not comfortable sharing information about my mental health with the folks I work with on a daily basis.'

![Conversation about Mental Health with Coworkers](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Conversation%20about%20Mental%20Health%20with%20Coworkers.png)


Finally, the last word cloud was generated in response to the prompt: Describe the conversation you had with your employer about your mental health, including their reactions and what actions were taken to address your mental health issue/questions.

Some examples of responses:
- The conversation went well, he too suffers mental illness... however, I was just fired for having a mental illness episode and not being about to get my work done.
- My current manager will be retiring in the next few months. We've talked about my mental illness and related mental health issues, but I'd be a lot less comfortable talking about it with my new/next manager. During a period when I wasn't doing well, my manager didn't feel like they could ask about how I was doing, or about what kind of support would be helpful. They were relieved when I (without a direct ask from them) let them know that I was not actively suicidal. They talked through some options with me, and expressed that it would be okay for me to take a leave-of-absence for a mental illness (with proper documentation). I navigated setting up intermittent FMLA leave on my own, with the LOA company that our company outsources all LOA-related info to. Several months into this, my manager and my future manager let me know that HR is hustling to make an intermittent-LOA policy because no one else in the company of 10,000+ people has ever taken FMLA leave on an intermittent basis. I let them know that $outsource_company has been tracking my leave, and that they had no problems setting it up under the existing FMLA policies. I'm seriously considering negotiating down to part time work because I don't want to spend my energy navigating the medical/legal parts of the healthcare/leave system. I'd rather get paid for the work I can do well then fight for accommodation.

![Conversation about Mental Health With Employer](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Conversation%20With%20Employeer.png)


### Graphs
![Rating of Support for Mental Health in Tech](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Rating%20of%20Support%20for%20Mental%20Health%20in%20Tech.png)

The first graph I generated included responses to the question, what would you give the overall rating of support for mental health in tech. Though the survey start in 2014, not all of the questions where used over the five years. You can also see that there were significantly more responses in 2017 than the following years. On a range of 1, being the lowest, and 5, being the highest, the average is in the middle at 3. The data is skewed to the right for all three years. Ideally, this graph would be skewed to the left instead.


![Importance Placed by Employer on Mental Health](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Importance%20Placed%20by%20Employer%20on%20Mental%20Health.png)

This led to a more detailed exploration of the Importance placed by the Employer on Mental Health. Again, there was a larger dataset in 2017. Overall the peak for each year was in the middle at 5. The peak is double the majority of the other values. You could also argue that besides the peak, a lot of the data for 2018 and 2019 is uniform. From this data, 17% of the responses were null values. 

![Importance Placed by Employer on Physical Health](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Importance%20Placed%20by%20Employer%20on%20Physical%20Health.png)

I then created a similar detailed graph, but focused on the perceived importance employers placed on physical health. I noticed a different distribution from the last graph. The peak was still at five, but now there were significantly more values within a close proximity to the right of the peak (skewed left). Again, 17% of those surveyed did not give a response.


![Comparison of the Importance Placed By Employer](https://github.com/laurmarshall/Burnout-In-Tech/blob/main/images/Comparison%202019.png)

This led to my final graph, a comparison of mental and physical health for 2019, the most recent year in the data. As you can see the most popular response is 5, the average. Both are mental and physical health are relatively close. However for the rest of the values there is a noticeable difference from the left and right side. On the right all the physical health values are higher, whereas on the left, all of the mental health values are higher. This significance led me to my final conclusion.



## Conclusion
Both the perceived importance of mental health and physical health share the same peak. Outside of that value, physical health had a higher rating for all values to the right of the middle and mental health had a higher rating for all values to the left of the peak. In general this dataset brings up more questions than answers. 

## Questions and Future Study
How can a dataset with limited absence of responses be obtained to generate a hypothesis test? There were too many imbalanced classes.
How does the tech industry compare to other fields? Another [survey](https://www.teamblind.com/blog/index.php/2018/05/29/close-to-60-percent-of-surveyed-tech-workers-are-burnt-out-credit-karma-tops-the-list-for-most-employees-suffering-from-burnout/) suggests that 60% of people in the tech industry are struggling with burnout, compared to 44% of [physicians](https://www.ama-assn.org/practice-management/physician-health/physician-burnout-which-medical-specialties-feel-most-stress).
How can a measurable value be established for burnout? Since this survey is largely qualitative in nature it can be hard to measure. But on the otherhand, the responses are very telling and imformative of issues like stigma (which could be challenging to quantify) around mental health.
What are action responses that can be implemented with better data? The word clouds generated suggest that steps do need to be taken. Focusing on improving the culture, reducing stigma, and increasing awareness are a few ways companies can take a step forward the help reduce burnout in their employees.
