# Determine FLSA Status With Categorical Data
Using predictive analytics based on existing jobs within our job structure, these models will predict FLSA status for overtime eligibility. Coded in Python with Jupyter Notebooks.

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
After taking a dataset with about 2000 rows and taking all the steps to clean the data and prepare for training, the model was split into training data (80% of the data) and testing data (the remainder). Two models were created: a decision tree and a logistic regression. 

## What are the results of the model?<br>
• Decision tree alone: 94% accuracy<br>
• Logistic regression alone: 82% accuracy<br>
• Combining both is the safest<br>
• Legal reviews would fall by 83% (only when the two models do not agree)<br>
• With the two models and legal review, accuracy would be 96.4%<br>

I still do not consider this accuracy good enough for model deployment because the 3.6% of the new jobs the two models would confidently agree and would get it wrong make me nervous about the legal risk, so at the end I decided to work on another project to use the job descriptions and natural language processing (NLP) to train other models to see if the accuracy would go up.
