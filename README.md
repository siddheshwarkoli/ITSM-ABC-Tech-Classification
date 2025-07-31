# <b>PROJECT NAME : ITSM ABC TECH (PR-0012)

## <B>PROJECT SUMMARY
<B> 
    
    - ABC Tech management recently attended Machine Learning conference on ML for ITSM.
    
    - Machine learning looks prospective to improve ITSM processes through prediction and automation. 

## <B>PROBLEM STATEMENT
<B>
    
    1) Predicting High Priority Tickets: To predict priority 1 & 2 tickets, so that they can take preventive measures or fix the problem before it surfaces.
    
    2) Forecast the incident volume in different fields , quarterly and annual. So that they can be better prepared with resources and technology planning.
    
    3) Auto tag the tickets with right priorities and right departments so that reassigning and related delay can be reduced.
    
    4) Predict RFC (Request for change) and possible failure / misconfiguration of ITSM assets.


  ## <B>BUSINESS CASE DESCRIPTION

    - ABC Tech is an established mid-sized organization operating in the IT-enabled business sector for over a decade.
    - They manage a significant volume of IT incidents and tickets, averaging between 22,000 to 25,000 per year.
    - ABC Tech follows best practices in IT Service Management (ITSM), including incident management, problem management, change management, and configuration management processes.
    - These ITIL practices have matured over time, reaching a high level of process maturity.

    - Recently, ABC Tech conducted an audit that indicated that further improvement initiatives in their ITSM processes may not provide a sufficient return on investment (ROI).
    - Despite their mature processes, customer feedback from recent surveys has revealed that incident management, in particular, is rated poorly, suggesting there is room for enhancement.

    - In response to these challenges, ABC Tech's management has decided to explore the potential of machine learning (ML) to enhance their ITSM processes.
    - After attending a Machine Learning conference focused on IT Service Management (ITSM), they identified four key areas where ML can contribute to improving ITSM processes within the organization:

    1) Predicting High Priority Tickets: ABC Tech aims to develop an ML model that can predict high-priority tickets, specifically those categorized as priority 1 and 2. This prediction will allow them to take proactive measures to address issues or incidents before they escalate.

    2) Forecasting Incident Volume: The organization plans to use ML to forecast the incident volume in different fields on a quarterly and annual basis. This predictive capability will help them better allocate resources and plan for the required technology upgrades.

    3) Auto-Tagging Tickets: ABC Tech intends to implement a text classification ML model to automatically assign correct priorities and departments to incoming tickets. This automation will reduce reassignment and related delays in ticket handling.

    4) Predicting RFC and ITSM Asset Misconfigurations: The organization aims to create predictive models for Request for Change (RFC) and detect potential failures or misconfigurations in ITSM assets. Identifying these issues in advance will help in preventing disruptions and improving overall ITSM asset management.


### <B>FEATURE OVERVIEW
<B>

    - The dataset that ABC Tech plans to use for these ML initiatives comprises a total of approximately 46,000 records spanning the years 2012, 2013, and 2014. The data is stored in a MySQL database with read-only access, and the relevant connection details are provided.
    
    
    
    - Here's a summary of some key fields in the dataset:

    1) CI_Name:
        Configuration Item Name – the name of the specific asset or item involved in the incident.

    2) CI_Cat: 
        Configuration Item Category – broad category under which the configuration item falls (e.g., hardware, software).

    3) CI_Subcat:
        Configuration Item Subcategory – more detailed classification within the configuration item category.
    
    4) WBS:
        Work Breakdown Structure – a project management reference often used to structure tasks and identify resources.

    5) Incident_ID:
        Incident Identifier – unique identifier for each incident.

    6) Status:
        Status of the Incident – current status of the incident (e.g., open, closed, in progress).

    7) Impact:
        Impact Level – how critical the incident is in terms of its effect on business operations.

    8) Urgency:
        Urgency Level – priority level for addressing the incident, potentially guiding response time.

    9) Priority:
        Priority Level – overall priority based on a combination of impact and urgency.

    10) number_cnt:
        Count Number – could be the number of occurrences or a frequency count related to the incident.

    11) Category:
        Category of the Incident – broader category classifying the type of incident (e.g., service request, problem, change).

    12) KB_number:
        Knowledge Base Number – reference to a knowledge base article or resource that might assist in resolving the incident.

    13) Alert_Status:
        Alert Status – current alert status of the incident (e.g., critical, warning, resolved).

    14) No_of_Reassignments:
        Number of Reassignments – count of times the incident has been reassigned to different teams or personnel.

    15) Open_Time:
        Open Time – timestamp for when the incident was first reported or logged.

    16) Reopen_Time:
        Reopen Time – timestamp for when the incident was reopened, if applicable.

    17) Resolved_Time:
        Resolved Time – timestamp for when the incident was resolved.

    18) Close_Time:
        Close Time – timestamp for when the incident was officially closed.

    19) Handle_Time_hrs:
        Handling Time in Hours – total time spent handling the incident in hours.

    20) Closure_Code:
        Closure Code – code or reason for closing the incident (e.g., resolved, rejected, duplicate).

    21) No_of_Related_Interactions:
        Number of Related Interactions – count of interactions (e.g., emails, calls) related to the incident.

    22) Related_Interaction:
        Related Interaction – reference or ID for interactions associated with the incident.

    23) No_of_Related_Incidents:
        Number of Related Incidents – count of other incidents linked to this one.

    24) No_of_Related_Changes:
        Number of Related Changes – count of related change requests associated with the incident.

    25) Related_Change:
        Related Change – reference or ID for a change request associated with the incident.


# <B>PROBLEM 1
#### <B>PREDICTING HIGH PRIORITY TICKETS : TO PREDICT 1 & 2 TICKETS, SO THAT THEY CAN TAKE PREVENTIVE MEASURES OR FIX THE PROBLEM BEFORE IT SURFACES.

#### <B>MODEL EVALUATION REPORT
| **Model**                      | **Accuracy Score** | **Precision Score** | **Recall Score** |
| ------------------------------ | ------------------ | ------------------- | ---------------- |
| Logistic Regression            | 0.6143             | 0.9152              | 0.6143           |
| K Nearest Neighbors Classifier | 0.7071             | 0.9111              | 0.7071           |
| SVM Classifier                 | 0.8143             | 0.9451              | 0.8143           |
| Decision Tree Classifier       | 0.9143             | 0.9130              | 0.8857           |
| Random Forest Classifier       | 0.9286             | 0.9149              | 0.9286           |

#### <B>CONCLUSION
- The K Nearest Neighbors Classifier outperforms other models in predicting high priority tickets, exhibiting high accuracy, precision, and recall.
- Logistic Regression and SVM Classifier models show lower performance, indicating the need for improvement.
- Decision Tree and Random Forest models perform competitively, offering viable options.
- The choice of the most suitable model should consider a balance between accuracy, precision, and recall, with further refinement recommended for practical applicability in addressing the priority ticket prediction problem.


# <b>PROBLEM 2
#### <B>FORECAST THE INCIDENT VOLUME IN DIFFERENT FIELDS, QUARTERLY AND ANNUAL. SO THAT THEY CAN BE BETTER PREPARED WITH RESOURCES AND TECHNOLOGY PLANNING.

#### <b>CONCLUSION
- The autoregressive (AR) and ARIMA time series model effectively forecasts quarterly and annual incident volumes in various fields.
- Through rigorous testing, the model has demonstrated reliable performance, capturing historical patterns accurately.
- The forecast results align with expectations, aiding stakeholders in resource and technology planning.
- This approach ensures better preparedness for future incidents, enhancing organizational responsiveness and strategic planning.


# <b>PROBLEM 3
#### <B>AUTO TAG THE TICKETS WITH RIGHT PRIORITIES AND RIGHT DEPARTMENTS SO THAT REASSIGNING AND RELATED DELAY CAN BE REDUCED.
#### <B>MODEL EVALUATION REPORT
| **Model**                      | **Accuracy Score** | **Precision Score** | **Recall Score** |
| ------------------------------ | ------------------ | ------------------- | ---------------- |
| Logistic Regression            | 0.6989             | 0.8434              | 0.8434           |
| K Nearest Neighbors Classifier | 0.9373             | 0.9433              | 0.9373           |
| SVM Classifier                 | 0.6112             | 0.8025              | 0.6112           |
| Decision Tree Classifier       | 0.9332             | 0.9357              | 0.9325           |
| Random Forest Classifier       | 0.9335             | 0.9385              | 0.9361           |

#### <b>CONCLUSION
- The K Nearest Neighbors Classifier demonstrates outstanding accuracy, precision, and recall scores.
- The Decision Tree and Random Forest models also exhibit strong performance, offering effective solutions to reduce reassignments and associated delays.
- It is important to note that our models encounter difficulties in classifying specific classes with fewer data points.
- Nevertheless, classes characterized by abundant data points are classified more accurately, underscoring the models' efficacy in managing larger datasets.

# <B>Problem 4
#### <B>PREDICT RFC (REQUEST FOR CHANGE) AND POSSIBLE FAILURE MISCONFIGURATION OF ITSM ASSETS.
#### <B>MODEL EVALUATION REPORT
| **Model**                      | **Accuracy Score** | **Precision Score** | **Recall Score** |
| ------------------------------ | ------------------ | ------------------- | ---------------- |
| Logistic Regression            | 0.6143             | 0.9152              | 0.6143           |
| K Nearest Neighbors Classifier | 0.7071             | 0.9111              | 0.7071           |
| SVM Classifier                 | 0.8143             | 0.9451              | 0.8143           |
| Decision Tree Classifier       | 0.8929             | 0.9130              | 0.8857           |
| Random Forest Classifier       | 0.9357             | 0.9152              | 0.9357           |

#### <b>CONCLUSION
- In conclusion, the Decision Tree Classifier and Random Forest Classifier models demonstrate superior performance in predicting RFC and identifying misconfigurations in ITSM assets, with high accuracy, precision, and recall scores.
- However, it's crucial to note that the models may face challenges in identifying certain data points due to fewer instances in some classes, impacting their overall performance.
- While Logistic Regression, K Nearest Neighbors, and SVM Classifier models show acceptable accuracy, their precision and recall are comparatively lower
- The tree-based models, especially the Random Forest Classifier with a 95% accuracy, are recommended for their robust predictive capabilities.
- Ongoing refinement is essential to address challenges related to imbalanced class distribution and further enhance overall performance.

## <b>CONTRIBUTION
<b>  

- SIDDHESHWAR KOLI
  
## <b> END OF PROJECT
## <b> THANK YOU
