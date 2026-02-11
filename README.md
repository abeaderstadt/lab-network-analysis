# Project Overview

This project explores how a network of clinical laboratories performs across different locations, facility types, and test categories. Using a simulated lab operations dataset, I analyzed testing volume, turnaround times, and cost versus reimbursement to uncover patterns that could inform operational decisions. The visualizations highlight which labs run efficiently, which tests are most profitable, and where there’s room for improvement.

Explore the full analysis and interactive Tableau dashboards below.
Screenshots and stories are included to highlight key takeaways, but you can also view the hosted PDF report of the project here: https://github.com/abeaderstadt/lab-network-analysis/blob/main/AlissaBeaderstadt_LabNetwork.pdf


---



# Inside the Lab Network: Performance, Volume, and Cost Across Facilities
Alissa Beaderstadt
February 10, 2026

## Section 1. Introduction 
Clinical laboratories play a huge role in healthcare operations. They have to balance speed, testing volume, and cost, all while supporting patient care. In this project, I took a closer look at how a lab network performs across different locations, facility types, and test categories.
Using a simulated healthcare lab operations dataset, I explored where labs are located, how much testing they handle, how quickly results are completed, and how costs compare to reimbursement.
The goal of this analysis was to identify patterns that could actually matter for operational decision making. By combining geographic views, trend analysis, and cost comparisons in Tableau, this project highlights where labs appear to be operating efficiently and where there may be room for improvement.

You can view my interactive Tableau project here:
https://public.tableau.com/views/Beaderstadt_LabNetworkAnalysis/Goal1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

## Section 2. Data Description  
## Data Domain
This dataset contains information about clinical laboratory testing performed across multiple facilities. It includes lab locations, facility types, test orders, turnaround times, test categories, and financial metrics such as cost and reimbursement.
## Data File
The data comes from an Excel file named healthcare-lab-test-utilization.xlsx. It is a simulated lab operations dataset sourced from GoMask.ai, an AI-powered test data management platform that generates realistic, compliant healthcare data.
The dataset contains 200 rows and 29 original columns. I created one additional calculated column, Turnaround Time (Days), by calculating the difference between the Test Order Date and the Test Completed Date.
The following columns were present and clean upon obtaining the file:
-	utilization_id
-	facility_id
-	facility_name
-	facility_type
-	facility_street_address
-	facility_city
-	facility_state
-	facility_postal_code
-	facility_country
- test_order_id
- test_code
-	test_name
-	test_category
-	test_order_date
-	test_completed_date	
-	ordering_physician_id	
-	ordering_physician_name
-	patient_id
-	patient_age
-	patient_gender
-	test_result_value
-	test_result_unit
-	test_result_flag
-	test_cost
-	test_reimbursed_amount
-	test_utilization_status
-	test_duplicate_flag
-	diagnosis_code	
-	diagnosis_description 

## Rows and Columns Used
All 200 rows are included in this analysis. After adding the calculated turnaround time column, the dataset contained 30 columns total. Of these, 12 columns were actively used in the visualizations.
## Data Source
The dataset is a simulated lab operations dataset sourced from GoMask.ai. It represents lab testing activity across states, facility types, and test categories, and includes metrics related to turnaround time, testing volume, and financial performance.

You can view my data source here: 
https://gomask.ai/marketplace/datasets/healthcare-lab-test-utilization


## Section 3. Data Cleaning Strategies 
Very little cleaning was needed for this project. State values were updated from abbreviations to full state names to improve readability in the geographic visualization. Other than that, the dataset was already well structured and ready to use.

## Section 4. Clean Dataset 
The clean dataset includes all original records, along with standardized state names and the calculated turnaround time column.
The data is structured at the individual test order level, which allows for analysis by facility, location, test type, and date. 


## Section 5. Visualization Tools 
Tableau was selected as the primary visualization tool because it supports interactive dashboards, geographic mapping, and clear comparisons across multiple dimensions such as location, facility type, and test category.
Its filtering and storytelling features made it the best choice for exploring patterns in a way that is easy to follow.


## Section 6. Visualizations and Stories
This section presents dashboards and charts that explore lab performance across locations, facility types, and test categories.
You can interact with the filters to explore results by state, facility type, or test type. Below, I’ve included screenshots and short stories to highlight key takeaways. The full interactive Tableau workbook is available online if you would like to explore the data.

### Goal 1: Where are labs located, and how is testing activity distributed across states?
*Story:* Labs are spread across multiple U.S. states and two Canadian provinces, but most testing happens in just a few hotspots. Not surprisingly, states with more facilities tend to see more tests. Colorado leads in total tests and has one of the highest numbers of facilities, along with California. Other states are more balanced, but Colorado’s darker shading hints that some labs there may act as regional hubs, handling bigger workloads.

![Goal 1](images/Goal1.png)
 
### Goal 2: How do average turnaround times differ by facility type, and how have they changed over time?
*Story:* Average turnaround times over the year were smoothed to see trends clearly. Labs surprisingly have the longest averages, probably because they deal with higher volumes or more complex tests. Hospitals show steady improvement, while most other facility types spike slightly in September. This may be due to seasonal demand or staffing shifts. Overall, facility type clearly impacts efficiency, and some facilities are already improving over time. 

![Goal 2](images/Goal2.png)
 
### Goal 3: How does test volume by facility type relate to turnaround time?
*Story:* Higher test volumes generally slow turnaround a bit, but it’s not a strict rule. Seven facilities manage fast processing even with heavy workloads, showing that good workflows make a difference. On the low-volume side, three clinics struggle despite fewer tests, which proves that less demand doesn’t automatically mean faster results.

![Goal 3](images/Goal3.png)

### Goal 4: What percentage of total testing does each test type represent, and which tests are ordered most frequently?
*Story:* BMI tops the list at 13%, followed by Cholesterol at 10.5%. Beyond that, testing is pretty spread out, almost half of all tests are a mix of various types. No single test dominates, keeping the workload fairly diverse. 

![Goal 4](images/Goal4.png)

### Goal 5: How does turnaround time vary by test type, and which tests take longer?
*Story:* Most tests finish around one day, with Complete Blood Count taking the longest at about 1.5 days. ALT, Vitamin D, and WBC Count are quick, almost zero days. Chemistry tests dominate, with consistent turnaround times within the category, while microbiology tests are slightly slower, likely due to extra processing. Overall, differences are more about test complexity than odd outliers

![Goal 5](images/Goal5.png)

### Goal 6: How do test costs compare to reimbursed amounts, and which tests appear to be the least cost effective?
*Story:* Every test brings in more than it costs, so the lab network is profitable overall. Base costs stay under $35 per test, but some tests are more profitable than others. BMI, Red Blood Cell Count, and WBC Count have the smallest margins, while COVID-19 PCR and LDL cholesterol bring in the biggest gains. This could guide pricing or service focus.

![Goal 6](images/Goal6.png)


## Dashboard Overview: Filters and Interactivity
These dashboards allow filtering by state, facility type, and test type to explore the data interactively. Screenshots above show each goal-specific chart in a clean view for clarity.

*Purpose:* Looking at these views together shows how facility locations and testing volume vary geographically. Filtering by state highlight’s location differences, while filtering by test type shows how tests are distributed across the lab network.

![Dashboard 1](images/Dashboard1.png)



*Purpose:* Looking at these views together shows how turnaround time relates to facility type and test volume. Filtering by facility type lets you focus on one type at a time, revealing trends over time and the relationship between volume and turnaround for that group.

 ![Dashboard 2](images/Dashboard2.png)
 
*Purpose:* Looking at these views together shows how turnaround time and cost efficiency vary by test type. Some tests combine fast turnaround with smaller reimbursement gaps, while others take longer and show larger gaps. Together, these metrics highlight which tests could benefit most from operational or pricing improvements. Overall, these views give a comprehensive look at lab performance, efficiency, and cost-effectiveness across the network.

![Dashboard 3](images/Dashboard3.png)


### Section 7.  Conclusions 
Lab performance isn’t one-size-fits-all, it changes by location, facility type, and the tests themselves. Some states handle a ton of tests, but high volume doesn’t always mean fast results. A few facilities manage big workloads efficiently, and these could be great examples for others to follow.
Turnaround times mostly depend on the type of test. Routine ones usually finish in about a day, while tests like Complete Blood Count take longer. Financially, every test makes money, but some are more profitable than others. BMI, Red Blood Cell Count, and WBC Count bring in smaller margins, while COVID-19 PCR and LDL cholesterol are real winners.
So, what does this mean for the network? Focus on helping slower, high-volume labs speed up and streamline longer tests. At the same time, leaning into those high-margin tests and finding ways to reduce costs on the lower-margin ones could give a nice boost to overall profits. By learning from the labs that are already crushing it and tweaking operations and test mix, the network could get faster results and stronger performance across the board.

