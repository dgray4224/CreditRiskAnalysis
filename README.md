# CreditRiskAnalysis
This project is done in R. We use machine learning algorithms to model whether a loan applicant is a good or bad credit risk.


to see html output, visit: https://dgray4224.github.io/CreditRiskAnalysis/

Tableau Dashboard:  https://public.tableau.com/views/Loan_prediction_16884892991690/Dashboard3?:language=en-US&:display_count=n&:origin=viz_share_link
<div class='tableauPlaceholder' id='viz1688655985684' style='position: relative'><noscript><a href='#'><img alt='Dashboard 3 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Q7&#47;Q7NP4PRS2&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='path' value='shared&#47;Q7NP4PRS2' /> <param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Q7&#47;Q7NP4PRS2&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1688655985684');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='800px';vizElement.style.height='827px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='800px';vizElement.style.height='827px';} else { vizElement.style.width='100%';vizElement.style.height='1577px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>            
# Credit Risk Analysis

### Introduction
  The purpose of this credit risk analysis is to evaluate the creditworthiness of a borrower and assess the risk associated 
  with offering a loan to them. In today's economy, lending institutions are exposed to a variety of risks, including credit 
  risk, which can result in significant financial losses. Therefore, it is critical for lenders to conduct a thorough credit 
  risk analysis before extending credit to any borrower. 
	In conducting this analysis, we have employed various machine learning techniques to analyze German financial data from the 
  UC Irvine Machine learning laboratory. The results of this analysis are aimed to inform decision makers on whether or not to 
  offer a loan based on specific features of candidates. 
 	The following analysis is structured to present our findings and recommendations in a clear and concise manner. The central 
  questions that guide this analysis are: 
1.	Which classification model best fits the data? Determined by (Accuracy, Specificity, etc.)?
2.	What attributes are significant in determining whether an applicant is a good or bad credit risk?
3.	Which type of applicants should the bank accept based on your findings?
4.	Which type of applicants should the bank reject based on your findings? 
	As we answer these questions, we hope that our analysis can help banks lead to more informed decision making when 
  evaluating a borrower's risk profile. 
### Data
  The original data set we used was taken from UCI Machine Learning repository and was titled “German Credit Data” [1]. The 
  specific data set we used for this analysis was a modified version of this original data set. We got this data set from 
  Kaggle [2], an online community of data scientists and machine learning practitioners who find and publish data sets. 
  The original data set contained 20 variables and 1000 observations. The modified data set, which we used, had only 11 
  variables and 1000 observations. 
	The variables included in our data set are: ID, Age, Sex, Job, Housing, Saving account, Checking account, Credit amount, 
  Duration, Purpose, and Risk. 
### Variable Information
1.	Age (Numeric)
2.	Sex (Character: male, female)
3.	Job (Numeric: 0- unskilled and non-resident, 1- unskilled and resident, 2- skilled, 3- highly skilled)
4.	Housing (Character: own, rent, or free)
5.	Saving account (Character: NA, little, moderate, quite rich, rich)
6.	Checking account (Character: NA, little, moderate, rich)
7.	Credit amount (numeric: in Deutsch Mark(German currency))
8.	Duration (numeric: in months)
9.	Purpose(Character: car, furniture/equipment, radio/TV, domestic appliances, repairs, education, business, vacation/other)
10.	 Risk (Character: good, bad)
 	Before beginning our analysis, we noticed that the “Checking accounts” and “Saving accounts” columns had 394 and 183 “NA” 
  values, respectively. We made the decision to change these “NA” values to “none”. Furthermore, we want to note that 
  409/478 applicants who had “NA” values in Saving accounts or Checking accounts were identified as good risk clients. We will 
  need to replicate this ratio in our train/test split. 


### References
[1]  UCIrvineMachineLearningRepositoryGermanCreditData. https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+ data)  

[2] Kaggle. https://www.kaggle.com/datasets/uciml/german-credit
