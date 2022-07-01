# School-District-Analysis
## Project Overview
Maria, the chief data scientist for a city school district, is responsible for analyzing all standardized test data to report and present insights
regarding performance trends and patterns. These insights will help others make strategic decisions at the school and district level. I will be aiding Maria with analyzing the data on student funding and standardized test scores. I am tasked with aggregating the data and showcasing trends in school performances. This analysis will assist the school board and super intendant to make decisions regarding the school budgets and priorities. However, after performing the original analysis, it has come to the attention of Maria's supervisor that there has been evidence of academic dishonesty for the grades of the Thomas High School ninth graders. Due to this, we will be reperforming the analysis and instead adding N/As to the scores for these reading and math grades. In this challenge, I will be rechecking how the analysis has been affected due to the academic dishonesty. 

## Results
With the help of Pandas and Jupyter Notebook, I have created many DataFrames to showcase the relationship between the student performances and the budget the school has been allocated per student. 

### How is the district summary affected?
Below is the original analysis for the district summary:

![original_district_summary](https://user-images.githubusercontent.com/105755095/176966099-f16b4853-b3e2-4fd4-a111-c1251dbf6eb6.png)

Now, below is the new district summary after cleaning up the ninth graders data from Thomas High School:

![cleaned_district_summary](https://user-images.githubusercontent.com/105755095/176966167-4500ec24-f355-49e2-880d-c74ee302081c.png)

From these dataframes, we can conclude that the averages for the district did go down:
- The average math score decreased by a point: from 79.0 to 78.9
- The percent passing math decreased from 75% to 74.8%
- The percent passing reading went down from 86% to 85.7%
- The overall passing has also decreased from 65% to 64.9%

### How is the school summary affected?
Below is the original analysis for the school summary:

![original_school_summary](https://user-images.githubusercontent.com/105755095/176967602-aa25d0cc-4489-4355-bef3-e760b58d4063.png)

Below is the cleaned version of the school summary:

![cleaned_school_summary](https://user-images.githubusercontent.com/105755095/176967656-2747f01d-0f40-41e6-9f5c-6091c3104d9f.png)

From these dataframes we can conclude that the summary for Thomas High School's results had a significant impact after taking care of the academic dishonesty.
- The averages of the reading and math scores did decrease, however it was not as significant as the rest of the data.
- The percentage of students overall passing has drastically decreased from 90.94% to 65.07%

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
After replacing the math and reading scores of the ninth graders at THS with only the averages of the 10th-12th graders, the data seems to be less skewed. 

![retouched_school_summary](https://user-images.githubusercontent.com/105755095/176969026-a8160ff7-7c92-457e-96af-b967762385db.png)

- The overall passing rate for the school has gone back up to 90.63%. It dipped down to 65.07% when the 9th graders unofficial data was added because the dataframe considered all the 9th graders as non passing students as their scores stated "N/A" all around. 
- If we take away the Thomas High School's ninth grader data we can see that Thomas High School is back on top with very good averages being protrayed from the rest of the grade levels. 

### How does replacing the ninth-grade scores affect the following:
#### Math and reading scores by grade
#### Scores by school spending
Orignal Data:

![original_spending_summary](https://user-images.githubusercontent.com/105755095/176969451-3889f078-d709-479b-a36a-75e845bf6d2f.png)

Cleaned Data

![cleaned_spending_summary](https://user-images.githubusercontent.com/105755095/176969531-96286452-5c3c-4262-8397-aabb18bb4ae1.png)

#### Scores by school size
Orignal Data:

![original_size_summary](https://user-images.githubusercontent.com/105755095/176969636-9d65f00a-ed89-4d06-bde1-cbccf2e45f3c.png)

Cleaned Data:

![cleaned_size_summary](https://user-images.githubusercontent.com/105755095/176969664-10c28c65-4775-44ae-a61a-171ccd6b4931.png)

#### Scores by school type
Orignial Data:

![Original_type_summary](https://user-images.githubusercontent.com/105755095/176969712-b7dc4d3d-6afe-48da-ac5c-ded339f17518.png)

Cleaned Data:

![Cleaned_type_summary](https://user-images.githubusercontent.com/105755095/176969695-d0e7b922-f500-40f5-af22-b066114e748f.png)

## Summary
