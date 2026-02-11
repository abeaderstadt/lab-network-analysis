# Inside the Lab Network: Performance, Volume, and Cost Across Facilities
Alissa Beaderstadt
February 10, 2026

## Section 1. Introduction 
Clinical laboratories sit at the center of healthcare operations, balancing speed, volume, and cost while supporting patient care. This project takes a closer look at how a lab network performs across different locations, facility types, and test categories. Using a simulated healthcare lab operations dataset, I explored where labs are located, how much testing they handle, how quickly results are turned around, and how costs compare to reimbursement.
The goal of this analysis is not just to describe the data, but to identify patterns that could matter for operational decision-making. By combining geographic views, trend analysis, and cost comparisons in Tableau, this project highlights where labs appear to be operating efficiently and where there may be opportunities for improvement.
You can view my interactive Tableau project here:
https://public.tableau.com/views/Beaderstadt_LabNetworkAnalysis/Goal1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
## Section 2. Data Description  
Data Domain
The dataset contains information about clinical laboratory testing performed across multiple facilities. It includes details about lab locations, facility types, test orders, turnaround times, test categories, and cost and reimbursement information.
Data File
The data comes from an Excel file named healthcare-lab-test-utilization.xlsx. This is a simulated lab operations dataset sourced from GoMask.ai, an AI-powered test data management platform that generates realistic, compliant healthcare data. The dataset contains 200 rows and 29 original columns.
I created an additional calculated column, Turnaround Time (Days), by calculating the difference between the Test Order Date and the Test Completed Date.
The following columns were present and clean upon obtaining the file:

 
•	utilization_id
•	facility_id
•	facility_name
•	facility_type
•	facility_street_address
•	facility_city
•	facility_state
•	facility_postal_code
•	facility_country
•	test_order_id
•	test_code
•	test_name
•	test_category
•	test_order_date
•	test_completed_date	
•	ordering_physician_id	
•	ordering_physician_name
•	patient_id
•	patient_age
•	patient_gender
•	test_result_value
•	test_result_unit
•	test_result_flag
•	test_cost
•	test_reimbursed_amount
•	test_utilization_status
•	test_duplicate_flag
•	diagnosis_code	
•	diagnosis_description 

Rows and Columns Used
All 200 rows are used in this project. After adding the calculated turnaround time, the dataset contains 30 columns. Of these, 12 columns are actively used in the visualizations.
Data Source
The dataset is a simulated lab operations dataset sourced from GoMask.ai. It represents lab testing activity across states, facility types, and test categories, and includes metrics related to turnaround time, testing volume, and financial performance.

## Section 3. Data Cleaning Strategies 
Only minor cleaning was required for this project. State values were updated from abbreviations to full state names to improve readability and consistency in geographic visualizations.
## Section 4. Clean Dataset 
The clean dataset includes all original records with standardized state names and a calculated turnaround time column. The data is structured at the individual test order level, allowing analysis by facility, location, test type, and time. An excerpt of the dataset is included below to show the structure and key fields used for visualization.







## Section 5. Visualization Tools 
Tableau was selected as the primary visualization tool for this project because it allows for interactive dashboards, geographic mapping, and easy comparison across multiple dimensions such as location, facility type, and test category. Tableau’s filtering and storytelling features make it well-suited for exploring operational patterns and communicating insights clearly.
The final dashboards and storyboards are published to GitHub and can be accessed here:

















## Section 6. Visualizations and Stories
### Goal 1: Where are labs located, and how is testing activity distributed across states?
Story: Facilities are spread across several U.S. states and two Canadian provinces. The states with the most facilities are California, Colorado, and Wyoming. Bigger circles represent more lab facilities, and darker blue shades show higher test volumes, which makes sense since more labs tend to process more tests.
 
### Goal 2: How do average turnaround times differ by facility type, and how have they changed over time?
Story: These values use a moving average to smooth out month-to-month ups and downs. Overall, laboratories have the highest average turnaround times throughout 2023, which is somewhat surprising given that labs are dedicated to test processing. This may reflect higher test volumes or more complex testing handled by labs. 
 
### Goal 3: How does test volume by facility type relate to turnaround time?
Story: Generally, higher test volumes come with slower turnaround times. That said, seven labs manage high volume while keeping turnaround fast showing they’ve got efficient processes in place. On the flip side, one low-volume lab is slower than average, which could be a spot to focus on for improvement. 
### Goal 4: What percentage of total testing does each test type represent, and which tests are ordered most frequently?
Story: BMI is the most commonly ordered test at 13.0%, with Cholesterol coming in second at 10.5%. Some other tests get ordered more often than others, but almost half of all testing is spread across a variety of types. No single test really dominates the labs’ workload. 
### Goal 5: How does turnaround time vary by test type, and which tests take longer?
Story: Complete Blood Count takes the longest on average at 1.5 days. ALT, Vitamin D, and WBC Count are much faster, close to zero days. Most tests hover around a 1-day average, which is a good sign for overall lab performance. Microbiology tests tend to be a bit slower than the rest of the categories.

### Goal 6: How do test costs compare to reimbursed amounts, and which tests appear to be the least cost effective?
Story: Across all test types, reimbursement is higher than cost, so overall the labs appear to be profitable. That said, not all tests perform the same. BMI, Red Blood Cell Count, and White Blood Cell Count have the smallest margins, making them the least cost-effective. On the other hand, COVID-19 PCR stands out as the most profitable test based on the size of its reimbursement gap.







## Dashboard Overview: Filters and Interactivity
These dashboards allow filtering by state, facility type, and test type to explore the data interactively. Screenshots above show each goal-specific chart in a clean view for clarity.
Purpose: Looking at these views together shows how lab locations and testing volume vary geographically. Filtering by state highlight’s location differences, while filtering by test type shows how tests are distributed across the lab network.















Purpose: Looking at these views together shows how turnaround time relates to facility type and test volume. Filtering by facility type lets you focus on one type at a time, revealing trends over time and the relationship between volume and turnaround for that group.
 
Purpose: Looking at these views together shows how turnaround time and cost efficiency vary by test type. Some tests combine fast turnaround with smaller reimbursement gaps, while others take longer and show larger gaps. Together, these metrics highlight which tests could benefit most from operational or pricing improvements. Overall, these views give a comprehensive look at lab performance, efficiency, and cost-effectiveness across the network.


















### Section 7.  Conclusions 
Lab performance varies across location, facility type, and test category. States with more labs process higher test volumes, though higher volume can mean slower turnaround. A few high-volume labs handle workloads efficiently, highlighting potential best practices.
Turnaround time differs by test type: most tests finish within about a day, while specialized tests take longer. Financially, reimbursement exceeds cost for all tests, showing overall profitability. Tests with smaller reimbursement-cost gaps, like BMI, Red Blood Cell Count, and White Blood Cell Count, are relatively less cost-effective, while COVID-19 PCR shows the largest margins.
These findings point to actionable opportunities: review workflows for slower labs, use fast, high-volume labs as benchmarks, and consider test-specific cost-effectiveness when making pricing or operational decisions. Overall, this analysis gives a clear picture of lab network performance and where targeted improvements could have the greatest impact.

# lab-network-analysis
