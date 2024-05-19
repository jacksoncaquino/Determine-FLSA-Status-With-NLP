# Determine FLSA Status With Natural Language Processing
Using predictive analytics based on job descriptions and natural language processing, these models will predict FLSA status for overtime eligibility, this time with 4 models instead of 2. Coded in Python with Jupyter Notebooks

## What is the FLSA?
Fair Labor Standards Act

FLSA determines:<br>
• Minimum Wage<br>
• Overtime pay<br>
• Youth employment standards

## How does the FLSA classify overtime pay?
Exempt employees are not eligible for overtime pay. They are paid salary, not hourly. Their salary has to be greater than $35k/year. These are usually Executives/management, administrators, higher level professionals. They are not required to log their work hours.
Non-Exempt employees, on the other hand, are eligible for overtime pay. They are required to log their work hours, paid overtime for any hour worked above 40 hours a week.

## What happens when we misclassify?
We incur several costs, such as back pay for unpaid overtime, attorney’s fees, lawsuits, and the costs associated with damaged employer brand reputation (higher costs of hiring, for example, as prospective applicants could be hesitant to apply if the company is seen as unethical).

## How does this classification process usually work in organizations?
When a new job profile needs to be created, HR consults with legal to determine exemption status. Legal or HR reads the job description, determines exemption status, and responds to the case.

## How does this project intend to change this process?
After taking a dataset with about 2000 rows and taking all the steps to clean the data and prepare for training, this time I used another report that contained job descriptions, tokenized and vectorized them and trained two additional models, one decision tree and one logistic regression, both based on the words of the job descriptions to determine overtime pay eligibility. The data was split into training data (80% of the data) and testing data (the remainder). 

## What are the results of the model?<br>
• Decision tree alone (previous project): 94% accuracy<br>
• Logistic regression alone (previous project): 82% accuracy<br>
• Combining both was the safest, but models agreed and got wrong in 3.6% of the cases<br>
• With the NLP models, the number of cases that the 4 models agreed to get the wrong answer fell to 1.5%<br>
• Cases where the 4 models did not agree: 16% (legal review)<br>

## What would be the Next Steps to implement these models?
• When implementing the models, run in parallel for six months to keep measuring accuracy<br>
• After that, add spot audit for 16% of the cases where all four models agree<br>
• Reserve money from these savings for legal fund<br>
