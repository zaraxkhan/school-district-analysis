# School-District-Analysis
## Project Overview
Maria, the chief data scientist for a city school district, is responsible for analyzing all standardized test data to report and present insights
regarding performance trends and patterns. These insights will help others make strategic decisions at the school and district level. I will be aiding Maria with analyzing the data on student funding and standardized test scores. I am tasked with aggregating the data and showcasing trends in school performances. This analysis will assist the school board and super intendant to make decisions regarding the school budgets and priorities. However, after performing the original analysis, it has come to the attention of Maria's supervisor that there has been evidence of academic dishonesty for the grades of the Thomas High School ninth graders. Due to this, we will be reperforming the analysis and instead adding N/As to the scores for these reading and math grades. In this challenge, I will be rechecking how the analysis has been affected due to the academic dishonesty. 

## Results
With the help of Pandas and Jupyter Notebook, I have created many DataFrames to showcase the relationship between the student performances and the budget the school has been allocated per student. 

### How is the District Summary Affected?
Below is the original analysis for the district summary:

![original_district_summary](https://user-images.githubusercontent.com/105755095/176966099-f16b4853-b3e2-4fd4-a111-c1251dbf6eb6.png)

Now, below is the new district summary after cleaning up the ninth graders data from Thomas High School:

![cleaned_district_summary](https://user-images.githubusercontent.com/105755095/176966167-4500ec24-f355-49e2-880d-c74ee302081c.png)

From these dataframes, we can conclude that the averages for the district did go down:
- The average math score decreased by a point: from 79.0 to 78.9
- The percent passing math decreased from 75% to 74.8%
- The percent passing reading went down from 86% to 85.7%
- The overall passing has also decreased from 65% to 64.9%

### How is the School Summary Affected?
Below is the original analysis for the school summary:

![original_school_summary](https://user-images.githubusercontent.com/105755095/176967602-aa25d0cc-4489-4355-bef3-e760b58d4063.png)

Below is the cleaned version of the school summary:

![cleaned_school_summary](https://user-images.githubusercontent.com/105755095/176967656-2747f01d-0f40-41e6-9f5c-6091c3104d9f.png)

From these dataframes we can conclude that the summary for Thomas High School's results had a significant impact after taking care of the academic dishonesty.
- The averages of the reading and math scores did decrease, however it was not as significant as the rest of the data.
- The percentage of students overall passing has drastically decreased from 90.94% to 65.07%

### How Does Replacing the Ninth Graders’ Math and Reading Scores Affect Thomas High School’s Performance Relative to the Other Schools?
After replacing the math and reading scores of the ninth graders at THS with only the averages of the 10th-12th graders, the data seems to be less skewed. 

![retouched_school_summary](https://user-images.githubusercontent.com/105755095/176969026-a8160ff7-7c92-457e-96af-b967762385db.png)

- The overall passing rate for the school has gone back up to 90.63%. It dipped down to 65.07% when the 9th graders unofficial data was added because the dataframe considered all the 9th graders as non passing students as their scores stated "N/A" all around. 
- If we take away the Thomas High School's ninth grader data we can see that Thomas High School is back on top with very good averages being protrayed from the rest of the grade levels. 

### How Does Replacing the Ninth-grade Scores Affect the Following:
#### Math and Reading Scores by Grade
Original Math Scores:

![og_math_scores](https://user-images.githubusercontent.com/105755095/176970211-49636e10-067d-428d-a0f7-e6d75ce2e26a.png)

Orignial Reading Scores:

![og_reading_scores](https://user-images.githubusercontent.com/105755095/176970237-f535d230-4bf6-4d55-a26d-bdbe92d300e7.png)

Cleaned Math Scores:

![clean_math_scores](https://user-images.githubusercontent.com/105755095/176970255-0787efe9-6b9e-4ef8-b40a-7744ca06287a.png)

Cleaned Reading Scores:

![clean_reading_scores](https://user-images.githubusercontent.com/105755095/176970270-7a54e2c3-431a-4bce-b7a8-60b4ddd48c18.png)

These scores stayed the same for the rest of the data set. Even for Thomas High School the only thing that changed was that these 9th graders' scores now show Nan (for N/A) instead of the original dishonest scores of 83.6 and 83.7 for math and reading scores respectively. 

#### Scores by School Spending
Orignal Data:

![original_spending_summary](https://user-images.githubusercontent.com/105755095/176969451-3889f078-d709-479b-a36a-75e845bf6d2f.png)

Cleaned Data

![cleaned_spending_summary](https://user-images.githubusercontent.com/105755095/176969531-96286452-5c3c-4262-8397-aabb18bb4ae1.png)

These scores also remained the same for each spending range bin. When we cleaned out the 9th graders' scores, the overall spending summary did not change. 
THS is in the $631-645 spending range and those averages did not change.

#### Scores by School Size
Orignal Data:

![original_size_summary](https://user-images.githubusercontent.com/105755095/176969636-9d65f00a-ed89-4d06-bde1-cbccf2e45f3c.png)

Cleaned Data:

![cleaned_size_summary](https://user-images.githubusercontent.com/105755095/176969664-10c28c65-4775-44ae-a61a-171ccd6b4931.png)

THS is in the medium school size bin, and from this data it looks like the averages based on the overall school sizes were not effected at all. 
#### Scores by School Type
Orignial Data:

![Original_type_summary](https://user-images.githubusercontent.com/105755095/176969712-b7dc4d3d-6afe-48da-ac5c-ded339f17518.png)

Cleaned Data:

![Cleaned_type_summary](https://user-images.githubusercontent.com/105755095/176969695-d0e7b922-f500-40f5-af22-b066114e748f.png)

THS is a Charter school and from the summaries above, it looks like taking out the 9th graders' scores did not affect the overall scores based on the type. 

## Summary
If we really look into the data, overall, the summaries stay the same as the original. This is because after we took away the 9th graders' scores from Thomas High School, they were not affecting the averages anymore. Instead, the scores now reflect the averages from 10th-12th graders attending THS. The averages change by .005 or less in most of the summaries which is not enough to affect the overall scores. However, it was a good call to reclean the data and reprocess the analysis as the numbers now accurately reflect the district and the board can use this data to allocate their fundings as needed. 
