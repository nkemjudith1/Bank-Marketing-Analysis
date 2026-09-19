# Bank Marketing Data Analysis and Prediction

## Table Contents

- [Introduction](Introduction)
- [Problem Statement](Problem-Statement)
- [Aim and Objectives](Aim-and-Objectives)
- [Methodology](Methodology)
- [Descriptive Analysis](Descriptive-Analysis)
- [Results and Discussion](Results-and-Discussion)
- [Ethical Guidelines](Ethical-Guidelines)
- [Conclusion and Recommendation](Conclusion-and-Recommendation)


### Introduction
To enable a shift from intuition-driven to evidence-based decision-making, banking institutions must analyze customer behavior toward their products and services using effective marketing strategies. This forms the basis of this study.

### Problem Statement
Despite large outreach efforts, low subscription rates remain a challenge. The bank lacks efficient targeting strategies to improve campaign effectiveness.

### Aim and Objectives
The main aim is to improve subscription rates and the objectives are:
- Analyze client behavior in term deposit marketing campaigns
- Identify patterns and build predictive models
- Provide segmentation and contact strategy insights
- Explore temporal trends in marketing campaign success
- Create customer profiles
- Improve marketing strategy

### Methodology
<img width="722" height="539" alt="Methodology" src="https://github.com/user-attachments/assets/4afc9b62-ade8-4406-8536-676e17d07bb7" />

### Descriptive Analysis 
- Source: Portuguese Bank Marketing Campaigns
-  Records: 45,211 clients who were contacted through phone calls; 17 features.
-  Variables: Numeric and Categorical Features
-  Data Types: Integers and object

<img width="637" height="477" alt="Bank dataset on Colab" src="https://github.com/user-attachments/assets/1c99cc42-5a98-4cc4-a6e1-0d6041a8cf46" />



The bank dataset includes detailed information on client:
- Demographics: age, job, marital, and education
- Financial status:  Has credit in default, housing loan, or a personal loan
- Past interactions: Contact type, month, day_of_week, and duration
- Campaign History: Number of contacts made during and before this campaign
- Pdays: Number of days passed since the client was last contacted from a previous campaign
- Previous: Number of contacts made before this campaign and for this client (numeric).
- Poutcome: Outcome of the previous marketing campaign 
- Target Variable ‘y’: indicates if the client subscribed to a term deposit (yes or no)

<img width="634" height="478" alt="Summary statistics" src="https://github.com/user-attachments/assets/8cb64f16-91f0-49af-b36c-c6a72c8a7b9b" />


<img width="636" height="479" alt="Boxplots of Numeric variables" src="https://github.com/user-attachments/assets/758cdc41-78f1-437a-9934-2982ffa3fb22" />

# Results and Discussion

### Exploratory Data Analysis Visualization

<img width="636" height="480" alt="EDA" src="https://github.com/user-attachments/assets/2d04d785-ccdb-4ada-a210-c408c66e68c4" />

Highest term deposit subscribers: 
- 60+ years
- 25-40 years
- Clients aged 60 years and above are more likely to subscribe to the term deposit, followed by clients in the 25-40 years age bracket.


### Segmentation Analysis
Students, singles, and highly educated (tertiary) clients showed higher subscription rates, while loan holders were less likely to subscribe.

<img width="635" height="477" alt="Segmentation Analysis" src="https://github.com/user-attachments/assets/c9268651-4271-4fcb-a1b1-00326d4f2a52" />


### Temporal Trends
Best and worst days to reach clients based on day of week and month:

- Best days: Monday, Tuesday, Wednesday and Sunday. This are the best days to reach clients, because they may be more open to financial decisions at the start of the week.
- Worst: Friday, and Saturday. Possibly because it is a weekend and people are unwinding.

<img width="637" height="479" alt="Temporal Trends" src="https://github.com/user-attachments/assets/43b9ecc6-5be5-43d7-b888-89dfecb0ba1a" />


### Customer Profiling
#### High Value Customer Segments: Shows high subscription rate
- Student
- Retired
- Singles
- Tertiary-educated
- No loan/default history
- contacted recently via cellular (mobile)
- Called early in the week (Sun, Mon, Tue, and Wed) and in (May, or September) month

#### Low Value Customer Segments: Tend to have lower response rates:
- Blue-collar jobs
- Married + low education (primary)
- Clients with multiple loans
- Clients with multiple loans

  

### Contact Strategy Evaluation
Duration
- Long calls (>4–8 minutes): Customers who engaged in longer conversations are more likely to convert, ask questions, receive explanations, and ultimately say "yes".
- Short calls (<1 minute) rarely convert. Quick calls often indicate disinterest, busy customers, or early termination ("not now", "don't call again").



Poutcome

<img width="636" height="481" alt="Contact strategy evaluation" src="https://github.com/user-attachments/assets/0cec5732-af0e-4532-808c-b2b63aca9521" />


Contact-Related Insights
Cellular contact yields higher conversion than telephone indicating that mobile outreach works well. 



### Ethical Guidelines
Ethical considerations are central to any data analytics project, particularly when working with customer information. 
- The dataset contains no personally identifiable information (PII)
- Methods such as SMOTE were used to reduce model bias toward the majority class
- No variables suggesting sensitive attributes (race, ethnicity, religion) were used
- Care is taken to prevent discrimination based on non-relevant demographic attributes (e.g., age or marital status) when interpreting or   applying insights
- Results are communicated honestly, emphasizing limitations such as class imbalance. Model predictions are not presented as absolute       truths but as supportive tools for decision-making



 ### Conclusion
Customer behaviour varies strongly across demographic and financial segments. The analysis reveals:
- Subscription rates are low (11.7%) and many customers were contacted via cellular method
- Many clients were never contacted in previous campaigns (pdays=871)
- Certain customer profiles, such as students and singles with tertiary education, shows high subscription likelihood.
- March, September, October, and December are the most successful months for conversion, with Sunday, Monday, Tuesday, and Wednesday        yielding the highest conversions.
- Customers with a previous successful campaign outcome are prime targets for re-engagement.
- Call duration and past outcomes are critical behavioural predictors
- Predictive models with AUC ~0.85 show strong classification capability


Ideal Target Customer
Young students or retirees, singles, no loans, contacted recently via cellular preferably in March/September and on Sundays to Wednesdays, with past positive outcomes and long call engagement. 



### Recommendation
- Prioritize high-value customer segments for targeted outreach e.g., students, retirees, singles, higher education, and clients without loans.
- Focus contact in high-performing months/days (Sun–Wed, March/Sept)
- Improve agent training to increase call engagement duration
- Use predictive models to rank and target high-probabaility leads
- Prioritize cellular contacts over telephone calls, keeping calls concise yet engaging
- Prioritize customers with previous successes through loyalty offers or personalized 	communication
- Reduce “unknown” values in attributes such as job, education, contact, and previous outcome (poutcome) by improving data collection       processes.


