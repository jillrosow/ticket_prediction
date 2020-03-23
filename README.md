# Citation prediction
 Files included: 
    <ul>
        <li>Python Jupyter Notebook: contains the full code and visualizations for data cleaning, wrangling, analysis, visualization, and predictive modeling.</li>
        <li>Slide Deck: Presentation of the project in powerpoint form</li>
        </ul>

Summary
Records of over 250,000 police pull-overs in the state of Vermont between the years 2010-2015 were analyzed alongside various features such as driver demographics, location information, and datetime information. Findings:

1. Introduction
Problem statement:
In today’s society, there is an increasing dialogue around policing and community-police relations. As a result, it is increasingly important to ensure officers are acting justly in routine police pull-overs. Using features such as the time of an incident, date, race, and which police force is responsible for the citation, one may be able to predict or anticipate the outcome of a certain traffic incident.

This problem is important because if there is a bias within the police force, it can possibly be narrowed down to a specific department and corrected. Additionally, if a certain instance is common and predictable through specific features, it can help a police force focus on proper preventative measures. Through an accurate predictive model, this could be useful as a way to make sure police departments are accurately and unbiasedly giving proper citations to perpetrators, which would result in a more just and fortified law enforcement, and potentially a better relationship between the community and police.

The dataset:
I acquired the dataset from Enigma Public, which is a website dedicated to providing information to the open public derived from local, state, and federal governments as well as universities, NGOs, and nonprofits. The direct link to the dataset is as follows: https://public.enigma.com/datasets/vermont/a34af967-056f-48e6-8838-c511d795f3ec

The dataset contains traffic stop outcomes from 14 police departments in Vermont along with other relevant stop data such as demographics and incident specific information collected between the years 2010 and 2015.

During the data exploration phase, I saw a clear bias and skew in data toward certain features. For example, approximately 95% of our data from ‘driver_race’ consisted of white people, whereas the remaining 5% involved people of at least three other races. This particular imbalance is logical, since the state of Vermont as a whole has an overwhelming population of cauasian descent according to the U.S. Census Bureau from 2018. However, the most important observation that I made was when I uncovered a large class imbalance in ‘stop_outcome’; a decision was made to drop the rare classes ‘Arrest for Violation’, ‘Warrant Arrest’, and ‘Verbal Warning’, which only accounted for 1.19% of the data. As a result, I turned the classification into a binary problem and kept ‘Written Warning’ (170,980) and ‘Citation’ (106,638), as these were the most prevalent categories in the class.

Questions of interest:
The following questions guided my data exploration and analysis:

How does stop outcome vary with driver age, race, and gender? Are there significant differences among groups?
Is there consistency across Vermont police departments in number of police pull overs and stop outcome? Does a specific police department make more stops than others?
Trends in stop outcome over time: time of day, day of week, month of year, yearly averages.
Is there a consistent relationship between violation type and stop outcome? We would expect this.

A random forest classifier was trained on the data and further optimized to produce an accuracy of 66% and an AUC of 69%.
